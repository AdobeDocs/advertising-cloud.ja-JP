---
title: ブランドの安全性とメディア品質
description: ブランドの安全性とメディア品質の機能の詳細を説明します。
feature: DSP Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: e0713f3717a684fb5ef2808d7de769424b8972d2
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# ブランドの安全性とメディア品質

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSPは、ブランド保護機能のスイートを提供し、各キャンペーンがブランドセーフ環境で実際のユーザーに届くようにします。

当社の不正監視チームは、 [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)]および [!DNL WhiteOps]を使用して、プラットフォーム上の在庫を慎重にキュレーションします。 DSPは、アドビの供給を積極的に管理することで、プラットフォーム全体のすべての広告主を非人間トラフィック（ボット、クローラー、データセンタートラフィック、不正）から保護し、ブランドに安全なコンテキストでのみ配信します。

当社は、一元的な品質管理を提供するだけでなく、広告主が自社のブランドに合わせた制御を設計できるようにすることを信じています。 Adobe Advertising Cloudは、 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud]および [!DNL Peer39]を使用することで、各広告主が目的とするレベルの詐欺対策、コンテキストフィルタリング、キーワードターゲティングを選択できるようになります。

## Advertising Cloud DSP Quality Initiatives

### との在庫の検証 [!DNL Ads.txt] サポート

[[!DNL Ads.txt], which stands for [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) は、 [!DNL Interactive Advertising Bureau] ([!DNL IAB]) 2017 年 6 月にオープン市場でのインベントリの適切な表示を促進し、トラフィックの不正なソースとドメインのスプーフィングと戦う。 参加する出版社や販売業者は、デジタルインベントリを販売する権限を持つ企業と、その関係性を、 `ads.txt` ドメインの最上位レベルのページ ( `example.com/ads.txt`) をクリックします。

DSPサポート [!DNL ads.txt] 各出版社の `ads.txt` ファイルを作成し、検証済みからのみ購入するオプションを提供 [!DNL ads.txt] 販売者 例えば、販売者を照合すると、 `nytimes.com` ニューヨーク・タイムズに `ads.txt` ファイルを作成すると、正当でないものとそうでないものを特定できます。また、認定販売者のみから購入するように設定されている場合は、違反者をブロックします。 <!-- can we actually mention NY Times? -->

デフォルトを設定できます [!DNL ads.txt] 各広告主のコントロール<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->を選択し、 [各配置の設定のカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md) 次の値に設定：

* ドメインの正規直売人のみから在庫を購入する

* ドメインの認定直販業者と再販業者のみから在庫を購入する

* ドメインの承認された直接販売者および再販売者からの在庫の購入を優先する

* 全販業者から在庫を買う

### プラットフォーム不正監視

DSPは、アドビのプラットフォーム全体で詐欺を管理し、次のような主要な業界ベンダーと提携するための強力な内部ツールおよびシステムを構築しています。 [!DNL Whiteops] および [!DNL Integral Ad Science].

また、Adobeは [!DNL IAB] および [!DNL TAG] 業界標準の堅牢な詐欺ブロックを確保し、広告主を保護するために、 [!DNL ads.txt] （前の節を参照）、 [!DNL IAB] ボットおよびスパイダーリスト、および [!DNL TAG] データセンターの IP リスト。

品質に対する多次元的なアプローチを通じて、チームは異常値と無効なトラフィックパターンを監視し、保護されたインベントリで無効なトラフィックが 3 %未満になるようにします。 特定のドメイン上の在庫や、特定のパブリッシャーまたは販売者からの在庫など、疑わしい在庫は、プラットフォーム全体で直ちにブロックされます。

### 在庫のマッピング、階層化、分類

在庫マッピングは、新しい在庫をプラットフォームに追加する前に必要となる詳細なレビューとオンボーディングプロセスです。 このプロセスは、DSP上のすべてのインベントリの安全性と品質を確保するように設計されています。

* **マッピング：** アドビのインベントリチームは、各ドメインを慎重にレビューし、次のような側面を評価します。

   * ブランドの安全性

   * 広告タイプの検証

   * 汎用コンテンツ、重複ドメイン、および偽の広告配信

* **階層化：** エコシステム全体でのブランドの存在を総合的に調べ、異なる階層にわたる在庫を分類します。 次の操作が可能です。 [配置のターゲット設定](/help/dsp/campaign-management/placements/placement-settings.md) を次の階層に追加して、必要なリーチレベルを絞り込みます。

   * **[!UICONTROL T1]**  — ブランド名、国際的に認識可能なサイト

   * **[!UICONTROL T2]**  — 最新で最新の、ユーザー生成のコンテンツを含まず、通常はグローバル認識に欠ける優れたサイト

   * **[!UICONTROL T3]**  — ユーザー生成コンテンツとニッチコンテンツ

* **サイトの分類：** コンテンツのターゲティングとブロックを容易におこなえるように、各プロパティに、プロパティのコンテンツに基づいてAdvertising Cloud定義のサイトカテゴリをタグ付けします。 次の操作が可能です。 [各プレースメントに対してこれらのサイトカテゴリをターゲットにするか除外します。](/help/dsp/campaign-management/placements/placement-settings.md) 配置目標に基づいて。

### サイトブロックの包括的なサポート

Advertising Cloud DSPは、グローバルにブロックされたサイトリストと、広告主やアカウント用のカスタムブロックされたサイトリストを作成するオプションの両方を提供します。

#### Advertising Cloud DSPグローバルにブロックされたサイトのリスト

Advertising Cloud DSPは、広告の実行が安全でないと見なされる、グローバルにブロックされたサイトのリストを管理しています。 このリストには、不快なコンテンツ（憎しみや恐怖など）や、ボットに感染したサイト、偽のプリロール、不一致のドメイン、その他の不正な活動を含むサイトが含まれています。

広告主を欺く活動を根付かせるための Brand Safety イニシアチブの一環として、すべてのサイトは、グラフブロックサイトリストの測定を使用してスクリーニングされます。 ブランドの安全性チェックに合格しないすべてのサイトは、グローバルにブロックされたサイトのリストに追加されます。 Advertising Cloud DSPはこのリストを動的に管理するので、最新のブランド安全性分析に基づいて、サイトはいつでもリストのオン/オフを切り替えることができます。

グローバルにブロックされたサイトのリストにサイトを配置のターゲットとして含めると、そのサイトには赤い感嘆符 (!) のフラグが付けられます。 これは、フラグが設定されたサイトで広告が実行されないことを示します。

#### アカウントレベルのサイトリストと広告主レベルのブロックされたサイトリスト

また、アカウントレベルのサイトリストや広告主レベルのブロックサイトリストを管理することもできます<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->：すべての配置に自動的に使用されます。 下位レベルのブロックサイトのリストは、グローバルにブロックされたサイトのリストに加えて適用されます。

## サードパーティ統合

### コンテキストフィルター

コンテキストフィルタリングを使用すると、広告が提供されるページのコンテキストに基づいて、広告オポチュニティをターゲティングまたはブロックできます。 Adobeは、業界の主要ベンダーとの統合を通じて、コンテキストフィルタリングを提供します。 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]および [!DNL Peer39]. 現在のフィルターの例は次のとおりです。 [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics]および [!UICONTROL G-rated Sites].

