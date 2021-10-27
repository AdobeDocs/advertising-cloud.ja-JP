---
title: プラットフォーム内レポートについて
description: キャンペーン管理ビューに含まれるレポートデータについて説明します。
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: b2393d5e66ba5d3d2dc9816825c05eda076eaad1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# プラットフォーム内レポートについて

<!-- rename "About Performance Reports in Campaign Management Views?" -->
キャンペーン管理ビューには、包括的なレポートデータが含まれます。 使用可能なレポートは、パフォーマンスの高いパッケージや配置、および注意が必要なパッケージを特定するのに役立ちます。 クイックアクションボタンを使用すると、生産性が向上します。

## すべてのキャンペーンリスト

10. [!UICONTROL Campaigns] 「表示」を選択すると、アカウント内のすべてのキャンペーンのリストが表示されます。 10. [!UICONTROL Subtotals] 行には、表示されているすべての行の各指標の合計値または平均値が表示されます。

![キャンペーンリスト](/help/dsp/assets/campaigns-list.png)

デフォルトでは、各キャンペーン行には、ペーシングと配信指標が含まれます。 ペーシング指標は、 [!UICONTROL Gross Spend (Lifetime)]：実際の目標時間と、キャンペーン内のすべてのパッケージで予想される目標時間の支出のゲージを含むので、パフォーマンスの低いキャンペーンを一目で特定できます。 オプションで、 [列表示の変更](column-view-change.md) または [カスタム列表示の作成](column-view-create.md).

さらに詳しく [データテーブルのカスタマイズ](campaign-data-views-about.md) 追加の方法と [表示データのフィルタリング](campaign-data-filter.md).

キャンペーンの詳細を表示するには、キャンペーン名をクリックします。

## 単一キャンペーンレポート {#single-campaign-reporting}

キャンペーン内では、キャンペーンエンティティに基づいてデータをフィルタリングできます。 [!UICONTROL Packages], [!UICONTROL Placements]および [!UICONTROL Ads]. さらに詳しく [表示データのフィルタリング](campaign-data-filter.md) を使用して、表示するパッケージ、配置、広告のみを含めます。

![キャンペーンエンティティタブ](/help/dsp/assets/campaign-subtabs.png)

各エンティティタブでは、各行にデフォルトでペーシングと配信指標が含まれますが、 [列表示の変更](column-view-change.md) または [カスタム列表示の作成](column-view-create.md) をクリックして、キャンペーンのすべてのサブタブに適用します。 さらに詳しく [データテーブルのカスタマイズ](campaign-data-views-about.md) その他の方法で 各データテーブルには、 [!UICONTROL Subtotals] 行：表示されているすべての行の各指標の合計または平均値を示します。

各キャンペーンで、時系列トレンドグラフを 3 つの指標でカスタマイズし、各エンティティビューで利用できます。 デフォルトでは、 [!UICONTROL Net Spend], [!UICONTROL Impressions]および [!UICONTROL Net CPM] は別々のグラフ（トレリス図）に含まれます。 オプションで指標を変更できます。

![3 つの指標に関する個別のトレンドグラフ](/help/dsp/assets/trend-chart-separate.png)

また、オプションで 3 つの指標をオーバーレイして、異常値や、スケールやパフォーマンスを向上させる領域を簡単に検出することもできます。

![オーバーレイを使用したトレンドグラフ](/help/dsp/assets/trend-chart.png)

次の操作が可能です。 [トレンドグラフのカスタマイズ](campaign-data-visualization-manage.md) キャンペーンごとに保存され、同じ指標がキャンペーンのすべてのトレンドグラフで保持されます。

### 配置検査

各配置に対して、次の操作を実行できます。 [( 詳細ビューを開く [!UICONTROL Inspector])](placement-details-view.md)：以下の詳細データを含みます。

* **[!UICONTROL Sites]:** 配置にインプレッションがあったすべてのサイト。

   10. [!UICONTROL Sites] タブには、検索およびフィルター機能、メインページで使用できる標準およびカスタムの列表示オプション、 [!UICONTROL Exclude] 」ボタンをクリックして、配置からサイトをすばやく除外できます。

* **[!UICONTROL Ads]:** 配置内のすべての広告。

   10. [!UICONTROL Ads] タブには、検索およびフィルタ機能、メインページで使用できる標準およびカスタムの列表示オプション、および各行のクイックアクションボタン ( [!UICONTROL Pause] （広告をすばやく一時停止できます）。

* **[!UICONTROL Frequency]:** 配置の広告頻度レベルごとのデータ。次を含みます。
   * 広告頻度レベル（ユーザーが 1 回広告を閲覧したすべてのインスタンスの「1」など）
   * デバイス/ブラウザーまたはユーザーの推定ユニーク数 ( 指定した [!UICONTROL Cross Device Level] （配置に関して）指定された頻度レベルでインプレッションを受け取った人
   * 指定した頻度レベルでのインプレッション数の推定
   * 指定した頻度レベルの推定平均頻度。 この値は、 (Estimated Impressions)/(Estimated Uniques) と等しくなります。

![配置検査](/help/dsp/assets/placement-inspector-sites.png)

データを [!UICONTROL Sites], [!UICONTROL Ads]または [!UICONTROL Frequency] 」タブをクリックし、XLSM 形式のレポートとしてブラウザーのデフォルトのダウンロードフォルダーに移動します。

### その他のタイプのキャンペーンレベルのレポート

その他のデータブレークアウトの場合は、 [従来のキャンペーンレベルのレポートページ](/help/dsp/campaign-management/campaigns/campaign-view-report.md) から [!UICONTROL Campaigns Classic]. レガシーレポートには、 [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]および [!UICONTROL Audience Performance] データ。

>[!MORELIKETHIS]
>
>* [サイト、広告、頻度の詳細を表示](placement-details-view.md)
>* [Campaign のデータビューについて](campaign-data-views-about.md)
>* [カスタム列表示の作成](column-view-create.md)
>* [列表示の変更](column-view-change.md)
>* [データビジュアライゼーションの管理](campaign-data-visualization-manage.md)
>* [キャンペーン管理ビューからのデータのエクスポート](campaign-export-data.md)
>* [キャンペーンの詳細レポートの表示](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

