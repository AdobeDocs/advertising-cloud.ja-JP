---
title: ブランドの安全性とメディアの品質
description: ブランドの安全性とメディア品質の機能の詳細を説明します。
feature: Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 0%

---

# ブランドの安全性とメディアの品質

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSPは、ブランド保護機能のスイートを提供し、各キャンペーンがブランドセーフ環境で実際のユーザーに届くようにします。

当社の不正監視チームは、[!DNL Interactive Advertising Bureau]、[!DNL Trust and Accountability Group][!DNL (TAG)]、[!DNL WhiteOps]などの業界をリードするパートナーと緊密に連携し、プラットフォーム上の在庫を慎重にキュレートします。 DSPは、アドビの供給を積極的に管理することで、プラットフォーム全体のすべての広告主を非人間トラフィック（ボット、クローラー、データセンタートラフィック、不正）から保護し、ブランドセーフなコンテキストでのみ配信します。

一元的な品質管理を提供するだけでなく、広告主がブランドに合わせた制御を設計できるようにすることを信じています。 Adobe Advertising Cloudは、[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]、[!DNL Oracle Data Cloud]および[!DNL Peer39]との統合を提供し、各広告主が適切なレベルの不正保護、コンテキストフィルタリング、キーワードターゲティングを選択できるようにします。

## Advertising Cloud DSPの品質イニシアティブ

### [!DNL Ads.txt]をサポートしたインベントリの検証

