---
title: 配置設定
description: 使用可能な配置設定の説明を参照してください。
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '3281'
ht-degree: 0%

---

# 配置設定

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** 配置名。

>[!TIP]
>状況に合った命名規則を使用します。 推奨される命名規則の1つは、「*\&lt;キャンペーン名\>」です。\&lt;広告単位\>:\&lt;期間\>:\&lt;ターゲット設定\>*.&quot;

**[!UICONTROL Status]:** 配置ステータス： *[!UICONTROL Active]* （デフォルト）または *[!UICONTROL Paused]*。

>[!TIP]
>配置を開始する準備が整うまで一時停止することをお勧めします。

**[!UICONTROL Details]:** （読み取り専用）該当する広告タイプ、プレースメントを作成または作成したアカウント、親キャンペーン。詳細を確認するには、**[!UICONTROL Show more]**&#x200B;をクリックします。

**[!UICONTROL Templates]:** 既存の配置テンプレートのリストを開きます。テンプレートからターゲティング設定を自動入力するには：

1. 次のいずれかの操作を行います。

   * テンプレートのすべてのターゲットを再利用するには、テンプレート名の横にあるチェックボックスをオンにします。

   * テンプレートから個々のターゲットタイプを再利用するには、テンプレート名を展開し、再利用するターゲットタイプの横にあるチェックボックスをオンにします。

1. クリック **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** （ビデオ広告フォーマットのみ）広告の期間や広告の仕様。右側の予測投影法の計算に使用されます。フィールドは広告タイプによって異なります。

**[!UICONTROL Placement tags]:** （オプション）この配置を見つけるのに役立つキーワードまたはニックネーム。

## 目標

**[!UICONTROL Package]:** （オプション）配置が割り当てられるパッケージ。「![編集](/help/dsp/assets/edit.png)」をクリックして、既存のパッケージを選択するか、新しいパッケージを作成します。 パッケージに配置を割り当てると、[!UICONTROL Goals]セクションが更新され、パッケージのフライト日、配信目標、予算が反映されます。

**[!UICONTROL Flight Dates]:** プレースメントの開始日と終了日。承認済みの広告は、配置がアクティブで、アクティブなパッケージまたはキャンペーンに割り当てられると、フライト中に実行する資格があります。

パッケージまたはキャンペーンの日付は、デフォルトで自動入力されます。

>[!NOTE]
>
>* フライト日は、キャンペーンのフライト日とパッケージのフライト日に含める必要があります。


### パッケージレベルのペーシングを使用してパッケージに割り当てられた配置

**[!UICONTROL Placement Funding]:** プレースメントの予算方法：

* *[!UICONTROL Optimize based on performance]:* パッケージレベルの予算を制御します。
* *[!UICONTROL Set a fixed budget cap]:* 日別、週別、月別、全時間の配置予算を設定できます。値と期間(*[!UICONTROL All time]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*)を入力します。

**[!UICONTROL Max Bid]:** 1000件のインプレッションに対して支払う上限。

**[!UICONTROL Placement Pre-bid Filters]:** 入札をおこなうために満たす必要がある最大5つのKPIしきい値（視認性の最小指標やクリックスルー率など）。事前入札フィルターを最適化戦術として使用できますが、各ルールでこの配置で入札できるオポチュニティが制限される可能性があることを理解してください。 フィルターを追加または編集するには：

1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
1. 次のいずれかの操作を行います。
   * フィルターを追加するには：
      1. クリック **[!UICONTROL Add Filter]**.
      1. **[!UICONTROL Only bid if]**&#x200B;の横にある指標を選択し、値を入力します。
   * フィルターを削除するには、フィルター行の&#x200B;**[!UICONTROL X]**&#x200B;をクリックします。
1. クリック **[!UICONTROL Save]**.

各入札前フィルターの説明については、「[配置レベルの入札前フィルターと使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md)」を参照してください。

### その他すべての配置

**[!UICONTROL Budget Goal]:** 総予算の上限と予算間隔(*[!UICONTROL All time]*、 *[!UICONTROL Daily]*、 *[!UICONTROL Weekly]*、 *[!UICONTROL Monthly]*)。

**[!UICONTROL Gross Budget Goal]:** （マージン管理を使用するキャンペーン内の配置のみ）総予算の上限と予算間隔(*[!UICONTROL All time]*、 *[!UICONTROL Daily]*、 *[!UICONTROL Weekly]*、 *[!UICONTROL Monthly]*)。

