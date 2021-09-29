---
title: ブランドの安全性とメディア品質
description: ブランドの安全性とメディア品質の機能の詳細を説明します。
feature: DSP Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: cebe80fa8ed4f6410a7ea3ee7be6e0bf03631a49
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 0%

---

# ブランドの安全性とメディア品質

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSPは、ブランド保護機能のスイートを提供し、各キャンペーンがブランドセーフ環境で実際のユーザーに届くようにします。

当社の不正監視チームは、[!DNL Interactive Advertising Bureau]、[!DNL Trust and Accountability Group][!DNL (TAG)]、[!DNL WhiteOps] など、業界をリードするパートナーと緊密に連携し、プラットフォーム上の在庫を慎重にキュレートします。 DSPは、アドビの供給を積極的に管理することで、プラットフォーム全体のすべての広告主を非人間トラフィック（ボット、クローラー、データセンタートラフィック、不正）から保護し、ブランドに安全なコンテキストでのみ配信します。

当社は、一元的な品質管理を提供するだけでなく、広告主が自社のブランドに合わせた制御を設計できるようにすることを信じています。 Adobe Advertising Cloudは、[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]、[!DNL Oracle Data Cloud] および [!DNL Peer39] との統合を提供し、各広告主が適切なレベルの詐欺対策、コンテキストフィルタリング、キーワードターゲティングを選択できるようにします。

## Advertising Cloud DSP Quality Initiatives

### [!DNL Ads.txt] をサポートしたインベントリの検証

