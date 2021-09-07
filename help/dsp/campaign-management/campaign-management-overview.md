---
title: Advertising Cloud DSPのキャンペーン管理の概要
description: キャンペーン管理の階層とコンポーネントについて説明します。
feature: Packages, Placements, Ads, Creatives
exl-id: c94e08d0-0dd5-4cf9-8df2-9eb4c591375c
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Advertising Cloud DSPのキャンペーン管理の概要

Advertising Cloud DSPキャンペーンの階層は次のとおりです。

* キャンペーン
   * パッケージ
      * 配置
         * 広告
            * クリエイティブ

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising Cloud DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[](/help/dsp/campaign-management/campaigns/campaign-about.md) キャンペーンは、フライト設定の包括的なフレームワークです。各キャンペーンには、広告主、開始日と終了日、全体的な予算、クロスデバイスターゲティングオプションとデフォルトの頻度制限、および視認性、不正行為、ブランド安全性、オーディエンス検証のレポートオプションが設定されます。 すべてのキャンペーンレベルの設定は、キャンペーン内の各パッケージおよび配置に自動的に適用されます。

## [!UICONTROL Packages]

各キャンペーンには、1つ以上の[パッケージ](/help/dsp/campaign-management/packages/package-about.md)を含めることができます。各パッケージには、一連の配置が含まれます。

パッケージを使用して、設定された予算、パフォーマンス目標、カスタムペーシング戦略に配信する配置をグループ化します。 DSPは、予算をパッケージ内の最もパフォーマンスの高い配置に移行することで、パッケージを最適化します。 配置形式、在庫のタイプ、データプロバイダー、ペルソナ、またはその他の区別可能な特性別にパッケージを整理できます。

パッケージはオプションですが、推奨されます。

## [!UICONTROL Placements]

[配置](/help/dsp/campaign-management/placements/placement-about.md)は、同じ広告タイプの1つ以上の広告のターゲティングパラメーターを格納します。 1つのキャンペーンまたはパッケージ用にプレースメントを作成し、そのキャンペーンに広告を割り当てることができます。

## [!UICONTROL Ads]

[](/help/dsp/campaign-management/ads/ad-about.md) クリエイティブアセットとトラッキングURLを追加します。クリエイティブアセットをアップロードして、DSPでそれらを使用する広告を無料で提供するか、サードパーティの広告配信タグをアップロードできます。

広告を設定したら、各広告を配置に添付する必要があります。 1つの広告を1つ以上のプレースメントに添付できます。

アクティブなキャンペーン内のアクティブなプレースメントにある、アクティブで承認済みの広告は、すべて、プレースメントターゲットパラメーターに基づいて実行できます。

## [!UICONTROL Creatives]

指定したキャンペーンの広告で使用するオーディオおよびビデオファイルをアップロードできます。
<!-- add link to [About Creative Management](/help/dsp/campaign-management/creatives/creative-about.md) when it's available-->

アップロードしたクリエイティブを使用して広告を直ちに作成することも、後でクリエイティブビューまたは広告ビューから広告を作成することもできます。

>[!MORELIKETHIS]
>
>* [キャンペーン管理について](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [パッケージ管理について](/help/dsp/campaign-management/packages/package-about.md)
>* [プレースメント管理について](/help/dsp/campaign-management/placements/placement-about.md)
>* [広告管理について](/help/dsp/campaign-management/ads/ad-about.md)
>* [Campaign Launchチェックリスト](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [パフォーマンスキャンペーンの設定のベストプラクティス](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [プラットフォーム内レポートについて](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Campaignのデータビューについて](/help/dsp/campaign-management/reports/campaign-data-views-about.md)

