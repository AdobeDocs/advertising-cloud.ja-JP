---
title: Deal IDの詳細の手動作成
description: Deal IDの詳細を手動で入力する方法を説明します。
feature: Private Inventory, Deal IDs
exl-id: cd9763a7-99d4-4881-9df9-b4e24c55be0f
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# Deal IDの詳細の手動作成

1. メインメニューで&#x200B;**[!UICONTROL Inventory]> [!UICONTROL Deals].**&#x200B;をクリックします。

1. データテーブルの上にある&#x200B;**[!UICONTROL Create]**&#x200B;をクリックし、「**[!UICONTROL Deal ID]**」を選択します。

1. [Deal設定](deal-id-settings.md)を入力します。

   1. [!UICONTROL Deal ID basics]セクションで、取引の詳細と、取引にアクセスできる広告主を指定します。 保証されたオファーの場合は、追跡の目的でのみ、計画されたフライト日とインプレッションの推定値も指定する必要があります。

   1. （管理者ユーザーのみ）（オプション） [!UICONTROL Technical]セクションで、必要に応じてデフォルト設定を編集します。

   1. クリック **[!UICONTROL Save]**.

1. （保証された取引のみ）取引に使用する広告を選択し、デフォルトのプログラム保証(PG)配置を作成します。

   デフォルトのPG配置により、取引が常にすべての入札リクエストの入札を返すようになります。 デフォルトのPG配置を作成しない場合、正しく設定されていない限り、その配置をターゲットにしても入札は行われません。 常にデフォルトのPG配置を作成する必要があります。 [!UICONTROL Placements]ビューでは、デフォルトのPG配置には[!UICONTROL Sub-type]列の値「[!UICONTROL PG Default]」が設定されます。

   オプションで、追加の配置で在庫ターゲットとしてこの取引を使用できますが、入札をおこなうには正しく設定する必要があります。

   1. [!UICONTROL Ad & Campaign Selection]設定で、取引に使用する広告を選択します。

      1. 広告主、キャンペーン、広告タイプを選択します。

      1. 使用可能な広告のリストから、その取引に使用する各広告の横にあるチェックボックスを選択します。

      1. クリック **[!UICONTROL Apply]**.
   1. 配置設定画面で、次の操作を行います。

      1. 配置名を入力します。

      1. （オプション）配置設定[を編集し、デフォルトの入札額を上書きします。デフォルトの入札額は、案件のCPM値で自動的に入力されます。日付範囲の変更広告を添付する。](/help/dsp/campaign-management/placements/placement-settings.md)

      この案件は、「Inventory Targets」セクションで自動的にターゲットになります。 その他のすべてのターゲティングオプションは適用できません。

      1. クリック **[!UICONTROL Create placement]**.



デールを作成した後は、そのデールを複数のプレースメントの在庫ターゲットとして使用できます。

>[!NOTE]
>
> 発行者に取引タグを送信して確認する必要はありません。

>[!TIP]
>
>* [!UICONTROL Inventory] > [!UICONTROL Deals]ビューの[!UICONTROL Pacing & Budget]列には、取引が指定されたフライト日とインプレッションの目標にどのようにペーシングされているかが示されます。
>
>* 配信のペーシング率が低い場合や超過している場合は、パブリッシャーに問い合わせて、配信がデールを通じて送信するボリュームを調整します。


>[!MORELIKETHIS]
>
>* [手動のDeal ID設定](deal-id-settings.md)
>* [プログラム保証契約の設定](programmatic-guaranteed-set-up.md)
>* [プログラムで保証された取引の広告を送信する [!DNL FreeWheel]](freewheel-submit.md)
>* [プログラム保証取引について](programmatic-guaranteed-about.md)

