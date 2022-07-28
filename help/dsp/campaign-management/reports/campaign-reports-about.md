---
title: プラットフォーム内レポートについて
description: キャンペーン管理ビューに含まれるレポートデータについて説明します。
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: 82c906c87fd3aad0d7a04d0b0e58e54c5485499a
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# プラットフォーム内レポートについて

<!-- rename "About Performance Reports in Campaign Management Views?" -->
キャンペーン管理ビューには、包括的なレポートデータが含まれます。 利用可能なレポートは、パフォーマンスの高いパッケージや配置、および注意を必要とするパッケージや配置を特定するのに役立ちます。 また、クイックアクションボタンを使用すると、生産性が向上します。

## すべてのキャンペーン表示

この [!UICONTROL Campaigns] [ 表示 ] をクリックすると、一連のパフォーマンスデータグラフと、アカウント内のすべてのキャンペーンの一覧が開きます。

### グラフ表示 {#chart-view}

以下が可能です。 [時系列トレンドグラフのカスタマイズ](campaign-data-visualization-manage.md) を 3 つの指標で示します。 デフォルトでは、 [!UICONTROL Net Spend], [!UICONTROL Impressions]、および [!UICONTROL Net CPM] は別々のグラフ（トレリス図）に含まれます。 オプションで指標を変更できます。 時系列トレンドグラフの時間別データを有効にするには、日付の選択を 1 日 ([!UICONTROL Today], [!UICONTROL Yesterday]、または特定の日 )。

![3 つの指標に関する個別のトレンドグラフ](/help/dsp/assets/trend-chart-separate.png)

また、オプションで 3 つの指標をオーバーレイして、異常値や、スケールやパフォーマンスを向上させる領域を容易に検出できます。

![オーバーレイを含むトレンドグラフ](/help/dsp/assets/trend-chart.png)

### テーブル表示

![キャンペーンリスト](/help/dsp/assets/campaigns-list.png)

デフォルトでは、各キャンペーン行には、ペーシングと配信指標が含まれます。 ペーシング指標には以下が含まれます [!UICONTROL Gross Spend (Lifetime)]：キャンペーン内のすべてのパッケージでの実際の目標上の支出に対する予想される目標上の支出のゲージを含むので、効果の低いキャンペーンを一目で特定できます。 オプションで、 [列表示を変更する](column-view-change.md) または [カスタム列表示の作成](column-view-create.md).

さらに [データテーブルのカスタマイズ](campaign-data-views-about.md) 追加の方法と [表示されるデータのフィルター](campaign-data-filter.md).

キャンペーンの詳細を表示するには、キャンペーン名をクリックします。

## 単一キャンペーンレポート {#single-campaign-reporting}

キャンペーン内では、キャンペーンエンティティに基づいてデータをフィルタリングできます。 [!UICONTROL Packages], [!UICONTROL Placements]、および [!UICONTROL Ads]. さらに [表示されるデータのフィルター](campaign-data-filter.md) を使用して、表示するパッケージ、プレースメントまたは広告のみを含めます。

![キャンペーンエンティティタブ](/help/dsp/assets/campaign-subtabs.png)

### グラフ表示

キャンペーンごとに、以下の操作を実行できます。 [時系列トレンドグラフのカスタマイズ](campaign-data-visualization-manage.md) と 3 つの指標を組み合わせ、各エンティティ表示で使用できます。 キャンペーンのすべてのトレンドグラフで、同じ指標が保持されます。

詳しくは、 [クロスキャンペーン指標に関する「グラフ表示」の節](#chart-view) を参照してください。

### テーブル表示

各エンティティタブでは、デフォルトで、各行にペーシングと配信指標が含まれますが、 [列表示を変更する](column-view-change.md) または [カスタム列表示の作成](column-view-create.md) をクリックして、キャンペーンのすべてのサブタブに適用します。 さらに [データテーブルのカスタマイズ](campaign-data-views-about.md) その他の方法では 各データテーブルには、 [!UICONTROL Subtotals] 行：表示されているすべての行の各指標の合計または平均値を表示します。

### 配置 [!UICONTROL Inspector] {#placement-inspector}

各配置に対して、次の操作を実行できます。 [（詳細ビューを開く） [!UICONTROL Inspector])](placement-details-view.md)：以下の詳細データを含みます。

* **[!UICONTROL Sites]:** 配置にインプレッションがあるすべてのサイト。

   この [!UICONTROL Sites] 「 」タブには、検索およびフィルター機能、メインページで使用できる標準およびカスタムの列表示オプション、 [!UICONTROL Exclude] ボタンを使用して、配置からサイトをすばやく除外できます。

