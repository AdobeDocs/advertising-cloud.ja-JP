---
title: 永続 ID パートナーから認証済みセグメントをアクティブ化する
description: 永続的な ID ソリューションを使用して認証済みのオーディエンスをアクティブ化する方法について説明します。
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# 永続 ID パートナーから認証済みセグメントをアクティブ化する

*ベータ版機能*

Advertising DSPの永続的な ID ソリューションを通じて認証済みオーディエンスをアクティブ化するには、セグメントを [!DNL RampIDs]：入札可能な環境で認識可能です。 これは、次のいずれかの方法で実行できます。

* DSPと [!DNL Adobe Real-Time Customer Data Profile (CDP)] そして [!DNL Adobe-LiveRamp Retrieval API].

* 認証済みセグメントを、 [!DNL LiveRamp] [!DNL Connect] ダッシュボード。

## タスク

1. どちらのオプションの場合も、連絡先 `adcloud-support@adobe.com` を有効にして、DSPで次の設定を有効にします。これにより、DSPキャンペーンで認証済みのセグメントを 1 回ターゲットに設定できます。 [アクティベーションワークフローのすべての手順が完了します](source-about.md#workflow-sources):

   1. [!DNL LiveRamp] [!DNL RampID] セグメント共有の前のキャンペーン設定 [!DNL Real-Time CDP].

   1. アカウントレベルの[!UICONTROL LiveRamp segments]&quot;オプション。

1. ( ユーザーが手動で、 [!DNL LiveRamp]) 次の手順 ( [!DNL LiveRamp] [!DNL Connect] ダッシュボード：

   1. 宛先タイルをアクティブにする **[!DNL AAC API 1P Onboarding]**.

   1. 設定 [!DNL Identifier Settings] から **[!DNL Ramp ID]** のみ。

      ![識別子設定](/help/dsp/assets/liveramp-tile-settings.png)

   1. （オプション）Cookie ベースの識別子を引き続き受け取りたい場合、 [!DNL AAC API 1P Onboarding] 「 」を含む宛先タイル[!DNL Cookies],&quot; &quot;[!DNL IDFA],&quot;および&quot;[!DNL AAID]&quot;が選択されました。

## テストとデータ検証のベストプラクティス

* **ターゲット [!DNL RampID]に基づくセグメントと Cookie ベースのセグメントを別々のキャンペーンに組み込むことができます。**

   * キャンペーンの設定では、優先度を設定できる識別子は 1 つだけです。

   * 現在、 [!DNL RampIDs] オンサイトイベント中にを取得できません。 つまり、最も低い CPA や ROAS などの特定のカスタム目標は、認証済みのセグメントでは使用できません。 パフォーマンス KPI に制限がある場合にのみ、Cookie ベースのセグメントを使用してください。

* **両方で 1 つの配置を作成 [!DNL RampID] および Cookie ベースのキャンペーンに含まれます。**

   * 共有元のセグメントをターゲティング [!DNL LiveRamp] 標準のセグメントアクティベーションプロセスを使用して、

   * 適切なデータ配布を検証するには、Adobeの Advertising サポートチームと協力してください。

DSPとの統合の詳細については、以下を参照してください。 [!DNL LiveRamp]，連絡先 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [オーディエンスソースからの認証済みセグメントのアクティブ化について](source-about.md)
>* [オーディエンスソースを作成してファーストパーティオーディエンスをアクティブ化する](source-create.md)
>* [Audience Source 設定](source-settings.md)
>* [AdobeAdvertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)

