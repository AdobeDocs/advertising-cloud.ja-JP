---
title: 配置設定
description: 使用可能な配置設定の説明を参照してください。
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: e0713f3717a684fb5ef2808d7de769424b8972d2
workflow-type: tm+mt
source-wordcount: '3280'
ht-degree: 0%

---

# 配置設定

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** 配置名。

>[!TIP]
>状況に合った命名規則を使用します。 推奨される命名規則の 1 つは、「*\&lt;campaign name=&quot;&quot;>:\&lt;ad unit=&quot;&quot;>:\&lt;duration>:\&lt;targeting>*.」

**[!UICONTROL Status]:** 配置ステータス： *[!UICONTROL Active]* （デフォルト）または *[!UICONTROL Paused]*.

>[!TIP]
>配置を開始する準備が整うまで一時停止することをお勧めします。

**[!UICONTROL Details]:** （読み取り専用）該当する広告タイプ、プレースメントを作成または作成したアカウント、親キャンペーン。 詳細を表示するには、 **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** 既存の配置テンプレートのリストを開きます。 テンプレートからターゲティング設定を自動入力するには：

1. 次のいずれかの操作を行います。

   * テンプレートのすべてのターゲットを再利用するには、テンプレート名の横にあるチェックボックスをオンにします。

   * テンプレートから個々のターゲットタイプを再利用するには、テンプレート名を展開し、再利用するターゲットタイプの横にあるチェックボックスをオンにします。

1. クリック **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** （ビデオ広告フォーマットのみ）広告の期間や広告の仕様。右側の予測投影の計算に使用されます。 フィールドは広告タイプによって異なります。

**[!UICONTROL Placement tags]:** （オプション）この場所を探すのに役立つキーワードまたはニックネーム。

## 目標

**[!UICONTROL Package]:** （オプション）配置が割り当てられるパッケージ。 クリック ![編集](/help/dsp/assets/edit.png) をクリックして、既存のパッケージを選択するか、新しいパッケージを作成します。 パッケージに配置を割り当てると、 [!UICONTROL Goals] セクションは、パッケージのフライト日、配信目標、予算で更新されます。

**[!UICONTROL Flight Dates]:** 配置の開始日と終了日。 承認された広告は、フライト中に、配置がアクティブで、アクティブなパッケージまたはキャンペーンに割り当てられたときに実行できます。

パッケージまたはキャンペーンの日付は、デフォルトで自動入力されます。

>[!NOTE]
>
>* フライト日は、キャンペーンのフライト日とパッケージのフライト日に含める必要があります。


### パッケージレベルのペーシングによるパッケージに割り当てられた配置

**[!UICONTROL Placement Funding]:** 配置の予算方法：

* *[!UICONTROL Optimize based on performance]:* パッケージレベルで予算を制御します。
* *[!UICONTROL Set a fixed budget cap]:* 日別、週別、月別、全時間の配置予算を設定できます。 値と期間 (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*) をクリックします。

**[!UICONTROL Max Bid]:** 1,000 インプレッションの支払いが最大です。

**[!UICONTROL Placement Pre-bid Filters]:** 入札を行うために満たす必要がある最大 5 つの KPI しきい値（視認性の最小指標やクリックスルー率など）。 事前入札フィルターを最適化戦術として使用できますが、各ルールでこの配置で入札できる機会が制限される可能性があることを理解してください。 フィルターを追加または編集するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作を行います。
   * フィルターを追加するには：
      1. クリック **[!UICONTROL Add Filter]**.
      1. の横 **[!UICONTROL Only bid if]**&#x200B;で、指標を選択して、値を入力します。
   * フィルターを削除するには、 **[!UICONTROL X]** 」と入力します。
1. クリック **[!UICONTROL Save]**.

各入札前フィルターの説明については、「[配置レベルの事前入札フィルターとその使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md).」

### その他すべての配置

**[!UICONTROL Budget Goal]:** 予算の上限と予算間隔 (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*) をクリックします。

**[!UICONTROL Gross Budget Goal]:** （利益管理を使用するキャンペーン内の配置のみ）予算の上限と予算間隔 (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*) をクリックします。

