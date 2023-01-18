---
title: '''[!UICONTROL Simple Ad Serving] 契約設定`'
description: 使用可能な設定の詳細 [!UICONTROL Simple Ad Serving] 契約
feature: DSP Simple Ad Serving
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] 契約設定

## 新規 [!UICONTROL Simple Ad Serving] 契約

### [!UICONTROL Select Ad Source]

| パラメータ | 説明 |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | この契約のメディアタイプ： *[!UICONTROL Video],* *[!UICONTROL Display],* または *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | この在庫を販売している発行者の名前。 名前の最初の 2 文字以上を入力して、投稿者を検索します。 リストに表示されていない投稿者を追加するには、 [!DNL Adobe] アカウントチーム。 |
| **[!UICONTROL Advertiser]** | この契約にアクセスできる、アカウント内の 1 人の広告主。 また、キャンペーンと、その契約が使用可能なパッケージ（オプション）も選択します。 |
| **[!UICONTROL Media Quality Assessment?]** | （一部のユーザー）サードパーティの検証のために、別のDSPで広告を実行できるようにします。 <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | 唯一のオプションは *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | （新規契約のみ）次のいずれを実行するかを選択します。<ul><li>*[!UICONTROL Create New]:* この契約の広告を作成するには、以下を実行します。</li><li>*[!UICONTROL Select Ads]:* この契約に既存の広告を使用するには、以下を実行します。</li></ul> |
| **[!UICONTROL Ad Type]** | この契約の広告タイプ。 契約の広告を作成する場合は、リクエストに応じて、広告のサイズまたは期間を含めます。 使用可能なオプションは、メディアタイプによって異なります。 |

{style=&quot;table-layout:auto&quot;}

### [!UICONTROL Select Ad(s)]

（既存の広告を使用している場合）契約に含める広告。 含める各広告の横にあるチェックボックスを選択します。

### [!UICONTROL Select & Upload [Media Type]]

（新しい広告のみ）新しい [サードパーティ広告](/help/dsp/campaign-management/ads/ad-create-multiple.md).

### [!UICONTROL Feed Details]

| パラメータ | 説明 |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | 1,000 インプレッションあたりのコスト (CPM)。契約の料金カードに反映されます。 お問い合わせ [!DNL Adobe] この値のアカウントチーム。 <br><br>契約の通貨も指定します。 すべてのユーザーが USD を選択できます。SSP が追加の通貨をサポートしている場合は、DSPアカウントの通貨を選択できます。 |
| **[!UICONTROL Third Party Billed Fees]** | （オプション）請求不可コストとして追跡される静的なサードパーティ料金と、契約の通貨。<br><br>すべてのユーザーが USD を選択できます。SSP が追加の通貨をサポートしている場合は、DSPアカウントの通貨を選択できます。 **注意：** 請求可能な料金は、 [!UICONTROL Net CPM] 指標。 |
| **[!UICONTROL Third Party Fee Description]** | （オプション）サードパーティの料金の説明。 |
| **[!UICONTROL Flight Dates]** | この契約を使用するトラフィックの開始日と終了日。 フライト日は、キャンペーンのフライト日に含める必要があります。 広告タグは、指定されたフライト中にのみ応答を返します。<br><br> 1 年間の期間を持つ個別のシンプルな広告配信キャンペーンを作成し、その中にトラッキングピクセルを作成することをお勧めします。 |
| **[!UICONTROL Impressions]** | （オプション）この契約を使用して実行すると予想されるインプレッション数。 この値は、トラッキング目的でのみ使用され、配信の目標を満たしたときにフラグを設定します。パブリッシャーは、実際の広告配信を制御します。 ベストプラクティスは、DSP内でタグをアクティブにしておくインプレッション数を多く入力し、必要に応じて更新または拡張できるようにすることです。 |
| **[!UICONTROL Deal Name]** | 契約名。 名前を入力するか、 *[!UICONTROL Auto Generate Deal Name]* 契約の詳細に基づいてDSPが名前を生成できるようにします。<br><br>自動生成された名前の例： `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | （読み取り専用）契約に含まれる広告。 広告を編集するには、広告名をクリックします。 契約から広告を削除するには、 **[!UICONTROL X]** 広告名の横に表示されます。 |

{style=&quot;table-layout:auto&quot;}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [について [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [の作成 [!UICONTROL Simple Ad Serving] 契約](simple-deal-create.md)
>* [編集 [!UICONTROL Simple Ad Serving] 契約設定](simple-deal-edit.md)
>* [契約の詳細レポートの表示](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
