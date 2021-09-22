---
title: パッケージの複製
description: パッケージの複製方法を説明します。
feature: DSP Packages
exl-id: 4c37883f-5feb-4513-9573-ed4e32606132
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# パッケージの複製

パッケージを複製して、類似の設定のパッケージを作成します。 次の操作が可能です。

* 元の広告主とキャンペーン内または別のキャンペーン内でパッケージを複製します
* オプションで、パッケージ内の配置を複製します
* （元のキャンペーン内で重複したパッケージの場合）オプションで、元の広告と配置レベルのイベントピクセルを複製します
* 新しいパッケージのフライト日を変更します

重複しない配置設定のリストについては、「[重複しないもの](#package-not-duplicated)」を参照してください。

1. メインメニューで&#x200B;**[!UICONTROL Campaigns]**&#x200B;をクリックします。
1. キャンペーンの名前をクリックして、[!UICONTROL Packages]ビューを開きます。
1. パッケージ名の横にある&#x200B;**[!UICONTROL ...]>[!UICONTROL Duplicate]**&#x200B;をクリックします。
1. 新しいパッケージ設定を指定します。
   1. 新しいパッケージ名を入力します。
   1. （オプション）デフォルト設定を変更します。

      デフォルト：

      * 新しいパッケージが元の広告主とキャンペーンに割り当てられます。
      * 新しいパッケージは、現在の日にアクティブになります。<!-- and the flight continues for NN  days. -->
      * 元のパッケージ内の配置が新しいパッケージにコピーされます。
      * 広告と配置レベルのイベントピクセルは、新しいパッケージにコピーされません。
1. クリック **[!UICONTROL Submit]**.

## 重複しないもの {#package-not-duplicated}

元の配置のすべての設定は、次を除いて複製されます。

* 実験設定
* （フライト日を変更した場合）カスタム広告スケジュール
* （広告を添付しない場合）カスタム広告の重み付けとスケジュール
* プログラム保証(PG)取引と[!UICONTROL Simple Ad Serving]取引の場合のデフォルトの配置
* （配置を別のキャンペーンにコピーする場合）:
   * 地域ターゲット
   * イベントピクセル
   * 広告
   * 配置レベルの[!DNL DoubleVerify Authentic Brand Safety]セグメント（広告主レベルのセグメントを上書き）

>[!MORELIKETHIS]
>
>* [パッケージ管理について](package-about.md)
>* [パッケージの作成](package-create.md)
>* [パッケージの編集](package-edit.md)
>* [パッケージ設定](package-settings.md)