**[!UICONTROL Optimization Goal]:**  パッケージの最適化目標。 各最適化目標の説明は、「[最適化の目標とその使用方法](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** パフォーマンスの追跡に使用されるターゲットの目標。

>[!NOTE]
>
>このフィールドはベンチマークに過ぎず、判定には使用されません。

**[!UICONTROL Pace on]:** どのペーシングが基になるか：

* **[!UICONTROL Budget goal]:** （デフォルト）このオプションは、割り当てられた予算内で可能な限り多くのインプレッションを提供します。

* **[!UICONTROL Impressions]:** このオプションは、指定した数量が指定した間隔内に達するまで、インプレッション数を配信します。 このオプションを選択する場合は、インプレッション数と間隔を指定します。 *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* または *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** 1,000 インプレッションの支払いが最大です。

**[!UICONTROL Pacing Fill Strategy]:** （パッケージレベルのペーシングのみのパッケージ）広告配信を遅らせる方法：

* *[!UICONTROL Even]:* （デフォルト）各フライトを通して配信が均等に配置され、フライトの前半の配信のターゲットは 50%になります。

* *[!UICONTROL Frontload]:* 飛行の途中で 65～75%完了するように配信を加速します。

* *[!UICONTROL Aggressive Frontload]:* 75～85%が飛行中に完了するように配信を加速します。

**[!UICONTROL Placement Pre-bid Filters]:** （オプション）入札を行うために満たす必要があるフィルターを 5 つまで選択できます。 入札前フィルターを最適化戦術として使用できますが、各ルールでこの配置で入札できる機会が制限される場合があることに注意してください。 フィルターを追加または編集するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作を行います。
   * フィルターを追加するには：
      1. クリック **[!UICONTROL Add Filter]**.
      1. の横 **[!UICONTROL Only bid if]**&#x200B;で、指標を選択して、値を入力します。
   * フィルターを削除するには、 **[!UICONTROL X]** 」と入力します。
1. クリック **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** （オプション）配置に広告を含めるまたは除外する特定の場所。 場所を指定しない場合、すべての場所がターゲットになります。

>[!NOTE]
>
>市区町村と DMA の場所は、Roku プレースメントでは使用できません。

場所を指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作を行います。
   * 国、都道府県、市区町村、DMA、連邦立法地区または州立法地区を含めるか除外するには：
      1. 左の列で位置のタイプを選択します。
      1. （必要に応じて）場所をクリックして展開します。
      1. 場所の横にある *[!UICONTROL Include]* ターゲットとして含めるか *[!UICONTROL Exclude]* をクリックして、ターゲットから除外します。
   * 郵便番号を検索し、選択したすべての結果を含めるか除外するには：
      1. クリック **[!UICONTROL Search Postal Code]**.
      1. 国を選択します。
      1. 市区町村名を入力し、「 ![編集](/help/dsp/assets/search.png).
      1. 正しい検索結果をクリックします。
      1. クリック *[!UICONTROL Include All]* すべての場所をターゲットまたは *[!UICONTROL Exclude All]* をクリックすると、すべてのロケーションがターゲットとして除外されます。
   * 郵便番号を入力または貼り付け、すべてを含めるか除外するには、次の手順に従います。
      1. クリック **[!UICONTROL Paste Postal Code]**.
      1. 国を選択します。
      1. 最大 1,000 個の郵便番号を入力または貼り付けます。
1 行につき郵便番号を 1 つ含めるか、コンマまたはタブで区切って複数の値を入力します。
      1. クリック *[!UICONTROL Include All]* すべての場所をターゲットまたは *[!UICONTROL Exclude All]* をクリックすると、すべてのロケーションがターゲットとして除外されます。
   * 場所を [!UICONTROL Included] または [!UICONTROL Excluded] リストを開き、 **[!UICONTROL X]** をクリックします。
1. クリック **[!UICONTROL Done]**.

>[!NOTE]
>
>* 都道府県、市区町村、郵便番号の場所がある国もあります。
>* DMA（指定販売地域）、連邦立法府および州立法府は、米国の場所でのみ使用できます。


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** ターゲットとして含めるまたは除外する在庫ソース。 ほとんどの配置タイプでは、すべての在庫タイプと各タイプのすべてのソースがデフォルトで含まれます。 の場合 [!DNL Roku] 配置を指定する場合は、在庫のタイプとソースを指定する必要があります。 次のタイプの在庫から選択できます。

* [!UICONTROL Public]:（Roku を除くすべての配置タイプ）Advertising Cloudがアクセスできるすべてのオープン為替在庫です。 公開在庫を含めたり除外したりできます。

   リストは、ソース別またはフィード別に表示できます。 フィード別にリストを表示する場合、フィード名、フィードキーまたは選択した特性タグで検索できます。

* [!UICONTROL Private] | [!UICONTROL Roku Private]:既存の個人取引（または既存の個人取引） [!DNL Roku] ～を扱う [!DNL Roku] 配置 ) をDSPで設定した公開者と共に使用する必要があります。 公開インベントリを含めることができますが、除外することはできません。

   リストは、キーワード、キー、案件 ID、カスタムタグで検索できます。

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]:すべて [プレミアム、保証なし [!UICONTROL On Demand] 在庫](/help/dsp/inventory/on-demand-inventory-about.md) ( または [!UICONTROL On Demand] [!DNL] Roku での取引 [!DNL Roku] 配置を参照 ) [!DNL DSP]. 以下を含めたり除外したりできます。 [!UICONTROL On Demand] 在庫。

   リストは、ソース別またはフィード別に表示できます。 フィード別にリストを表示する場合、フィード名、フィードキー、または選択した発行者の地域、カテゴリタグ、特性タグで検索できます。

