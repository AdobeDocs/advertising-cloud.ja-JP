---
title: ブランドの安全性とメディア品質
description: ブランドの安全性とメディア品質の機能の詳細をご覧ください。
feature: DSP Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '1350'
ht-degree: 0%

---

# ブランドの安全性とメディア品質

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSPは、ブランド保護機能のスイートを提供し、各キャンペーンがブランドセーフ環境で実際のユーザーに届くようにします。

当社の不正監視チームは、次のような業界をリードするパートナーと密接に連携しています。 [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)]、および [!DNL WhiteOps]を使用して、プラットフォーム上の在庫を慎重にキュレーションします。 DSPは、アドビの供給を積極的に管理することで、プラットフォーム全体のすべての広告主が非人間トラフィック（ボット、クローラー、データセンタートラフィック、不正）から保護され、ブランドに安全なコンテキストでのみ配信できるようにします。

一元的な品質管理を提供するだけでなく、広告主がブランドに合わせた制御を設計できるようにすることを信じています。 DSPは、 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud]、および [!DNL Peer39]を使用することで、各広告主が適切なレベルの不正保護、コンテキストフィルタリング、キーワードターゲティングを選択できるようになります。

## 品質イニシアチブ

### との在庫の検証 [!DNL Ads.txt] サポート

