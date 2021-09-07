---
title: 配置の複製
description: 1つ以上の配置を複製する方法を説明します。
feature: Placements
exl-id: d22a61a8-4f1b-41ee-b4fb-3124bec81a2f
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# 配置の複製

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

1つ以上の配置を複製して、類似の設定の配置を作成します。 次の操作が可能です。

* 配置を複数複製する
* 元の広告主とキャンペーン内または異なる広告内に配置を複製する
* （元のキャンペーン内で重複した配置の場合）オプションで元の広告を複製します
* 新しい配置のステータスとフライト日を変更する

重複しない配置設定のリストについては、「[重複しないもの](#placement-not-duplicated)」を参照してください。

1. メインメニューで&#x200B;**[!UICONTROL Campaigns]**&#x200B;をクリックします。
1. キャンペーンの名前をクリックします。
1. サブメニューで&#x200B;**[!UICONTROL Placements]**&#x200B;をクリックします。
1. 次のいずれかの操作を行います。
   * 1つの配置を複製するには、パッケージ名の横にある&#x200B;**[!UICONTROL ...]>[!UICONTROL Duplicate]**&#x200B;をクリックします。
   * 複数の配置を複製するには：
      1. 複製する各配置の横にあるチェックボックスを選択します。
      1. バルクアクションツールバーで、「**[!UICONTROL Duplicate]**」をクリックします。
1. 新しい配置設定を指定します。
   1. （単一の配置）新しい配置名を入力します。
   1. **[!UICONTROL Choose Package (Required)]**&#x200B;メニューで、親パッケージまたは**[!UICONTROL No package]*を選択します。
   1. （オプション）デフォルト設定を変更します。

   設定は、選択したすべての配置に適用されます。

   デフォルトでは、新しい配置は元の広告タイプ用で、元の広告主とキャンペーンに割り当てられ、現在の日に開始するフライトスケジュールを設定し、一時停止し、元の広告は含まれません。

   複数の配置を作成する場合、「My Placement #2」のような規則&lt;*original_placement_name #N*&#x200B;を使用して、新しい配置名に順に番号が追加されます。

1. クリック **[!UICONTROL Submit]**.

## 重複しないもの {#placement-not-duplicated}

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
>* [プレースメント管理について](placement-about.md)
>* [プレースメントの作成](placement-create.md)
>* [プレースメントの編集](placement-edit.md)
>* [配置設定](placement-settings.md)

