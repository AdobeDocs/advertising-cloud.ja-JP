---
title: 配置設定
description: 使用可能な配置設定の説明を参照してください。
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '3280'
ht-degree: 0%

---

# 配置設定

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** 配置名。

>[!TIP]
>状況に合った命名規則を使用します。 推奨される命名規則の 1 つは、*\&lt;campaign name=&quot;&quot;>:\&lt;ad unit=&quot;&quot;>:\&lt;duration>:\&lt;targeting>*.&quot;

**[!UICONTROL Status]:** 配置ステータス： *[!UICONTROL Active]* （デフォルト）または *[!UICONTROL Paused]*.

>[!TIP]
>配置を開始する準備が整うまで一時停止することをお勧めします。

**[!UICONTROL Details]:** （読み取り専用）該当する広告のタイプ、プレースメントを作成または作成したアカウント、親キャンペーン。 詳細を表示するには、 **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** 既存の配置テンプレートのリストを開きます。 テンプレートからターゲティング設定を自動入力するには：

1. 次のいずれかの操作を行います。

   * テンプレートのすべてのターゲットを再利用するには、テンプレート名の横にあるチェックボックスをオンにします。

   * テンプレートから個々のターゲットタイプを再利用するには、テンプレート名を展開し、再利用するターゲットタイプの横にあるチェックボックスをオンにします。

1. クリック **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** （ビデオ広告形式のみ）広告の期間や広告の仕様。右側の予測投影の計算に使用されます。 フィールドは広告タイプによって異なります。

**[!UICONTROL Placement tags]:** （オプション）この配置を探すのに役立つキーワードまたはニックネーム。

## 目標

**[!UICONTROL Package]:** （オプション）配置の割り当て先となるパッケージ。 クリック ![編集](/help/dsp/assets/edit.png) をクリックして、既存のパッケージを選択するか、新しいパッケージを作成します。 パッケージに配置を割り当てると、 [!UICONTROL Goals] セクションが更新され、パッケージのフライト日、配信目標、予算が表示されます。

**[!UICONTROL Flight Dates]:** 配置の開始日と終了日です。 承認された広告は、プレースメントがアクティブで、アクティブなパッケージまたはキャンペーンに割り当てられている場合、フライト中に実行する資格があります。

パッケージまたはキャンペーンの日付が、デフォルトで自動入力されます。

>[!NOTE]
>
>* フライト日は、キャンペーンのフライト日とパッケージのフライト日に含める必要があります。


### パッケージレベルのペーシングでパッケージに割り当てられた配置

**[!UICONTROL Placement Funding]:** プレースメントの予算方法：

* *[!UICONTROL Optimize based on performance]:* パッケージレベルで予算を制御します。
* *[!UICONTROL Set a fixed budget cap]:* 日次、週次、月次、全期間の配置予算を設定できます。 値と期間 (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*) をクリックします。

**[!UICONTROL Max Bid]:** 1,000 インプレッションに対して支払う最大額。

**[!UICONTROL Placement Pre-bid Filters]:** 入札を行うために満たす必要がある最大 5 つの KPI しきい値（最小視認性指標やクリックスルー率など）。 入札前フィルターを最適化戦術として使用できますが、各ルールがこの配置で入札できる商談を制限する可能性があることを理解してください。 フィルターを追加または編集するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作を行います。
   * フィルターを追加するには、次の手順に従います。
      1. クリック **[!UICONTROL Add Filter]**.
      1. 次の隣 **[!UICONTROL Only bid if]**&#x200B;で指標を選択し、値を入力します。
   * フィルターを削除するには、 **[!UICONTROL X]** をクリックします。
1. クリック **[!UICONTROL Save]**.