[[!DNL Ads.txt]は、 [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) は、 [!DNL Interactive Advertising Bureau] ([!DNL IAB]) 2017 年 6 月にオープンマーケットでのインベントリの適切な表示を容易にし、トラフィックの不正なソースとドメインのスプーフィングと戦う。 参加するパブリッシャーおよびディストリビューターは、デジタルインベントリを販売する権限を持つ企業を、 `ads.txt` ドメインの最上位レベルのページ ( `example.com/ads.txt`) をクリックします。

DSPサポート [!DNL ads.txt] 各出版社の `ads.txt` ファイルを作成し、検証済みからのみを購入するオプションを提供する [!DNL ads.txt] 販売者 例えば、販売者と照合すると、にアクセスしているのがわかります `nytimes.com` ニューヨーク・タイムズに `ads.txt` ファイルを編集すると、正当なものと正当でないものを特定できます。認定販売者のみから購入するように配置が設定されている場合は、違反者をブロックします。 <!-- can we actually mention NY Times? -->

デフォルトを設定できます [!DNL ads.txt] 各広告主のコントロール<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->（オプション） [各配置の設定をカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md) 移動先：

* ドメインの許可された直接販売者のみから在庫を購入する

* ドメインの許可された直接販売者および再販売者のみから在庫を購入する

* ドメインの許可された直接販売者および再販売者から在庫を購入することを優先する

* すべての販売者から在庫を購入する

### プラットフォーム不正監視

DSPは、アドビのプラットフォーム全体で不正を管理するための強力な内部ツールおよびシステムを構築し、次のような業界の主要ベンダーと提携しています。 [!DNL Whiteops] および [!DNL Integral Ad Science].

さらに、Adobeは [!DNL IAB] および [!DNL TAG] 業界標準の堅牢な不正ブロックを確保して広告主を保護するために、 [!DNL ads.txt] （前の節を参照）、 [!DNL IAB] ボットおよびスパイダーのリスト、および [!DNL TAG] データセンターの IP リスト。

品質に対する多次元的なアプローチを通じて、チームは異常値と無効なトラフィックパターンを監視し、保護された在庫で無効なトラフィックが 3%未満になるようにします。 特定のドメイン上の在庫や特定の発行者または販売者からの在庫など、疑わしい在庫は、プラットフォーム全体で即座にブロックされます。

### インベントリのマッピング、階層化、分類

在庫マッピングは、新しいすべての在庫がアドビのプラットフォームに追加される前に必要となる詳細なレビューとオンボーディングプロセスです。 このプロセスは、DSP上のすべてのインベントリの安全性と品質を確保するように設計されています。

* **マッピング：** アドビのインベントリチームは、各ドメインを慎重にレビューし、次のような側面を評価します。

   * ブランドの安全性

   * 広告タイプの検証

   * 汎用コンテンツ、重複ドメイン、および偽の広告配信

* **階層化：** エコシステム全体でのブランドの存在を総合的に調べ、異なる階層にわたるインベントリを分類します。 以下が可能です。 [配置のターゲット設定](/help/dsp/campaign-management/placements/placement-settings.md) を次の層に追加して、必要なリーチレベルに設定します。

   * **[!UICONTROL T1]**  — ブランド名、国際的に認識可能なサイト

   * **[!UICONTROL T2]**  — 最新で最新の、ユーザー生成コンテンツを含まない、通常グローバルな認識に欠ける優れた外観のサイト

   * **[!UICONTROL T3]**  — ユーザー生成コンテンツとコンテンツのニッチ化

* **サイトの分類：** コンテンツのターゲティングとブロックを容易におこなえるように、各プロパティに、プロパティのコンテンツに基づいてDSPで定義されたサイトカテゴリでタグ付けします。 以下が可能です。 [各プレースメントに対してこれらのサイトカテゴリをターゲット化または除外](/help/dsp/campaign-management/placements/placement-settings.md) 配置目標に基づいて

### サイトブロックの包括的なサポート

DSPは、グローバルにブロックされたサイトリストと、広告主やアカウントのカスタムブロックされたサイトリストを作成するオプションの両方を提供します。

#### グローバルにブロックされたサイトリストをDSP {#global-blocked-sites}

DSPは、広告の実行が安全でないと見なされる、グローバルにブロックされたサイトリストを管理します。 このリストには、好ましくないコンテンツ（憎しみや恐怖など）や、ボットに感染したサイト、偽のプリロール、不一致のドメイン、その他の不正なアクティビティを含むサイトが含まれています。

広告主を欺く活動を根絶するための Brand Safety イニシアティブの一環として、すべてのサイトは、グラフブロックサイトリストの測定を使用してスクリーニングされます。 ブランドの安全性チェックに合格しないすべてのサイトは、グローバルにブロックされたサイトリストに追加されます。 DSPはこのリストを動的に管理するので、最新のブランド安全性分析に基づいて、サイトはいつでもリストのオン/オフを切り替えることができます。

グローバルにブロックされたサイトのリストにサイトを配置のターゲットとして含めると、サイトには赤い感嘆符 (!) でフラグが付けられます。 これは、フラグ付きのサイトで広告が実行されないことを示します。

>[!NOTE]
>
>オプションで、信頼できる非公開取引に添付された標準ディスプレイ広告に対して、グローバルブロックサイトリストをバイパスするには、「[!UICONTROL Allow unscreened sites]」オプションが [配置設定](/help/dsp/campaign-management/placements/placement-settings.md). 必要に応じて、 [!DNL Adobe] アカウントチームは、オプションで、契約のパブリッシャー設定で、公開（オークションレベル）契約のサイトブロックを無効にすることもできます。

#### アカウントレベルのサイトリストと広告主レベルのブロック済みサイトリスト

また、アカウントレベルのサイトリストと、広告主レベルのブロック済みサイトリストを管理することもできます<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->：すべての配置に自動的に使用されます。 下位レベルのブロック済みサイトのリストは、グローバルにブロックされたサイトのリストに加えて適用されます。

## サードパーティ統合

### コンテキストフィルター

コンテキストフィルタリングを使用すると、広告が提供されるページのコンテキストに基づいて、広告オポチュニティをターゲットにしたりブロックしたりできます。 Adobeは、業界の主要ベンダーとの統合を通じて、コンテキストフィルタリングを提供します。 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]、および [!DNL Peer39]. 現在のフィルターの例を次に示します。 [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics]、および [!UICONTROL G-rated Sites].

各広告主に対して、デフォルトのコンテキストフィルターコントロールを設定できます<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->（オプション） [各配置の設定をカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md). この機能を使用する場合は、追加料金が適用される場合があります。

![Comscore ロゴ](/help/dsp/assets/comscore-logo.png) ![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science ロゴ](/help/dsp/assets/ias-logo.png) ![Peer39 ロゴ](/help/dsp/assets/peer39-logo.png)

### 入札前の不正ブロック