在庫のターゲティングを指定するには：

* 在庫タイプを除外するには、名前の横にあるチェックボックスをオフにします。
* 在庫タイプをターゲットにする手順は、次のとおりです。
   1. 在庫タイプ名の横にあるチェックボックスを選択します。
   1. （オプション）以下を含めるようにソースを変更します。
      1. クリック ![編集](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] および [!UICONTROL On Demand] 在庫 ) をクリックします。 *[!UICONTROL *View by Source]**または **[!UICONTROL View by Feed]** をクリックして、ソースの表示方法を変更します。
      1. （該当する場合）必要に応じて在庫をフィルターします。
      1. 含めるソースと除外するソースを指定します。
         * を [!UICONTROL Public] または [!UICONTROL On Demand] ソース、クリック **[!UICONTROL Include]** をクリックします。
         * を含めるには [!UICONTROL Private] ソース：
            * すべての在庫を取引に含めるには、 **[!UICONTROL Include all]** をクリックします。
            * 個々の在庫ソースを含めるには、取引名を展開し、ソース名の横にあるチェックボックスをクリックします。
         * を除外するには [!UICONTROL Public] または [!UICONTROL On ] ソース、クリック **[!UICONTROL Exclude]** をクリックします。
   1. （オプション）ターゲット情報を含む CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Save & Export]**.
   1. クリック **[!UICONTROL Save]**.

>[!TIP]
>
>を購読している場合、 [!UICONTROL On Demand] 在庫はありますが、ターゲットとするパブリッシャーやオファーを見つけることができないので、オファーのステータスを確認してください。 ステータスについて詳しくは、 [について [!DNL On Demand] プレミアム在庫](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** （ビデオ配置のみ）アウトストリームトラフィックを除外します。

アウトストリーム広告は、通常、ビデオプレーヤーで通常のビデオ広告としてではなく、ポップアップとして、または（ネイティブエクスペリエンスで）コンテンツに詰め込まれて表示されます。

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** ターゲットにするトラフィックのタイプ。 オプションは次のとおりです。 **[!UICONTROL Websites]** および **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** ( **[!UICONTROL Paste list of targeted sites]** が *[!UICONTROL Off]*) ターゲットとするサイトの品質。 階層 1 ～ 3 はすべてブランドに安全で、DSPマッピングチームによって検証および承認されています。

* *[!UICONTROL Tier 1]:* プレミアムのサイトやアプリケーションが全国的に認識可能。
* *[!UICONTROL Tier 2]:* 階層 1 に加え、階層 1 よりも広く知られていない品質の高いサイトやアプリケーションをターゲットにします。
* *[!UICONTROL Tier 3]:* Tier 1-2 に加え、ニッチなオーディエンスに対応する正当でブランドに安全なサイトおよびアプリケーションをターゲットに設定します。 リーチまたはデータターゲティングの購入には階層 3 を使用します。
* *[!UICONTROL All Sites]:* ターゲット Tier 1 ～ 3 と、スクリーニングまたは分類されていない新しい在庫（リーチに使用できます）。

>[!NOTE]
>
>在庫は、配置の広告ユニットに固有です。

>[!TIP]
>
>パフォーマンスキャンペーンのベストプラクティスは、 *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** ( オプション；～に使える **[!UICONTROL Paste list of targeted sites]** が *[!UICONTROL Off]*) 選択したサイト層内のサイトカテゴリをターゲットとして含めるか除外するか（両方を除く）。 サイトの件名に基づいてAdvertising Cloudがマッピングした垂直サイトリストから選択します。

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 含めるか除外するサイトカテゴリを指定します。
   * サイトカテゴリを含めるには：
      1. クリック **[!UICONTROL Include categories]**.
      1. ターゲットとする各カテゴリの横にあるチェックボックスを選択します。
   * サイトカテゴリを除外するには：
      1. クリック **[!UICONTROL Exclude categories]**.
      1. 除外する各カテゴリの横にあるチェックボックスをオンにします。
1. （オプション）ターゲット情報を含む CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Export]**.
1. クリック **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** ( オプション；～に使える **[!UICONTROL Paste list of targeted sites]** が *[!UICONTROL Off]*) 除外するサイト。 サイトを検索して選択するか、ドメイン名を入力または貼り付けることができます。