各入札前フィルターの説明については、「 」を参照してください。[配置レベルの事前入札フィルターとその使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### その他すべての配置

**[!UICONTROL Budget Goal]:** 予算の上限と予算間隔 (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*) をクリックします。

**[!UICONTROL Gross Budget Goal]:** （利益管理のあるキャンペーンの配置のみ）総予算額と予算間隔 (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*) をクリックします。

**[!UICONTROL Optimization Goal]:**  パッケージの最適化目標。 各最適化目標の説明については、「 」を参照してください。[最適化目標とその使用方法](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** ターゲットの目標。パフォーマンスの追跡に使用されます。

>[!NOTE]
>
>このフィールドは、単なるベンチマークであり、決定には使用されません。

**[!UICONTROL Pace on]:** ペーシングの基準は次のとおりです。

* **[!UICONTROL Budget goal]:** （デフォルト）このオプションでは、割り当てられた予算内で可能な限り多くのインプレッションを配信します。

* **[!UICONTROL Impressions]:** このオプションでは、指定された数量が指定された間隔内に達するまで、インプレッションを配信します。 このオプションを選択する場合は、インプレッション数と間隔を指定します。 *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* または *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** 1,000 インプレッションに対して支払う最大額。

**[!UICONTROL Pacing Fill Strategy]:** （パッケージレベルのペーシングのみのパッケージ）広告配信のペースを調整する方法：

* *[!UICONTROL Even]:* （デフォルト）各フライトを通じて配信を均等に配置し、フライトの前半の配信のターゲットは 50%になります。

* *[!UICONTROL Frontload]:* 配信を加速し、飛行中に 65～75%完了するようにします。

* *[!UICONTROL Aggressive Frontload]:* 配信を加速し、飛行中に 75～85%完了するようにします。

**[!UICONTROL Placement Pre-bid Filters]:** （オプション）入札を実行するために満たす必要がある最大 5 つのフィルター。 入札前フィルターを最適化戦術として使用できますが、各ルールでは、この配置で入札できる商談が制限される場合があることに注意してください。 フィルターを追加または編集するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作を行います。
   * フィルターを追加するには、次の手順に従います。
      1. クリック **[!UICONTROL Add Filter]**.
      1. 次の隣 **[!UICONTROL Only bid if]**&#x200B;で指標を選択し、値を入力します。
   * フィルターを削除するには、 **[!UICONTROL X]** をクリックします。
1. クリック **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** （オプション）配置に広告を含めるか除外する特定の場所。 場所を指定しない場合、すべての場所がターゲットになります。

>[!NOTE]
>
>Roku プレースメントでは、市区町村と DMA の場所は使用できません。

場所を指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作を行います。
   * 国、都道府県、市区町村、DMA、連邦立法地区または州立法地区を含めるか除外するには、次の手順に従います。
      1. 左の列で場所のタイプを選択します。
      1. （必要に応じて）場所をクリックして展開します。
      1. 場所の横にある *[!UICONTROL Include]* ターゲットとして含めるか *[!UICONTROL Exclude]* をクリックして、ターゲットとして除外します。
   * 郵便番号を検索し、選択したすべての結果を含めるか除外するには、次の手順に従います。
      1. クリック **[!UICONTROL Search Postal Code]**.
      1. 国を選択します。
      1. 市区町村名を入力し、「 ![編集](/help/dsp/assets/search.png).
      1. 正しい検索結果をクリックします。
      1. クリック *[!UICONTROL Include All]* すべての場所をターゲットとして含めるか、 *[!UICONTROL Exclude All]* ：すべてのロケーションをターゲットとして除外します。
   * 郵便番号を入力または貼り付け、すべてを含めるまたは除外するには、次の手順に従います。
      1. クリック **[!UICONTROL Paste Postal Code]**.
      1. 国を選択します。
      1. 最大 1,000 個の郵便番号を入力または貼り付けます。
1 行につき郵便番号を 1 つ含めるか、コンマまたはタブで区切って複数の値を入力します。
      1. クリック *[!UICONTROL Include All]* すべての場所をターゲットとして含めるか、 *[!UICONTROL Exclude All]* ：すべてのロケーションをターゲットとして除外します。
   * 場所を [!UICONTROL Included] または [!UICONTROL Excluded] リスト、クリック **[!UICONTROL X]** をクリックします。
1. クリック **[!UICONTROL Done]**.

>[!NOTE]
>
>* すべての国に、都道府県、市区町村、郵便番号の場所があるわけではありません。
>* DMA（指定販売地域）、連邦立法府 (FLA) および州立法府 (FLA) は、米国の地域でのみ使用できます。


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** ターゲットとして含める、または除外する在庫ソース。 ほとんどの配置タイプでは、すべての在庫タイプと各タイプのすべてのソースがデフォルトで含まれます。 の場合 [!DNL Roku] 配置を使用する場合は、在庫のタイプとソースを指定する必要があります。 次のタイプの在庫から選択できます。

* [!UICONTROL Public]:（Roku を除くすべての配置タイプ）Advertising Cloudがアクセスできるすべてのオープン為替在庫です。 公開在庫を含めたり除外したりできます。

   リストは、ソース別またはフィード別に表示できます。 フィード別にリストを表示する場合、フィード名、フィードキー、または選択した特性タグで検索できます。

* [!UICONTROL Private] | [!UICONTROL Roku Private]:既存の個人契約（または既存の個人契約） [!DNL Roku] ～の契約 [!DNL Roku] 配置 ) をDSPで設定した公開者と共に使用する必要があります。 公開在庫は含めることができますが、除外することはできません。

   キーワード、キー、Deal ID、カスタムタグでリストを検索できます。

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]:すべて [プレミアム、保証なし [!UICONTROL On Demand] 在庫](/help/dsp/inventory/on-demand-inventory-about.md) ( または [!UICONTROL On Demand] [!DNL] Roku での契約 [!DNL Roku] 配置 ) を購読している [!DNL DSP]. 含めたり除外したりできます [!UICONTROL On Demand] 在庫。

   リストは、ソース別またはフィード別に表示できます。 フィード別にリストを表示する場合、フィード名、フィードキー、または選択した投稿者の地域、カテゴリタグ、特性タグで検索できます。

