---
title: 配置診断レポートの表示
description: 配置の設定とペーシングに関する問題を診断する方法を説明します。
feature: Placements
exl-id: d64406b6-83b5-4ae7-984c-98610fc1ee40
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# 配置診断レポートの表示

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

以下のツールを使用すると、キャンペーンの実稼働後に、配置の設定とペースの問題を診断するのに役立ちます。

* **[!UICONTROL Change Log]:** 名前、ステータス、最大入札額など、キー配置設定に対する変更を表示します。各エントリには、変更をおこなったユーザーの日付とユーザー名が含まれます。
* **[!UICONTROL Ad Approvals]:** 在庫プロバイダーによって広告が承認されたか拒否されたかを表示します。オプションで、任意の広告のステータスを変更したり（拒否された広告の一時停止など）、広告設定を開いたりできます。
* **[!UICONTROL Non Bids]:** 配置でDSPが入札しなかった理由を表示します。

1. 診断レポートを開きます。
   1. 配置設定を開きます。
      1. メインメニューで&#x200B;**[!UICONTROL Campaigns]**&#x200B;をクリックします。
      1. キャンペーンの名前をクリックし、「**[!UICONTROL Placements]**」をクリックします。
      1. 配置名の横にある&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**&#x200B;をクリックします。
   1. 右上の「![配置の診断](/help/dsp/assets/placement-diagnostics.png)」または「**[!UICONTROL Diagnostic]**」をクリックします。
1. 次のいずれかの操作を行います。
   * 変更ログを表示するには、次の手順に従います。
      1. クリック **[!UICONTROL Change Log]**.
      1. （オプション）レポート結果をフィルターします。
         * 日付メニューで、レポート期間を「過去14日間」のデフォルトから別の期間（*[!UICONTROL Last 30 days]、* *[!UICONTROL Last 60 days]、* *[!UICONTROL Last 90 days]、*&#x200B;または&#x200B;*[!UICONTROL Last 1 year]*）に変更します。
         * 左側のメニューで、特定のユーザー名でレポートをフィルターします。
         * 右側のメニューで、特定の配置設定でレポートをフィルターします。
   * 広告承認のステータスを表示するには：
      1. 右上の「**[!UICONTROL Ad Approvals]**」をクリックします。
      1. （オプション）広告を一時停止またはアクティブ化するには、「広告」列のステータススイッチ（![ステータススイッチ](/help/dsp/assets/status-switch.png)）をクリックします。
      1. （オプション）広告の設定を開くには、広告の横にある&#x200B;**[!UICONTROL View Ad]**&#x200B;をクリックします。
   * DSPがプレースメントに入札しなかった理由を確認するには：
      1. 右上の「**[!UICONTROL Non Bids]**」をクリックします。
      1. （オプション）日付範囲を変更するには、日付フィールドをクリックして、別の日付または日付範囲を選択します。

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [プラットフォーム内レポートについて](campaign-reports-about.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

