---
title: PG案件の広告を [!DNL FreeWheel]に送信
description: FreeWheel上のパブリッシャーとのプログラム的に保証された取引に対して広告の承認をリクエストする方法を説明します。
feature: Private Inventory, Deal IDs
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# プログラムで保証された契約の広告をFreeWheelに送信

*Programmatic  [!DNL FreeWheel] Guaranteed権限のみを持つアカウント*

広告の選択や契約に使用するプログラム的に保証されたデフォルト配置の作成を含め、FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)の発行者とのプログラム的な保証契約を[承認したら、広告をFreeWheelに送信して承認を受ける必要があります。

>[!PREREQUISITES]
>
>Adobeアカウントチームと協力して、[!DNL DSP]アカウントに[!DNL FreeWheel]プログラムで保証されたワークフローを使用する権限があることを確認します。

1. FreeWheel取引で使用する広告の広告キーをコピーします。

   1. キャンペーンの名前をクリックします。

   1. サブメニューで&#x200B;**[!UICONTROL Ads]**&#x200B;をクリックします。

   1. 広告名の横にある&#x200B;**[!UICONTROL ...]/[!UICONTROL Edit]**&#x200B;をクリックします。

   1. 広告設定が開いたら、ブラウザーのアドレスバーに表示されるURLの英数字の広告キーをコピーします。

      例えば、次のURLでは、広告キーは`3NtNC5ZbaGZtqbei8jD3`です。

      `https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

1. 広告をFreeWheelに送信：

   1. [!UICONTROL Deals]ビューで、取引を探します。

   1. Deal行で、![Options menu](/help/dsp/assets/options-menu.png) **[!UICONTROL submit to [!DNL FreeWheel]]**&#x200B;をクリックします。

   1. 取引IDを確認し、手順1でコピーした&#x200B;**[!UICONTROL Ad Key]**&#x200B;を入力し、「**[!UICONTROL Submit]**」をクリックします。

   広告を実行する前に、送信し承認する必要があります。

1. [広告送信ステータスを確認します](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [FreeWheelでのプログラム保証取引の設定の概要](freewheel-overview.md)
>* [Deal IDインボックスでのDealの承認](deal-id-inbox-accept.md)
>* [プログラムで保証された取引の広 [!DNL FreeWheel] 告のステータスの確認](freewheel-check-status.md)
>* [FreeWheel広告送信のエラーコード](freewheel-error-codes.md)

