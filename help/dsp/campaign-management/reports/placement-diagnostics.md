---
title: 配置診断レポートの表示
description: 配置の設定とペーシングに関する問題を診断する方法を説明します。
feature: DSP Placements
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 配置診断レポートの表示

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

以下のツールを使用すると、キャンペーンの運用開始後に、配置の設定とペースの問題を診断するのに役立ちます。

* **[!UICONTROL Change Log]:** 名前、ステータス、最大入札額など、キー配置設定の変更を表示します。 各エントリには、変更を加えた人の日付とユーザー名が含まれます。
* **[!UICONTROL Ad Approvals]:** 広告が在庫プロバイダーによって承認されたか拒否されたかを示します。 オプションで、任意の広告のステータスを変更したり（拒否された広告の一時停止など）、広告設定を開いたりできます。
* **[!UICONTROL Non Bids]:** DSPが配置で入札しなかった理由を示します。

1. 診断レポートを開きます。
   1. 配置設定を開きます。
      1. メインメニューで、 **[!UICONTROL Campaigns]**.
      1. キャンペーン名をクリックし、 **[!UICONTROL Placements]**.
      1. 配置名の横にある  **[!UICONTROL ...]>[!UICONTROL Edit]**.
   1. 右上で、 ![配置診断](/help/dsp/assets/placement-diagnostics.png) または **[!UICONTROL Diagnostic]**.
1. 次のいずれかの操作を行います。
   * 変更ログを表示するには、次の手順に従います。
      1. クリック **[!UICONTROL Change Log]**.
      1. （オプション）レポート結果をフィルターします。
         * 日付メニューで、レポート期間をデフォルトの「過去 14 日間」から別の期間 (*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* または *[!UICONTROL Last 1 year]*) をクリックします。
         * 左側のメニューで、特定のユーザー名でレポートをフィルタリングします。
         * 右側のメニューで、特定の配置設定でレポートをフィルタリングします。
   * 広告承認のステータスを表示するには：
      1. 右上で、 **[!UICONTROL Ad Approvals]**.
      1. （オプション）広告を一時停止またはアクティブ化するには、ステータススイッチ (![ステータススイッチ](/help/dsp/assets/status-switch.png)) をクリックします )。
      1. （オプション）広告の設定を開くには、 **[!UICONTROL View Ad]** 広告の横に表示されます。
   * DSPがプレースメントで入札しなかった理由を確認するには：
      1. 右上で、 **[!UICONTROL Non Bids]**.
      1. （オプション）日付範囲を変更するには、日付フィールドをクリックして、別の日付または日付範囲を選択します。

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [プラットフォーム内レポートについて](campaign-reports-about.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