* **[!UICONTROL Ads]:** 配置内のすべての広告。

   この [!UICONTROL Ads] タブには、検索およびフィルタ機能、メインページで使用可能な標準およびカスタムの列表示オプション、各行のクイックアクションボタン ( [!UICONTROL Pause] （広告をすばやく一時停止できます）。

* **[!UICONTROL Frequency]:** 配置の広告頻度レベルごとのデータ。以下を含みます。
   * 広告頻度レベル（ユーザーが 1 回広告を表示したすべてのインスタンスの「1」など）
   * デバイス/ブラウザーまたはユーザーの推定ユニーク数（指定した数に応じて異なる） [!UICONTROL Cross Device Level] （配置に関して）指定された頻度レベルでインプレッションを受け取った人
   * 指定された頻度レベルでの推定インプレッション数
   * 指定した頻度レベルの推定平均頻度。 この値は、 (Estimated Impressions)/(Estimated Uniques) と等しくなります。

* **[!UICONTROL Inventory]:** プレースメントのターゲットとなるすべての契約に関する情報。

   この [!UICONTROL Inventory] 「 」タブには、パフォーマンス統計を表示することで、すばやくトラブルシューティングできます。 [!UICONTROL Auctions], [!UICONTROL Bids]、および [!UICONTROL Win Rate]. このタブには、検索およびフィルタ機能、メインページで使用可能な標準およびカスタムの列表示オプション、および各行のクイックアクションボタン ( [!UICONTROL Edit], [!UICONTROL View Report]、および [[!UICONTROL Auction Insights] その他のトラブルシューティング](/help/dsp/inventory/private-deal-auction-insights.md).

#### 在庫のトラブルシューティング

| 問題 | 考えられる原因 | 実行すべきアクション |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 発行者が入札リクエストの送信を開始していません。 | 契約を有効化するには、発行者に問い合わせてください。 |
|  | 取引が正しく設定されていない（不正な外部取引 ID の入力など）。 | 契約の詳細を確認し、契約を編集します。 |
| [!UICONTROL Auctions but no Bids] | 配置のターゲティングが、契約の受信入札リクエストと一致しません。 <br><br> 例えば、プレースメントは、契約に対する資格のない地域をターゲットとしている場合があります。 | ターゲティングの不一致を避けるために、必要に応じて配置ターゲットを編集します。 |
|  | 配置には、契約に必要なメディアタイプを持つアクティブな広告がありません。 | 正しいメディアタイプの広告を作成し、配置に添付します。 |
|  | 配置に十分な予算がありません。 | 受信リクエストでの入札を許可するように配置予算を増やします。 |
|  | 配置のフライト日は、契約のインプレッションの配信日と重複しません。 | 必要に応じて、プレースメントのフライト日を編集します。 |
| [!UICONTROL Low Win Rate] | プレースメントの最大入札額（下限または固定）は、契約で必要とされる最小入札額を下回っています。 | 配置の [!UICONTROL Max Bid] 必要に応じて。 |
|  | 配置では、入札を制限する入札前フィルターを使用します。 | 入札前フィルターのしきい値を下げて、より多くの入札を許可します。 |
|  | プレースメントのオーディエンスのターゲティングが制限されすぎます。 | 指定したオーディエンスターゲットに十分なアクティブユーザーがあるかどうかを確認し、可能であればオーディエンスを拡張します。 |

![配置インスペクター](/help/dsp/assets/placement-inspector.png)

データを [!UICONTROL Sites], [!UICONTROL Ads]または [!UICONTROL Frequency] をタブに設定し、ブラウザーのデフォルトのダウンロードフォルダーを XLSM 形式のレポートとして表示します。

### その他のキャンペーンレベルのレポートタイプ

その他のデータ分類の場合は、 [キャンペーンレベルのレポートページ](/help/dsp/campaign-management/campaigns/campaign-view-report.md). この <!--legacy --> レポートには次のセクションが含まれます： [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]、および [!UICONTROL Audience Performance] データ。

>[!MORELIKETHIS]
>
>* [プレースメントのサイト、広告、頻度の詳細を表示](placement-details-view.md)
>* [Campaign のデータビューについて](campaign-data-views-about.md)
>* [カスタム列表示の作成](column-view-create.md)
>* [列表示の変更](column-view-change.md)
>* [データビジュアライゼーションの管理](campaign-data-visualization-manage.md)
>* [Campaign Managementビューからのデータの書き出し](campaign-export-data.md)
>* [キャンペーンの詳細レポートの表示](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

