---
title: 広告ターゲティング用のAdobe Audience Managerセグメントのインポート
description: インポート方法を学ぶ [!DNL Adobe] Adobe Audience Managerを使用して Advertising DSPと Search にオーディエンスを追加
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# 広告ターゲティング用のAdobe Audience Managerセグメントのインポート

Advertising DSP and [!DNL Advertising Search] は、すべての広告主や代理店のメタデータ、階層データ、一意のオーディエンスデータを取り込むことができます [!DNL Adobe] audiences<!-- segments or audiences? Standardize terms per AAM's docs -->. これには、以下のデータが含まれます。

* Adobe Audience Managerセグメント

* Adobe Experience Cloudに公開されたAdobe Analyticsセグメント

* Adobe Experience Cloudで [!DNL People core service]

* Adobe Experience Platformで作成され、Audience Managerを介してAdobe広告に送信されるセグメント

アクセスするには [!DNL Adobe] DSPまたは [!DNL Creative]の場合、オーディエンスをDSPにインポートする必要があります。 アクセスするには [!DNL Adobe] [!DNL のオーディエンス [!DNL Search]」の場合、オーディエンスを [!DNL] にインポートする必要があります。 [!DNL Search]].

## 前提条件

* 広告主は、 [の [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) バージョン 2.0 以降。 この [!DNL Identity Service] は、Experience Cloudのすべてのソリューションにわたって訪問者を識別する、普遍的、永続的な ID を提供します。

   実装には、 [!DNL Identity service] コードを広告主のサイトの各 web ページに追加します。

* 組織は [Experience Cloudサービス](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) そしてExperience Cloud [!DNL Organization ID] ( 以前の [!DNL IMS org ID]) をクリックします。

   この [!UICONTROL Organization ID] を使用すると、複数のAdobe Experience Cloud製品を持つ組織が一部の製品でデータを共有できます。

* ( [!DNL Analytics]) 広告主は [実装する [!DNL Analytics] using `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) バージョン 1.6.4 以降。

* 広告主の Web サイトの訪問者数が多くを含んでいない [!DNL Apple Safari] ユーザー。

* ( 広告主がAudience Managerと [!DNL Analytics]) 各 Web ページへの呼び出しを減らすには、既存のAudience Managerを削除します [!DNL Data Integration Library] データ収集用のコードと、各 [!DNL Analytics] レポートスイートを使用します。 詳しくは、[サーバー側転送の概要](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* （推奨）一致率を高めるには、ファーストパーティの Web サイトデータのみをAdobe広告に送信します。 広告主が顧客関係管理システムのサードパーティのデータやオフラインのデータをバンドルする場合、データの漏洩によって一致率が低下する可能性があります。

## Audience ManagerオーディエンスをDSPにインポート

### オーディエンスをDSPにインポートする手順

この [!DNL Adobe] アカウントおよびデータ操作チームは、次の手順を実行します。

1. この [!DNL Adobe] アカウントチームは、広告主レベルの設定「 」を設定する必要があります。[!UICONTROL Adobe Analytics Cloud].&quot;

1. この [!DNL Adobe] アカウントチームはリクエストを送信する必要があります<!-- Submit a request as a JIRA task? --> データ運用チームに<!-- implementation team? --> :Advertising DSPのネイティブ API 統合を使用して、組織のAudience Managerセグメントを読み込みます。

### どのような変更がAudience Managerに

API は自動的に以下をおこないます。

* 次の 2 つのDSPの宛先をAudience Managerに作成します。

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* 2 つの宛先をすべてのAudience Managerセグメントにマッピングし、Audience Managerは、同じExperience Cloudに関連付けられているDSP広告主アカウントとセグメントを共有できます [!DNL Organization ID] Audience Managerに使用 <!-- Verify -->

   組織は、必要のないセグメントをオプションで、Audience Manager内の宛先から削除できます。

* 顧客キャンペーンのリーチを向上させるために、組織のAudience Managerコンテナに次の exchange cookie-sync ピクセルを追加します。

   * AdobeAdCloud:411 ( 標準で、 [!DNL Identity Service] バージョン 2.0. [!DNL Identity Service] 2.0 より前のバージョンでは、このピクセルをAudience Managerコンテナに追加する必要があります。

## Audience Managerオーディエンスのインポート先 [!DNL Search]

### オーディエンスのインポート手順 [!DNL Search]

[!DNL Adobe] の担当者は、次の手順のほとんどまたはすべてを実行します。

1. この [!DNL Adobe] アカウントチームは、データ運用チームにリクエストを送信して、 [!DNL Search] とAudience Manager。 書き出し先のAudience Managerセグメントの名前を含めます [!DNL Search].

1. Audience Manager内で、 [!DNL Search]:

   1. 次の 2 つの新しい宛先を作成します。 `[!UICONTROL Adobe Media Optimizer (HTTP)]` および `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] は、 [!DNL Search].

   1. 各宛先のセグメントを指定します。

      を使用 [!UICONTROL Automatically map all current and future segments] 」オプションを使用すると、すべてのセグメントが毎日マッピングおよび同期されます。

      この [!UICONTROL Manually map segments] オプションを使用すると、バッチ保存先 (`[!UICONTROL Adobe Media Optimizer Batch Destination]`) をクリックします。 HTTP 宛先にセグメントを手動でマッピングする必要はありません。

1. 内 [!DNL Search]、 [!DNL Search] 直接アクセスクライアントマネージャーの役割を持つ実装チームまたはユーザーは、 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   組織のExperience Cloudを入力する必要があります [!DNL Organization ID] ([!DNL IMS org ID]) をクリックします。 この ID は、組織の組織アカウントで使用される ID と同じである必要がありますAudience Manager。

### どのような変更がAudience Managerに

組織には 2 つの [!DNL Search] Audience Manager内の宛先：

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## データの同期

最初の読み込みには約 24 時間かかります。 最初のインポートの後、データはリアルタイムで同期され、1～2 秒の遅延が生じます。

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].
 
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## 同期されたセグメントの場所

### DSP内

DSPでは、セグメント名はAudience Managerの分類別に整理され、で対応するセグメントメンバーシップカウントと共に使用できます。

* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting):の [!UICONTROL Adobe Segments] タブ [!UICONTROL Audience Targeting] 」セクションに入力します。

* In [オーディエンス設定](/help/dsp/audiences/audience-settings.md):の [!UICONTROL Adobe Segments] タブをクリックします。

### Advertising Creative 内

In [!DNL Creative]の場合、セグメントはターゲットノードのエクスペリエンス設定で使用できます。

### In [!DNL Advertising Search]

[!DNL [!DNL Search]」と入力すると、 [!DNL Google] オーディエンスを [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]から [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

各 [!DNL Google] オーディエンスを作成します。 [!DNL Google] は、オーディエンスサイズを提供します。

>[!MORELIKETHIS]
>
>* [Adobe Audience ManagerとのAdobe広告の統合](/help/integrations/audience-manager/overview.md)

