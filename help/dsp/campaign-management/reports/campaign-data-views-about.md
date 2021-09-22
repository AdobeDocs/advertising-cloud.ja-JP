---
title: Campaignのデータビューについて
description: キャンペーン、パッケージ、プレースメントおよび広告のデータ表示をカスタマイズする方法について説明します。
feature: DSP Campaign Data Views
exl-id: acc312b9-2de4-4e2f-9b59-b91f23d82357
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# Campaignのデータビューについて

すべてのキャンペーン管理ビュー（[!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements]および[!UICONTROL Ads]）で、データテーブル内に表示されるデータをカスタマイズできます。 データは、次の方法でカスタマイズできます。

* データ列とその順序を指定するには、表示セレクターからビューを選択するか、既存のビューの列を編集して変更を一時的に適用するか、カスタム列表示を作成します。

   各キャンペーン管理レベル([!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements]、[!UICONTROL Ads])には、そのエンティティの関連指標を含む組み込みの[!UICONTROL Pacing]ビューと[!UICONTROL Performance]ビューが含まれます。 デフォルトでは、[!UICONTROL Pacing]ビューが表示されるので、パフォーマンスの低いキャンペーンやキャンペーンのコンポーネントを一目で確認できます。 オプションで[列ビュー](column-view-change.md)を変更して、（[!UICONTROL Performance]ビューを使用して）パフォーマンスデータや、保存されている列セットを表示できます。 オプションで[[!UICONTROL Pacing]ビューまたは[!UICONTROL Performance]ビューの列](column-view-edit.md)を編集して、変更を一時的に適用できます。

   また、任意の列を含む[カスタムの列セット](column-view-create.md)を、任意の順序で保存することもできます。

   ![列表示セレクター](/help/dsp/assets/column-view-selector.png)

   列表示エディターでは、すべての指標がカテゴリ別にアルファベット順に表示されます。[!UICONTROL Settings]、[!UICONTROL Spend]、[!UICONTROL Pacing]、[!UICONTROL Reporting](DSPが追跡する標準指標)、[!UICONTROL Viewability]、および[!UICONTROL Conversions]を示します。 指標に「([!UICONTROL Lifetime])」が付加され、ページで選択されている日付範囲に関係なく、キャンペーンの開始時の戻り値が返されます。

   ![列表示エディター](/help/dsp/assets/column-view-editor.png)

   DSPでは、最新の表示がデフォルトの表示として保存されるので、ページに戻るたびに、常に自分に関連する指標が表示されます。

* [filters](campaign-data-filter.md)を適用して、現在のタブに表示されるデータを変更します。 使用可能なフィルターは、エンティティのタイプによって異なりますが、エンティティ名、ステータス、追加のプロパティ列を含む場合があります。

* すべての標準ビューとカスタムビューで使用する日付範囲を変更します。

* [任意の列の値でデータを並べ替えます](campaign-data-sort.md)。

* ページの右下に25行、50行、100行を表示するかどうかを制御します。

>[!MORELIKETHIS]
>
>* [プラットフォーム内レポートについて](campaign-reports-about.md)
>* [列表示の変更](column-view-change.md)
>* [カスタム列表示の作成](column-view-create.md)
>* [カスタム列表示の編集](column-view-edit.md)
>* [データビジュアライゼーションの管理](campaign-data-visualization-manage.md)
>* [プレースメントのサイト、広告、頻度の詳細の表示](placement-details-view.md)
>* [配置診断レポートの表示](placement-diagnostics.md)
>* [キャンペーン管理ビューからのデータのエクスポート](campaign-export-data.md)