[[!DNL Ads.txt], which stands for [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) は、2017 年 6 月に ( [!DNL Interactive Advertising Bureau] [!DNL IAB]) が開始した、公開市場における在庫の適切な表示を促進し、トラフィックの不正な源やドメインスプーフィングと競合するイニシアチブです。参加するパブリッシャーやディストリビューターは、ドメインの最上位レベル（`example.com/ads.txt` など）に `ads.txt` ページを維持することで、デジタルインベントリを販売する権限を持つ企業とその関係性を公式に宣言します。

DSPは、各パブリッシャーの `ads.txt` ファイルを読み取り、検証済みの [!DNL ads.txt] 販売者のみから購入するオプションを提供することで、[!DNL ads.txt] をサポートします。 例えば、`nytimes.com` にアクセスする販売者を New York Times の `ads.txt` ファイルと照合すると、正当でないものを特定でき、検証された販売者からのみ購入するように設定されている場合は、違反者をブロックします。<!-- can we actually mention NY Times? -->

各広告主 <!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> にデフォルトの [!DNL ads.txt] コントロールを設定し、オプションで [ 各配置の設定 ](/help/dsp/campaign-management/placements/placement-settings.md) をカスタマイズして次の操作を行うことができます。

* ドメインの正規直売人のみから在庫を購入する

* ドメインの認定直販業者と再販業者のみから在庫を購入する

* ドメインの承認された直接販売者および再販売者からの在庫の購入を優先する

* 全販業者から在庫を買う

### プラットフォーム不正監視

DSPは、アドビのプラットフォーム全体で詐欺を管理する強力な内部ツールおよびシステムを構築し、[!DNL Whiteops] や [!DNL Integral Ad Science] などの主要な業界ベンダーと提携しています。

また、Adobeは [!DNL IAB] と [!DNL TAG] と緊密に連携し、[!DNL ads.txt]（前の節を参照）、[!DNL IAB] ボットとスパイダーリスト、[!DNL TAG] データセンターの IP リストなどのツールを活用して、業界標準の堅牢な詐欺ブロックを保護します。

品質に対する多次元的なアプローチを通じて、チームは異常値と無効なトラフィックパターンを監視し、保護されたインベントリで無効なトラフィックが 3 %未満になるようにします。 特定のドメイン上の在庫や、特定のパブリッシャーまたは販売者からの在庫など、疑わしい在庫は、プラットフォーム全体で直ちにブロックされます。

### 在庫のマッピング、階層化、分類

在庫マッピングは、新しい在庫をプラットフォームに追加する前に必要となる詳細なレビューとオンボーディングプロセスです。 このプロセスは、DSP上のすべてのインベントリの安全性と品質を確保するように設計されています。

* **マッピング：** 在庫チームが各ドメインを慎重にレビューし、次のような側面を評価します。

   * ブランドの安全性

   * 広告タイプの検証

   * 汎用コンテンツ、重複ドメイン、および偽の広告配信

* **階層化：** エコシステム全体でのブランドの存在を総合的に調べ、異なる階層にわたるインベントリを分類します。[ 必要な範囲で、これらの層に配置 ](/help/dsp/campaign-management/placements/placement-settings.md) をターゲット設定できます。

   * **[!UICONTROL T1]**  — ブランド名、国際的に認識可能なサイト

   * **[!UICONTROL T2]**  — 最新で最新の、ユーザー生成のコンテンツを含まず、通常はグローバル認識に欠ける優れたサイト

   * **[!UICONTROL T3]**  — ユーザー生成コンテンツとニッチコンテンツ

* **サイトの分類：** コンテンツのターゲティングとブロックを容易におこなうために、各プロパティに、プロパティのコンテンツに基づくAdvertising Cloud定義のサイトカテゴリをタグ付けします。配置目標に基づいて、各配置 ](/help/dsp/campaign-management/placements/placement-settings.md) に対して、これらのサイトカテゴリを [ ターゲットにしたり除外したりできます。

### サイトブロックの包括的なサポート

Advertising Cloud DSPは、グローバルにブロックされたサイトリストと、広告主やアカウント用のカスタムブロックされたサイトリストを作成するオプションの両方を提供します。

#### Advertising Cloud DSPグローバルにブロックされたサイトのリスト

Advertising Cloud DSPは、広告の実行が安全でないと見なされる、グローバルにブロックされたサイトのリストを管理しています。 このリストには、不快なコンテンツ（憎しみや恐怖など）や、ボットに感染したサイト、偽のプリロール、不一致のドメイン、その他の不正な活動を含むサイトが含まれています。

広告主を欺く活動を根付かせるための Brand Safety イニシアチブの一環として、すべてのサイトは、グラフブロックサイトリストの測定を使用してスクリーニングされます。 ブランドの安全性チェックに合格しないすべてのサイトは、グローバルにブロックされたサイトのリストに追加されます。 Advertising Cloud DSPはこのリストを動的に管理するので、最新のブランド安全性分析に基づいて、サイトはいつでもリストのオン/オフを切り替えることができます。

グローバルにブロックされたサイトのリストにサイトを配置のターゲットとして含めると、そのサイトには赤い感嘆符 (!) のフラグが付けられます。 これは、フラグが設定されたサイトで広告が実行されないことを示します。

#### アカウントレベルのサイトリストと広告主レベルのブロックされたサイトリスト

また、アカウントレベルおよび広告主レベルのブロックサイトリスト <!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) --> を管理することもできます。これらは、すべての配置に自動的に使用されます。 下位レベルのブロックサイトのリストは、グローバルにブロックされたサイトのリストに加えて適用されます。

## サードパーティ統合

### コンテキストフィルター

コンテキストフィルタリングを使用すると、広告が提供されるページのコンテキストに基づいて、広告オポチュニティをターゲティングまたはブロックできます。 Adobeは、業界の主要ベンダーとの統合を通じて、コンテキストフィルタリングを提供します。[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]、および [!DNL Peer39]。 現在のフィルターの例としては、[!UICONTROL Adult Content]、[!UICONTROL Natural Disasters]、[!UICONTROL Legal Drinking Age]、[!UICONTROL MANGA]、[!UICONTROL Epidemics]、[!UICONTROL G-rated Sites] があります。

各広告主に対してデフォルトのコンテキストフィルターコントロールを設定し、オプションで [ 各配置の設定をカスタマイズ ](/help/dsp/campaign-management/placements/placement-settings.md) できます。 <!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->この機能を使用すると、追加料金が発生する場合があります。