[[!DNL Ads.txt], which stands for [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) は、2017年6月に( [!DNL Interactive Advertising Bureau] [!DNL IAB])が開始したイニシアチブで、公開市場における在庫の適切な表示を促進し、トラフィックの不正なソースやドメインスプーフィングと競合します。参加するパブリッシャーやディストリビューターは、ドメインの最上位レベルに`ads.txt`ページを維持することで、デジタルインベントリを販売する権限を持つ会社と、それらの関係の性質を公に宣言します（`example.com/ads.txt`など）。

DSPは、各パブリッシャーの`ads.txt`ファイルを読み取り、検証済みの[!DNL ads.txt]販売者のみから購入するオプションを提供することで、[!DNL ads.txt]をサポートします。 例えば、`nytimes.com`にアクセスする販売者をNew York Timesの`ads.txt`ファイルと照合することで、正当でないかどうかを特定でき、検証された販売者のみから購入するように配置が設定されている場合は、違反者をブロックします。<!-- can we actually mention NY Times? -->

各広告主<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->のデフォルトの[!DNL ads.txt]コントロールを設定し、オプションで[各配置の設定をカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md)して次の操作を行うことができます。

* ドメインの正規直売人のみから在庫を購入する

* ドメインの認定直接販売者および再販売者のみから在庫を購入する

* ドメインの承認済み直販業者および再販業者からの在庫の購入を優先する

* 全販売業者から在庫を買う

### プラットフォーム不正監視

DSPは、[!DNL Whiteops]や[!DNL Integral Ad Science]などの主要な業界ベンダーと提携し、アドビのプラットフォーム全体で不正を管理する強力な内部ツールおよびシステムを構築しています。

さらに、Adobeは[!DNL IAB]と[!DNL TAG]と緊密に連携し、[!DNL ads.txt]（前の節を参照）、[!DNL IAB]ボットとスパイダーリスト、[!DNL TAG]データセンターのIPリストなどのツールを活用して、業界標準の堅牢な不正ブロックを保証します。

品質に対する多次元的なアプローチを通じて、アドビのチームは異常値と無効なトラフィックパターンを監視し、保護されたインベントリ上で無効なトラフィックが3%未満になるようにします。 特定のドメイン上の在庫や、特定の発行者または販売者からの在庫など、疑わしい在庫は、プラットフォーム全体で直ちにブロックされます。

### インベントリのマッピング、階層化、および分類

在庫マッピングは、新しい在庫がプラットフォームに追加される前に必要となる詳細なレビューとオンボーディングプロセスです。 このプロセスは、DSP上のすべてのインベントリの安全性と品質を確保するように設計されています。

* **マッピング：** 在庫チームは各ドメインを慎重にレビューし、次のような側面を評価します。

   * ブランドの安全性

   * 広告タイプの検証

   * 汎用コンテンツ、重複ドメイン、および偽の広告配信

* **階層化：** エコシステム全体でのブランドのプレゼンスを総合的に調べ、異なる階層にわたってインベントリを分類します。目的のリーチレベルに合わせて、プレースメント](/help/dsp/campaign-management/placements/placement-settings.md)をこれらの層に[ターゲット設定できます。

   * **[!UICONTROL T1]**  — ブランド名、国際的に認識可能なサイト

   * **[!UICONTROL T2]**  — 最新で最新の、ユーザー生成コンテンツを含まない、通常はグローバル認識に欠ける優れたサイト

   * **[!UICONTROL T3]**  — ユーザー生成コンテンツとニッチコンテンツ

* **サイトの分類：** コンテンツのターゲティングとブロックを容易におこなうために、各プロパティに、プロパティのコンテンツに基づくAdvertising Cloud定義のサイトカテゴリをタグ付けします。配置目標に基づいて、各配置](/help/dsp/campaign-management/placements/placement-settings.md)に対して、これらのサイトカテゴリを[ターゲットにしたり除外したりできます。

### サイトブロックの包括的なサポート

Advertising Cloud DSPは、グローバルにブロックされたサイトのリストと、広告主やアカウント用にカスタムのブロックされたサイトのリストを作成するオプションの両方を提供します。

#### Advertising Cloud DSP Globally Blocked Sites List

Advertising Cloud DSPは、広告の実行が安全でないと見なされる、グローバルにブロックされたサイトのリストを管理します。 このリストには、不快なコンテンツ（憎しみやテロなど）や、ボットに感染したサイト、偽のプリロール、不一致のドメイン、その他の不正行為を含むサイトが含まれています。

広告主を欺く活動を根付かせるBrand Safetyイニシアティブの一環として、すべてのサイトは、グラフブロックサイトリストの測定を使用してスクリーニングされます。 ブランドの安全性チェックに合格しないすべてのサイトは、グローバルにブロックされたサイトのリストに追加されます。 Advertising Cloud DSPはこのリストを動的に管理するので、最新のブランド安全性分析に基づいて、サイトはいつでもリストのオン/オフを切り替えることができます。

グローバルにブロックされたサイトのリストにサイトを配置ターゲットとして含めると、そのサイトには赤い感嘆符(!)のフラグが付けられます。 これは、フラグ付きのサイトで広告が実行されないことを示します。

#### アカウントレベルのサイトリストと広告主レベルのブロックされたサイトリスト

また、アカウントレベルおよび広告主レベルのブロックされたサイトリスト<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->を管理することもできます。これらは、すべての配置に自動的に使用されます。 下位レベルのブロックサイトのリストは、グローバルにブロックされたサイトのリストに加えて適用されます。

## サードパーティ統合

### コンテキストフィルタリング

コンテキストフィルタリングを使用すると、広告が提供されるページのコンテキストに基づいて広告オポチュニティをターゲットにしたりブロックしたりできます。 Adobeは、業界の主要ベンダーとの統合を通じて、コンテキストフィルタリングを提供します。[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]、および[!DNL Peer39]です。 現在のフィルターの例としては、[!UICONTROL Adult Content]、[!UICONTROL Natural Disasters]、[!UICONTROL Legal Drinking Age]、[!UICONTROL MANGA]、[!UICONTROL Epidemics]、[!UICONTROL G-rated Sites]があります。

各広告主<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->に対してデフォルトのコンテキストフィルターコントロールを設定し、オプションで[各配置の設定をカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md)できます。 この機能を使用する場合は、追加料金が適用される場合があります。

![Comscore ](/help/dsp/assets/comscore-logo.png) ![logoDoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![logoIntegral Ad Science ](/help/dsp/assets/ias-logo.png) ![logoPeer39 logo](/help/dsp/assets/peer39-logo.png)

### 入札前の不正ブロック

[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]および[!DNL Peer39]とのサードパーティ統合を活用して、非人道的なトラフィックをキャンペーンからブロックします。 これらの統合により、キャンペーンの一般的な無効なトラフィックと高度な無効なトラフィック（GIVTおよびSIVT）の両方を最小限に抑える、業界をリードする入札前のブロック機能が提供されます。

各広告主<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->に対してデフォルトの入札前不正ブロック制御を設定し、オプションで[各配置の設定をカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md)できます。 この機能を使用する場合は、追加料金が適用される場合があります。

機能の詳細については、お使いのベンダーに直接お問い合わせいただくか、担当のAdobeアカウントマネージャーにお問い合わせください。

![Comscore ](/help/dsp/assets/comscore-logo.png) ![logoDoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![logoIntegral Ad Science ](/help/dsp/assets/ias-logo.png) ![logoPeer39 logo](/help/dsp/assets/peer39-logo.png)

### 入札前の視認性 {#pre-bid-viewability}

業界をリードするパートナー[!DNL DoubleVerify]、[!DNL Oracle Advertising]([!DNL Moat])、[!DNL Integral Ad Science]を活用した入札前の視認性フィルターにより、広告主はキャンペーンがビデオやディスプレイの在庫全体で目的の視認性パフォーマンス目標を満たすことができます。

各広告主<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->のデフォルトの視認性フィルターを設定し、オプションで[各配置の設定をカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md)できます。 この機能を使用する場合は、追加料金が適用される場合があります。

![DoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![logoOracle Advertising ](/help/dsp/assets/oracle-advertising-logo.png) ![logoIntegral Ad Scienceロゴ](/help/dsp/assets/ias-logo.png)

### トピックのターゲット設定

DSPトピックのターゲット設定では、業界をリードするコンテキストパートナー[!DNL Comscore]と[!DNL Oracle Data Cloud]([!DNL Grapeshot])を活用して、キーワードリストをターゲット化またはブロックできます。

トピックのターゲティングを使用すると、有害なコンテンツのブロックや、より大きな結果を確実に得るためのコンテキストでの支出など、ブランドに合致した環境で広告を常に提供できます。

トピックのターゲティングでは、[!DNL Comscore]または[!DNL Grapeshot]（[!DNL Oracle Data Cloud]を使用）を使用してトピックセグメントを直接作成する必要があります。 これらをパートナープラットフォームで作成したら、[各プレースメントの](/help/dsp/campaign-management/placements/placement-settings.md)セクションでセグメントIDを[!UICONTROL  Audience Targeting]ターゲットにしたり除外したりできます。 この機能には追加料金が適用される場合があります。

使用を開始するには、お使いのベンダーまたはAdobeのアカウントマネージャーにお問い合わせください。

![Comscore ](/help/dsp/assets/comscore-logo.png) ![logoGrapeshotロゴ](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSPは[!DNL DoubleVerify]と提携し、[!DNL Authentic Brand Safety]ターゲティングソリューションを提供しています。これにより、すべての購入プラットフォームを対象とし、一貫性を保つために、一元化されたブランド安全要件を作成できます。

必要なターゲティングを備えた[!DNL DoubleVerify]ブランドの安全セグメントを構築したら、DSP内でそのセグメントを使用して、Web環境全体で入札前のブロックルールを複製できます。

各広告主<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->に[!DNL DoubleVerify]セグメントIDを指定し、オプションで[各プレースメント](/help/dsp/campaign-management/placements/placement-settings.md)の[!UICONTROL Authentic Brand Safety]を有効または無効にすることができます。 DSPは、セグメントIDの使用を考慮してアカウントを請求します。

機能の詳細については、[!DNL DoubleVerify]に直接お問い合わせいただくか、担当のAdobeアカウントマネージャーにお問い合わせください。

![DoubleVerifyロゴ](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
