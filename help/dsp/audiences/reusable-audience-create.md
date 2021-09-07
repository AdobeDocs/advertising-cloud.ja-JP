---
title: 再利用可能なオーディエンスの作成
description: オーディエンスセグメントと他の保存済みオーディエンスで構成される再利用可能なオーディエンスを作成する方法を説明します。
feature: Audiences
exl-id: 48e3dc4c-6e2d-452c-8d69-7e6211d808e0
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# 再利用可能なオーディエンスの作成

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

オーディエンスセグメントのグループや、複数の配置のターゲットまたは除外として使用できる他の保存済みオーディエンスである、再利用可能なオーディエンスを保存および管理できます。

1. メインメニューで、**[!UICONTROL Audiences]>[!UICONTROL All Audiences]**&#x200B;をクリックします。

1. データテーブルの上にある&#x200B;**[!UICONTROL Create]**&#x200B;をクリックします。

1. 一意の[!UICONTROL Audience Name]を入力します。

1. （オプション）**[!UICONTROL Share with all advertisers in my account]**&#x200B;を選択解除します。

   オーディエンスを共有すると、そのオーディエンスはターゲットまたは除外としてアカウント内のすべての広告主に提供されます。 ただし、オーディエンスの個々のセグメントは、そのセグメントが共有されているユーザーにのみ使用できます。 例えば、Adobe Analyticsセグメントを含むオーディエンスを、同じ[!DNL Analytics]アカウントにマッピングされていない広告主と共有すると、そのセグメントはその広告主のオーディエンスでプレビューされません。 その広告主がプレビューできるセグメントのみがオーディエンスに表示されます。

1. クリック **[!UICONTROL Save]**.

1. オーディエンスの構築：

   >[!NOTE]
   >
   >オーディエンスを構築すると、右側のパネルで詳細な[オーディエンスサイズデータ](audience-about.md)が更新されます。

   * [[!UICONTROL Third Party Segments]、[!UICONTROL First Party Segments]、[!UICONTROL Adobe Segments]、[!UICONTROL Custom Segments]および[!UICONTROL Saved Audiences]のタブ](audience-settings.md)で使用できるセグメントを使用して、セグメントロジックを手動で作成するには、次の手順を実行します。

      * 最初のセグメントを追加するには、左側のパネルでセグメントを探し、セグメント名の横にあるチェックボックスをオンにします。

      * セグメントを既存のセグメントグループに追加するには：

         1. 右側のパネルでセグメントグループをクリックします。

         1. （オプション）必要に応じて、グループロジックを&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*、または&#x200B;*[!UICONTROL Exclude All]*&#x200B;に変更します。

            *[!UICONTROL Exclude All]* は、最初のセグメントグループでは使用できません。除外のみを含むオーディエンスの場合は、*[!UICONTROL Include Any]*&#x200B;としてこのオーディエンスを作成し、配置内で、除外されたオーディエンスメニューからそのオーディエンスを選択します。

         1. 左側のパネルで新しいセグメントを見つけ、セグメント名の横にあるチェックボックスをオンにします。

            セグメントグループは、新しいセグメントで自動的に更新されます。
      * 新しいセグメントグループを追加するには：

         1. 右側のパネルで&#x200B;**[!UICONTROL + New Group]**&#x200B;をクリックします。

         1. （オプション）必要に応じて、前のグループと新しいグループの間のロジックを&#x200B;*[!UICONTROL And]*&#x200B;または&#x200B;*[!UICONTROL Or]*&#x200B;に変更します。

         1. 左側のパネルで新しいグループのセグメントを探し、セグメント名の横にあるチェックボックスをオンにします。

         1. （オプション）必要に応じて、グループロジックを&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*、または&#x200B;*[!UICONTROL Exclude All]*&#x200B;に変更します。
   * 既存のオーディエンスのセグメントロジックを使用するには：

      1. 次のいずれかの方法で、既存のオーディエンスからセグメントロジックをコピーします。

         * すべてのオーディエンスビューで、オーディエンス行の上にカーソルを置き、**[!UICONTROL More]/[!UICONTROL Copy to Clipboard]**&#x200B;をクリックします。

         * 既存のオーディエンスの設定で、セグメントロジックパネルの上部にある&#x200B;**[!UICONTROL More]/[!UICONTROL Copy to Clipboard]**&#x200B;をクリックします。

         * テキストエディターで、英数字のセグメントIDと[ブール構文](audience-segment-logic-syntax.md)を使用してセグメントロジックを手動で作成し、クリップボードにコピーします。
      1. 「**[!UICONTROL paste in an audience rule to begin building]**」をクリックし、既存のセグメントロジックを入力フィールドに貼り付けて、「**[!UICONTROL Apply]**」をクリックします。

         >[!NOTE]
         >
         >オーディエンスに既にセグメントロジックが含まれている場合、新しいセグメントロジックに貼り付けると、既存のロジックが上書きされます。




1. クリック **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Audience Managementについて](audience-about.md)
>* [オーディエンス設定](audience-settings.md)
>* [オーディエンスセグメントロジックの構文](audience-segment-logic-syntax.md)
>* [使用可能なサードパーティデータプロバイダー](third-party-data-providers.md)
>* [カスタムセグメントの作成と実装](custom-segment-create.md)
>* [セグメントの作成と [!UICONTROL CCPA Opt-Out-of-Sale] 実装](ccpa-opt-out-segment-create.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

