---
title: ～間で予想されるデータの相違 [!DNL Analytics] とAdvertising Cloud
description: ～間で予想されるデータの相違 [!DNL Analytics] とAdvertising Cloud
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: d2ad7d47d9cf13411fc831526a6fa4ff698b0a15
workflow-type: tm+mt
source-wordcount: '3282'
ht-degree: 0%

---

# ～間で予想されるデータの相違 [!DNL Analytics] とAdvertising Cloud

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

を持つ [!DNL Analytics for Advertising Cloud] <!-- (A4AdC) --> 統合では、Advertising CloudとAdobe Analyticsを通じて有料広告を追跡します。 複数のシステムを使用してメディア、キャンペーンおよびチャネルを追跡する場合、異なるシステムの同じデータセットが完全に一致することはほとんどありません。 このドキュメントでは、Advertising Cloudを通じて配信されるメディアのデータを、そのメディアが追跡される様々なシステムのデータと比較する方法を説明します [!DNL Analytics].

>[!NOTE]
>
>このドキュメントはAdvertising Cloudと Analytics に焦点を当てていますが、主なポイントの多くは他のトラッキングソリューションにも渡すことができます。

## 類似レポートでのアトリビューションの違い

### 潜在的に異なるルックバックウィンドウとアトリビューションモデル

10. [!DNL Analytics for Advertising Cloud] 統合では、2 つの変数（eVar または rVars \[reserved eVars]\）を使用して [EF ID と AMO ID](ids.md). これらの変数は、単一のルックバックウィンドウ（クリックスルーとビュースルーに関連付けられる時間）とアトリビューションモデルを使用して設定されます。 特に指定のない限り、変数は、Advertising Cloudのデフォルトの広告主レベルのクリックルックバックウィンドウとアトリビューションモデルに一致するように設定されます。

ただし、ルックバックウィンドウとアトリビューションモデルは、Analytics（eVar を使用）とAdvertising Cloudの両方で設定できます。 さらに、Advertising Cloudでは、アトリビューションモデルは広告主レベル（入札の最適化）でのみならず、個々のデータビューおよびレポート内（レポート目的のみ）で設定できます。 例えば、最適化のために偶数配分アトリビューションモデルを使用し、Advertising Cloud DSPのレポートや [!DNL Search]. アトリビューションモデルを変更すると、アトリビューションに属するコンバージョンの数が変更されます。

レポートのルックバックウィンドウまたはアトリビューションモデルが、一方の製品で変更され、他方の製品で変更されなかった場合、各システムの同じレポートには、異なるデータが表示されます。

