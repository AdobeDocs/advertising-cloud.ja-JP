---
title: FreeWheelでのPG取引の設定の概要
description: 'FreeWheel上のパブリッシャーとプログラム的に保証された取引を行うために必要な前提条件と追加手順について説明します。 '
feature: Private Inventory, Deal IDs
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# FreeWheelでのプログラム保証取引の設定の概要

FreeWheel上でプログラム保証取引を設定するには、追加の権限と手順が必要です。

>[!PREREQUISITES]
>
>Adobeアカウントチームと協力して、[!DNL DSP]アカウントに次の権限があることを確認します。
>
>1. [!DNL FreeWheel]プログラムで保証されたワークフローを使用する権限。プログラムで保証された取引の広告を[!DNL FreeWheel]に送信するために必要です。
>
>1. （各広告にClearcastクロック番号を必要とする英国のパブリッシャーと連携する場合）広告にクロック番号を含める権限。


## ワークフロー

1. 取引で指定されたメディアタイプで広告を作成します。

   英国のパブリッシャーによっては、広告にClearcastの時計番号を含める必要があります。

1. [Deal IDインボッ](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) クスを使用して、FreeWheel上で既にPublisherとネゴシエートした取引IDを受け入れます。

   取引を承認した後、プロンプトに従って1)取引に使用する広告を選択し、2)広告を提供するためのプログラム的に保証されたデフォルトの配置を作成します。

1. [広告をFreeWheelに送信](freewheel-submit.md)

   広告を実行する前に、送信し承認する必要があります。

1. [広告送信ステータスを確認します](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [Deal IDインボックスでのDealの承認](deal-id-inbox-accept.md)
>* [プログラムで保証された契約の広告をFreeWheelに送信](freewheel-submit.md)
>* [プログラムで保証された取引の広 [!DNL FreeWheel] 告のステータスの確認](freewheel-check-status.md)
>* [FreeWheel広告送信のエラーコード](freewheel-error-codes.md)

