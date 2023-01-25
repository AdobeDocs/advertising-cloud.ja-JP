---
title: Deal ID の詳細の手動作成
description: Deal ID の詳細を手動で入力する方法を説明します。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: bc5f05faf96d455bd8954e7f7f44cc9fe849e562
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Deal ID の詳細の手動作成

1. メインメニューで、 **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. データテーブルの上にある **[!UICONTROL Create]**&#x200B;を選択し、 **[!UICONTROL Deal ID]**.

1. 次を入力します。 [取引設定](deal-id-settings.md):

   1. 内 [!UICONTROL Deal ID basics] 「 」セクションで、契約の詳細と、契約にアクセスできる広告主を指定します。 保証された契約の場合は、トラッキングの目的でのみ、計画されたフライト日と推定インプレッション数も指定する必要があります。

      「在庫/契約」表示に「PG Impression Pacing」支出列を含めることで、保証された契約のペーシングを追跡できます。

   1. ( 管理者ユーザーのみ、（オプション） [!UICONTROL Technical] 「 」セクションで、必要に応じてデフォルト設定を編集します。

   1. クリック **[!UICONTROL Save]**.

1. （保証された契約のみ）契約に使用する広告を選択し、デフォルトのプログラム保証 (PG) 配置を作成します。

   デフォルトの PG 配置により、契約が常に各入札リクエストの入札を返すようになります。 デフォルトの PG 配置を作成しない場合、その契約をターゲットとする配置は、正しく設定されていない限り入札されません。 常にデフォルトの PG 配置を作成する必要があります。 内 [!UICONTROL Placements] ビュー、デフォルトの PG 配置には [!UICONTROL Sub-type] 列の値&quot;[!UICONTROL PG Default].&quot;

   オプションで、追加の配置でこの契約を在庫ターゲットとして使用できますが、入札をおこなうには正しく設定する必要があります。

   1. 内 [!UICONTROL Ad & Campaign Selection] 設定で、契約に使用する広告を選択します。

      1. 広告主、キャンペーン、広告のタイプを選択します。 オプションで、広告のフィルターに使用する広告ステータスを選択します。

      1. 使用可能な広告のリストから、契約に使用する各広告の横にあるチェックボックスを選択します。

      1. クリック **[!UICONTROL Apply]**.
   1. 配置設定画面で、次の操作を実行します。

      1. 配置名を入力します。

      1. （オプション） [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)デフォルトの入札額が上書きされます。この入札額は、契約の CPM 値が自動的に入力されます。日付範囲の変更広告を添付する。

      この契約は、「在庫ターゲット」セクションで自動的にターゲットになります。 その他のすべてのターゲット設定オプションは適用できません。

      1. クリック **[!UICONTROL Create placement]**.



契約を作成した後は、その契約を複数の配置の在庫ターゲットとして使用できます。

>[!NOTE]
>
> 契約タグを発行者に送信して検証する必要はありません。

>[!TIP]
>
>* 内 [!UICONTROL Inventory] > [!UICONTROL Deals] ビュー、 [!UICONTROL Pacing & Budget] 列には、指定したフライト日とインプレッション目標に対する契約のペーシングが示されます。
>
>* 配信のペーシングが不十分または過剰な場合は、パブリッシャーに連絡して、契約を通じて送信するボリュームを調整します。


>[!MORELIKETHIS]
>
>* [手動の Deal ID 設定](deal-id-settings.md)
>* [プログラム的に保証された契約の設定](programmatic-guaranteed-set-up.md)
>* [プログラム的に保証された取引に対する広告の送信 [!DNL FreeWheel]](freewheel-submit.md)
>* [プログラムで保証された契約について](programmatic-guaranteed-about.md)

<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->
