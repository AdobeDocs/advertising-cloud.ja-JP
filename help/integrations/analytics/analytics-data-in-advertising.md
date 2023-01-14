---
title: '"[!DNL Analytics] Adobe広告のデータ»'
description: '"[!DNL Analytics] Adobe広告のデータ»'
feature: Integration with Adobe Analytics
exl-id: 79fbc809-9965-41c1-971f-3652cc78fee3
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# [!DNL Analytics] Adobe広告のデータ

*Advertising とAdobe AnalyticsのAdobeの統合のみの広告主*

## Analytics セグメント

で作成されたすべてのセグメント [!DNL Analytics] Experience Cloud

新しいセグメントがAdobe広告に表示されるまでに 24 ～ 48 時間かかります。 既存のセグメントの更新は、約 8 時間以内に同期されます。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## サイトエンゲージメント指標

>[!NOTE]
>
>* [!DNL Analytics] は EF ID イベントをAdobe広告に渡します。  デフォルトの統合では、計算指標または他のディメンション (eVar) のAdobe広告への送信はサポートされていません。 ただし、計算指標がカスタムイベントで完全にキャプチャできる場合は、Adobe広告でカスタムイベントを取り込むことができます。
>* [!DNL Analytics] は、時間ごとにAdobe広告にデータを渡します。


* [!UICONTROL Timespent_secs_1stvisit]:訪問者の初回訪問時にサイトで費やした秒数。
* [!UICONTROL Timespent_secs_total]:クリックのルックバックウィンドウ内のすべての訪問でサイトで費やした合計秒数。
* [!UICONTROL Pageviews_1stvisit]:訪問者の初回訪問中のサイトでのページビュー数。
* [!UICONTROL Pageviews_total]:クリックのルックバックウィンドウ内のすべての訪問における、サイトでのページビューの合計数。
* [[!UICONTROL Bounces] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]:次の回数： [!DNL Analytics] 収集された [!UICONTROL EF ID].

## コンバージョン指標

[!DNL Analytics] はコンバージョン指標を毎日Adobe広告に渡します。

### 標準コンバージョン指標

* [[!UICONTROL Revenue] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### カスタムコンバージョン指標

これらの指標はレポートスイートに固有なので、利用できる指標は顧客とレポートスイートごとに異なります。

### 予約済みのコンバージョン指標

これらの指標はレポートスイートに固有なので、利用できる指標は顧客とレポートスイートごとに異なります。

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [Analysis WorkspaceのAdobe広告指標](/help/integrations/analytics/advertising-metrics-in-analytics.md)

