---
title: ' [!DNL Analytics] とAdvertising Cloudの間で予想されるデータの相違'
description: ' [!DNL Analytics] とAdvertising Cloudの間で予想されるデータの相違'
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '3285'
ht-degree: 0%

---

# [!DNL Analytics]とAdvertising Cloudの間で予想されるデータの相違

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

[!DNL Analytics for Advertising Cloud] <!-- (A4AdC) -->統合を持つ広告主は、Advertising CloudとAdobe Analyticsを通じて有料広告を追跡します。 複数のシステムを使用してメディア、キャンペーンおよびチャネルを追跡する場合、異なるシステムの同じデータセットが完全に一致することはほとんどありません。 このドキュメントでは、Advertising Cloudを通じて配信されるメディアのデータと、[!DNL Analytics]内でメディアが追跡される様々なシステムのデータとを比較する方法について説明します。

>[!NOTE]
>
>このドキュメントはAdvertising CloudとAnalyticsに焦点を当てていますが、主なポイントの多くは、他のトラッキングソリューションにも引き渡すことができます。

## 類似のレポートにおけるアトリビューションの違い

### 潜在的に異なるルックバックウィンドウとアトリビューションモデル

[!DNL Analytics for Advertising Cloud]統合では、2つの変数（eVarsまたはrVars \[reserved eVars]\）を使用して[EF IDとAMO ID](ids.md)を取り込みます。 これらの変数は、単一のルックバックウィンドウ（クリックスルーとビュースルーに関連付けられる時間）とアトリビューションモデルを使用して設定されます。 特に指定のない限り、変数は、Advertising Cloudのデフォルトの広告主レベルのクリックルックバックウィンドウとアトリビューションモデルに一致するように設定されます。

ただし、ルックバックウィンドウとアトリビューションモデルは、Analytics（eVarを使用）とAdvertising Cloudの両方で設定できます。 さらに、Advertising Cloudでは、アトリビューションモデルは広告主レベル（入札の最適化用）でのみならず、個々のデータビューおよびレポート内（レポート目的のみ）で設定できます。 例えば、Advertising Cloud DSPのレポートや[!DNL Search]のレポートでは、最適化のために偶数配分アトリビューションモデルを使用し、ラストタッチアトリビューションを使用したい場合があります。 アトリビューションモデルを変更すると、アトリビュートされたコンバージョンの数が変更されます。

レポートのルックバックウィンドウまたはアトリビューションモデルが1つの製品で変更され、他の製品では変更されなかった場合、各システムの同じレポートには、異なるデータが表示されます。