**[!UICONTROL Optimization Goal]:**  パッケージの最適化目標。各最適化目標の説明については、「[最適化目標とその使用方法](/help/dsp/optimization/optimization-goals.md)」を参照してください。

**[!UICONTROL Target Goal]:** パフォーマンスの追跡に使用されるターゲットの目標。

>[!NOTE]
>
>このフィールドは、ベンチマークに過ぎず、判定には使用されません。

**[!UICONTROL Pace on]:** どのペーシングが基になるか：

* **[!UICONTROL Budget goal]:** （デフォルト）割り当てられた予算内で可能な限り多くのインプレッションを配信します。

* **[!UICONTROL Impressions]:** このオプションは、指定した数量が指定した期間内に達するまで、インプレッション数を配信します。このオプションを選択する場合は、インプレッション数と間隔を指定します。*[!UICONTROL All time]、* *[!UICONTROL Daily]、* *[!UICONTROL Monthly]、*&#x200B;または&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Max Bid]:** 1000件のインプレッションに対して支払う上限。

**[!UICONTROL Pacing Fill Strategy]:** （パッケージレベルのペーシングのみを含むパッケージ）広告配信のペースを調整する方法：

* *[!UICONTROL Even]:* （デフォルト）各フライトを通して配信を均等に配置し、フライトの前半の配信のターゲットを50%に設定します。

* *[!UICONTROL Frontload]:* 配信を加速し、飛行の途中で65～75%完了するようにします。

* *[!UICONTROL Aggressive Frontload]:* 配信を加速し、75～85%が飛行の途中で完了するようにします。

**[!UICONTROL Placement Pre-bid Filters]:** （オプション）入札を実行するために満たす必要があるフィルターを5つまで選択します。事前入札フィルターを最適化戦術として使用できますが、各ルールでこの配置で入札できるオポチュニティが制限される場合があることに注意してください。 フィルターを追加または編集するには：

1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
1. 次のいずれかの操作を行います。
   * フィルターを追加するには：
      1. クリック **[!UICONTROL Add Filter]**.
      1. **[!UICONTROL Only bid if]**&#x200B;の横にある指標を選択し、値を入力します。
   * フィルターを削除するには、フィルター行の&#x200B;**[!UICONTROL X]**&#x200B;をクリックします。
1. クリック **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** （オプション）配置に広告を含めるまたは除外する特定の場所。場所を指定しない場合、すべての場所がターゲットになります。

>[!NOTE]
>
>市区町村とDMAの場所は、Rokuプレースメントでは使用できません。

場所を指定するには：

1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
1. 次のいずれかの操作を行います。
   * 国、都道府県、市区町村、DMA、連邦立法地区または州立法地区を含めるか除外するには：
      1. 左の列で場所のタイプを選択します。
      1. （必要に応じて）場所をクリックして展開します。
      1. 場所の横にある「*[!UICONTROL Include]*」をクリックしてターゲットとして含めるか、「*[!UICONTROL Exclude]*」をクリックしてターゲットとして除外します。
   * 郵便番号を検索し、選択したすべての結果を含めるか除外するには：
      1. クリック **[!UICONTROL Search Postal Code]**.
      1. 国を選択します。
      1. 都市名を入力し、[![編集](/help/dsp/assets/search.png)]をクリックします。
      1. 正しい検索結果をクリックします。
      1. *[!UICONTROL Include All]*&#x200B;をクリックしてすべての場所をターゲットとして含めるか、*[!UICONTROL Exclude All]*&#x200B;をクリックしてすべての場所をターゲットとして除外します。
   * 郵便番号を入力または貼り付け、すべてを含めるまたは除外するには、次の手順に従います。
      1. クリック **[!UICONTROL Paste Postal Code]**.
      1. 国を選択します。
      1. 最大1,000個の郵便番号を入力または貼り付けます。
1行に1つの郵便番号を含めるか、コンマまたはタブで区切って複数の値を入力します。
      1. *[!UICONTROL Include All]*&#x200B;をクリックしてすべての場所をターゲットとして含めるか、*[!UICONTROL Exclude All]*&#x200B;をクリックしてすべての場所をターゲットとして除外します。
   * [!UICONTROL Included]または[!UICONTROL Excluded]リストから場所を削除するには、右側の列で場所の横にある&#x200B;**[!UICONTROL X]**&#x200B;をクリックします。
1. クリック **[!UICONTROL Done]**.

