---
title: ダウンロード/アップロード済みスプレッドシートの列
description: ダウンロードおよびアップロードした Excel QA スプレッドシートの列を参照します。
feature: DSP Placements
exl-id: 8a8dceed-f77d-4b6b-a842-f57528125c92
source-git-commit: 39f491a39bdc9d8dd820eb4c69594dda71d8b3c2
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# ダウンロード/アップロード済みスプレッドシートの列

<!-- rename -- not specific enough - I think you can download Excel files of other things too -->

<!-- see notes within the table about descriptions that need to be edited -->

>[!TIP]
>
> ダウンロードしたスプレッドシートでは、編集可能なすべての列が青色でハイライト表示されます。

| セクション | 列 | 説明 | 編集可能？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | プレースメントの数値 ID。 | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | 配置の名前。 | はい |
| [!UICONTROL Basic] | [!UICONTROL Labels] | レポート用に適用されたラベル。 | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | プレースメントを編集モードで開くためのリンク。 | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | 配置ステータス： *[!UICONTROL active]* または *[!UICONTROL inactive]*. | はい |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | 配置タイプ。 | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | 親パッケージの名前（該当する場合）。 | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | 配置の開始日。 | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | 配置の終了日。 | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | 時間帯区分が *[!UICONTROL ON]* または *[!UICONTROL OFF]*.<br><b>注意：</b> 実際の時間帯区分スケジュールを確認するには、 [!DNL DSP]. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | 配置予算（存在する場合）。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | 予算間隔： &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*&#x200B;または *[!UICONTROL All Time]*.[!UICONTROL >Daily] | はい |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | パッケージの目的。 | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | 目標のターゲット値。 | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | 配置が *[!UICONTROL Budget]* または *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | プレースメントの最大入札額。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Pacing Fill Strategy] | 配置のペーシングフィル戦略： *[!UICONTROL evenly]*, *[!UICONTROL frontload]*&#x200B;または *[!UICONTROL aggressive frontload]*. | はい |
| [!UICONTROL Goals] | [!UICONTROL  Pre-Bid Filters] | 適用する入札前のフィルター条件。 | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | 入札ルール（非推奨）が *[!UICONTROL ON]* または *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | 指定した配置の主な頻度キャップ [!UICONTROL Frequency Cap Interval]. | はい |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | プライマリ周波数キャップの間隔： *[!UICONTROL Day]*, *[!UICONTROL Week]*&#x200B;または *[!UICONTROL Month]*. | はい |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | 指定した配置のセカンダリ頻度キャップ [!UICONTROL Secondary Frequency Cap Interval] | はい |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | セカンダリ周波数キャップの間隔のタイプ： *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*&#x200B;または *[!UICONTROL Minute]*. 該当する週、日、時間または分の数は、 [!UICONTROL Secondary Frequency Cap Interval Value]. | はい |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | が属する週、日、時間または分の数 [!UICONTROL Secondary Frequency Cap] 適用されます。 たとえば、セカンダリキャップが 6 時間に 3 インプレッション数である場合、この値は次のようになります。 <b>6&lt;/>. | はい |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | ターゲットとする地理的な場所の数 *[!UICONTROL All]*&#x200B;または *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | ターゲットの地理的な場所（セミコロンで区切る）。 *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | 地理的な場所の数、または *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | 除外された地理的な場所（セミコロンで区切られる）。 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | 公共の在庫の掘り出し物が指定されている場合は、その数。 *[!UICONTROL All]*&#x200B;または *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | 公共の在庫取引が指定されている場合は除外された数、または *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | ターゲットとするプライベート在庫取引の数（指定されている場合）。 *[!UICONTROL All]*&#x200B;または *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | 非公開在庫取引が指定されている場合は、除外された数。 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | ターゲットの数 [!UICONTROL On-Demand Inventory] 契約が指定されている場合は、 *[!UICONTROL All]*&#x200B;または *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | オンデマンドの在庫取引が指定されている場合は除外された数、または *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | ターゲットとするトラフィックのタイプ： *[!UICONTROL Website]* および/または *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | アウトストリームトラフィックを除外する「在庫ターゲティング」オプションが &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*または *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>アウトストリーム広告は、通常、ビデオプレーヤーで通常のビデオ広告とは異なり、コンテンツ上にポップアップとして表示されたり、（ネイティブエクスペリエンスで）コンテンツに埋め込まれたりします。 | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | ターゲットにするサイトの品質： *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*&#x200B;または *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | ターゲットサイトカテゴリが指定されている場合は、その数、または *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | 除外されたサイトカテゴリが指定されている場合の数、または *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | 除外されるサイト（指定されている場合）、または *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | ターゲットのサイト言語。 | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | 非監査サイトでの広告配信を許可するかどうか： *[!UICONTROL ON]* または *[!UICONTROL OFF]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | ターゲットサイトが指定されている場合はその数、 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | ターゲットオーディエンス（指定されている場合）、または *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | 除外されたオーディエンス（指定されている場合）、または *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | どうか [!DNL Comscore] 人口統計セグメントは、配置（およびキャンペーン内の他の配置）に対して有効になります。 *[!UICONTROL ON]* または *[!UICONTROL OFF]*. この機能は、 [!DNL Audience Verification] 機能は次の場合に有効です： [!DNL Nielsen] および/または [!DNL Comscore].  追加料金が必要です。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | デバイスをまたいで広告ターゲティングを拡張するかどうか： *[!UICONTROL ON]* または *[!UICONTROL OFF]*.<!-- Whether or not the Cross Device Targeting setting is enabled for the placement : *ON* or *OFF*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings.--> | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting]  — 含まれる# | ターゲットとするトピックコードが指定されている場合は、その数、または *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | 除外されるトピックコードの数（指定されている場合）、または *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | ターゲットデバイスターゲットの数（指定されている場合）、または *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | 除外されるデバイスターゲットの数（指定されている場合）、または *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | ターゲットとする ISP プロバイダーの数（指定されている場合）、または*[!UICONTROL All]/i> です。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | ISP プロバイダーが指定されている場合は、その数、または *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | 適用されるブランドの安全フィルターの数（指定されている場合）、または *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | 適用された入札前の不正ブロックフィルターの数（指定されている場合）、または *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | 適用された入札前の視認性フィルターの数（指定されている場合）、または *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | サイトの安全ブロックが有効かどうか： *[!UICONTROL ON]* または *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | 配置に関連付けられているサードパーティのイベント追跡ピクセルの数、または *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | 配置に関連付けられているコンバージョントラッキングピクセルの数、または *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | 該当する場合、1,000 インプレッションあたりの請求不可コストとして追跡される、静的なサードパーティの料金。 | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | 配置に添付されている広告の数（添付されている場合）、または *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | 配置に関連付けられている広告の名前（関連付けられている場合）、または *[!UICONTROL None]*. | — |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [スプレッドシートを使用したキャンペーンの配置設定の修正について](qa-about.md)
>* [キャンペーンの配置設定のダウンロード](qa-sheet-download.md)
>* [キャンペーンの配置設定のアップロード](qa-sheet-upload.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

