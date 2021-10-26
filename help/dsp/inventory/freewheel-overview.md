---
title: FreeWheel での PG の設定の概要
description: 'FreeWheel 上のパブリッシャーとプログラム的に保証された取引を行うために、広告を実行するために必要な前提条件と追加手順について説明します。 '
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: dfd5992f059645622b3a75d092d3eb7fe1bfa696
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# FreeWheel でのプログラム保証取引の設定の概要

FreeWheel でプログラム的に保証された取引を行う場合は、追加の権限と手順が必要です。

>[!PREREQUISITES]
>
>の使用 [!DNL Adobe] アカウントチームが、 [!DNL DSP] アカウントには次の権限があります。
>
>1. を使用する権限 [!DNL FreeWheel] プログラム的に保証された取り引きのために広告を送信する必要がある、プログラム的に保証されたワークフロー [!DNL FreeWheel].
>
>1. （各広告で Clearcast クロック番号を必要とする英国のパブリッシャーと連携する場合）広告にクロック番号を含める権限。


## ワークフロー

1. 取引で指定されたメディアタイプで広告を作成します。

   英国のパブリッシャーによっては、広告に Clearcast クロック番号を含める必要があります。

1. [取引 ID の承認](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) 既に、Deal ID Inbox を使用して FreeWheel のパブリッシャーとネゴシエートしています。

   取引を承認した後、プロンプトに従って 1) 取引に使用する広告を選択し、2) 広告を提供するためのプログラム的に保証されたデフォルトの配置を作成します。

1. [広告を FreeWheel に送信](freewheel-submit.md)

   広告を実行する前に、送信して承認する必要があります。

1. [広告送信ステータスの確認](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Deal ID インボックスでの Deal の承認](deal-id-inbox-accept.md)
>* [プログラムで保証された契約の広告を FreeWheel に送信](freewheel-submit.md)
>* [広告のステータスの確認 [!DNL FreeWheel] プログラム保証取引](freewheel-check-status.md)
>* [FreeWheel 広告送信のエラーコード](freewheel-error-codes.md)