在庫のターゲティングを指定するには：

* 在庫タイプを除外するには、名前の横にあるチェックボックスをオフにします。
* 在庫タイプをターゲットにする手順は、次のとおりです。
   1. 在庫タイプ名の横にあるチェックボックスを選択します。
   1. （オプション）以下を含めるようにソースを変更します。
      1. クリック ![編集](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] および [!UICONTROL On Demand] 在庫 ) クリック *[!UICONTROL *View by Source]**または **[!UICONTROL View by Feed]** をクリックして、ソースの表示方法を変更します。
      1. （該当する場合）必要に応じて在庫をフィルターします。
      1. 含める、および除外するソースを指定します。
         * を含めるには、以下を実行します。 [!UICONTROL Public] または [!UICONTROL On Demand] ソース、クリック **[!UICONTROL Include]** をクリックします。
         * 含める [!UICONTROL Private] ソース：
            * 1 つの契約にすべての在庫を含めるには、 **[!UICONTROL Include all]** をクリックします。
            * 個々の在庫ソースを含めるには、契約名を展開し、ソース名の横にあるチェックボックスをクリックします。
         * を除外するには [!UICONTROL Public] または [!UICONTROL On ] ソース、クリック **[!UICONTROL Exclude]** をクリックします。
   1. （オプション）ターゲット情報を含む CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Save & Export]**.
   1. クリック **[!UICONTROL Save]**.

>[!TIP]
>
>を購読している場合、 [!UICONTROL On Demand] 在庫はありますが、ターゲットとするパブリッシャーやオファーを見つけることができないので、オファーのステータスを確認してください。 ステータスについて詳しくは、 [について [!DNL On Demand] プレミアム在庫](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** （ビデオ配置のみ）アウトストリームトラフィックを除外します。

アウトストリーム広告は、通常、ビデオプレーヤーで通常のビデオ広告とは異なり、コンテンツ上にポップアップとして表示されたり、（ネイティブエクスペリエンスで）コンテンツに埋め込まれたりします。

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** ターゲットにするトラフィックのタイプ。 次のオプションがあります **[!UICONTROL Websites]** および **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** （次の場合に使用可能） **[!UICONTROL Paste list of targeted sites]** が *[!UICONTROL Off]*) ターゲットにするサイトの品質。 階層 1 ～ 3 はすべてブランドに安全で、DSPマッピングチームによって検証および承認されています。

