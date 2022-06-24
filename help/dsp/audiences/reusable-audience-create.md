---
title: 再利用可能なオーディエンスを作成
description: オーディエンスセグメントと他の保存済みのオーディエンスで構成される再利用可能なオーディエンスを作成する方法を説明します。
feature: DSP Audiences
exl-id: 48e3dc4c-6e2d-452c-8d69-7e6211d808e0
source-git-commit: 37e5a4fbb7e2ccda77ab0afd49054ec4d1dabf76
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 再利用可能なオーディエンスを作成

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

再利用可能なオーディエンス（オーディエンスセグメントのグループ、および他の保存済みのオーディエンスのグループ）を保存および管理できます。これらは、複数の配置のターゲットまたは除外として使用できます。

1. メインメニューで、 **[!UICONTROL Audiences]>[!UICONTROL All Audiences]**.

1. データテーブルの上にある **[!UICONTROL Create]**.

1. 一意の [!UICONTROL Audience Name].

1. （オプション）次のオプションの選択を解除します。 **[!UICONTROL Share with all advertisers in my account]**.

   オーディエンスを共有すると、そのオーディエンスは、アカウント内のすべての広告主に対してターゲットまたは除外として利用できるようになります。 ただし、オーディエンスの個々のセグメントは、セグメントが共有されているユーザーのみ利用できます。 例えば、Adobe Analyticsセグメントを含むオーディエンスを、同じにマッピングされていない広告主と共有する場合、 [!DNL Analytics] アカウントを選択した場合、その広告主のそのオーディエンスではセグメントはプレビューされません。 その広告主が使用できるセグメントのみが、オーディエンスでプレビューされます。

1. クリック **[!UICONTROL Save]**.

1. オーディエンスを構築します。

   >[!NOTE]
   >
   >オーディエンスの構築に伴い、詳細な [オーディエンスサイズデータ](audience-about.md) は、右側のパネルで更新されます

   * セグメントロジックを手動で作成するには、 [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]、および [!UICONTROL Saved Audiences] タブ](audience-settings.md)、次の操作を実行します。

      * 最初のセグメントを追加するには、左のパネルでセグメントを探し、セグメント名の横にあるチェックボックスをオンにします。

      * セグメントを既存のセグメントグループに追加するには：

         1. 右側のパネルでセグメントグループをクリックします。

         1. （オプション）グループロジックを *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*&#x200B;または *[!UICONTROL Exclude All]*&#x200B;必要に応じて。

            *[!UICONTROL Exclude All]* は、最初のセグメントグループで使用できません。 除外のみを含むオーディエンスの場合は、このオーディエンスを次のように作成します。 *[!UICONTROL Include Any]* 次に、配置内で、除外されたオーディエンスメニューからそのオーディエンスを選択します。

         1. 左のパネルで新しいセグメントを見つけ、セグメント名の横にあるチェックボックスをオンにします。

            セグメントグループは、新しいセグメントで自動的に更新されます。
      * 新しいセグメントグループを追加するには：

         1. クリック **[!UICONTROL + New Group]** をクリックします。

         1. （オプション）前のグループと新しいグループの間のロジックを次に変更します。 *[!UICONTROL And]* または *[!UICONTROL Or]*&#x200B;必要に応じて。

         1. 左のパネルで新しいグループのセグメントを探し、セグメント名の横にあるチェックボックスをオンにします。

         1. （オプション）グループロジックを *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*&#x200B;または *[!UICONTROL Exclude All]*&#x200B;必要に応じて。
   * 既存のオーディエンスからセグメントロジックを使用するには：

      1. 次のいずれかの方法で、既存のオーディエンスからセグメントロジックをコピーします。

         * 「すべてのオーディエンス」表示で、オーディエンス行の上にカーソルを置き、 **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * 既存のオーディエンスの設定で、セグメントのロジックパネルの上部にある「 **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * テキストエディターで、英数字のセグメント ID と [ブール構文](audience-segment-logic-syntax.md)をクリップボードにコピーします。
      1. クリック **[!UICONTROL paste in an audience rule to begin building]**」で、既存のセグメントロジックを入力フィールドに貼り付けて、「 **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >オーディエンスに既にセグメントロジックが含まれている場合は、新しいセグメントロジックに貼り付けると、既存のロジックが上書きされます。




1. クリック **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Audience Management について](audience-about.md)
>* [オーディエンス設定](audience-settings.md)
>* [オーディエンスセグメントロジックの構文](audience-segment-logic-syntax.md)
>* [利用可能なサードパーティデータプロバイダー](third-party-data-providers.md)
>* [カスタムセグメントの作成と実装](custom-segment-create.md)
>* [の作成と実装 [!UICONTROL CCPA Opt-Out-of-Sale] セグメント](ccpa-opt-out-segment-create.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