1. クリック ![編集](/help/dsp/assets/edit.png).
1. サイトの指定：
   * サイトを検索するには：
      1. クリック **[!UICONTROL Search]**.
      1. キーワードを入力し、サイト層を選択し、サイトカテゴリを選択します。
      1. 検索結果で、除外するサイトを選択します。
         * 個々のサイトを除外するには、そのサイトの横にあるチェックボックスをオンにします。
         * （50 件を超える結果が得られた場合）最初の 50 件の結果を除外するには、 **[!UICONTROL Exclude these 50]**. すべての検索結果を除外するには、 **[!UICONTROL Exclude these \<*NN *\>]**.
   * ドメイン名を入力するには：
      1. クリック **[!UICONTROL Paste]**.
      1. 1 つ以上のドメイン名を別々の行に入力します。
      1. クリック **[!UICONTROL Exclude All]**.
1. クリック **[!UICONTROL Done]** 終わったら。

>[!NOTE]
>
>* Advertising Cloud DSPに加えて、アカウントレベルおよび広告主レベルのブロックサイトリストも適用されます [グローバルにブロックされたサイトリスト](/help/dsp/introduction/features/brand-safety-media-quality.md)：広告で安全でないと見なされるサイトを含みます。
>* ブロックされたサイトリストは、常にターゲットサイトリストより優先されます。 配置が広告に対して同じターゲットを除外し、含む場合、そのターゲットは除外されます。


**[!UICONTROL Language]:** （オプション）ターゲットとする単一の言語です。

**[!UICONTROL Site List Preview]:** （読み取り専用）配置のターゲットサイトとブロックされたサイト。

オプションで、ターゲットサイトおよびブロックサイトのリストをコンマ区切り値 (CSV) ファイルとして書き出すことができます。 リストを書き出すには、 **[!UICONTROL Export full site list]**&#x200B;をクリックし、ブラウザーの通常の手順に従ってファイルを開くか保存します。

<!-- **[!UICONTROL Allow unscreened sites]:** (XXX placements only) Allows you to XXXX.   Optional available for https://advertising.adobe.com/configurator/placement/edit/2432022 -->

**[!UICONTROL Paste list of targeted sites]:** 特定のサイトのみをターゲットにできます。 このオプションを有効にすると、他のサイトターゲティングオプションは無効になります。

**[!UICONTROL Sites]:** ( **[!UICONTROL Paste list of targeted sites]** が *[!UICONTROL On]*) ターゲットとするサイト。 サイトを検索して選択するか、ドメイン名を入力または貼り付けることができます。

1. クリック ![編集](/help/dsp/assets/edit.png).
1. サイトの指定：
   * サイトを検索するには：
      1. クリック **[!UICONTROL Search]**.
      1. キーワードを入力し、サイト層を選択し、サイトカテゴリを選択します。
      1. 検索結果で、含めるサイトを選択します。
         * 個々のサイトを除外するには、そのサイトの横にあるチェックボックスをオンにします。
         * （50 件を超える結果が得られる場合）最初の 50 件の結果を含めるには、 **[!UICONTROL Include these 50]**. すべての検索結果を含めるには、 **[!UICONTROL Include these \<*NN *\>]**.
   * ドメイン名を入力するには：
      1. click **[!UICONTROL Paste]**.
      1. 1 つ以上のドメイン名を別々の行に入力します。
      1. クリック **[!UICONTROL Include All]**.
