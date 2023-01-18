---
title: オーディエンスソースからの認証済みセグメントのアクティブ化について
description: 顧客データプラットフォームからファーストパーティセグメントを取り込む方法について説明します。
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# オーディエンスソースからの認証済みセグメントのアクティブ化について

<!-- Doesn't specifically explain what you can do in our UI -->
*ベータ版機能*

DSPは、顧客データプラットフォーム (CDP) 内で作成された認証済みのシグナルで構成されるファーストパーティセグメントを取り込むことができます。 取り込んだセグメントを配置のターゲットとして使用できます。

## [!DNL Adobe Real-Time Customer Data Profile]

DSPは [の [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)(Adobe Experience Platformの一部 )

In [!DNL Real-time CDP], *宛先* は、シームレスなデータアクティベーションを可能にする、外部データプラットフォームへの接続です。 例えば、宛先を使用して、DSPでサポートされる複数のデジタル形式にわたるターゲット化した広告に関する既知の顧客関係（ハッシュ化された電子メールアドレスなど）をアクティブ化できます。

宛先について詳しくは、「Experience Platform [宛先ガイド](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)（製品の概要、手順を含む） [宛先ワークスペースの作成](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) および [宛先接続の作成](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)、および [宛先へのデータのアクティブ化](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### とのDSP統合を使用する際のワークフロー [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [DSPによる顧客データセグメントの変換を許可 [!DNL LiveRamp RampIDs]](source-durable-id.md) 入札可能な環境で認識可能な<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your DSP account team will perform this configuration. -->

1. [オーディエンスソースの作成](source-create.md) オーディエンスをDSPアカウントまたは広告主アカウントにインポートする場合。

1. [の設定 [!DNL Real-Time CDP] Experience Platformの宛先接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).

その他のサポートについては、 [!DNL Adobe] アカウントチームまたは `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [永続 ID パートナーから認証済みセグメントをアクティブ化](source-durable-id.md)
>* [オーディエンスソースを作成してファーストパーティオーディエンスをアクティブ化する](source-create.md)
>* [Audience Source 設定](source-settings.md)
>* [AdobeAdvertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [宛先カタログの概要](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)