* **様々なルックバックウィンドウが原因で生じる不一致の例：**

   Advertising Cloudに 60 日間のクリックルックバックウィンドウがあり、 [!DNL Analytics] には、30 日間のルックバックウィンドウがあります。 また、ユーザーがAdvertising Cloudで追跡されている広告を通じてサイトにアクセスし、を離れ、45 日目に戻ってコンバージョンしたとします。 60 日間のルックバックウィンドウ内で変換がおこなわれたので、Advertising Cloudは最初の訪問に変換を結び付けます。 [!DNL Analytics]ただし、30 日間のルックバックウィンドウの有効期限が切れた後にコンバージョンが発生したので、は最初の訪問にコンバージョンを関連付けることができません。 この例では、Advertising Cloudのコンバージョン数は、 [!DNL Analytics] 」と入力します。

   ![Advertising Cloudに属するが属さないコンバージョンの例 [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **様々なアトリビューションモデルによる不一致の例：**

   ユーザーがコンバージョンをおこなう前に、3 つの異なるAdvertising Cloud広告を操作し、コンバージョンタイプに売上高を指定したとします。 Advertising Cloudレポートで、アトリビューションに均等配分モデルを使用する場合、すべての広告の売上高を均等にアトリビューションします。 If [!DNL Analytics] はラストタッチアトリビューションモデルを使用しますが、その後は売上高を最後の広告に関連付けます。 次の例では、Advertising Cloudは、3 つの広告のそれぞれに取り込まれた売上高の 30 米ドルのうち、10 米ドルを差し引いています。 [!DNL Analytics] は、ユーザーが最後に閲覧した広告に対する売上高の 30 USD すべてを属性にします。 Advertising Cloudと [!DNL Analytics]の場合、アトリビューションの違いの影響を確認できます。

   ![Advertising Cloudと [!DNL Analytics] 様々なアトリビューションモデルに基づいて](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>ベストプラクティスは、Advertising Cloudと [!DNL Analytics]. の使用 [!DNL Adobe] 必要に応じて、現在の設定を特定し、設定の同期を維持するためのアカウントマネージャー。

これらの同じ概念は、異なるルックバックウィンドウやアトリビューションモデルを使用する他のチャネルなどにも当てはまります。

#### ビュースルートラッキングのための様々なルックバックウィンドウ {#impression-lookback}

Advertising Cloudでは、アトリビューションはクリック数とインプレッション数に基づいており、クリック数やインプレッション数に応じて様々なルックバックウィンドウを設定できます。 In [!DNL Analytics]ただし、アトリビューションはクリックスルーとビュースルーに基づいており、クリックスルーとビュースルーに対して異なるアトリビューションウィンドウを設定するオプションはありません。のトラッキングは、サイトの初回訪問時に開始されます。 インプレッションは、ビュースルーが発生する同じ日または複数日前に発生する可能性があり、これは各システムでアトリビューションウィンドウが開始する場所に影響を与える可能性があります。

通常、ビュースルーコンバージョンの大部分は迅速に発生し、両方のシステムがクレジットを考慮に入れます。 ただし、Advertising Cloudインプレッションのルックバックウィンドウの外側で、 [!DNL Analytics] ルックバックウィンドウこのような変換は、 [!DNL Analytics] しかしAdvertising Cloudの印象には

次の例では、訪問者が 1 日目に広告を提供し、2 日目にビュースルー訪問（つまり、広告を以前にクリックせずに広告のランディングページを訪問）を実行し、45 日目に変換したとします。 この場合、Advertising Cloudは（14 日間のルックバックを使用して）Days 1 ～ 14 のユーザーを追跡します。 [!DNL Analytics] が 2 ～ 61 日（60 日間のルックバックを使用）からユーザーを追跡し、45 日目のコンバージョンは [!DNL Analytics] しかしAdvertising Cloudの中では

![に属するビュースルーコンバージョンの例 [!DNL Analytics] しかしAdvertising Cloudは](/help/integrations/assets/a4adc-viewthrough-example.png)

不一致のさらなる原因は、Advertising Cloudでは、ビュースルーコンバージョンをカスタム *ビュースルーの重み* これは、クリックベースの変換に起因する重みに対して相対的です。 デフォルトのビュースルーの重み付けは 40%です。つまり、ビュースルーのコンバージョンは、クリックベースのコンバージョンの値の 40%としてカウントされます。 [!DNL Analytics] では、ビュースルーコンバージョンにこのような重み付けはおこなわれません。 例えば、 [!DNL Analytics] は、デフォルトのビュースルーの重み付け（60 USD の違い）を使用している場合、Advertising Cloudで 40 USD に割引されます。

Advertising Cloudと [!DNL Analytics] レポート。

#### 使用可能なアトリビューションモデル

| Advertising Cloud Attribution | [!DNL Analytics] 帰属 | eVar/rVar の配分 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | 該当なし | 該当なし |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>使用しない* |
| [!UICONTROL Weight Last Event More] | 該当なし | 該当なし |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | 該当なし |
| 該当なし | [!UICONTROL J-Shaped] | 該当なし |
| 該当なし | [!UICONTROL Inverse-J] | 該当なし |
| 該当なし | [!UICONTROL Custom] | 該当なし |
| 該当なし | [!UICONTROL Participation] | 該当なし |
| 該当なし | [!UICONTROL Algorithmic] | 該当なし |

>[!NOTE]
>
>線形配分の場合、 [!DNL Analytics] 属性は、1 回の訪問でのすべてのeVar値に均等に配分されるので、線形配分を使用し、「訪問」のeVarの有効期限を設定します。 ただし、広告の場合、線形アトリビューションを使用すると、配分が線形ではなく、理想的なレポートよりも短くなります。 例えば、訪問者が 3 つの広告を操作してから 3 回の個別の訪問にコンバージョンした場合、最後の訪問で表示された広告のみが、3 つすべての広告ではなく、コンバージョンに関連付けられます。
>
>また、「線形」へのコンバージョン配分を切り替えたり、「線形」から切り替えたりすると、履歴データが表示されなくなり、レポートに誤ったデータが表示される可能性があります。 例えば、線形配分では売上高を様々なeVar値で割ることができます。 配分を「最新」に変更すると、その売上高の 100%が最新の単一値に関連付けられます。 この関連付けは、誤った結論を導く可能性があります。
>
>混乱を防ぐために [!DNL Analytics] は、レポートインターフェイスで履歴データを使用できなくします。 履歴eVarは、eVar割り当て設定を変更して履歴データにアクセスするだけではなく、データを初期割り当て設定に戻した場合に表示できます。 Adobeでは、既に大量の履歴eVarを持つeVarの割り当て設定を変更するのではなく、記録済みのデータに対して新しい割り当て設定を適用する場合に、新しいデータを使用することをお勧めします。

以下の [!DNL Analytics] アトリビューションモデルとその定義 ( [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Advertising Cloudにログインしている場合、アトリビューションモデルのリストは、
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm).

#### Advertising Cloudのイベント日アトリビューション

Advertising Cloudでは、関連するクリック日/イベント日（クリックイベントまたはインプレッションイベントの日付）またはトランザクション日（コンバージョン日）のいずれかで、コンバージョンデータをレポートできます。 クリック/イベント日付レポートの概念は、 [!DNL Analytics];で追跡されているすべてのコンバージョン [!DNL Analytics] トランザクション日別にレポートされます。 その結果、Advertising Cloudでは同じコンバージョンが異なる日付でレポートされ、 [!DNL Analytics]. 例えば、1 月 1 日に広告をクリックし、1 月 5 日にコンバージョンするユーザーを考えてみましょう。 Advertising Cloudでイベント日別にコンバージョンデータを表示している場合、クリックが発生した 1 月 1 日にコンバージョンがレポートされます。 In [!DNL Analytics]の場合、同じコンバージョンが 1 月 5 日にレポートされます。

![異なる日付に関連付けられたコンバージョンの例](/help/integrations/assets/a4adc-conversions-based-on.png)

## のアトリビューション [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] レポート](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html) では、ヒット情報の様々な側面に基づいて様々なマーケティングチャネルを識別するルールを設定できます。 Advertising Cloudで追跡されたチャネル ([!UICONTROL Display Click Through], [!UICONTROL Display View Through]および [!UICONTROL Paid Search]) [!DNL Marketing Channels] を使用して、 `ef_id` チャネルを識別するクエリー文字列パラメーター。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> ただし、 [!DNL Marketing Channels] レポートではAdvertising Cloudチャネルを追跡できますが、いくつかの理由でデータがAdvertising Cloudレポートと一致しない場合があります。 詳しくは、次の節を参照してください。

>[!NOTE]
>
> 次の中心概念は、Advertising Cloudで追跡されないキャンペーン ( [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) 変数 (「トラッキングコード」Dimensionまたは「eVar0」とも呼ばれます ) とカスタムeVarトラッキング。

### では様々なアトリビューションモデルが生成される可能性がある [!DNL Marketing Channels]

最も多い [!DNL Marketing Channels] レポートは、 [!UICONTROL Last Touch] アトリビューション。最後に検出されたマーケティングチャネルに、コンバージョン値の 100%が割り当てられます。 の様々なアトリビューションモデルの使用 [!DNL Marketing Channels] レポートとAdvertising Cloudレポートでは、属性別コンバージョンの不一致が生じます。

### のルックバックウィンドウが異なる可能性がある [!DNL Marketing Channels]

のルックバックウィンドウ [!DNL Marketing Channels] カスタマイズ可能です。 Advertising Cloudでは、クリックのルックバックウィンドウは設定できますが、60 日間の固定ウィンドウは一般的です。 2 つの製品で異なるルックバックウィンドウが使用されている場合は、データの相違が生じる可能性があります。

### での様々なチャネルアトリビューション [!DNL Marketing Channels]

Advertising Cloudレポートは、Advertising Cloud(Advertising Cloud Search広告の有料検索とAdvertising Cloud DSP広告の表示 ) を介してトラフィックされた有料メディアのみをキャプチャします。 [!DNL Marketing Channels] レポートでは、すべてのデジタルチャネルを追跡できます。 その結果、コンバージョンに関連するチャネルに矛盾が生じる可能性があります。

例えば、有料検索と自然検索のチャネルは、多くの場合共生的な関係を持ち、各チャネルが相互に支援します。 10. [!DNL Marketing Channels] レポートは、Advertising Cloudが自然検索を追跡しないのではない自然検索のコンバージョンを、一部のコンバージョンと見なします。

また、ディスプレイ広告を表示し、有料検索広告をクリックし、電子メールメッセージ内をクリックして、30 米ドルの注文をする顧客も考えます。 たとえAdvertising Cloudと [!DNL Marketing Channels] 両方のラストタッチアトリビューションモデルを使用している場合でも、コンバージョンのアトリビューションはそれぞれ異なります。 Advertising Cloudは [!UICONTROL Email] チャネルにコンバージョンの有料検索のクレジットが付与されます。 [!DNL Marketing Channels]ただし、は 3 つのチャネルすべてにアクセスできるので、 [!UICONTROL Email] を返します。

![Advertising Cloudと [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

指標が異なる理由について詳しくは、[Advertising Cloudと [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).」

## Adobe Analyticsのデータの違い [!DNL Paid Search Detection]

10. [レガシー [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) 特徴 [!DNL Analytics] 企業が [有料およびオーガニック検索トラフィックを追跡するルールを定義する](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) （特定の検索エンジンの場合） 10. [!DNL Paid Search Detection] ルールでは、クエリ文字列と参照ドメインの両方を使用して、有料検索トラフィックと自然検索トラフィックを識別します。 10. [!DNL Paid Search Detection] レポートは、 [検索方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) レポート。指定したイベント（買い物かごのチェックアウトなど）が発生したとき、または訪問が終了したときに期限切れになります。

次に、 [!DNL Paid Search Detection] ルールセット：

![有料検索検知ルールの例 ( [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

結果 [!DNL Paid Search Detection] レポートには、 [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine]および [!UICONTROL Natural Search Keywords] レポート。

のデータには、次の 2 つの制限があります [!DNL Paid Search Detection] レポート：

* 10. [!UICONTROL Paid Search Keywords] および [!UICONTROL Natural Search Keywords] レポートには、ユーザーが入札するキーワードではなく、参照 URL で識別される検索クエリが表示されます。 Advertising Cloudと [!DNL Analytics] レポートには実際のキーワードが表示されるので、 [!DNL Paid Search Detection] キーワードレポート。

* この [!DNL Paid Search Detection] 元々の検索クエリ（検索エンジンの検索バーにユーザーが入力した文字列）は、参照 URL を使用して、より簡単に広告主に提供されるようになりました。 現在、検索エンジンは、検索クエリと [!DNL Paid Search Detection] ほとんどのクエリデータが「未指定」に該当するので、キーワードレポートの値は制限されます。

   を使用 [!DNL Analytics for Advertising Cloud]を使用して、広告主は有料キーワードを引き続き追跡できます。 [!DNL Analytics]. 参照ドメインは、トラフィックを駆動した検索エンジンをエンジンレポートに知らせます。 広告主固有のアカウント情報は参照ドメインに結び付けられないので、すべてのトラフィックが検索エンジンの下に表示されます。 同じ検索エンジンに複数のアカウントを持つ広告主は、Advertising Cloudまたは [!DNL Analytics] レポートを参照してください。

### 設定する理由 [!DNL Paid Search Detection]?

10. [!DNL Paid Search Detection] レポートでは、 [[!DNL Analytics Marketing Channels] レポート](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html). 有料検索トラフィックと自然検索トラフィックを区別することは、自然検索がフルマーケティングエコシステムにもたらす価値を理解する優れた方法です。

## クリックスルーデータの検証： [!DNL Analytics for Advertising Cloud] {#data-validation}

統合の場合は、クリックスルーデータを検証して、サイト上のすべてのページでクリックスルーが適切に追跡されていることを確認する必要があります。

In [!DNL Analytics]（を検証する最も簡単な方法の 1 つ） [!DNL Analytics for Advertising Cloud] 追跡は、「AMO ID インスタンスへのクリック数」計算指標を使用して、クリック数をインスタンスと比較するものです。この指標は次のように計算されます。

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] は、AMO ID の数 (`s_kwcid` パラメーター ) は、サイトで追跡されます。 広告がクリックされるたびに、 `s_kwcid` パラメーターがランディングページの URL に追加されます。 数 [!UICONTROL AMO ID Instances]したがって、はクリック数に似ており、実際の広告クリックに対して検証できます。 通常、のマッチ率は 80%です。 [!DNL Search] に対して 30%の一致率 [!DNL DSP] トラフィック（クリックスルーのみを含むようにフィルタリングした場合） [!UICONTROL AMO ID Instances]) をクリックします。 検索と表示の期待値の違いは、予想されるトラフィック行動によって説明できます。 検索は意図をキャプチャし、そのため、ユーザーは通常、クエリの検索結果をクリックする必要があります。 ただし、ディスプレイ広告やオンラインビデオ広告を見たユーザーは、意図せずに広告をクリックした後、サイトからバウンスするか、ページアクティビティが追跡される前に読み込まれる新しいウィンドウを破棄する可能性が高くなります。

Advertising Cloudレポートでは、[!UICONTROL ef_id_instances]「」指標 ( [!UICONTROL AMO ID Instances]:

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

AMO ID と EF ID の間で高い一致率が予想されますが、AMO ID と EF ID は基本的に異なるデータを追跡するので、100%のパリティは期待しないでください。この違いは、合計のわずかな違いを招く可能性があります [!UICONTROL AMO ID Instances] および [!UICONTROL EF ID Instances]. 合計 [!UICONTROL AMO ID Instances] in [!DNL Analytics] ～とは異なる [!UICONTROL EF ID Instances] ただし、Advertising Cloudでは、 [!DNL Adobe] アカウントマネージャーを参照してください。

AMO ID と EF ID について詳しくは、 [Analytics で使用されるAdvertising Cloud ID](ids.md).

次に、インスタンスに対するクリック数を追跡するワークスペースの例を示します。

![インスタンスに対するクリック数を追跡するワークスペースの例](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## でのデータセットの比較 [!DNL Analytics for Advertising Cloud] Advertising Cloudとの比較

10. [AMO ID](ids.md) （s_kwcid クエリー文字列パラメーター）は、 [!DNL Analytics]、および [EF ID](ids.md) は、Advertising Cloudのレポートに使用されます。 異なる値なので、1 つの値が破損したり、ランディングページに追加されなかったりする可能性があります。

例えば、次のランディングページがあるとします。

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

EF ID は「`test_ef_id`」で、AMO ID は「`test_amo_id`.」

サイト側のリダイレクトが発生した場合、URL は次のようになります。

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

EF ID は「`test_ef_id`」で、AMO ID は「`test_amo_id#redirectAnchorTag`.」

この例では、アンカータグを追加すると、AMO ID に予期しない文字が追加されるので、Analytics では値が認識されません。 この AMO ID は分類されず、それに関連付けられたコンバージョンは「[!UICONTROL unspecified]&quot;または&quot;[!UICONTROL none]」が [!DNL Analytics] レポート。

幸いにも、このような問題は一般的ですが、一般的に大きな食い違いは生じません。 ただし、 [!DNL Analytics] およびAdvertising Cloudの EF ID。 [!DNL Adobe] アカウントマネージャーを参照してください。

## その他の指標に関する考慮事項

### クリック数と訪問数の違い {#clicks-vs-visits}

似ていますが、クリック数と訪問数は異なるデータを表します。

* **クリック：** [!DNL DSP] または、訪問者がパブリッシャーの Web サイトで広告をクリックした場合に、クリックを記録します。

* **訪問：** [!DNL Analytics] を定義する [訪問](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) を使用して、無操作状態が 30 分間続くなど、いくつかの条件のいずれかに従って終了する、ユーザーによる一連のページビュー数として渡されます。

定義によると、1 回のクリックで複数の訪問が発生する可能性があります。

次の例を考えてみましょう。ユーザー 1 とユーザー 2 の両方が、Advertising Cloud広告をクリックしてサイトにアクセスします。 ユーザー 1 は 4 つのページを閲覧し、その日は離れたので、最初のクリックは 1 回の訪問になります。 ユーザー 2 が 2 ページを閲覧し、45 分の昼食を取るために出て、戻り、さらに 2 ページを閲覧し、出て行く。この場合、最初のクリックは 2 回の訪問になります。

![クリック数と訪問数の違いの例](/help/integrations/assets/a4adc-visits-example.png)

### クリック数とクリックスルー数の違い

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

クリック数とクリックスルー数は、2 つの異なる指標です。

* **クリック：** [!DNL DSP] または、訪問者がパブリッシャーの Web サイトで広告をクリックした場合に、クリックを記録します。

* **クリックスルー：** [!DNL Analytics] は、訪問者が宛先の Web サイトに到着したときのクリックスルー、ランディングページの読み込み、 [!DNL Analytics] ページ下部のリクエストは、 [!DNL Analytics].

クリック数とクリックスルー数は、誤った広告クリック数があるので、大きく異なる場合があります。 ディスプレイ広告でのほとんどのクリックは誤ってクリックされ、これらの誤った訪問者がランディングページを読み込む前に「戻る」ボタンを押したので、 [!DNL Analytics] クリックスルーを記録できない。 これは、特に、モバイル広告、ビデオ広告、広告など、誤ってクリックされる可能性が高い広告で特に当てはまります。広告は、画面いっぱいに表示され、ユーザーがページを表示する前に閉じる必要があります。

また、モバイルデバイスに読み込まれたサイトでは、帯域幅が低く処理能力が高く、ランディングページの読み込みに時間がかかるので、クリックスルーが発生する可能性が低くなります。 50 ～ 70%のクリックでクリックスルーに至らないことは珍しくありません。 モバイル環境では、この差は 90%まで高くなります。これは、低速のブラウザーを組み合わせると、ページをスクロールしたり広告を閉じようとしたときにユーザーが誤って広告をクリックする可能性が高くなるからです。

クリックデータは、現在の追跡メカニズム（モバイルアプリへのクリック、モバイルアプリからのクリックなど）でクリックスルーを記録できない環境や、1 つの追跡手法のみを導入した環境（JavaScript のビュースルーアプローチでは、サードパーティ Cookie をブロックするブラウザーはクリックスルーではない）にも記録されます。 Adobeがクリック URL の追跡方法とビュースルー JavaScript の追跡方法の両方をデプロイすることを推奨する主な理由は、追跡可能なクリックスルーの範囲を最大限に広げることです。

### Advertising Cloud以外のDimensionに対するAdvertising Cloudトラフィック指標の使用

Advertising Cloudは、 [広告固有のトラフィック指標およびDSPと Search からの関連ディメンション](advertising-cloud-metrics-in-analytics.md). Advertising Cloudが提供する指標は、指定されたAdvertising Cloudディメンションにのみ適用でき、 [!DNL Analytics].

例えば、 [!UICONTROL AMO Clicks] および [!UICONTROL AMO Cost] Advertising Cloudのディメンションであるアカウント別の指標を選択すると、合計が表示されます [!UICONTROL AMO Clicks] および [!UICONTROL AMO Cost] アカウント別。

![Advertising Cloudディメンションを使用したレポート内のAdvertising Cloud指標の例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

ただし、 [!UICONTROL AMO Clicks] および [!UICONTROL AMO Cost] Advertising Cloudがデータを提供しないページ上のディメンション（ページなど）に基づく指標の場合、 [!UICONTROL AMO Clicks] および [!UICONTROL AMO Cost] 各ページの値は 0 になります。

![サポートされていないディメンションを使用したレポート内のAdvertising Cloud指標の例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### の使用 [!UICONTROL AMO ID Instances] をAdvertising Cloud以外のDimensionのクリックの代わりに使用

を使用できないので、 [!UICONTROL AMO Clicks] オンサイトディメンションを使用すると、クリック数に相当するディメンションを見つけることができます。 訪問回数を代わりに使用したい場合がありますが、各訪問者が複数回訪問する可能性があるので、これらは最適な選択肢ではありません。 (「[クリック数と訪問数の違い](#clicks-vs-visits).」 代わりに、 [!UICONTROL AMO ID Instances]:AMO ID が取り込まれた回数です。 While [!UICONTROL AMO ID Instances] 一致しない [!UICONTROL AMO Clicks] 正確には、これらはサイト上のクリックトラフィックを測定する最適なオプションです。 詳しくは、[のデータ検証 [!DNL Analytics for Advertising Cloud]](#data-validation).」

![の例 [!UICONTROL AMO ID Instances] 代わりに [!UICONTROL AMO Clicks] サポートされていないディメンションの](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud ID で使用 [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Analysis WorkspaceのAdvertising Cloud指標](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloudのデータ](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)
>* [Advertising Cloudと [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

