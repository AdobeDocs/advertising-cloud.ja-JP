---
title: Adobe Audience ManagerとのAdobe広告の統合
description: Adobe広告がAdobe Audience Managerとデータを交換する様々な方法について説明します。
feature: Integration with Adobe Audience Manager
exl-id: 0f88235b-6f9c-4b97-9517-22e8c47e1846
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Adobe Audience ManagerとのAdobe広告の統合

以下の方法で、Adobe広告とAudience Managerを統合できます。

## Audience Managerとその他の同期 [!DNL Adobe] 広告ターゲティングのセグメント

[!DNL Search] とDSPは、すべての広告主や代理店のAudience Managerやその他の情報用に、メタデータ、階層データ、一意のオーディエンスデータを取り込むことができます [!DNL Adobe] オーディエンス。 この一意の接続は、Adobe広告を使用するマーケターのみが使用できます。 参照：[広告ターゲティング用のAdobe Audience Managerセグメントのインポート](/help/integrations/audience-manager/import-audiences.md).&quot;

### Audience Managerとその他を使用 [!DNL Adobe] 作成するセグメント [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*次を使用してオプトインした広告主 [!DNL Advertising Search] のみ*

[!DNL 内 [!DNL Search]」をクリックします。 [!DNL Google Ads] Googleの顧客一致オーディエンスを、 [!UICONTROL Adobe Media Optimizer (HTTP)] および [!UICONTROL Adobe Media Optimizer Batch Destination] を宛先として使用する場合。 ([!DNL Media Optimizer] は、[!DNL [!DNL Search]].) これには、Adobe Experience Cloudに公開されたAdobe Analyticsセグメントや、 [!DNL People core service]. 詳しくは、[!DNL] 内の製品内ヘルプを参照してください。 [!DNL Search]].

[ユーザー ID からの顧客一致オーディエンス](https://support.google.com/google-ads/answer/9199250) は web サイトのタグベースのオーディエンスと同様に機能しますが、一意のオーディエンスメンバーには、標準の顧客一致や web サイトのタグベースのオーディエンスよりも明確なメリットを得るために、PII 以外の ID が割り当てられます。

必要なユーザー ID を作成するには、Adobe広告 JavaScript タグを使用する必要があります <!-- with a user ID parameter -->を Web サイト上でクリックします。 担当の [!DNL [!DNL Search]] アカウントチームを参照してください。

![セグメント作成プロセス](/help/integrations/assets/ad_search_user_id_pic.png)

オーディエンスを作成したら、 [!DNL Google Ads] キャンペーンとして [キャンペーンレベルまたは広告グループレベルのターゲットまたは除外](#audience-manager-targets).

### Audience Managerとその他を使用 [!DNL Adobe] 広告のターゲティングまたは除外するセグメント {#audience-manager-targets}

* ([!DNL] を使用したオプトイン型広告主 [!DNL Search]]) 任意の [!DNL Google Ads] オーディエンス [次を使用して作成 [!DNL Adobe] セグメント](#audience-manager-google-audiences) キャンペーンレベルまたは広告グループレベルのターゲットまたは除外として [!DNL Google Ads] キャンペーン。

* (DSPの広告主 ) 既存の [!DNL Adobe] セグメントを、広告プレースメントのターゲットとして使用します。 オプションで、セグメントを再利用可能なオーディエンスに含めることができます。このオーディエンスは、複数の配置のターゲットまたは除外として使用できます。

* （Advertising Creative を使用する広告主）既存の [!DNL Adobe] セグメントを、広告エクスペリエンスの特定のクリエイティブのターゲットとして使用します。

>[!NOTE]
>
>Audience ManagerとExperience Cloud [!DNL Audience Library] 様々なオーディエンスタイプに対するインターフェイス、および一般的な使用例については、[オーディエンス作成オプション](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## DSP Media Exposure データをAudience Managerに送信

*DSPのみの広告主*

Adobe Audience Managerをご使用のDSPのお客様は、Audience Managerへのピクセル呼び出しを使用して広告キャンペーンからデータをキャプチャできます。 その後、キャンペーンデータを使用してルールベースの特性を作成し、新しいセグメントを定義して、より高度なセグメント化、頻度管理、マーケティング分析、レポートインサイトなど、様々なDSPのユースケースを有効にできます。

参照：[DSP Media Exposure データのAdobe Audience Managerへの送信の概要](/help/integrations/audience-manager/media-data-integration/overview.md)」を参照してください。

## Audience Analytics

Adobe広告のお客様 [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) は、広告追跡AdobeとAudience Managerセグメントの両方を [!DNL Analytics] サイトアクティビティに関するインサイトを強化します。

詳しくは、[[!DNL Adobe][!DNL Audience Analytics] (Adobe広告のお客様向け )](/help/integrations/audience-manager/audience-analytics.md).&quot;