1. クリック **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** 配置のオーディエンスターゲット ( [サードパーティセグメント、ファーストパーティセグメント、Adobeセグメント、カスタムセグメント、保存されたオーディエンス](/help/dsp/audiences/audience-settings.md). 選択したすべてのセグメントおよび保存されたオーディエンスの合計およびアクティブな重複排除オーディエンスサイズも表示されます。 既存のオーディエンスを選択したり、新しいオーディエンスを作成して後で再利用したり、特定のオーディエンスセグメントを選択したりできます。

* 既存のオーディエンスを選択するには、 ![選択](/help/dsp/assets/chevron-down.png) 隣に [!UICONTROL Included Audiences]をクリックし、オーディエンスを選択します。
* 新しいオーディエンスを作成するには、 ![選択](/help/dsp/assets/chevron-down.png) 隣に [!UICONTROL Included Audiences]を選択し、 **[!UICONTROL + Create Audience]**. 手順については、 [再利用可能なオーディエンスの作成](/help/dsp/audiences/reusable-audience-create.md)手順 3 から始まる
* 特定のオーディエンスセグメントを選択するには、 **[!UICONTROL Select segments for this placement only]**. セグメントロジックを選択します。手順については、「[再利用可能なオーディエンスの作成](/help/dsp/audiences/reusable-audience-create.md).」 完了したら、「 **保存**.

**[!UICONTROL Excluded Audiences]:** 配置の対象として除外するオーディエンス ( [サードパーティセグメント、ファーストパーティセグメント、Adobeセグメント、カスタムセグメント、保存されたオーディエンス](/help/dsp/audiences/audience-settings.md). 除外されたすべてのオーディエンスに対する合計とアクティブな重複排除オーディエンスのサイズも表示されます。 既存のオーディエンスを選択するか、新しいオーディエンスを作成して後で再利用できます。

* 既存のオーディエンスを選択するには、 ![選択](/help/dsp/assets/chevron-down.png) 隣に [!UICONTROL Excluded Audiences]をクリックし、オーディエンスを選択します。
* 新しいオーディエンスを作成するには、 ![選択](/help/dsp/assets/chevron-down.png) 隣に [!UICONTROL Excluded Audiences]を選択し、 **+オーディエンスを作成**. 手順については、 [再利用可能なオーディエンスの作成](/help/dsp/audiences/reusable-audience-create.md)手順 3 から始まる

**[!UICONTROL Cross Device Targeting]:** (1 つ以上のセグメントまたはオーディエンスを選択し、 [キャンペーンは、ユーザーベースのクロスデバイスターゲティング用に設定されます。](/help/dsp/campaign-management/campaigns/campaign-settings.md). 指定したセグメントに含まれていないデバイスも含め、（キャンペーン設定で指定したデバイスグラフごとに）ユーザーのすべての既知のデバイスにわたってターゲティングを拡張できます。 費用は、キャンペーンに指定したグラフに応じて適用される場合があります。 デバイスグラフデータは、現在、北米でのみ使用できます。

**[!UICONTROL Placement Cap]:** （オプション）個別のデバイスまたはユーザーの回数 ( 指定した [!UICONTROL Cross Device Level]) は、配置から広告を提供します。 オプションは次のとおりです。 *[!UICONTROL Unlimited]* または日、週、月ごとの特定の金額。

>[!NOTE]
>
> 頻度キャップは、キャンペーン、パッケージ、配置のレベルで設定できます。 DSPは、キャンペーン階層で最も厳格な頻度キャップに従います。

**[!UICONTROL Secondary Cap]:** ( オプション；数値を含める場合に使用できます [!UICONTROL Placement Cap]) プライマリ配置キャップの範囲内の追加の制限。 インプレッション数と期間（12 時間あたり 3 回など）を選択します。

**[!UICONTROL Day Parting]:** （オプション）広告を実行できる曜日と時刻を指定します。 時間帯区分間隔を指定するには：
1. クリック ![編集](/help/dsp/assets/edit.png).
1. 該当するタイムゾーンを選択します。
1. 間隔を指定します。
   * あらかじめ設定されている間隔を選択するには、間隔ボタンの 1 つをクリックします。 オプションは以下のとおりです*[!UICONTROL Weekends]** *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]*&#x200B;または *[!UICONTROL Prime]* (primetime)。
   * 間隔を手動で選択するには、セル内をクリックし、必要に応じてドラッグして間隔を選択します。
1. クリック **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** ( オプション；が [!DNL Comscore] および [!DNL Grapeshot] セグメント ) [!DNL Comscore] および [!DNL Grapeshot] をターゲットとして含めます。 この機能には追加料金が適用される場合があります。 この機能を有効にしてトピックセグメントを設定するには、 [!DNL Adobe] アカウントマネージャー

トピックのターゲット設定を指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. ターゲットとするセグメントを指定します。
   1. 左の列で、パートナー (*[!UICONTROL Comscore]* または *[!UICONTROL Grapeshot]*) をクリックします。
   1. 入力フィールドに、セグメント名またはセグメント ID を入力します。
1. （オプション）トピック情報を含む CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Export]**.
1. クリック **[!UICONTROL Save]**.

>[!TIP]
>
>* トピックのターゲティングでは、配置で入札できる在庫が制限されるので、トピックのターゲティングは、購入全体のごく一部に限られます。
>
>* セグメント内での除外ターゲティングを [!DNL Comscore] または [!DNL Grapeshot].


**[!UICONTROL Device Targeting]:** （オプション）ターゲットに含める、または除外するデバイスの種類、製造元、オペレーティングシステム、ブラウザー、接続の種類など、特定のデバイス情報。 デバイスのターゲット設定を指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 含めるおよび除外するデバイスの詳細を指定します。
   1. 左の列で、カテゴリを選択します。
   1. ターゲット設定の指定：
      * 値を含めるには、 **[!UICONTROL Include]** をクリックします。
      * 値を除外するには、 **[!UICONTROL Exclude]** をクリックします。
1. （オプション）デバイスのターゲット情報を含む CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Export]**.
1. クリック **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** （オプション）ターゲットに含めるか除外するか（両方は除外しない）を指定する特定のインターネットサービスプロバイダー (ISP)。 ISP のターゲティングを指定するには：

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

