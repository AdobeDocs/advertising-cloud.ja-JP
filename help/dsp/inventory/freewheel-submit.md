---
title: PG 取引の広告をに送信 [!DNL FreeWheel]
description: FreeWheel 上のパブリッシャーとのプログラム的に保証された取引に対して、広告の承認をリクエストする方法を説明します。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: b149804bc3e9de5cd48a00f0611c09d1f2e7c7ca
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# プログラムで保証された契約の広告を FreeWheel に送信

*を持つ [!DNL FreeWheel] Programmatic Guranted 権限のみ*

一度 [FreeWheel の出版社とのプログラム的に保証された契約を受け入れる](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)広告の選択や、契約に使用するプログラムで保証されたデフォルト・プレースメントの作成を含め、広告は FreeWheel に送信して承認を受ける必要があります。

>[!PREREQUISITES]
>
>の使用 [!DNL Adobe] アカウントチームが、 [!DNL DSP] アカウントには、 [!DNL FreeWheel] プログラムで保証されたワークフロー。

1. FreeWheel 取引で使用する広告の広告キーをコピーします。

   1. キャンペーンの名前をクリックします。

   1. サブメニューで、 **[!UICONTROL Ads]**.

   1. クリック  **[!UICONTROL ...]>[!UICONTROL Edit]** をクリックします。

   1. 広告設定が開いたら、ブラウザーのアドレスバーに表示される URL の英数字の広告キーをコピーします。

      例えば、次の URL では、広告キーは `3NtNC5ZbaGZtqbei8jD3`

      `https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

1. 広告を FreeWheel に送信：

   1. の [!UICONTROL Deals] を表示し、取引を検索します。

   1. 取引行で、「 ![オプションメニュー](/help/dsp/assets/options-menu.png) **>[!UICONTROL submit to [!DNL FreeWheel]]**.

   1. 取引 ID を確認し、 **[!UICONTROL Ad Key]** 手順 1 でコピーし、 **[!UICONTROL Submit]**.

   広告を実行する前に、送信して承認する必要があります。

1. [広告送信ステータスの確認](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [FreeWheel でのプログラム保証取引の設定の概要](freewheel-overview.md)
>* [Deal ID インボックスでの Deal の承認](deal-id-inbox-accept.md)
>* [広告のステータスの確認 [!DNL FreeWheel] プログラム保証取引](freewheel-check-status.md)
>* [FreeWheel 広告送信のエラーコード](freewheel-error-codes.md)

