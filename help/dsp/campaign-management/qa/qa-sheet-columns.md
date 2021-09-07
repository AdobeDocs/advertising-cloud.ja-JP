---
title: ダウンロード/アップロードされたスプレッドシートの列
description: ダウンロードおよびアップロードしたExcel QAスプレッドシートの列を参照します。
feature: Placements
exl-id: 8a8dceed-f77d-4b6b-a842-f57528125c92
source-git-commit: fcd55f882f56c9eacd82d554d30364400b99555c
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# ダウンロード/アップロードされたスプレッドシートの列

<!-- rename -- not specific enough - I think you can download Excel files of other things too -->

<!-- see notes within the table about descriptions that need to be edited -->

>[!TIP]
>
> ダウンロードしたスプレッドシートでは、編集可能なすべての列が青色でハイライト表示されます。

| セクション | 列 | 説明 | 編集可能？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | 配置の数値ID。 | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | 配置の名前。 | はい |
| [!UICONTROL Basic] | [!UICONTROL Labels] | レポート用に適用されたラベル。 | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | 編集モードで配置を開くためのリンク。 | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | 配置ステータス：*[!UICONTROL active]*&#x200B;または&#x200B;*[!UICONTROL inactive]*。 | はい |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | 配置タイプ。 | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | 親パッケージの名前（該当する場合）。 | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | 配置の開始日。 | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | 配置の終了日。 | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | 時間帯区分が&#x200B;*[!UICONTROL ON]*&#x200B;か&#x200B;*[!UICONTROL OFF]*&#x200B;か。<br><b>注意：</b> 実際の時間帯区分スケジュールを確認するには、の配置設定を開きま [!DNL DSP]す。 | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | 配置予算（ある場合）。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | 予算間隔：&lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*&#x200B;または&#x200B;*[!UICONTROL All Time]*。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | パッケージの目的。 | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | 目標のターゲット値。 | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | 配置が&#x200B;*[!UICONTROL Budget]*&#x200B;または&#x200B;*[!UICONTROL Impressions]*&#x200B;の方向に移動しているかどうか。 | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | プレースメントの最大入札額。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Pacing Fill Strategy] | 配置のペーシングフィル戦略：*[!UICONTROL evenly]*、*[!UICONTROL frontload]*、または&#x200B;*[!UICONTROL aggressive frontload]*。 | はい |
| [!UICONTROL Goals] | [!UICONTROL  Pre-Bid Filters] | 適用する入札前のフィルター条件。 | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | 入札ルール（非推奨）が&#x200B;*[!UICONTROL ON]*&#x200B;か&#x200B;*[!UICONTROL OFF]*&#x200B;か。 | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | 指定した[!UICONTROL Frequency Cap Interval]の間の配置の主な頻度キャップ。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | プライマリ周波数キャップの間隔：*[!UICONTROL Day]*、*[!UICONTROL Week]*、または&#x200B;*[!UICONTROL Month]*。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | 指定した[!UICONTROL Secondary Frequency Cap Interval]の間の配置のセカンダリ周波数キャップ | はい |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | セカンダリ周波数キャップの間隔のタイプ：*[!UICONTROL Week]*、*[!UICONTROL Day]*、*[!UICONTROL Hour]*、または&#x200B;*[!UICONTROL Minute]*。 週、日、時間、または分の数は、[!UICONTROL Secondary Frequency Cap Interval Value]で示されます。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | [!UICONTROL Secondary Frequency Cap]を適用する週、日、時間または分の数。 たとえば、セカンダリキャップが6時間に3インプレッションの場合、この値は<b>6&lt;/>になります。 | はい |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | ターゲットとする地理的な場所の数（*[!UICONTROL All]*&#x200B;または&#x200B;*[!UICONTROL None]*）。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | ターゲットとなる地理的な場所をセミコロン(*[!UICONTROL All Locations]*)で区切って指定します。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | 地理的な場所を除外した数(*[!UICONTROL None]*)。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | 除外された地理的な場所(セミコロン(*[!UICONTROL None]*)で区切られます。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | 対象となる公的な在庫取引の数（指定されている場合）:*[!UICONTROL All]*&#x200B;または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | 公的な在庫取引が指定されている場合は除外された数、または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | ターゲットとするプライベート在庫取引の数（指定されている場合）:*[!UICONTROL All]*&#x200B;または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | 除外されたプライベート在庫取引が指定されている場合は、その数、または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | ターゲット[!UICONTROL On-Demand Inventory]取引の数（指定されている場合）、*[!UICONTROL All]*、*[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | オンデマンド在庫取引が指定されている場合は除外された数、または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | ターゲットとするトラフィックのタイプ：*[!UICONTROL Website]*&#x200B;や&#x200B;*[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | アウトストリームトラフィックを除外する「在庫ターゲティング」オプションが&lt;i[!UICONTROL >ON]*か&#x200B;*[!UICONTROL OFF]*&#x200B;か。<br>アウトストリーム広告は、通常、ビデオプレーヤーで通常のビデオ広告としてではなく、ポップアップとして、または（ネイティブエクスペリエンスで）コンテンツに詰め込まれてコンテンツ上に表示されます。 | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | ターゲットとするサイトの品質：*[!UICONTROL Tier 1]*、*[!UICONTROL Tier 2]*、*[!UICONTROL Tier 3]*、または&#x200B;*[!UICONTROL All Sites]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | ターゲットサイトカテゴリが指定されている場合は、その数、または&#x200B;*[!UICONTROL All]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | サイトカテゴリが指定されている場合は除外される数、または&#x200B;*[!UICONTROL All]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | 除外されたサイト（指定されている場合）または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | ターゲットサイトの言語。 | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | 監査されていないサイトでの広告配信を許可するかどうか：*[!UICONTROL ON]*&#x200B;または&#x200B;*[!UICONTROL OFF]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | ターゲットサイトが指定されている場合は、その数、または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | ターゲットオーディエンスが指定されている場合は&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | 除外されたオーディエンス（指定されている場合）または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | 人口統計セグメントを配置（およびキャンペーン内の他の配置）に対して有効化するかどうかを指定します。[!DNL Comscore]*[!UICONTROL ON]*&#x200B;または&#x200B;*[!UICONTROL OFF]*。 この機能は、[!DNL Audience Verification]機能が[!DNL Nielson]や[!DNL Comscore]に対して有効になっているキャンペーンに対してのみ有効にできます。  追加料金が必要です。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | デバイスをまたいで広告ターゲティングを拡張するかどうか：*[!UICONTROL ON]*&#x200B;または&#x200B;*[!UICONTROL OFF]*.<!-- Whether or not the Cross Device Targeting setting is enabled for the placement : *ON* or *OFF*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings.--> | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting]  — 含まれる# | 対象のトピックコードが指定されている場合は、その数、または&#x200B;*[!UICONTROL All]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | 除外されたトピック・コードが指定されている場合は、*[!UICONTROL None]*&#x200B;の数。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | ターゲット・デバイス・ターゲットの数（指定されている場合）、または&#x200B;*[!UICONTROL All]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | 除外されたデバイスターゲットの数（指定されている場合）、または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | ターゲットISPプロバイダー（指定されている場合）の数、または*[!UICONTROL All]/i>。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | ISPプロバイダが指定されている場合は除外される数、または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | 適用されるブランドの安全フィルターの数（指定されている場合）または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | 指定されている場合は、適用される入札前の不正ブロックフィルターの数、または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | 適用された入札前の視認性フィルターの数（指定されている場合）または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | サイト安全ブロックが有効かどうか：*[!UICONTROL ON]*&#x200B;または&#x200B;*[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | 配置に添付されているサードパーティのイベント追跡ピクセルの数、または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | 配置に関連付けられているコンバージョントラッキングピクセルの数、または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | 1,000件のインプレッションあたりの請求不可コストとして追跡される静的なサードパーティの料金（該当する場合）。 | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | 配置に関連付けられている広告の数（添付されている場合）または&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | 配置に関連付けられている広告の名前（添付されている場合）または&#x200B;*[!UICONTROL None]*。 | — |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [スプレッドシートを使用したキャンペーンの配置設定の修正について](qa-about.md)
>* [キャンペーンのダウンロード配置設定](qa-sheet-download.md)
>* [キャンペーンのプレースメント設定のアップロード](qa-sheet-upload.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

