---
title: プラットフォーム内レポートについて
description: キャンペーン管理ビューに含まれるレポートデータについて説明します。
feature: Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# プラットフォーム内レポートについて

<!-- rename "About Performance Reports in Campaign Management Views?" -->
キャンペーン管理ビューには、包括的なレポートデータが含まれます。 使用可能なレポートは、パフォーマンスの高いパッケージや配置、および注意が必要なパッケージを特定するのに役立ちます。 また、クイックアクションボタンを使用すると、生産性が向上します。

## すべてのキャンペーンリスト

[!UICONTROL Campaigns]ビューが開き、アカウント内のすべてのキャンペーンのリストが表示されます。 [!UICONTROL Subtotals]行には、表示されているすべての行の各指標の合計値または平均値が表示されます。

![キャンペーンリスト](/help/dsp/assets/campaigns-list.png)

デフォルトでは、各キャンペーン行には、ペーシングと配信指標が含まれます。 ペーシング指標には[!UICONTROL Gross Spend (Lifetime)]が含まれます。これには、キャンペーン内のすべてのパッケージでの実際の目標支出と予想される目標支出の比較が含まれます。これにより、パフォーマンスの低いキャンペーンを一目で特定できます。 オプションで[列ビュー](column-view-change.md)を変更することも、[カスタム列ビュー](column-view-create.md)を作成することもできます。

さらに[データテーブル](campaign-data-views-about.md)をカスタマイズし、[表示データ](campaign-data-filter.md)をフィルタリングすることもできます。

キャンペーンの詳細を表示するには、キャンペーン名をクリックします。

## 単一キャンペーンレポート

キャンペーン内で、キャンペーンエンティティに基づいてデータをフィルタリングできます。[!UICONTROL Packages]、[!UICONTROL Placements]、および[!UICONTROL Ads]。 さらに[表示データ](campaign-data-filter.md)をフィルターして、表示するパッケージ、配置、広告のみを含めることができます。

![キャンペーンエンティティタブ](/help/dsp/assets/campaign-subtabs.png)

各エンティティタブでは、デフォルトで各行にペーシングと配信指標が含まれますが、列ビュー](column-view-change.md)を[変更するか、[カスタム列ビュー](column-view-create.md)を作成してキャンペーンのすべてのサブタブに適用できます。 さらに[データテーブル](campaign-data-views-about.md)をカスタマイズする方法もあります。 各データテーブルには[!UICONTROL Subtotals]行が含まれ、表示されているすべての行の各指標の合計値または平均値が表示されます。

各キャンペーンについて、3つの指標を使用して時系列トレンドグラフをカスタマイズすることもできます。これらの指標は、各エンティティビューで使用できます。 デフォルトでは、[!UICONTROL Net Spend]、[!UICONTROL Impressions]および[!UICONTROL Net CPM]のデータは別々のグラフ（トレリス図）に含まれます。 オプションで指標を変更できます。

![3つの指標に関する個別のトレンドグラフ](/help/dsp/assets/trend-chart-separate.png)

また、オプションで3つの指標をオーバーレイして、スケールやパフォーマンスを向上させる異常値や領域を簡単に検出できます。

![オーバーレイを使用したトレンドグラフ](/help/dsp/assets/trend-chart.png)

[キャンペーン別にトレンドグラフ](campaign-data-visualization-manage.md)をカスタマイズでき、同じ指標がキャンペーンのすべてのトレンドグラフで保持されます。

### 配置インスペクタ

各配置に対して、 （詳細ビュー[!UICONTROL Inspector]）](placement-details-view.md)を[開くことができます。この中には、次の詳細データが含まれています。

* **[!UICONTROL Sites]:** プレースメントにインプレッションがあるすべてのサイト。

   [!UICONTROL Sites]タブには、検索およびフィルター機能、メインページで使用可能な標準およびカスタムの列表示オプション、各行に[!UICONTROL Exclude]ボタンが含まれているので、配置からサイトをすばやく除外できます。

* **[!UICONTROL Ads]:** 配置内のすべての広告。

   [!UICONTROL Ads]タブには、検索およびフィルター機能、メインページで使用可能な標準およびカスタムの列表示オプション、および[!UICONTROL Pause]などの各行のクイックアクションボタンが含まれています（広告をすばやく一時停止できます）。

* **[!UICONTROL Frequency]:** 配置の広告頻度レベルごとのデータ。以下を含みます。
   * 広告頻度レベル（ユーザーが1回広告を見たすべてのインスタンスの「1」など）
   * 指定した頻度レベルでインプレッションを受け取ったデバイス/ブラウザーまたはユーザーの推定ユニーク数（配置に指定した[!UICONTROL Cross Device Level]に応じて異なる）
   * 指定された頻度レベルでのインプレッション数の推定値
   * 指定した頻度レベルの推定平均頻度。 この値は（推定インプレッション数）/（推定ユニーク数）と等しくなります。

![配置検査](/help/dsp/assets/placement-inspector-sites.png)

[!UICONTROL Sites]、[!UICONTROL Ads]または[!UICONTROL Frequency]タブのデータを、XLSM形式のレポートとしてブラウザーのデフォルトのダウンロードフォルダーに書き出すことができます。

### その他のタイプのキャンペーンレベルのレポート

その他のデータ分類については、[従来のキャンペーンレベルのレポートページ](/help/dsp/campaign-management/campaigns/campaign-view-report.md)を[!UICONTROL Campaigns Classic]から参照してください。 レガシーレポートには、[!UICONTROL Geography]、[!UICONTROL Device]、[!UICONTROL Viewability]、[!UICONTROL Audience Performance]の各データに関する節が含まれます。

>[!MORELIKETHIS]
>
>* [プレースメントのサイト、広告、頻度の詳細の表示](placement-details-view.md)
>* [Campaignのデータビューについて](campaign-data-views-about.md)
>* [カスタム列表示の作成](column-view-create.md)
>* [列表示の変更](column-view-change.md)
>* [データビジュアライゼーションの管理](campaign-data-visualization-manage.md)
>* [キャンペーン管理ビューからのデータのエクスポート](campaign-export-data.md)
>* [キャンペーンの詳細レポートの表示](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