>[!NOTE]
>
>* 都道府県、市区町村、郵便番号の場所がない国もあります。
>* DMA（指定販売地域）、連邦立法府および州立法府は、米国の場所でのみ使用できます。


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** ターゲットとして含めるまたは除外する在庫ソース。ほとんどの配置タイプでは、すべての在庫タイプと各タイプのすべてのソースがデフォルトで含まれます。 [!DNL Roku]配置の場合、在庫のタイプとソースを指定する必要があります。 次のタイプの在庫から選択できます。

* [!UICONTROL Public]:（Rokuを除くすべての配置タイプ）Advertising Cloudがアクセスできるオープン為替在庫。公開在庫を含めたり除外したりできます。

   リストは、ソース別またはフィード別に表示できます。 フィード別にリストを表示する場合、フィード名、フィードキーまたは選択した特性タグで検索できます。

* [!UICONTROL Private] |  [!UICONTROL Roku Private]:DSPで設定した発行者との既存の [!DNL Roku] 個人 [!DNL Roku] 取引（または既存の個人取引）。公開在庫を含めることはできますが、除外することはできません。

   リストは、キーワード、キー、ディールIDまたはカスタムタグで検索できます。

* [!UICONTROL On Demand] |  [!UICONTROL Roku On Demand]:購 [読したすべての [!UICONTROL On Demand] プレミアム、保証されない在庫](/help/dsp/inventory/on-demand-inventory-about.md) (またはプ [!UICONTROL On Demand] [!DNL] レースメン [!DNL Roku] トのRokuでの取引) [!DNL DSP]。[!UICONTROL On Demand]インベントリを含めたり除外したりできます。

   リストは、ソース別またはフィード別に表示できます。 フィード別にリストを表示する場合、フィード名、フィードキー、または選択した発行者の地域、カテゴリタグ、特性タグで検索できます。

在庫のターゲティングを指定するには：

* 在庫タイプを除外するには、名前の横にあるチェックボックスをオフにします。
* 在庫タイプをターゲットにする手順は、次のとおりです。
   1. 在庫タイプ名の横にあるチェックボックスを選択します。
   1. （オプション）以下を含めるようにソースを変更します。
      1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
      1. （[!UICONTROL Public]と[!UICONTROL On Demand]インベントリ）*[!UICONTROL *View by Source]**または&#x200B;**[!UICONTROL View by Feed]**&#x200B;をクリックして、ソースの表示方法を変更します。
      1. （該当する場合）必要に応じて在庫をフィルターします。
      1. 含めるソースと除外するソースを指定します。
         * [!UICONTROL Public]または[!UICONTROL On Demand]ソースを含めるには、ソース名の横にある&#x200B;**[!UICONTROL Include]**&#x200B;をクリックします。
         * [!UICONTROL Private]ソースを含めるには：
            * 1つの案件にすべての在庫を含めるには、取引名の横にある&#x200B;**[!UICONTROL Include all]**&#x200B;をクリックします。
            * 個々の在庫ソースを含めるには、取引名を展開し、ソース名の横にあるチェックボックスをクリックします。
         * [!UICONTROL Public]または[!UICONTROL On ]ソースを除外するには、ソース名の横にある&#x200B;**[!UICONTROL Exclude]**&#x200B;をクリックします。
   1. （オプション）ターゲット情報を含むCSVファイルをブラウザーのダウンロード場所にダウンロードするには、「**[!UICONTROL Save & Export]**」をクリックします。
   1. クリック **[!UICONTROL Save]**.

>[!TIP]
>
>[!UICONTROL On Demand]インベントリを購読したが、ターゲットとするパブリッシャーやオファーが見つからない場合は、オファーのステータスを確認します。 ステータスについて詳しくは、[ [!DNL On Demand] Premium Inventory](/help/dsp/inventory/on-demand-inventory-about.md)を参照してください。

**[!UICONTROL Exclude out-stream]:** （ビデオ配置のみ）アウトストリームトラフィックを除外します。

アウトストリーム広告は、通常、ビデオプレーヤーで通常のビデオ広告としてではなく、ポップアップとして、または（ネイティブエクスペリエンスで）コンテンツに詰め込まれてコンテンツ上に表示されます。

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** ターゲットにするトラフィックのタイプ。**[!UICONTROL Websites]**&#x200B;と&#x200B;**[!UICONTROL Apps]**&#x200B;のオプションがあります。