* *[!UICONTROL Tier 1]:* Premium のサイトやアプリケーションが国内で認識可能です。
* *[!UICONTROL Tier 2]:* Tier 1 と同様に、Tier 1 よりも広く知られていない品質の高いサイトやアプリケーションをターゲットにします。
* *[!UICONTROL Tier 3]:* Tier 1 ～ 2 に加えて、ニッチオーディエンスに対応する正当でブランドに安全なサイトおよびアプリケーションをターゲットに設定します。 リーチやデータターゲティングの購入には、階層 3 を使用します。
* *[!UICONTROL All Sites]:* ターゲット Tier 1 ～ 3 と、スクリーニングまたは分類されていない新しい在庫（リーチに使用できます）。

>[!NOTE]
>
>在庫は、配置の広告ユニットに固有です。

>[!TIP]
>
>パフォーマンスキャンペーンのベストプラクティスは、次を選択することです。 *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** ( オプション、次の場合に使用可能 **[!UICONTROL Paste list of targeted sites]** が *[!UICONTROL Off]*) 選択したサイト層内のサイトカテゴリのうち、ターゲットとして含める、または除外する（両方を除く）もの。 サイトの件名に基づいてAdvertising Cloudがマッピングした垂直方向のサイトリストから選択します。

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 含めるか除外するサイトカテゴリを指定します。
   * サイトカテゴリを含めるには：
      1. クリック **[!UICONTROL Include categories]**.
      1. ターゲットとする各カテゴリの横にあるチェックボックスをオンにします。
   * サイトカテゴリを除外するには：
      1. クリック **[!UICONTROL Exclude categories]**.
      1. 除外する各カテゴリの横にあるチェックボックスをオンにします。
1. （オプション）ターゲット情報を含む CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Export]**.
1. クリック **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** ( オプション、次の場合に使用可能 **[!UICONTROL Paste list of targeted sites]** が *[!UICONTROL Off]*) 除外するサイト。 サイトを検索して選択するか、ドメイン名を入力または貼り付けることができます。

1. クリック ![編集](/help/dsp/assets/edit.png).
1. サイトを指定します。
   * サイトを検索するには：
      1. クリック **[!UICONTROL Search]**.
      1. キーワードを入力し、サイト層を選択し、サイトカテゴリを選択します。
      1. 検索結果で、除外するサイトを選択します。
         * 個々のサイトを除外するには、そのサイトの横にあるチェックボックスをオンにします。
         * （結果が 50 件を超える場合）最初の 50 件を除外するには、 **[!UICONTROL Exclude these 50]**. すべての検索結果を除外するには、 **[!UICONTROL Exclude these \<*NN *\>]**.
   * ドメイン名を入力するには：
      1. クリック **[!UICONTROL Paste]**.
      1. 1 つ以上のドメイン名を別々の行に入力します。
      1. クリック **[!UICONTROL Exclude All]**.
1. クリック **[!UICONTROL Done]** 終わったら。

>[!NOTE]
>
>* Advertising Cloud DSP [グローバルブロックサイトリスト](/help/dsp/introduction/features/brand-safety-media-quality.md)：広告で安全でないと見なされるサイトを含みます。
>* ブロックされたサイトリストは、常にターゲットサイトリストを上書きします。 配置が広告の同じターゲットを除外して含む場合、そのターゲットは除外されます。


**[!UICONTROL Language]:** （オプション）ターゲットとする単一の言語です。

**[!UICONTROL Site List Preview]:** （読み取り専用）配置のターゲットサイトとブロックされたサイトですべて。

オプションで、ターゲットサイトとブロックされたサイトのリストをコンマ区切り値 (CSV) ファイルとして書き出すことができます。 リストを書き出すには、 **[!UICONTROL Export full site list]**&#x200B;をクリックし、ブラウザーの通常の手順に従ってファイルを開くか保存します。