* **様々なルックバックウィンドウが原因で生じる不一致の例：**

   Advertising Cloudに60日間のクリックルックバックウィンドウがあり、[!DNL Analytics]に30日間のルックバックウィンドウがあるとします。 また、ユーザーがAdvertising Cloudで追跡された広告を通じてサイトにアクセスし、離れ、45日目に戻ってコンバージョンしたとします。 Advertising Cloudは、60日間のルックバックウィンドウ内でコンバージョンが発生したので、最初の訪問にコンバージョンを関連付けます。 [!DNL Analytics]ただし、は、30日間のルックバックウィンドウの有効期限が切れた後にコンバージョンが発生したので、最初の訪問にコンバージョンを関連付けることができません。この例では、Advertising Cloudは[!DNL Analytics]よりも多くのコンバージョンをレポートします。

   ![Advertising Cloudに属するが属さないコンバージョンの例  [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **様々なアトリビューションモデルに起因する不一致の例：**

   コンバージョンを行う前に、ユーザーが3つの異なるAdvertising Cloud広告を操作し、コンバージョンタイプに売上高を指定したとします。 Advertising Cloudレポートで、アトリビューションに均等配分モデルが使用されている場合は、すべての広告の売上高を均等にアトリビューションします。 ただし、[!DNL Analytics]がラストタッチアトリビューションモデルを使用する場合は、売上高を最後の広告に関連付けます。 次の例では、Advertising Cloudは、3つの広告のそれぞれに対して取り込まれた売上高の30米ドルのうち、10米ドルを属性にしていますが、[!DNL Analytics]は、すべての売上高を、ユーザーが最後に閲覧した広告の30米ドルに属性化しています。 Advertising Cloudと[!DNL Analytics]からのレポートを比較すると、アトリビューションの違いの影響を期待できます。

   ![Advertising Cloudに起因し、異なるアトリビューション [!DNL Analytics] モデルに基づく異なる売上高](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>ベストプラクティスは、Advertising Cloudと[!DNL Analytics]の両方で同じルックバックウィンドウとアトリビューションモデルを使用することです。 必要に応じて、Adobeのアカウントマネージャーと協力して、現在の設定を特定し、設定を同期させます。

これらの同じ概念は、異なるルックバックウィンドウやアトリビューションモデルを使用する他のチャネルなどにも当てはまります。

#### ビュースルートラッキング用の様々なルックバックウィンドウ {#impression-lookback}

Advertising Cloudでは、アトリビューションはクリック数とインプレッション数に基づいており、クリック数とインプレッション数に応じて様々なルックバックウィンドウを設定できます。 ただし、[!DNL Analytics]では、アトリビューションはクリックスルーとビュースルーに基づいており、クリックスルーとビュースルーに対して異なるアトリビューションウィンドウを設定するオプションはありません。最初のサイト訪問時に開始する各の追跡を追跡します。 インプレッションは、ビュースルーが発生する同じ日または複数日前に発生する可能性があり、各システムでアトリビューションウィンドウが開始する場合に影響を与える可能性があります。

通常、ビュースルーコンバージョンの大部分は、両方のシステムがクレジットを考慮するほど迅速に発生します。 ただし、変換の中には、Advertising Cloudインプレッションのルックバックウィンドウの外側で、 [!DNL Analytics]ルックバックウィンドウ内で発生する場合があります。このようなコンバージョンは、[!DNL Analytics]のビュースルーに起因しますが、Advertising Cloudのインプレッションに起因しません。

次の例では、訪問者が1日目に広告を提供し、2日目にビュースルー訪問（つまり、広告を以前にクリックせずに広告のランディングページを訪問）し、45日目にコンバージョンしたとします。 この場合、Advertising Cloudでは1 ～ 14日（14日のルックバックを使用）からのユーザーを追跡し、[!DNL Analytics]では2 ～ 61日（60日のルックバックを使用）からのユーザーを追跡し、Day 45のコンバージョンは[!DNL Analytics]内の広告に関連付けられ、Advertising Cloud内では追跡されません。

![で特定されるが [!DNL Analytics] Advertising Cloudではないビュースルーコンバージョンの例](/help/integrations/assets/a4adc-viewthrough-example.png)

不一致のさらなる原因は、Advertising Cloudで、ビュースルーコンバージョンに、クリックベースのコンバージョンに起因する重みに関連するカスタムの&#x200B;*ビュースルーの重み*&#x200B;を割り当てることができる点です。 デフォルトのビュースルーの重み付けは40%です。つまり、ビュースルーのコンバージョンは、クリックベースのコンバージョンの値の40%としてカウントされます。 [!DNL Analytics] では、ビュースルーコンバージョンにこのような重み付けはおこなわれません。例えば、[!DNL Analytics]で取り込まれた100米ドルの売上高注文は、デフォルトのビュースルーの重み付け（60米ドルの違い）を使用している場合、Advertising Cloudでは40米ドルに割引されます。

Advertising Cloudと[!DNL Analytics]レポートの間のビュースルーコンバージョンを比較する際には、次の違いを考慮してください。

#### 使用可能なアトリビューションモデル

| Advertising Cloud Attribution | [!DNL Analytics] 帰属 | eVar/rVarの配分 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | なし | なし |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>使用しない* |
| [!UICONTROL Weight Last Event More] | なし | なし |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | なし |
| なし | [!UICONTROL J-Shaped] | なし |
| なし | [!UICONTROL Inverse-J] | なし |
| なし | [!UICONTROL Custom] | なし |
| なし | [!UICONTROL Participation] | なし |
| なし | [!UICONTROL Algorithmic] | なし |

>[!NOTE]
>
>線形配分の場合、[!DNL Analytics]は成功イベントを1回の訪問のすべてのeVar値に均等に配分するので、「訪問」のeVar有効期限を持つ線形配分を使用します。 ただし、広告の場合、線形アトリビューションを使用すると、配分が実際には線形ではなく、理想的なレポートよりも短くなります。 例えば、訪問者が3回の個別の訪問にコンバージョンする前に3つの広告を操作した場合、3回の広告すべてではなく、最後の訪問で表示された広告のみがコンバージョンに関連付けられます。
>
>また、「線形」へのコンバージョン配分を切り替えたり、「線形」から切り替えたりすると、履歴データが表示されなくなり、レポートに誤ったデータが表示される可能性があります。 例えば、線形配分では売上高を様々なeVar値で除算します。 配分を「最新」に変更すると、その売上高の100%が最新の単一値に関連付けられます。 この関連付けは、誤った結論を引き起こす可能性があります。
>
>混乱を防ぐために、[!DNL Analytics]は、履歴データをレポートインターフェイスで使用できなくします。 履歴eVarは、eVar割り当ての設定を変更して履歴データにアクセスするのではなく、データを初期割り当て設定に戻した場合に表示できます。 Adobeでは、既に大量の履歴eVarを持つeVarの割り当て設定を変更するのではなく、記録済みのデータに対して新しい割り当て設定を適用する場合に、新しいデータを使用することをお勧めします。

[!DNL Analytics]アトリビューションモデルとその定義のリストについては、[https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html)を参照してください。

Advertising Cloudにログインしている場合、アトリビューションモデルのリストは、
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm).

#### Advertising Cloudのイベント日アトリビューション

Advertising Cloudでは、関連するクリック日/イベント日（クリックイベントまたはインプレッションイベントの日付）またはトランザクション日（コンバージョン日）のいずれかでコンバージョンデータをレポートできます。 クリック/イベント日のレポートの概念は[!DNL Analytics]に存在しません。[!DNL Analytics]で追跡されたすべてのコンバージョンは、トランザクション日別にレポートされます。 その結果、Advertising Cloudと[!DNL Analytics]では、異なる日付で同じコンバージョンがレポートされる場合があります。 例えば、1月1日に広告をクリックして1月5日にコンバージョンするユーザーを考えます。 Advertising Cloudでイベント日別にコンバージョンデータを表示している場合、クリックが発生した1月1日にコンバージョンがレポートされます。 [!DNL Analytics]では、同じコンバージョンが1月5日に報告されます。

![異なる日付に関連付けられたコンバージョンの例](/help/integrations/assets/a4adc-conversions-based-on.png)

## [!DNL Analytics Marketing Channels]の属性

[[!DNL Analytics Marketing Channels] ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html) レポートを使用すると、ヒット情報の様々な側面に基づいて様々なマーケティングチャネルを識別するルールを設定できます。`ef_id`クエリ文字列パラメーターを使用してチャネルを識別することで、Advertising Cloudで追跡されたチャネル([!UICONTROL Display Click Through]、[!UICONTROL Display View Through]、[!UICONTROL Paid Search])を[!DNL Marketing Channels]として追跡できます。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> ただし、レポートでAdvertising Cloudチャネルを追 [!DNL Marketing Channels] 跡できますが、いくつかの理由でデータがAdvertising Cloudレポートと一致しない場合があります。詳しくは、以下の節を参照してください。

>[!NOTE]
>
> 次の中心概念は、Advertising Cloudで追跡しないキャンペーン([`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html)変数(「トラッキングコード」Dimensionや「eVar0」とも呼ばれます)やカスタムeVarトラッキングにも当てはまります。

### [!DNL Marketing Channels]のアトリビューションモデルが異なる可能性

ほとんどの[!DNL Marketing Channels]レポートは、[!UICONTROL Last Touch]アトリビューションを使用して設定されます。このアトリビューションに対して、最後に検出されたマーケティングチャネルに、コンバージョン値の100%が割り当てられます。 [!DNL Marketing Channels]レポートとAdvertising Cloudレポートで異なるアトリビューションモデルを使用すると、アトリビュートコンバージョンに相違が生じます。

### [!DNL Marketing Channels]のルックバックウィンドウが異なる可能性がある

[!DNL Marketing Channels]のルックバックウィンドウはカスタマイズできます。 Advertising Cloudでは、クリックのルックバックウィンドウは設定できますが、60日間の固定ウィンドウは一般的です。 2つの製品で異なるルックバックウィンドウが使用されている場合は、データの相違が生じる可能性があります。

### [!DNL Marketing Channels]の異なるチャネルアトリビューション

Advertising Cloudレポートは、Advertising Cloud(Advertising Cloud Search広告の有料検索、Advertising Cloud DSP広告の表示)を通じて配信された有料メディアのみを取り込みますが、[!DNL Marketing Channels]レポートは、すべてのデジタルチャネルを追跡できます。 これは、コンバージョンが関連付けられるチャネルに矛盾が生じる可能性があります。

例えば、有料検索と自然検索のチャネルは、多くの場合共生的な関係を持ち、各チャネルが相互に支援します。 [!DNL Marketing Channels]レポートは、Advertising Cloudが自然検索を追跡しないので、自然検索に対するコンバージョンの一部を明らかにします。

また、ディスプレイ広告を表示し、有料検索広告をクリックし、電子メールメッセージ内をクリックして、30米ドルの注文をする顧客も考えます。 Advertising Cloudと[!DNL Marketing Channels]の両方がラストタッチアトリビューションモデルを使用している場合でも、コンバージョンの属性はそれぞれ異なります。 Advertising Cloudは[!UICONTROL Email]チャネルにアクセスできないので、有料検索にコンバージョンが計上されます。 [!DNL Marketing Channels]ただし、は3つのチャネルすべてにアクセスできるので、コンバージョンの [!UICONTROL Email] クレジットを受けます。

![Advertising Cloudと  [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

指標が異なる理由について詳しくは、「[Advertising Cloudと [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)でチャネルデータが異なる理由」を参照してください。

## Adobe Analyticsのデータの違い[!DNL Paid Search Detection]

[!DNL Analytics]の[従来の [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html)機能を使用すると、企業は[ルールを定義して、指定した検索エンジンの有料および自然検索トラフィック](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html)を追跡できます。 [!DNL Paid Search Detection]ルールは、クエリ文字列と参照ドメインの両方を使用して、有料検索トラフィックと自然検索トラフィックを識別します。 [!DNL Paid Search Detection]レポートは、[検索方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html)レポートの大きなグループに含まれ、指定したイベント（買い物かごのチェックアウトなど）が発生したときまたは訪問が終了したときに期限が切れます。

次に、[!DNL Paid Search Detection]ルールセットを作成するためのインターフェイスを示します。

![有料検索検知ルールの例(  [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

結果の[!DNL Paid Search Detection]レポートには、[!UICONTROL Paid Search Engine]、[!UICONTROL Paid Search Keywords]、[!UICONTROL Natural Search Engine]、[!UICONTROL Natural Search Keywords]の各レポートが含まれます。

[!DNL Paid Search Detection]レポートのデータには、次の2つの制限があることに注意してください。

* [!UICONTROL Paid Search Keywords]レポートと[!UICONTROL Natural Search Keywords]レポートには、ユーザーが入札するキーワードではなく、参照URLで識別される検索クエリが表示されます。 Advertising Cloudと[!DNL Analytics]のレポートには、実際のキーワードが表示されるので、[!DNL Paid Search Detection]キーワードレポートと一致しないでください。

* [!DNL Paid Search Detection]機能を最初に作成したとき、元の検索クエリ（検索エンジンの検索バーにユーザーが入力した文字列）は、参照URLを使用して、より簡単に広告主に提供されるようになりました。 現在、検索エンジンは検索クエリをほとんど難読化し、[!DNL Paid Search Detection]キーワードレポートの値は制限されています。これは、ほとんどのクエリデータが「未指定」に該当するためです。

   [!DNL Analytics for Advertising Cloud]では、広告主は引き続き[!DNL Analytics]内の有料キーワードを追跡できます。 参照ドメインは、トラフィックを駆動した検索エンジンをレポートするエンジンを通知します。 広告主固有のアカウント情報は参照ドメインに結び付けられないので、すべてのトラフィックが検索エンジンの下に表示されます。 同じ検索エンジンに複数のアカウントを持つ広告主は、アカウント固有のレポートについて、Advertising Cloudまたは[!DNL Analytics]レポートを参照してください。

### [!DNL Paid Search Detection]を設定する理由

[!DNL Paid Search Detection]レポートを使用すると、[[!DNL Analytics Marketing Channels] reports](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html)で自然検索トラフィックを識別できます。 有料検索トラフィックと自然検索トラフィックを区別することは、自然検索がフルマーケティングエコシステムにもたらす価値を理解する上で最適です。

## [!DNL Analytics for Advertising Cloud]のクリックスルーデータ検証 {#data-validation}

統合の場合、クリックスルーデータを検証して、サイト上のすべてのページでクリックスルーが正しく追跡されていることを確認する必要があります。

[!DNL Analytics]で[!DNL Analytics for Advertising Cloud]追跡を検証する最も簡単な方法の1つは、「AMO IDインスタンスへのクリック数」計算指標を使用して、クリック数をインスタンスと比較することです。この指標は次のように計算されます。

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] は、AMO ID（パラメーター）がサイトで追跡された回数を表しま`s_kwcid` す。広告がクリックされるたびに、ランディングページのURLに`s_kwcid`パラメーターが追加されます。 したがって、[!UICONTROL AMO ID Instances]の数はクリック数に相当し、実際の広告クリック数に対して検証できます。 通常、[!DNL Search]のマッチ率は80%、[!DNL DSP]のトラフィックのマッチ率は30%です（クリックスルー[!UICONTROL AMO ID Instances]のみを含めるようにフィルタリングする場合）。 検索と表示の期待値の違いは、予想されるトラフィック行動によって説明できます。 検索は目的をキャプチャするので、ユーザーは通常、クエリの検索結果をクリックする必要があります。 ただし、ディスプレイ広告やオンラインビデオ広告を見たユーザーは、意図せずに広告をクリックした後、サイトからバウンスするか、ページアクティビティが追跡される前に読み込まれる新しいウィンドウを破棄する可能性が高くなります。

Advertising Cloudのレポートでは、[!UICONTROL AMO ID Instances]ではなく「[!UICONTROL ef_id_instances]」指標を使用して、クリック数をインスタンス数と同様に比較できます。

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

AMO IDとEF IDの間の一致率は高くなりますが、AMO IDとEF IDは基本的に異なるデータを追跡するので、100%のパリティは期待しないでください。この違いにより、[!UICONTROL AMO ID Instances]と[!UICONTROL EF ID Instances]の合計がわずかに異なる可能性があります。 ただし、[!DNL Analytics]の合計[!UICONTROL AMO ID Instances]がAdvertising Cloudの[!UICONTROL EF ID Instances]と1%以上異なる場合は、Adobeのアカウントマネージャーにお問い合わせください。

AMO IDとEF IDについて詳しくは、[Analyticsで使用されるAdvertising Cloud ID](ids.md)を参照してください。

次に、インスタンスに対するクリックを追跡するワークスペースの例を示します。

![インスタンスに対するクリックを追跡するワークスペースの例](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## [!DNL Analytics for Advertising Cloud]のデータセットとAdvertising Cloudのデータセットの比較

[AMO ID](ids.md)（s_kwcidクエリー文字列パラメーター）は[!DNL Analytics]でのレポートに使用され、[EF ID](ids.md)はAdvertising Cloudでのレポートに使用されます。 異なる値なので、1つの値が破損したり、ランディングページに追加されなかったりする可能性があります。

例えば、次のランディングページがあるとします。

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

ここで、EF IDは「`test_ef_id`」、AMO IDは「`test_amo_id`」です。

サイト側のリダイレクトが発生すると、URLは次のようになります。

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

ここで、EF IDは「`test_ef_id`」、AMO IDは「`test_amo_id#redirectAnchorTag`」です。

この例では、アンカータグを追加すると、AMO IDに予期しない文字が追加されるので、Analyticsが認識しない値になります。 このAMO IDは分類されず、それに関連付けられたコンバージョンは[!DNL Analytics]レポートの「[!UICONTROL unspecified]」または「[!UICONTROL none]」に分類されます。

幸いにも、このような問題は一般的ですが、通常、大きな相違は生じません。 ただし、[!DNL Analytics]のAMO IDとAdvertising CloudのEF IDの間に大きな相違がある場合は、Adobeのアカウントマネージャーにお問い合わせください。

## その他の指標に関する考慮事項

### クリック数と訪問数の違い {#clicks-vs-visits}

これらは似ていますが、クリック数と訪問数は異なるデータを表します。

* **クリック：** [!DNL DSP] 。または、訪問者がパブリッシャーのWebサイトで広告をクリックした場合に、検索エンジンがクリックを記録します。

* **訪問：** [!DNL Analytics] 訪問は、ユーザーが [](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) 一連のページビューを定義し、無操作状態が30分間続いたなど、いくつかの条件のいずれかに従って終了します。

定義によると、1回のクリックで複数の訪問が発生する可能性があります。

次の例を考えてみましょう。ユーザー1とユーザー2は共に、Advertising Cloud広告をクリックしてサイトにアクセスします。 ユーザー1は4つのページを表示し、1日の間は離れたので、最初のクリックは1回の訪問になります。 ユーザー2は2ページを閲覧し、45分の昼食を取るために出発し、戻り、さらに2ページを閲覧し、その後出発する。この場合、最初のクリックでは2回の訪問になります。

![クリック数と訪問数の違いの例](/help/integrations/assets/a4adc-visits-example.png)

### クリック数とクリックスルー数の違い

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

クリック数とクリックスルー数は、次の2つの異なる指標です。

* **クリック：** [!DNL DSP] 。または、訪問者がパブリッシャーのWebサイトで広告をクリックした場合に、検索エンジンがクリックを記録します。

* **クリックスルー：** [!DNL Analytics] は、訪問者が宛先Webサイトに到達した場合、ランディングページが読み込ま [!DNL Analytics] れ、ページ下部のリクエストがにデータを送信した場合にクリックスルーを記録しま [!DNL Analytics]す。

クリック数とクリックスルー数は、誤った広告クリック数があるので、大きく異なる場合があります。 ディスプレイ広告でのクリックの多くは、偶然にクリックされたもので、ランディングページが読み込まれる前にこれらの誤った訪問者が「戻る」ボタンを押したので、[!DNL Analytics]はクリックスルーを記録できません。 これは、特に、モバイル広告、ビデオ広告、広告など、誤ってクリックされる可能性が高い広告で特に当てはまります。広告は、画面いっぱいに表示され、ユーザーがページを表示する前に閉じる必要があります。

また、モバイルデバイスに読み込まれるサイトでは、帯域幅が低く処理能力が高く、ランディングページの読み込みに時間がかかるので、クリックスルーが発生する可能性が低くなります。 50 ～ 70%のクリックでクリックスルーが発生しないのは珍しくありません。 モバイル環境では、差は90%まで高くなります。これは、低速なブラウザーを組み合わせると、ページをスクロールしたり広告を閉じようとしたときにユーザーが誤って広告をクリックする可能性が高くなるからです。

クリックデータは、現在のトラッキングメカニズム（モバイルアプリへのクリック、モバイルアプリからのクリックなど）でクリックスルーを記録できない環境や、広告主が1つのトラッキングアプローチ（ビュースルーJavaScriptアプローチでは、サードパーティCookieをブロックするブラウザー）でも記録できます。 AdobeがクリックURLの追跡方法とビュースルーJavaScriptの追跡方法の両方をデプロイすることを推奨する主な理由は、追跡可能なクリックスルーを最大限に活用できることです。

### Advertising Cloud以外のDimensionに対するAdvertising Cloudトラフィック指標の使用

Advertising Cloudは、Analyticsに[広告固有のトラフィック指標と、DSPおよびSearch](advertising-cloud-metrics-in-analytics.md)の関連ディメンションを提供します。 Advertising Cloudが提供する指標は、指定されたAdvertising Cloudディメンションにのみ適用でき、[!DNL Analytics]内の他のディメンションではデータを使用できません。

例えば、Advertising Cloudディメンションのアカウント別に[!UICONTROL AMO Clicks]指標と[!UICONTROL AMO Cost]指標を表示すると、アカウント別の合計[!UICONTROL AMO Clicks]と[!UICONTROL AMO Cost]が表示されます。

![Advertising Cloudディメンションを使用したレポート内のAdvertising Cloud指標の例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

ただし、Advertising Cloudでデータを提供しないページ上のディメンション（ページなど）で[!UICONTROL AMO Clicks]と[!UICONTROL AMO Cost]の指標を表示する場合、各ページの[!UICONTROL AMO Clicks]と[!UICONTROL AMO Cost]は0(0)になります。

![サポートされていないディメンションを使用するレポート内のAdvertising Cloud指標の例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Advertising Cloud以外のDimensionでのクリックの代わりに[!UICONTROL AMO ID Instances]を使用

オンサイトディメンションで[!UICONTROL AMO Clicks]を使用できないので、クリック数と同じ値を見つけたい場合があります。 訪問回数を代わりに使用したいと考えるかもしれませんが、各訪問者が複数回訪問する可能性があるので、訪問回数は最適な選択肢ではありません。 （「[クリック数と訪問数の違い](#clicks-vs-visits)」を参照）。 代わりに、AMO IDが取り込まれた回数である[!UICONTROL AMO ID Instances]を使用することをお勧めします。 [!UICONTROL AMO ID Instances]は[!UICONTROL AMO Clicks]と厳密には一致しませんが、これらはサイト上のクリックトラフィックを測定する最適なオプションです。 詳しくは、「[ [!DNL Analytics for Advertising Cloud]](#data-validation)のデータ検証」を参照してください。

![サポートされて [!UICONTROL AMO ID Instances] いないデ [!UICONTROL AMO Clicks] ィメンションの代わりの例](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloudで使用されるID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Analysis WorkspaceのAdvertising Cloud指標](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloudのデータ](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)
>* [Advertising Cloudと [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

