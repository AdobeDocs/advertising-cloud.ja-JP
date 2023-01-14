---
title: キャンペーンの複製
description: キャンペーンの複製方法を説明します。
feature: DSP Campaigns
exl-id: 2bb4030d-22b0-4a16-aeed-35f64a19df6a
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# キャンペーンの複製

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

キャンペーンを複製して、類似した設定の新しいキャンペーンを作成します。 次の操作が可能です。

* 元の広告主または別の広告主のキャンペーンを複製します
* オプションで、元のパッケージと配置を複製します
* 新しいキャンペーンのフライト日を変更

参照：[重複していないもの](#campaign-not-duplicated)」と入力します。

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. キャンペーン名の横にある **... >[!UICONTROL Duplicate]**.

1. 新しいキャンペーン設定を指定します。

   1. 新しいキャンペーン名と終了フライト日を入力します。

   1. （オプション）デフォルト設定を変更します。

      デフォルトでは、新しいキャンペーンは元の広告主に割り当てられ、現在の日に開始するフライトスケジュールを持ち、元のパッケージと配置が含まれます。

1. クリック **[!UICONTROL Submit]**.

## 重複していないもの {#campaign-not-duplicated}

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
>* [Campaign Managementについて](campaign-about.md)
>* [キャンペーンの作成](campaign-create.md)
>* [キャンペーンの編集](campaign-edit.md)
>* [キャンペーン設定](campaign-settings.md)

