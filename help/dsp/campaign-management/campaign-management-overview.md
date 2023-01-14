---
title: Advertising DSPのCampaign Managementの概要
description: キャンペーン管理の階層とコンポーネントについて説明します。
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: c94e08d0-0dd5-4cf9-8df2-9eb4c591375c
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Advertising DSPのCampaign Managementの概要

DSPキャンペーンの階層は次のとおりです。

* Campaign
   * パッケージ
      * 配置
         * 広告

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[キャンペーン](/help/dsp/campaign-management/campaigns/campaign-about.md) は、フライト設定の包括的なフレームワークです。 各キャンペーンには、広告主、開始日と終了日、予算全体、クロスデバイスターゲティングオプションとデフォルトの頻度キャップ、および視認性、詐欺、ブランドの安全性、オーディエンスの検証に関するレポートオプションが設定されています。 すべてのキャンペーンレベルの設定は、キャンペーン内の各パッケージおよび配置に自動的に適用されます。

## [!UICONTROL Packages]

各キャンペーンには、1 つ以上の [パッケージ](/help/dsp/campaign-management/packages/package-about.md)：それぞれに一連の配置が含まれます。

パッケージを使用して、設定された予算、パフォーマンス目標、カスタムペーシング戦略に対する配信用の配置をグループ化します。 DSPは、予算をパッケージ内の最もパフォーマンスの高い配置に移行することで、パッケージを最適化します。 配置形式、在庫のタイプ、データプロバイダー、ペルソナ、またはその他の区別可能な特性別にパッケージを整理できます。

パッケージはオプションですが、推奨されます。

## [!UICONTROL Placements]

A [配置](/help/dsp/campaign-management/placements/placement-about.md) は、同じ広告タイプの 1 つ以上の広告のターゲティングパラメーターを格納します。 単一のキャンペーンまたはパッケージ用のプレースメントを作成して、そのプレースメントに広告を割り当てることができます。

## [!UICONTROL Ads]

[広告](/help/dsp/campaign-management/ads/ad-about.md) クリエイティブアセットとトラッキング URL を含めます。 サードパーティの広告配信タグは、パートナータグシートまたは一括タグテンプレートを使用して、個別に、または一括でアップロードできます。 また、DSPで提供するネイティブディスプレイ広告を手動で作成することもできます。

広告を設定したら、各広告をプレースメントに添付する必要があります。 1 つの広告を 1 つ以上のプレースメントに添付できます。

アクティブなキャンペーン内のアクティブな配置にある、アクティブで承認済みの広告は、すべて、配置ターゲティングパラメーターに基づいて実行する資格があります。

>[!MORELIKETHIS]
>
>* [Campaign Managementについて](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [パッケージ管理について](/help/dsp/campaign-management/packages/package-about.md)
>* [配置管理について](/help/dsp/campaign-management/placements/placement-about.md)
>* [広告管理について](/help/dsp/campaign-management/ads/ad-about.md)
>* [Campaign Launch チェックリスト](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [パフォーマンスキャンペーンの設定のベストプラクティス](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [プラットフォーム内レポートについて](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Campaign のデータビューについて](/help/dsp/campaign-management/reports/campaign-data-views-about.md)
>* [ビデオ：DSPアカウント構造とユーザーインターフェイス](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/ui.html)