![Comscore ](/help/dsp/assets/comscore-logo.png) ![logoDoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![logoIntegral Ad Science ](/help/dsp/assets/ias-logo.png) ![logoPeer39 logo](/help/dsp/assets/peer39-logo.png)

### 入札前の不正ブロック

[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science] および [!DNL Peer39] とのサードパーティ統合を活用して、人道的でないトラフィックをキャンペーンからブロックします。 これらの統合により、業界をリードする入札前のブロック機能が提供され、キャンペーンの一般的な無効なトラフィックと高度な無効なトラフィック（GIVT および SIVT）の両方を最小限に抑えることができます。

各広告主に対してデフォルトの入札前詐欺ブロック制御を設定し、必要に応じて <!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> 各配置の設定をカスタマイズ ](/help/dsp/campaign-management/placements/placement-settings.md) できます。 [この機能を使用すると、追加料金が発生する場合があります。

機能の詳細については、お使いのベンダーに直接お問い合わせいただくか、担当のAdobeアカウントマネージャーにお問い合わせください。

![Comscore ](/help/dsp/assets/comscore-logo.png) ![logoDoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![logoIntegral Ad Science ](/help/dsp/assets/ias-logo.png) ![logoPeer39 logo](/help/dsp/assets/peer39-logo.png)

### 入札前の視認性 {#pre-bid-viewability}

業界をリードするパートナー [!DNL DoubleVerify]、[!DNL Oracle Advertising]([!DNL Moat])、[!DNL Integral Ad Science] を活用した入札前の視認性フィルターにより、広告主はキャンペーンがビデオやディスプレイインベントリ全体で目的の視認性の目標を満たすことができます。

各広告主 <!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> のデフォルトの視認性フィルターを設定し、オプションで [ 各配置の設定をカスタマイズできます。](/help/dsp/campaign-management/placements/placement-settings.md) この機能を使用すると、追加料金が発生する場合があります。

![DoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![logoOracle Advertising ](/help/dsp/assets/oracle-advertising-logo.png) ![logoIntegral Ad Science ロゴ](/help/dsp/assets/ias-logo.png)

### トピックのターゲティング

DSPトピックのターゲティングでは、業界をリードするコンテキストパートナー [!DNL Comscore] と [!DNL Oracle Data Cloud]([!DNL Grapeshot]) を活用して、キーワードリストをターゲット化またはブロックできます。

トピックのターゲティングを使用すると、有害なコンテンツのブロックや、より大きな結果を得るためのコンテキストでの支出を含め、広告が常にブランドと一致する環境で提供されることを確認できます。

トピックのターゲティングでは、[!DNL Comscore] または [!DNL Grapeshot]（[!DNL Oracle Data Cloud] を使用）を使用してトピックセグメントを直接作成する必要があります。 これらをパートナープラットフォームで作成したら、[!UICONTROL  Audience Targeting] セクションの各配置 ](/help/dsp/campaign-management/placements/placement-settings.md) に対して、セグメント ID を [ ターゲットにしたり除外したりできます。 この機能には追加料金が適用される場合があります。

開始するには、お使いのベンダーまたはAdobeのアカウントマネージャーにお問い合わせください。

![Comscore ](/help/dsp/assets/comscore-logo.png) ![logoGrapeshot ロゴ](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSPは [!DNL DoubleVerify] と提携し、その [!DNL Authentic Brand Safety] ターゲティングソリューションを提供しています。これにより、すべての購入プラットフォームを対象とし、一貫性を保つために、一元化されたブランド安全要件を作成できます。

必要なターゲットを設定して [!DNL DoubleVerify] ブランドの安全セグメントを構築したら、DSP内でそのセグメントを使用して、Web 環境間で入札前のブロックルールをレプリケートできます。

各広告主 <!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> に [!DNL DoubleVerify] セグメント ID を指定し、必要に応じて [ 各配置の ](/help/dsp/campaign-management/placements/placement-settings.md) を有効または無効にします。 [!UICONTROL Authentic Brand Safety]DSPは、セグメント ID の使用を考慮してアカウントを請求します。

機能の詳細については、[!DNL DoubleVerify] に直接お問い合わせいただくか、担当のAdobeアカウントマネージャーにお問い合わせください。

![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