<!-- **[!UICONTROL Allow unscreened sites]:** (XXX placements only) Allows you to XXXX.   Optional available for https://advertising.adobe.com/configurator/placement/edit/2432022 -->

**[!UICONTROL Paste list of targeted sites]:** 特定のサイトのみをターゲットにできます。 このオプションを有効にすると、その他のサイトのターゲット設定オプションは無効になります。

**[!UICONTROL Sites]:** （次の場合に使用可能） **[!UICONTROL Paste list of targeted sites]** が *[!UICONTROL On]*) ターゲットにするサイト。 サイトを検索して選択するか、ドメイン名を入力または貼り付けることができます。

1. クリック ![編集](/help/dsp/assets/edit.png).
1. サイトを指定します。
   * サイトを検索するには：
      1. クリック **[!UICONTROL Search]**.
      1. キーワードを入力し、サイト層を選択し、サイトカテゴリを選択します。
      1. 検索結果で、含めるサイトを選択します。
         * 個々のサイトを除外するには、そのサイトの横にあるチェックボックスをオンにします。
         * （結果が 50 件を超える場合）最初の 50 件を含めるには、 **[!UICONTROL Include these 50]**. すべての検索結果を含めるには、 **[!UICONTROL Include these \<*NN *\>]**.
   * ドメイン名を入力するには：
      1. クリック **[!UICONTROL Paste]**.
      1. 1 つ以上のドメイン名を別々の行に入力します。
      1. クリック **[!UICONTROL Include All]**.
