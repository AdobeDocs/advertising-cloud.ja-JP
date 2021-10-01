---
title: Deal ID の詳細の手動作成
description: Deal ID の詳細を手動で入力する方法を説明します。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: cd9763a7-99d4-4881-9df9-b4e24c55be0f
source-git-commit: 7e2a52e7b0d91f9206cd6e9a6ffb41a8399abf00
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Deal ID の詳細の手動作成

1. メインメニューで **[!UICONTROL Inventory]> [!UICONTROL Deals].** をクリックします。

1. データテーブルの上の **[!UICONTROL Create]** をクリックし、**[!UICONTROL Deal ID]** を選択します。

1. [Deal 設定 ](deal-id-settings.md) を入力します。

   1. [!UICONTROL Deal ID basics] セクションで、取引の詳細と、取引にアクセスできる広告主を指定します。 保証された取引の場合は、追跡の目的でのみ、計画されたフライト日とインプレッション数の見積もりも指定する必要があります。

   1. （管理者ユーザーのみ）（オプション） [!UICONTROL Technical] セクションで、必要に応じてデフォルト設定を編集します。

   1. クリック **[!UICONTROL Save]**.

1. （保証された取引のみ）取引に使用する広告を選択し、デフォルトのプログラム保証 (PG) の配置を作成します。

   デフォルトの PG 配置により、取引が常にすべての入札リクエストの入札を返すようになります。 デフォルトの PG 配置を作成しない場合は、正しく設定されていない限り、その配置をターゲットにした場合、入札は行われません。 常にデフォルトの PG 配置を作成する必要があります。 [!UICONTROL Placements] ビューでは、デフォルトの PG 配置には、[!UICONTROL Sub-type] 列の値&quot;[!UICONTROL PG Default]&quot;が設定されます。

   オプションで、追加の配置で在庫ターゲットとして取引を使用できますが、入札を行うには正しく設定する必要があります。

   1. [!UICONTROL Ad & Campaign Selection] 設定で、取引に使用する広告を選択します。

      1. 広告主、キャンペーン、広告のタイプを選択します。 オプションで、広告のフィルターに使用する広告のステータスを選択します。

      1. 使用可能な広告のリストから、取引に使用する各広告の横にあるチェックボックスを選択します。

      1. クリック **[!UICONTROL Apply]**.
   1. 配置設定画面で、次の操作をおこないます。

      1. 配置名を入力します。

      1. （オプション）配置設定 [ を編集します。デフォルトの入札額は、案件の CPM 値が自動的に入力され、上書きされます。日付範囲の変更広告を追加する。](/help/dsp/campaign-management/placements/placement-settings.md)

      この案件は、「在庫ターゲット」セクションで自動的にターゲットになります。 その他のすべてのターゲティングオプションは適用できません。

      1. クリック **[!UICONTROL Create placement]**.



取引を作成した後は、その取引を複数の配置の在庫ターゲットとして使用できます。

>[!NOTE]
>
> パブリッシャーに取引タグを送信して検証する必要はありません。

>[!TIP]
>
>* [!UICONTROL Inventory] > [!UICONTROL Deals] ビューでは、[!UICONTROL Pacing & Budget] 列は、指定したフライト日とインプレッションの目標に対して、取引がどのようにペーシングしているかを示します。
>
>* 配信のペーシング率が低い場合や超過している場合は、パブリッシャーに連絡して、配信がデールを通じて送信するボリュームを調整してください。


>[!MORELIKETHIS]
>
>* [手動の Deal ID 設定](deal-id-settings.md)
>* [プログラム的に保証された取引の設定](programmatic-guaranteed-set-up.md)
>* [プログラムで保証された取り引きの広告を送信 [!DNL FreeWheel]](freewheel-submit.md)
>* [プログラム保証取引について](programmatic-guaranteed-about.md)

<!-- >* [Specify Placements and Ads for a Private Deal](private-deal-attach-placements.md)-->