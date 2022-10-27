---
title: パッケージの複製
description: パッケージの複製方法を説明します。
feature: DSP Packages
exl-id: 4c37883f-5feb-4513-9573-ed4e32606132
source-git-commit: 5ed402a7c83072a7af6a06757050486c6d7d7080
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# パッケージの複製

パッケージを複製して、同様の設定のパッケージを作成します。 次の操作が可能です。

* 元の広告主とキャンペーン内または別のキャンペーン内でパッケージを複製します
* オプションでパッケージ内に配置を複製
* （元のキャンペーン内で重複したパッケージの場合）オプションで、元の広告と配置レベルのイベントピクセルを複製します。
* 新しいパッケージのフライト日を変更

参照：[重複していないもの](#package-not-duplicated)」と入力します。

1. メインメニューで、 **[!UICONTROL Campaigns]**.
1. キャンペーン名をクリックして、 [!UICONTROL Packages] 表示
1. パッケージ名の横にある  **[!UICONTROL ...]>[!UICONTROL Duplicate]**.
1. 新しいパッケージ設定を指定します。
   1. 新しいパッケージ名を入力します。
   1. （オプション）デフォルト設定を変更します。

      デフォルトでは：

      * 新しいパッケージが元の広告主とキャンペーンに割り当てられます。
      * 新しいパッケージは、現在の日にアクティブになります。<!-- and the flight continues for NN  days. -->
      * 元のパッケージ内の配置は、新しいパッケージにコピーされます。
      * 広告と配置レベルのイベントピクセルは、新しいパッケージにコピーされません。
1. クリック **[!UICONTROL Submit]**.

## 重複していないもの {#package-not-duplicated}

元の配置のすべての設定は、次を除いて複製されます。

* 実験設定
* （フライト日を変更した場合）カスタム広告スケジュール
* （広告を付加しない場合）カスタム広告の重み付けとスケジュール
* プログラム保証 (PG) 契約および配置のデフォルトの配置 [!UICONTROL Simple Ad Serving] 契約
* （配置を別のキャンペーンにコピーする場合）:
   * 地域ターゲット
   * イベントピクセル
   * 広告
   * 配置レベル [!DNL DoubleVerify Authentic Brand Safety] セグメント（広告主レベルのセグメントに優先）

>[!MORELIKETHIS]
>
>* [パッケージ管理について](package-about.md)
>* [パッケージの作成](package-create.md)
>* [パッケージの編集](package-edit.md)
>* [パッケージの変更ログの表示](package-change-log.md)
>* [パッケージ設定](package-settings.md)