1. クリック **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** 配置のオーディエンスターゲット ( [サードパーティセグメント、ファーストパーティセグメント、Adobeセグメント、カスタムセグメント、保存されたオーディエンス](/help/dsp/audiences/audience-settings.md). 選択したすべてのセグメントおよび保存されたオーディエンスの重複を除外した合計オーディエンスサイズも表示されます。 既存のオーディエンスを選択したり、新しいオーディエンスを作成して後で再利用したり、特定のオーディエンスセグメントを選択したりできます。

* 既存のオーディエンスを選択するには、 ![選択](/help/dsp/assets/chevron-down.png) 次の [!UICONTROL Included Audiences]をクリックし、オーディエンスを選択します。
* 新しいオーディエンスを作成するには、 ![選択](/help/dsp/assets/chevron-down.png) 次の [!UICONTROL Included Audiences]を選択し、 **[!UICONTROL + Create Audience]**. 手順については、 [再利用可能なオーディエンスを作成](/help/dsp/audiences/reusable-audience-create.md)手順 3 から始まる
* 特定のオーディエンスセグメントを選択するには、 **[!UICONTROL Select segments for this placement only]**. セグメントロジックを選択します。手順については、「[再利用可能なオーディエンスを作成](/help/dsp/audiences/reusable-audience-create.md).&quot; 完了したら、「 **保存**.

**[!UICONTROL Excluded Audiences]:** 配置に対して除外するオーディエンス（を持つオーディエンスを含む） [サードパーティセグメント、ファーストパーティセグメント、Adobeセグメント、カスタムセグメント、保存されたオーディエンス](/help/dsp/audiences/audience-settings.md). 除外されたすべてのオーディエンスに関する、重複を除外した合計オーディエンスサイズとアクティブなオーディエンスサイズも表示されます。 既存のオーディエンスを選択するか、新しいオーディエンスを作成して後で再利用できます。

* 既存のオーディエンスを選択するには、 ![選択](/help/dsp/assets/chevron-down.png) 次の [!UICONTROL Excluded Audiences]をクリックし、オーディエンスを選択します。
* 新しいオーディエンスを作成するには、 ![選択](/help/dsp/assets/chevron-down.png) 次の [!UICONTROL Excluded Audiences]を選択し、 **+オーディエンスを作成**. 手順については、 [再利用可能なオーディエンスを作成](/help/dsp/audiences/reusable-audience-create.md)手順 3 から始まる

**[!UICONTROL Cross Device Targeting]:** ( 少なくとも 1 つのセグメントまたはオーディエンスを選択し、 [キャンペーンはユーザーベースのクロスデバイスターゲティング用に設定されます](/help/dsp/campaign-management/campaigns/campaign-settings.md). 指定したセグメントにないデバイスも含め、（キャンペーン設定で指定したデバイスグラフごとに）個人の既知のすべてのデバイスにわたってターゲティングを拡張できます。 費用は、キャンペーン用に指定したグラフに応じて適用される場合があります。 デバイスグラフのデータは、現在、北米でのみ使用できます。

**[!UICONTROL Placement Cap]:** （オプション）個別のデバイスまたは人物が ( 指定した [!UICONTROL Cross Device Level]) は、配置から広告を提供します。 次のオプションがあります *[!UICONTROL Unlimited]* または 1 日、1 週間、1 ヶ月あたりの特定の金額。

>[!NOTE]
>
> 頻度キャップは、キャンペーン、パッケージ、配置の各レベルで設定できます。 DSPは、キャンペーン階層で最も厳格な頻度キャップに従います。

**[!UICONTROL Secondary Cap]:** ( オプション、数値を含める場合に使用できます [!UICONTROL Placement Cap]) プライマリ配置キャップの範囲内の追加の制限。 インプレッション数と期間（12 時間あたり 3 回など）を選択します。

**[!UICONTROL Day Parting]:** （オプション）広告が実行される曜日と時刻を指定します。 時間帯区分間隔を指定するには：
1. クリック ![編集](/help/dsp/assets/edit.png).
1. 該当するタイムゾーンを選択します。
1. 間隔を指定します。
   * あらかじめ設定されている間隔を選択するには、いずれかの間隔ボタンをクリックします。 オプションは以下のとおりです*[!UICONTROL Weekends]** *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]*&#x200B;または *[!UICONTROL Prime]* (primetime)。
   * 間隔を手動で選択するには、セル内をクリックし、必要に応じてドラッグして間隔を選択します。
1. クリック **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** ( オプション、次の条件で構成された広告主が利用できます： [!DNL Comscore] および [!DNL Grapeshot] セグメント ) [!DNL Comscore] および [!DNL Grapeshot] をターゲットとして含めます。 この機能には追加料金が適用される場合があります。 この機能を有効化し、トピックセグメントを設定するには、 [!DNL Adobe] アカウントチーム。

トピックのターゲット設定を指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. ターゲットとするセグメントを指定します。
   1. 左の列で、パートナー (*[!UICONTROL Comscore]* または *[!UICONTROL Grapeshot]*) をクリックします。
   1. 入力フィールドに、セグメント名またはセグメント ID を入力します。
1. （オプション）トピック情報を含む CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Export]**.
1. クリック **[!UICONTROL Save]**.

>[!TIP]
>
>* トピックのターゲティングは、配置で入札できる在庫を制限するので、トピックのターゲティングは、購入全体のごく一部に対してのみ使用します。
>
>* セグメント内での任意のネガティブターゲティングを [!DNL Comscore] または [!DNL Grapeshot].


**[!UICONTROL Device Targeting]:** （オプション）ターゲットに含めたり除外したりする特定のデバイス情報（デバイスの種類、製造元、オペレーティングシステム、ブラウザー、接続の種類など）。 デバイスのターゲティングを指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 含める、または除外するデバイスの詳細を指定します。
   1. 左の列で、カテゴリを選択します。
   1. ターゲット設定を指定：
      * 値を含めるには、 **[!UICONTROL Include]** 値名の横に表示されます。
      * 値を除外するには、 **[!UICONTROL Exclude]** 値名の横に表示されます。
1. （オプション）デバイスのターゲット情報を含む CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Export]**.
1. クリック **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** （オプション）ターゲットとしてを含めるか除外するか（両方を除く）を選択する特定のインターネットサービスプロバイダー (ISP)。 ISP のターゲット設定を指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 含めるまたは除外する ISP を指定します。
   * ISP を含めるには：
      1. クリック **[!UICONTROL Include ISPs]**.
      1. （オプション）キーワードでリストをフィルターします。
      1. ターゲットとする各 ISP の横にあるチェックボックスをオンにします。
   * ISP を除外するには：
      1. クリック **[!UICONTROL Exclude ISPs]**.
      1. （オプション）キーワードでリストをフィルターします。
      1. 除外する各 ISP の横にあるチェックボックスをオンにします。
