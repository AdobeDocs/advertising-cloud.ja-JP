---
title: '[!DNL Analytics] Advertising Cloudのデータ'
description: '[!DNL Analytics] Advertising Cloudのデータ'
feature: Integration with Adobe Analytics
exl-id: 79fbc809-9965-41c1-971f-3652cc78fee3
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# [!DNL Analytics] Advertising Cloudのデータ

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

## Analyticsセグメント

[!DNL Analytics]で作成され、Experience Cloudに公開されたすべてのセグメント。

新しいセグメントがAdvertising Cloudに表示されるまでに24 ～ 48時間かかります。 既存のセグメントの更新は、約8時間以内に同期されます。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## サイトのエンゲージメント指標

>[!NOTE]
>
>* [!DNL Analytics] は、EF IDイベントをAdvertising CloudにeVarに渡します。デフォルトの統合では、計算指標または他のディメンション(eVar)のAdvertising Cloudへの送信はサポートされません。 ただし、計算指標をカスタムイベントで完全にキャプチャできる場合は、Advertising Cloudはカスタムイベントを取り込むことができます。
>* [!DNL Analytics] は、1時間ごとにAdvertising Cloudにデータを渡します。


* [!UICONTROL Timespent_secs_1stvisit]:訪問者の初回訪問時にサイトで滞在した秒数。
* [!UICONTROL Timespent_secs_total]:クリックのルックバックウィンドウ内のすべての訪問でサイトで費やされた合計秒数。
* [!UICONTROL Pageviews_1stvisit]:訪問者の初回訪問中のサイトでのページビュー数。
* [!UICONTROL Pageviews_total]:クリックルックバックウィンドウ内のすべての訪問における、サイトでのページビューの合計数。
* [[!UICONTROL Bounces] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]:を収集した [!DNL Analytics] 回 [!UICONTROL EF ID]数。

## コンバージョン指標

[!DNL Analytics] はコンバージョン指標を毎日Advertising Cloudに渡します。

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

これらの指標はレポートスイートに固有なので、利用できる指標は顧客やレポートスイートごとに異なります。

### 予約済みコンバージョン指標

これらの指標はレポートスイートに固有なので、利用できる指標は顧客やレポートスイートごとに異なります。

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Analysis WorkspaceのAdvertising Cloud指標](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)