**[!UICONTROL Site tier]:** (がの場合に使 **[!UICONTROL Paste list of targeted sites]** 用可 *[!UICONTROL Off]*&#x200B;能)ターゲットとするサイトの品質。階層1 ～ 3はすべてブランドに安全で、DSPマッピングチームによって検証および承認されています。

* *[!UICONTROL Tier 1]:* 国内で認識可能なプレミアムサイトおよびアプリケーション。
* *[!UICONTROL Tier 2]:* Tier 1と、Tier 1よりも広く知られていない品質の高いサイトやアプリケーションをターゲットにします。
* *[!UICONTROL Tier 3]:* Tier 1 ～ 2に加え、ニッチなオーディエンスに対応する正当なブランドセーフのサイトおよびアプリケーションをターゲットに設定します。リーチまたはデータターゲティングの購入には階層3を使用します。
* *[!UICONTROL All Sites]:* ターゲット層1 ～ 3と、スクリーニングまたは分類されていない新しい在庫（リーチに使用できます）。

>[!NOTE]
>
>在庫は、配置の広告ユニットに固有です。

>[!TIP]
>
>パフォーマンスキャンペーンのベストプラクティスは、*[!UICONTROL All Sites]*&#x200B;を選択することです。

**[!UICONTROL Site Categories]:** (オプション。がの場合に使 **[!UICONTROL Paste list of targeted sites]** 用できま *[!UICONTROL Off]*&#x200B;す)選択したサイト層内のサイトカテゴリをターゲットとして含めるか除外するか（両方は不可）します。サイトの件名に基づいてAdvertising Cloudがマッピングした垂直サイトリストから選択します。

1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
1. 含めるまたは除外するサイトカテゴリを指定します。
   * サイトカテゴリを含めるには：
      1. クリック **[!UICONTROL Include categories]**.
      1. ターゲットとする各カテゴリの横にあるチェックボックスを選択します。
   * サイトカテゴリを除外するには：
      1. クリック **[!UICONTROL Exclude categories]**.
      1. 除外する各カテゴリの横にあるチェックボックスをオンにします。
1. （オプション）ターゲット情報を含むCSVファイルをブラウザーのダウンロード場所にダウンロードするには、「**[!UICONTROL Export]**」をクリックします。
1. クリック **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (オプション。がに該当する場 **[!UICONTROL Paste list of targeted sites]** 合に使 *[!UICONTROL Off]*&#x200B;用可能)除外するサイト。サイトの検索と選択、またはドメイン名の入力と貼り付けを行うことができます。

1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
1. サイトの指定：
   * サイトを検索するには：
      1. クリック **[!UICONTROL Search]**.
      1. キーワードを入力し、サイト層を選択し、サイトカテゴリを選択します。
      1. 検索結果で、除外するサイトを選択します。
         * 個々のサイトを除外するには、そのサイトの横にあるチェックボックスをオンにします。
         * （結果が50件を超える場合）最初の50件を除外するには、「**[!UICONTROL Exclude these 50]**」をクリックします。 すべての検索結果を除外するには、**[!UICONTROL Exclude these \<*NN *\>]**をクリックします。
   * ドメイン名を入力するには：
      1. クリック **[!UICONTROL Paste]**.
      1. 1つ以上のドメイン名を別々の行に入力します。
      1. クリック **[!UICONTROL Exclude All]**.
1. 終了したら&#x200B;**[!UICONTROL Done]**&#x200B;をクリックします。

>[!NOTE]
>
>* Advertising Cloud DSP [グローバルにブロックされたサイトリスト](/help/dsp/introduction/features/brand-safety-media-quality.md)（広告にとって安全でないと見なされるサイトも含む）に加えて、アカウントレベルおよび広告主レベルのブロックされたサイトリストも適用されます。
>* ブロックされたサイトのリストは、常にターゲットサイトのリストを上書きします。 配置が広告に対して除外され、同じターゲットを含む場合、そのターゲットは除外されます。


**[!UICONTROL Language]:** （オプション）ターゲットとする単一の言語。

**[!UICONTROL Site List Preview]:** （読み取り専用）配置のターゲットサイトとブロックされたサイト。

オプションで、ターゲットサイトとブロックサイトのリストをコンマ区切り値(CSV)ファイルとして書き出すことができます。 リストを書き出すには、**[!UICONTROL Export full site list]**&#x200B;をクリックし、ブラウザーの通常の手順に従ってファイルを開くか保存します。

<!-- **[!UICONTROL Allow unscreened sites]:** (XXX placements only) Allows you to XXXX.   Optional available for https://advertising.adobe.com/configurator/placement/edit/2432022 -->

**[!UICONTROL Paste list of targeted sites]:** 特定のサイトのみをターゲットにできます。このオプションを有効にすると、他のサイトターゲティングオプションは無効になります。

**[!UICONTROL Sites]:** (がの場合に使用 **[!UICONTROL Paste list of targeted sites]** 可能)ターゲ *[!UICONTROL On]*&#x200B;ットにするサイト。サイトの検索と選択、またはドメイン名の入力と貼り付けを行うことができます。

1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
1. サイトの指定：
   * サイトを検索するには：
      1. クリック **[!UICONTROL Search]**.
      1. キーワードを入力し、サイト層を選択し、サイトカテゴリを選択します。
      1. 検索結果で、含めるサイトを選択します。
         * 個々のサイトを除外するには、そのサイトの横にあるチェックボックスをオンにします。
         * （結果が50件を超える場合）最初の50件の結果を含めるには、**[!UICONTROL Include these 50]**&#x200B;をクリックします。 すべての検索結果を含めるには、**[!UICONTROL Include these \<*NN *\>]**をクリックします。
   * ドメイン名を入力するには：
      1. 「**[!UICONTROL Paste]**」をクリックします。
      1. 1つ以上のドメイン名を別々の行に入力します。
      1. クリック **[!UICONTROL Include All]**.
1. クリック **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** サードパーティセグメント、ファーストパーティセグメント、Adobeセグメン [ト、カスタムセグメント、保存済みオーディエンスを含む、配置のオーディエンスターゲット](/help/dsp/audiences/audience-settings.md)。選択したすべてのセグメントおよび保存されたオーディエンスの合計およびアクティブな重複排除オーディエンスサイズも表示されます。 既存のオーディエンスを選択したり、新しいオーディエンスを作成して後で再利用したり、特定のオーディエンスセグメントを選択したりできます。

* 既存のオーディエンスを選択するには、![[!UICONTROL Included Audiences]の横にある「](/help/dsp/assets/chevron-down.png)を選択」をクリックし、オーディエンスを選択します。
* 新しいオーディエンスを作成するには、![[!UICONTROL Included Audiences]の横にある「](/help/dsp/assets/chevron-down.png)を選択」をクリックし、「**[!UICONTROL + Create Audience]**」を選択します。 手順については、手順3から始まる「[再利用可能なオーディエンスの作成](/help/dsp/audiences/reusable-audience-create.md)」を参照してください。
* 特定のオーディエンスセグメントを選択するには、**[!UICONTROL Select segments for this placement only]**&#x200B;をクリックします。 セグメントロジックを選択します。手順については、「[再利用可能なオーディエンスの作成](/help/dsp/audiences/reusable-audience-create.md)」の手順6を参照してください。 完了したら、「**保存**」をクリックします。

**[!UICONTROL Excluded Audiences]:** サードパーティセグメントを持つオーディエンス、ファーストパーティセグメント、Adobeセグメント、カスタムセグメント、保存済みオーディエンスを含む、配置の対象として除外するオーディエンス [](/help/dsp/audiences/audience-settings.md)。除外されたすべてのオーディエンスの合計およびアクティブな重複排除オーディエンスのサイズも表示されます。 既存のオーディエンスを選択するか、新しいオーディエンスを作成して後で再利用できます。

* 既存のオーディエンスを選択するには、![[!UICONTROL Excluded Audiences]の横にある「](/help/dsp/assets/chevron-down.png)を選択」をクリックし、オーディエンスを選択します。
* 新しいオーディエンスを作成するには、![[!UICONTROL Excluded Audiences]の横にある「](/help/dsp/assets/chevron-down.png)を選択」をクリックし、「**+オーディエンスを作成**」を選択します。 手順については、手順3から始まる「[再利用可能なオーディエンスの作成](/help/dsp/audiences/reusable-audience-create.md)」を参照してください。

**[!UICONTROL Cross Device Targeting]:** (1つ以上のセグメントまたはオーディエンスを選択し、キャンペーンがユーザーベースのクロスデバイスターゲティング用 [に設定されている場合に使用できます](/help/dsp/campaign-management/campaigns/campaign-settings.md)。指定したセグメントに含まれていないデバイスも含め、（キャンペーン設定で指定したデバイスグラフに従って）ユーザーのすべての既知のデバイスにわたってターゲティングを拡張できます。 費用は、キャンペーン用に指定されたグラフに応じて適用されます。 デバイスグラフデータは、現在、北米でのみ使用できます。

**[!UICONTROL Placement Cap]:** （オプション）（指定したに応じて）一意のデバイスまたはユーザーがプレースメントから広告を [!UICONTROL Cross Device Level]提供される回数。*[!UICONTROL Unlimited]*&#x200B;や、日、週、月ごとの特定の金額を選択できます。

>[!NOTE]
>
> 頻度キャップは、キャンペーン、パッケージおよび配置レベルで設定できます。 DSPは、キャンペーン階層で最も厳格な頻度キャップを尊重します。

**[!UICONTROL Secondary Cap]:** (オプション。数値を含める場合に使用できま [!UICONTROL Placement Cap]す)プライマリ配置キャップの範囲内に追加の制限があります。インプレッション数と期間（12時間あたり3回など）を選択します。

**[!UICONTROL Day Parting]:** （オプション）広告が実行される曜日と時刻を指定します。時間帯区分間隔を指定するには：
1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
1. 適切なタイムゾーンを選択します。
1. 間隔を指定します。
   * あらかじめ設定されている間隔を選択するには、いずれかの間隔ボタンをクリックします。 オプションには、*[!UICONTROL Weekends]**、*[!UICONTROL Weekdays]*、*[!UICONTROL Morning]*、*[!UICONTROL Lunch]*、*[!UICONTROL Dinner]*、*[!UICONTROL Prime]*(primetime)があります。
   * 間隔を手動で選択するには、セル内をクリックし、必要に応じてドラッグして間隔を選択します。
1. クリック **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (オプション。とセグメントで設定した広告主 [!DNL Comscore] が使用で [!DNL Grapeshot] きる)、およびから特定のセグメント名またはIDを使 [!DNL Comscore] 用し [!DNL Grapeshot] て、ターゲットに含めます。この機能には追加料金が適用される場合があります。 この機能を有効にしてトピックセグメントを設定するには、担当のAdobeアカウントマネージャーにお問い合わせください。

トピックのターゲットを指定するには：

1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
1. ターゲットとするセグメントを指定します。
   1. 左側の列で、パートナー（*[!UICONTROL Comscore]*&#x200B;または&#x200B;*[!UICONTROL Grapeshot]*）を選択します。
   1. 入力フィールドに、セグメント名またはセグメントIDを入力します。
1. （オプション）トピック情報を含んだCSVファイルをブラウザーのダウンロード場所にダウンロードするには、「**[!UICONTROL Export]**」をクリックします。
1. クリック **[!UICONTROL Save]**.

>[!TIP]
>
>* トピックのターゲティングは、配置で入札できる在庫を制限するので、購入全体のごく一部に対してのみトピックのターゲティングを使用します。
>
>* [!DNL Comscore]または[!DNL Grapeshot]でセグメント内に負のターゲットを設定します。


**[!UICONTROL Device Targeting]:** （オプション）ターゲットとして含めたり除外したりする特定のデバイス情報（デバイスの種類、製造元、オペレーティングシステム、ブラウザー、接続の種類など）。デバイスのターゲット設定を指定するには：

1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
1. 含めるまたは除外するデバイスの詳細を指定します。
   1. 左側の列で、カテゴリを選択します。
   1. ターゲット設定の指定：
      * 値を含めるには、値名の横にある&#x200B;**[!UICONTROL Include]**&#x200B;をクリックします。
      * 値を除外するには、値名の横にある&#x200B;**[!UICONTROL Exclude]**&#x200B;をクリックします。
1. （オプション）デバイスのターゲット情報を含むCSVファイルをブラウザーのダウンロード場所にダウンロードするには、「**[!UICONTROL Export]**」をクリックします。
1. クリック **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** （オプション）ターゲットとして含めるか除外するか（両方は除外しない）を指定する特定のインターネットサービスプロバイダー(ISP)。ISPのターゲティングを指定するには：

1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
1. 含めるまたは除外するISPを指定します。
   * ISPを含めるには：
      1. クリック **[!UICONTROL Include ISPs]**.
      1. （オプション）キーワードでリストをフィルターします。
      1. ターゲットとする各ISPの横にあるチェックボックスをオンにします。
   * ISPを除外するには：
      1. クリック **[!UICONTROL Exclude ISPs]**.
      1. （オプション）キーワードでリストをフィルターします。
      1. 除外する各ISPの横にあるチェックボックスをオンにします。
1. （オプション）ISPのターゲット情報を含むCSVファイルをブラウザーのダウンロード場所にダウンロードするには、**[!UICONTROL Export]**&#x200B;をクリックします。
1. クリック **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** 適用する [!DNL Comscore]、、、およびコンテキ [!DNL DoubleVerify]ストフィ [!DNL Integral Ad Science]ルターの [!DNL Peer39] タイプ。広告主レベルのデフォルトは、新しい配置に対して選択されますが、設定は変更できます。

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** （オプション）デフォルトでブロックする1つ以上のタイプの在庫コンテキスト。追加料金が適用される場合があります。

* [!UICONTROL Peer 39]:

   * **ターゲットサイト：** （オプション）デフォルトでターゲットにする1つ以上の在庫属性。追加料金が適用される場合があります。

* [!UICONTROL ComScore]:

   * **次のサイトをブロックする：** （オプション）デフォルトでブロックする1つ以上の在庫属性タイプ。追加料金が適用される場合があります。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** （オプション）デフォルトで広告をブロックする成人向けコンテンツの程度。 *[!UICONTROL Do Not Block]* （デフォルト）、 *[!UICONTROL Standard]*&#x200B;または *[!UICONTROL Strict]*。追加料金が適用される場合があります。

   * **[!UICONTROL Alcohol Content]:** （オプション）デフォルトで広告をブロックするアルコールコンテンツの程度。 *[!UICONTROL Do Not Block]* （デフォルト）、 *[!UICONTROL Standard]*&#x200B;または *[!UICONTROL Strict]*。追加料金が適用される場合があります。

**[!UICONTROL Pre-bid fraud blocking]:** 不正なトラフィックや、およびで測定された疑わしいアクティビティに基づいてブロックす [!DNL DoubleVerify]るサイト [!DNL Integral Ad Science]のタイプ。 [!DNL Peer39]広告主レベルのデフォルトは、新しい配置に対して選択されますが、設定は変更できます。

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** デフォルトでは、は、新しい配置に対して、ハイジャックされたデバイス上のトラフィックを含む、100%の無効なトラフィックをすべてブロックします。追加料金が適用される場合があります。

   * **[!UICONTROL Also block sites with]:** （オプション）デフォルトでDSPが広告をブロックする原因となる、追加レベルの詐欺および無効なトラフィック：  *[!UICONTROL None]* （追加のトラフィックをブロックしないデフォルト）、 *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*、 *[!UICONTROL >4% Average Fraud/IVT levels]*、 *[!UICONTROL >6% Average Fraud/IVT levels]*、 *[!UICONTROL >10% Average Fraud/IVT levels]*、または *[!UICONTROL >25% Average Fraud/IVT levels]*。追加料金が適用される場合があります。

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** （オプション）DSPがデフォルトで広告をブロックする1つ以上のタイプの詐欺 *[!UICONTROL Fraud]* （詐欺のあるすべてのサイトをブロックします）、 *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*、または（または） *[!UICONTROL Fraud: Zero Ads]*。追加料金が適用される場合があります。

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** （オプション）DSPがデフォルトで広告をブロックする原因となる、疑わしいWebサイトまたはアプリアクティビティのタイプ。 *[!UICONTROL None]* （疑わしいアクティビティに基づいて広告をブロックしないデフォルト）、 *[!UICONTROL Suspicious Activity - High Risk]*、または *[!UICONTROL Suspicious Activity - High or Moderate Risk]*。追加料金が適用される場合があります。

**[!UICONTROL Ads.txt filtering]:**

各発行者のAuthorized Digital Sellersリストを活用して、使用する[Ads.txt](https://iabtechlab.com/ads-txt-about/)入札前のフィルタリングのレベル。 広告主レベルのデフォルトは、新しい配置に対して選択されますが、設定は変更できます。

* *[!UICONTROL Opt out of ads.txt (default)]*:全ての売り手から在庫を買う。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*:ドメインの承認済みダイレクトセラーおよびリセラーからの購入在庫を優先する。
* *[!UICONTROL Ads.txt sellers only]*:ドメインの許可された直接販売者および再販売者からのみ在庫を購入する。
* *[!UICONTROL Ads.txt sellers only]*:ドメインの許可された直接販売者からのみ在庫を購入する。

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (オプションを使用して設定された [!UICONTROL DoubleVerify Authentic Brand Safety] 広告主) [!DNL DoubleVerify Authentic Brand Safety]を有効にし、指定したセグメントIDに対して設定されたカスタムブランド安全ルールを使用して、入札後のインプレッションをブロックします。DSPは、広告主設定で指定されたセグメントIDの使用を考慮してアカウントを請求します。

## [!UICONTROL Tracking]

>[!NOTE]
>
>（[!DNL Roku]プレースメント） [!DNL Roku]が承認したサードパーティのトラッキングベンダーには、[!DNL Acxiom]、[!DNL comScore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、13/>、[!DNL Placed]、[!DNL Polk]、および[!DNL Research Now]。[!DNL Marketing Evolution][!DNL Oracle]

**[!UICONTROL Event Pixels]:** （オプション）配置のすべての新しい広告にデフォルトで添付されるサードパーティのイベント追跡ピクセル。イベントのピクセルを指定するには：

1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
1. 次のいずれかの操作を行います。
   * 既存のピクセルを選択するには、ピクセル行のチェックボックスをオンにします。
   * 新しいピクセルを作成するには：
      1. クリック **[!UICONTROL Create]**.
      1. 次の情報を入力します。
         * **[!UICONTROL Pixel name]:** ピクセル名。最大長は500文字です。ピクセルを簡単に識別できる名前を使用します。
         * **[!UICONTROL Pixel event fires on]:** 実行するピクセルをトリガー化するイベント。使用可能なイベントは、広告のタイプによって異なります。
         * **[!UICONTROL Pixel type]:** ピクセルが(1 x  *[!UICONTROL IMG URL]* 1ピクセルの画像ファイル)、またはの *[!UICONTROL HTML]*&#x200B;どちらであるか。 *[!UICONTROL JavaScript URL]*
         * **[!UICONTROL Pixel URL]:** ピクセル画像のURL。
      1. クリック **[!UICONTROL Create and attach]**.
   1. クリック **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** （オプション）配置内のすべての新しい広告にデフォルトで添付されるコンバージョントラッキングピクセル。変換ピクセルを指定するには：

1. 「![編集](/help/dsp/assets/edit.png)」をクリックします。
1. 次のいずれかの操作を行います。
   * 既存のピクセルを選択するには、ピクセル行のチェックボックスをオンにします。
   * 新しいピクセルを作成するには：
      1. クリック **[!UICONTROL Create]**.
      1. 次の情報を入力します。
         * **[!UICONTROL Conversion pixel name]:** ピクセル名。最大長は500文字です。ピクセルを簡単に識別できる名前を使用します。
         * **[!UICONTROL Conversion category]:** 変換のタイプ。
         * **[!UICONTROL Impression conversion window]:** インプレッションがコンバージョンに関連付けられる広告インプレッションが発生してからの日数。デフォルトは30日です。
         * **[!UICONTROL Click conversion window]:** 広告クリックが発生してからの日数で、クリックがコンバージョンに関連付けられる可能性がある。デフォルトは30日です。
         * **[!UICONTROL Notes]:** （オプション）ピクセルに関する説明またはその他の情報。
      1. クリック **[!UICONTROL Create and attach]**.
      1. 関連するWebページにコンバージョンピクセルを実装します。
         1. メインメニューで、**[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**&#x200B;に移動します。
         1. ピクセルの行で、「**[!UICONTROL edit]**」をクリックします。
         1. 必要に応じて、[!UICONTROL HTML Tag]フィールドと[!UICONTROL Flash Tag]フィールドの値をコピーし、広告主またはWebサイトの連絡先に提供します。

            広告主のIT部門やその他のグループは、タグの導入をスケジュールしたり、通知を受けたりする必要がある場合があります。
   1. クリック **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** （オプション）インプレッション数1,000回あたりの請求不可能なコストとして追跡される、静的なサードパーティの料金率。別の値を入力しない限り、新しい配置には、パッケージレベルのデフォルトが自動的に適用されます（該当する場合）。

>[!NOTE]
>
>請求可能な料金は[!UICONTROL Net CPM]指標に反映されます。

>[!MORELIKETHIS]
>
>* [プレースメント管理について](placement-about.md)
>* [プレースメントの作成](placement-create.md)
>* [プレースメントの編集](placement-edit.md)
>* [キーボードショートカット](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [キャンペーン管理に関するFAQ](/help/dsp/campaign-management/campaign-management-faq.md)