1. （オプション）ISP のターゲット情報を含む CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Export]**.
1. クリック **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** のタイプ [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]、および [!DNL Peer39] 適用するコンテキストフィルター。 広告主レベルのデフォルトは、新しい配置に対して選択されますが、設定は変更できます。

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** （オプション）デフォルトでブロックする 1 つ以上のタイプの在庫コンテキスト。 追加料金が適用される場合があります。

* [!UICONTROL Peer 39]:

   * **次のようなターゲットサイトです。** （オプション）デフォルトでターゲットにする 1 つ以上の在庫属性のタイプ。 追加料金が適用される場合があります。

* [!UICONTROL ComScore]:

   * **次のサイトをブロックします。** （オプション）デフォルトでブロックする 1 つ以上の在庫属性のタイプ。 追加料金が適用される場合があります。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** （オプション）デフォルトで広告をブロックする成人向けコンテンツの程度： *[!UICONTROL Do Not Block]* （デフォルト） *[!UICONTROL Standard]*&#x200B;または *[!UICONTROL Strict]*. 追加料金が適用される場合があります。

   * **[!UICONTROL Alcohol Content]:** （オプション）デフォルトで広告をブロックするアルコールコンテンツの程度： *[!UICONTROL Do Not Block]* （デフォルト） *[!UICONTROL Standard]*&#x200B;または *[!UICONTROL Strict]*. 追加料金が適用される場合があります。

**[!UICONTROL Pre-bid fraud blocking]:** 不正なトラフィックや、を通じて測定された疑わしいアクティビティに基づいてブロックするサイトのタイプ [!DNL DoubleVerify], [!DNL Integral Ad Science]、および [!DNL Peer39]. 広告主レベルのデフォルトは、新しい配置に対して選択されますが、設定は変更できます。

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** デフォルトでは、は、新しい配置に対する、ハイジャックされたデバイスでのトラフィックを含む、100%すべての無効なトラフィックをブロックします。 追加料金が適用される場合があります。

   * **[!UICONTROL Also block sites with]:** （オプション）デフォルトでDSPが広告をブロックする原因となる、追加レベルの詐欺および無効なトラフィック：  *[!UICONTROL None]* （デフォルトでは、追加のトラフィックはブロックされません）。 *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*&#x200B;または *[!UICONTROL >25% Average Fraud/IVT levels]*. 追加料金が適用される場合があります。

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** （オプション）デフォルトでDSPが広告をブロックする 1 つ以上のタイプの詐欺。 *[!UICONTROL Fraud]* （詐欺行為を伴うすべてのサイトをブロックします）。 *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*、または *[!UICONTROL Fraud: Zero Ads]*. 追加料金が適用される場合があります。

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** （オプション）デフォルトでDSPが広告をブロックする原因となる疑わしい Web サイトまたはアプリアクティビティのタイプ。 *[!UICONTROL None]* （疑わしいアクティビティに基づいて広告をブロックしないデフォルト） *[!UICONTROL Suspicious Activity - High Risk]*&#x200B;または *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 追加料金が適用される場合があります。

**[!UICONTROL Ads.txt filtering]:**

