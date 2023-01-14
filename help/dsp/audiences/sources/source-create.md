---
title: オーディエンスソースを作成してファーストパーティオーディエンスをアクティブ化する
description: オーディエンスをアカウントまたは広告主アカウントにインポートするソースを作成する方法を説明します。
feature: DSP Audiences
exl-id: 16eb7cdb-4364-4e94-ba73-0f2d4d200cb9
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# オーディエンスソースを作成してファーストパーティオーディエンスをアクティブ化する

*ベータ版機能*

<!-- Will this remain for admin users/Adobe account teams only? -->

オーディエンスをDSPアカウントまたは広告主アカウントにインポートするソースを作成します。 現在、次のオーディエンスをインポートできます： [の [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>ソースを作成した後、 [!DNL Real-Time CDP]を有効にするには、 [!DNL Real-Time CDP] 内のAdobeAdvertising DSPの宛先を通じてオーディエンス [!DNL Real-Time CDP] 読み込みを開始します。 詳しくは、 [アクティベーションワークフローの手順](source-about.md#workflow-sources).

1. メインメニューで、「**」をクリックします。[!UICONTROL Audiences] > [!UICONTROL Sources (BETA)].

1. クリック [!UICONTROL Add Source].

1. 内 [!UICONTROL Select a Type] メニューで、ソースタイプを選択します。

   *[!UICONTROL RT-CDP]*:このソースタイプ（の場合） [の [!DNL Adobe Real-Time Customer Data Profile]](source-about.md)は唯一のオプションです。

1. 次を指定： [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* または *[!UICONTROL Account]*.

1. 残りの [ソース設定](source-settings.md).

   のコピーを保持 [!UICONTROL Source Key] が生成されます。 値は後で必要になります。

1. クリック **[!UICONTROL Save]**.

1. Experience Platformで、 [!UICONTROL Source Key] DSPのソース設定で生成された

DSPの宛先接続をアクティブ化し、セグメントを選択し、制御権限にアクセスする手順については、「[Adobe Advertising Cloud DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [Audience Source 設定](source-settings.md)
>* [オーディエンスソースからの認証済みセグメントのアクティブ化について](source-about.md)
>* [永続 ID パートナーから認証済みセグメントをアクティブ化](source-durable-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)