各広告主に対して、デフォルトのコンテキストフィルターコントロールを設定できます<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->を選択し、 [各配置の設定のカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md). この機能を使用すると、追加料金が発生する場合があります。

![Comscore ロゴ](/help/dsp/assets/comscore-logo.png) ![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science ロゴ](/help/dsp/assets/ias-logo.png) ![Peer39 ロゴ](/help/dsp/assets/peer39-logo.png)

### 入札前の不正ブロック

とのサードパーティ統合を活用する [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]および [!DNL Peer39] を使用して、キャンペーンから非人間トラフィックをブロックします。 これらの統合により、業界をリードする入札前のブロック機能が提供され、キャンペーンの一般的な無効なトラフィックと高度な無効なトラフィック（GIVT および SIVT）の両方を最小限に抑えることができます。

各広告主に対して、デフォルトの入札前の不正ブロック制御を設定できます<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->を選択し、 [各配置の設定のカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md). この機能を使用すると、追加料金が発生する場合があります。

機能の詳細については、お客様のご希望のベンダーに直接お問い合わせいただくか、 [!DNL Adobe] アカウントマネージャー

![Comscore ロゴ](/help/dsp/assets/comscore-logo.png) ![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science ロゴ](/help/dsp/assets/ias-logo.png) ![Peer39 ロゴ](/help/dsp/assets/peer39-logo.png)

### 入札前の視認性 {#pre-bid-viewability}

業界をリードするパートナーによる入札前の視認性フィルタ [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) および [!DNL Integral Ad Science] 広告主は、キャンペーンがビデオ全体で目的の視認性能の目標を満たし、在庫を表示できるようになります。

各広告主に対して、デフォルトの視認性フィルターを設定できます<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->を選択し、 [各配置の設定のカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md). この機能を使用すると、追加料金が発生する場合があります。

![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png) ![Oracle広告ロゴ](/help/dsp/assets/oracle-advertising-logo.png) ![Integral Ad Science ロゴ](/help/dsp/assets/ias-logo.png)

### トピックのターゲティング

DSPトピックのターゲット設定を使用すると、業界をリードするコンテキストパートナーを活用して、キーワードリストをターゲティングまたはブロックできます。 [!DNL Comscore] および [!DNL Oracle Data Cloud] ([!DNL Grapeshot]) をクリックします。

トピックのターゲティングを使用すると、有害なコンテンツのブロックや、より大きな結果を得るためのコンテキストでの支出を含め、広告が常にブランドと一致する環境で提供されることを確認できます。

トピックのターゲティングでは、を使用してトピックセグメントを直接作成する必要があります。 [!DNL Comscore] または [!DNL Grapeshot] ( [!DNL Oracle Data Cloud]) をクリックします。 これらをパートナープラットフォームで作成したら、 [セグメント ID を[!UICONTROL  Audience Targeting] 各配置のセクション](/help/dsp/campaign-management/placements/placement-settings.md). この機能には追加料金が適用される場合があります。

利用を開始するには、お使いのベンダーまたは [!DNL Adobe] アカウントマネージャー

![Comscore ロゴ](/help/dsp/assets/comscore-logo.png) ![Grapeshot ロゴ](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSPは [!DNL DoubleVerify] 申し出る [!DNL Authentic Brand Safety] ターゲティングソリューション：すべての購入プラットフォームを対象とし、一貫性を保つために、一元化されたブランドの安全要件のセットを作成できます。

作成した [!DNL DoubleVerify] 必要なターゲティングを含む Brand Safety セグメントを使用すると、DSP内でそのセグメントを使用して、Web 環境全体で入札前のブロックルールをレプリケートできます。

次の [!DNL DoubleVerify] 各広告主のセグメント ID<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->を選択し、 [有効化または無効化 [!UICONTROL Authentic Brand Safety] 配置ごとに](/help/dsp/campaign-management/placements/placement-settings.md). DSPは、セグメント ID の使用を考慮してアカウントを請求します。

機能の詳細については、 [!DNL DoubleVerify] 直接、または [!DNL Adobe] アカウントマネージャー

![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