とのサードパーティ統合を活用する [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]、および [!DNL Peer39] を使用して、キャンペーンからの非人間トラフィックをブロックします。 これらの統合により、キャンペーンで一般的な無効なトラフィックと高度な無効なトラフィック（GIVT および SIVT）の両方を最小限に抑える、業界最先端の入札前ブロック機能が提供されます。

各広告主に対して、デフォルトの入札前不正ブロック制御を設定できます<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->（オプション） [各配置の設定をカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md). この機能を使用する場合は、追加料金が適用される場合があります。

機能の詳細については、ご希望のベンダーに直接お問い合わせいただくか、 [!DNL Adobe] アカウントチーム。

![Comscore ロゴ](/help/dsp/assets/comscore-logo.png) ![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science ロゴ](/help/dsp/assets/ias-logo.png) ![Peer39 ロゴ](/help/dsp/assets/peer39-logo.png)

### 入札前の視認性 {#pre-bid-viewability}

業界をリードするパートナーによる事前入札の視認性フィルター [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) および [!DNL Integral Ad Science] 広告主は、キャンペーンがビデオ全体で目標とする視認性のパフォーマンス目標を満たし、在庫を表示できるようにします。

各広告主に対して、デフォルトの視認性フィルターを設定できます<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->（オプション） [各配置の設定をカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md). この機能を使用する場合は、追加料金が適用される場合があります。

![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png) ![Oracle広告ロゴ](/help/dsp/assets/oracle-advertising-logo.png) ![Integral Ad Science ロゴ](/help/dsp/assets/ias-logo.png)

### トピックのターゲティング

DSPトピックのターゲット設定では、業界をリードするコンテキストパートナーを活用して、キーワードリストをターゲティングまたはブロックできます [!DNL Comscore] および [!DNL Oracle Data Cloud] ([!DNL Grapeshot]) をクリックします。 トピックのターゲティングを使用すると、有害なコンテンツのブロックや、より大きな成果を確実に得るためのコンテキストでの支出を含め、ブランドに沿った環境で広告を常に提供できます。

トピックのターゲティングでは、を使用してカスタムトピックセグメントを直接作成する必要があります。 [!DNL Comscore] または [!DNL Grapeshot] ( [!DNL Oracle Data Cloud]) をクリックします。 これらをパートナープラットフォームで作成したら、次の操作を実行できます。 [セグメント ID を [!UICONTROL Audience Targeting] 各配置のセクション](/help/dsp/campaign-management/placements/placement-settings.md). この機能には追加料金が適用される場合があります。

カスタムトピックセグメントを作成するには：

* を作成するには、以下を実行します。 [!DNL Comscore] アカウントを作成してカスタムセグメントを作成すると、 [!DNL Activation Segment Manager] 時刻 [https://agents.comscore.com](https://agents.comscore.com). 詳しくは、 [[!DNL Comscore] ヘルプセンター](https://comscoreactivation.zendesk.com/hc/) を参照してください。 カスタムセグメントの料金は、 [!DNL Segment Manager] 作成時に

* を使い始めるには、以下を実行します。 [!DNL Oracle Data Cloud]，連絡先 [!DNL Oracle Data Cloud] または [!DNL Adobe] アカウントチーム。

![Comscore ロゴ](/help/dsp/assets/comscore-logo.png) ![Grapeshot ロゴ](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSPは [!DNL DoubleVerify] 申し出る [!DNL Authentic Brand Safety] ターゲティングソリューション：一貫性を保つために、すべての購入プラットフォームを対象とする、一元化されたブランドの安全要件のセットを作成できます。

を作成したら、 [!DNL DoubleVerify] 必要なターゲット設定を含む brand safety セグメントを使用すると、DSP内でそのセグメントを使用して、web 環境全体で入札前のブロックルールをレプリケートできます。

次の項目を指定できます。 [!DNL DoubleVerify] 各広告主のセグメント ID<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->（オプション） [有効化または無効化 [!UICONTROL Authentic Brand Safety] 各配置に対して](/help/dsp/campaign-management/placements/placement-settings.md). DSPは、セグメント ID の使用を目的としてアカウントを請求します。

機能について詳しくは、 [!DNL DoubleVerify] 直接、または [!DNL Adobe] アカウントチーム。

![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