どのレベルの [Ads.txt](https://iabtechlab.com/ads-txt-about/) 各パブリッシャーの認証済みデジタル販売者リストを活用して、使用する入札前フィルタリング。 広告主レベルのデフォルトは、新しい配置に対して選択されますが、設定は変更できます。

* *[!UICONTROL Opt out of ads.txt (default)]*:すべての販売者から在庫を購入する。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*:ドメインの許可されたダイレクト販売者および再販売者からの在庫の購入を優先する。
* *[!UICONTROL Ads.txt sellers only]*:ドメインの許可された直接販売者および再販売者からのみ在庫を購入する。
* *[!UICONTROL Ads.txt sellers only]*:ドメインの許可されたダイレクトセラーからのみ在庫を購入する場合。

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** ( [!UICONTROL DoubleVerify Authentic Brand Safety] （オプション）有効 [!DNL DoubleVerify Authentic Brand Safety]：指定したセグメント ID に対して設定されたカスタムブランド安全ルールを使用して、入札後のインプレッションをブロックします。 DSPは、広告主の設定で指定されたセグメント ID の使用を目的としてアカウントを請求します。

## [!UICONTROL Tracking]

>[!NOTE]
>
>([!DNL Roku] プレースメント ) が承認したサードパーティのトラッキングベンダー [!DNL Roku] 含める [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]、および [!DNL Research Now].

**[!UICONTROL Event Pixels]:** （オプション）配置のすべての新しい広告にデフォルトで添付されるサードパーティのイベント追跡ピクセル。 イベントピクセルを指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作を行います。
   * 既存のピクセルを選択するには、ピクセル行のチェックボックスをオンにします。
   * 新しいピクセルを作成するには：
      1. クリック **[!UICONTROL Create]**.
      1. 次の情報を入力します。
         * **[!UICONTROL Pixel name]:** ピクセル名。最大長は 500 文字です。 ピクセルを簡単に識別できる名前を使用します。
         * **[!UICONTROL Pixel event fires on]:** 実行するピクセルをトリガーにするイベント。 使用可能なイベントは、広告タイプによって異なります。
         * **[!UICONTROL Pixel type]:** ピクセルが *[!UICONTROL IMG URL]* （1 x 1 ピクセルの画像ファイル）、 *[!UICONTROL HTML]*&#x200B;または *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** ピクセル画像の URL。
      1. クリック **[!UICONTROL Create and attach]**.
   1. クリック **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** （オプション）配置内のすべての新しい広告にデフォルトで添付されるコンバージョントラッキングピクセル。 変換ピクセルを指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作を行います。
   * 既存のピクセルを選択するには、ピクセル行のチェックボックスをオンにします。
   * 新しいピクセルを作成するには：
      1. クリック **[!UICONTROL Create]**.
      1. 次の情報を入力します。
         * **[!UICONTROL Conversion pixel name]:** ピクセル名。最大長は 500 文字です。 ピクセルを簡単に識別できる名前を使用します。
         * **[!UICONTROL Conversion category]:** 変換のタイプ。
         * **[!UICONTROL Impression conversion window]:** インプレッションがコンバージョンに関連付けられる広告インプレッションが発生してからの日数。 デフォルトは 30 日です。
         * **[!UICONTROL Click conversion window]:** 広告のクリックが発生してからの日数で、クリックはコンバージョンに関連付けられます。 デフォルトは 30 日です。
         * **[!UICONTROL Notes]:** （オプション）ピクセルに関する説明またはその他の情報。
      1. クリック **[!UICONTROL Create and attach]**.
      1. 関連する Web ページにコンバージョンピクセルを実装します。
         1. メインメニューで、に移動します。 **[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**.
         1. ピクセル行で、 **[!UICONTROL edit]**.
         1. 値を [!UICONTROL HTML Tag] および [!UICONTROL Flash Tag] フィールドに値を入力し、必要に応じて広告主または web サイトの連絡先に提供します。

            広告主の IT 部門やその他のグループは、タグの導入をスケジュールしたり、通知を受けたりする必要がある場合があります。
   1. クリック **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** （オプション）インプレッション数 1,000 回あたりの請求不可能なコストとして追跡される、静的なサードパーティの料金。 別の値を入力しない限り、新しい配置には、パッケージレベルのデフォルトが自動的に適用されます（該当する場合）。

>[!NOTE]
>
>請求可能な料金は、 [!UICONTROL Net CPM] 指標。

>[!MORELIKETHIS]
>
>* [配置管理について](placement-about.md)
>* [配置の作成](placement-create.md)
>* [配置の編集](placement-edit.md)
>* [キーボードショートカット](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [キャンペーン管理に関する FAQ](/help/dsp/campaign-management/campaign-management-faq.md)

