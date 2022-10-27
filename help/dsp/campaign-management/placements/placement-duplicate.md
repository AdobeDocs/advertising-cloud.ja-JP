---
title: 配置を複製
description: 1 つ以上の配置の複製方法を説明します。
feature: DSP Placements
exl-id: d22a61a8-4f1b-41ee-b4fb-3124bec81a2f
source-git-commit: 5ed402a7c83072a7af6a06757050486c6d7d7080
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# 配置を複製

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

1 つ以上の配置を複製して、類似の設定の配置を作成します。 次の操作が可能です。

* 配置の複数の複製
* 元の広告主やキャンペーン内または異なる広告内に配置を複製
* （元のキャンペーン内で重複した配置の場合）オプションで、元の広告を複製します
* 新しい配置のステータスとフライト日を変更する

参照：[重複していないもの](#placement-not-duplicated)」と入力します。

1. メインメニューで、 **[!UICONTROL Campaigns]**.
1. キャンペーンの名前をクリックします。
1. サブメニューで、 **[!UICONTROL Placements]**.
1. 次のいずれかの操作を行います。
   * 配置を複製するには、  **[!UICONTROL ...]>[!UICONTROL Duplicate]** をクリックします。
   * 複数の配置を複製するには：
      1. 複製する各配置の横にあるチェックボックスを選択します。
      1. バルクアクションツールバーで、 **[!UICONTROL Duplicate]**.
1. 新しい配置設定を指定します。
   1. （単一の配置）新しい配置名を入力します。
   1. 内 **[!UICONTROL Choose Package (Required)]** メニューで、親パッケージまたは**を選択します[!UICONTROL No package]*.
   1. （オプション）デフォルト設定を変更します。

   設定は、選択したすべての配置に適用されます。

   デフォルトでは、新しい配置は元の広告タイプ用で、元の広告主とキャンペーンに割り当てられ、現在の日に開始するフライトスケジュールを持ち、一時停止し、元の広告は含まれません。

   複数の配置を作成する場合、新しい配置名には、&lt; という規則を使用して、番号が順に追加されます&#x200B;*original_placement_name #N*>>(「My Placement #2」など )

1. クリック **[!UICONTROL Submit]**.

## 重複していないもの {#placement-not-duplicated}

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
>* [配置管理について](placement-about.md)
>* [配置の作成](placement-create.md)
>* [配置の編集](placement-edit.md)
>* [配置の変更ログの表示](placement-change-log.md)
>* [配置設定](placement-settings.md)

