---
title: 再利用可能なオーディエンスを編集
description: 再利用可能なオーディエンスを編集する方法を説明します。
feature: DSP Audiences
source-git-commit: 4310a5cb01fc1969ff28143c3a7cb652118b410e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# 再利用可能なオーディエンスを編集

任意の配置や他の再利用可能なオーディエンスで使用されているオーディエンスを編集すると、変更がそれらの配置やオーディエンスに直ちに適用されます。<!-- verify -->

1. メインメニューで、 **[!UICONTROL Audiences]>[!UICONTROL All audiences]**.

1. オーディエンス行にカーソルを置き、 **[!UICONTROL Edit]**.

1. 次のいずれかの方法でオーディエンス設定を編集します。

   >[!NOTE]
   >
   >オーディエンスセグメントロジックを編集する場合、詳細は [オーディエンスサイズデータ](audience-about.md) が右側のパネルで更新されました。

   * （オプション） **[!UICONTROL Audience Name]** クリック ![編集](/help/dsp/assets/edit.png) オーディエンス名の横に一意のオーディエンス名を入力し、 **[!UICONTROL Apply]**.

   * （オプション）セグメントロジックを手動で編集するには、 [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]、および [!UICONTROL Saved Audiences] タブ](audience-settings.md)、次の操作を実行します。

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





1. クリック **[!UICONTROL Save]**.

1. 確認メッセージで、 **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [Audience Management について](audience-about.md)
>* [再利用可能なオーディエンスを作成](reusable-audience-create.md)
>* [再利用可能なオーディエンスを複製](reusable-audience-duplicate.md)
>* [再利用可能なオーディエンスに関する詳細の表示](reusable-audience-view-details.md)
>* [再利用可能なオーディエンスの共有](reusable-audience-share.md)
>* [再利用可能なオーディエンスのエクスポート](reusable-audience-export.md)
>* [再利用可能なオーディエンスのセグメントキーをクリップボードにコピーする](reusable-audience-clipboard.md)
>* [再利用可能なオーディエンスの削除](reusable-audience-delete.md)
>* [オーディエンス設定](audience-settings.md)
>* [オーディエンスセグメントロジックの構文](audience-segment-logic-syntax.md)
>* [利用可能なサードパーティデータプロバイダー](third-party-data-providers.md)