**[!UICONTROL Contextual filtering]:** のタイプ [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]および [!DNL Peer39] 適用するコンテキストフィルター。 広告主レベルのデフォルトは、新しい配置に対して選択されますが、設定は変更できます。

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** （オプション）デフォルトでブロックする 1 つ以上の在庫コンテキスト。 追加料金が適用される場合があります。

* [!UICONTROL Peer 39]:

   * **次のようなターゲットサイト** （オプション）デフォルトでターゲットにする 1 つ以上の在庫属性タイプ。 追加料金が適用される場合があります。

* [!UICONTROL ComScore]:

   * **次のサイトをブロックします。** （オプション）デフォルトでブロックする 1 つ以上の在庫属性のタイプ。 追加料金が適用される場合があります。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** （オプション）デフォルトで広告をブロックする成人向けコンテンツの程度。 *[!UICONTROL Do Not Block]* （デフォルト） *[!UICONTROL Standard]*&#x200B;または *[!UICONTROL Strict]*. 追加料金が適用される場合があります。

   * **[!UICONTROL Alcohol Content]:** （オプション）デフォルトで広告をブロックするアルコールコンテンツの程度。 *[!UICONTROL Do Not Block]* （デフォルト） *[!UICONTROL Standard]*&#x200B;または *[!UICONTROL Strict]*. 追加料金が適用される場合があります。

**[!UICONTROL Pre-bid fraud blocking]:** 不正なトラフィックや、 [!DNL DoubleVerify], [!DNL Integral Ad Science]および [!DNL Peer39]. 広告主レベルのデフォルトは、新しい配置に対して選択されますが、設定は変更できます。

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** デフォルトでは、は、新しい配置に対して、ハイジャックされたデバイス上のトラフィックを含む、100%の無効なトラフィックをすべてブロックします。 追加料金が適用される場合があります。

   * **[!UICONTROL Also block sites with]:** （オプション）デフォルトで広告をブロックする原因となる、追加のレベルの詐欺および無効なトラフィック： DSP  *[!UICONTROL None]* （デフォルトでは、追加のトラフィックはブロックされません）。 *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*&#x200B;または *[!UICONTROL >25% Average Fraud/IVT levels]*. 追加料金が適用される場合があります。

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** （オプション）デフォルトで広告をブロックする 1 つ以上の詐欺行為をDSPが行います。 *[!UICONTROL Fraud]* （詐欺行為を行ったサイトをすべてブロックします）。 *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*、または *[!UICONTROL Fraud: Zero Ads]*. 追加料金が適用される場合があります。

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** （オプション）デフォルトで広告をブロックする原因となる疑わしい Web サイトまたはアプリのアクティビティのタイプ。 *[!UICONTROL None]* （疑わしいアクティビティに基づいて広告をブロックしないデフォルト） *[!UICONTROL Suspicious Activity - High Risk]*&#x200B;または *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 追加料金が適用される場合があります。

**[!UICONTROL Ads.txt filtering]:**

レベル [Ads.txt](https://iabtechlab.com/ads-txt-about/) 各パブリッシャーの承認済みデジタル販売者リストを活用して、使用する入札前フィルタリング。 広告主レベルのデフォルトは、新しい配置に対して選択されますが、設定は変更できます。

* *[!UICONTROL Opt out of ads.txt (default)]*:売り手全員から在庫を買う。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*:ドメインの許可された直接販売者および再販者からの在庫の購入を優先する。
* *[!UICONTROL Ads.txt sellers only]*:ドメインの許可された直接販売者および再販者のみから在庫を購入する。
* *[!UICONTROL Ads.txt sellers only]*:ドメインの許可された直接販売者からのみ在庫を購入する。

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** ( [!UICONTROL DoubleVerify Authentic Brand Safety] オプション ) 有効 [!DNL DoubleVerify Authentic Brand Safety]：指定したセグメント ID に対して設定されたカスタムブランド安全ルールを使用して、入札後のインプレッションをブロックします。 DSPは、広告主設定で指定されたセグメント ID の使用を考慮してアカウントを請求します。

## [!UICONTROL Tracking]

>[!NOTE]
>
>([!DNL Roku] （配置）によって承認されたサードパーティのトラッキングベンダー [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]および [!DNL Research Now].

**[!UICONTROL Event Pixels]:** （オプション）配置のすべての新しい広告にデフォルトで添付されるサードパーティのイベント追跡ピクセル。 イベントのピクセルを指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作を行います。
   * 既存のピクセルを選択するには、ピクセル行のチェックボックスをオンにします。
   * 新しいピクセルを作成するには：
      1. クリック **[!UICONTROL Create]**.
      1. 次の情報を入力します。
         * **[!UICONTROL Pixel name]:** ピクセル名。最大長は 500 文字です。 ピクセルを簡単に識別できる名前を使用します。
         * **[!UICONTROL Pixel event fires on]:** 実行するピクセルをトリガーするイベント。 使用可能なイベントは広告タイプによって異なります。
         * **[!UICONTROL Pixel type]:** ピクセルが *[!UICONTROL IMG URL]* （1 x 1 ピクセルのイメージファイル） *[!UICONTROL HTML]*&#x200B;または *[!UICONTROL JavaScript URL]*.
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
         * **[!UICONTROL Click conversion window]:** 広告クリックが発生してからの日数で、クリックはコンバージョンに関連付けられます。 デフォルトは 30 日です。
         * **[!UICONTROL Notes]:** （オプション）ピクセルに関する説明またはその他の情報。
      1. クリック **[!UICONTROL Create and attach]**.
      1. 関連する Web ページにコンバージョンピクセルを実装します。
         1. メインメニューで、に移動します。 **[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**.
         1. ピクセル行で、 **[!UICONTROL edit]**.
         1. 値を [!UICONTROL HTML Tag] および [!UICONTROL Flash Tag] フィールドに値を入力し、必要に応じて、広告主または Web サイトの連絡先に提供します。

            広告主の IT 部門やその他のグループは、タグの導入をスケジュールしたり、通知を受けたりする必要がある場合があります。
   1. クリック **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** （オプション）インプレッション数 1,000 回あたりの請求不可能なコストとして追跡される静的な、サードパーティの料金。 別の値を入力しない限り、該当する場合、パッケージレベルのデフォルトが新しい配置に自動的に適用されます。

>[!NOTE]
>
>請求可能な料金は [!UICONTROL Net CPM] 指標を使用します。

>[!MORELIKETHIS]
>
>* [配置管理について](placement-about.md)
>* [プレースメントの作成](placement-create.md)
>* [プレースメントの編集](placement-edit.md)
>* [キーボードショートカット](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [キャンペーン管理に関する FAQ](/help/dsp/campaign-management/campaign-management-faq.md)

