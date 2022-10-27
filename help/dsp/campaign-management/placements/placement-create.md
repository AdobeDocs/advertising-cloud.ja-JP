---
title: 配置の作成
description: プレースメントの作成方法を説明します。
feature: DSP Placements
exl-id: 4e37b571-9af4-4897-bff2-035a5f2600a5
source-git-commit: 5ed402a7c83072a7af6a06757050486c6d7d7080
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 1%

---

# 配置の作成

>[!TIP]
>
>特定のキャンペーンの目標またはレポートのニーズに基づいて、プレースメントを作成します。

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. 配置を含めるキャンペーンの名前をクリックします。

1. データテーブルの上にある **[!UICONTROL Create]**. 内 [!UICONTROL Placement Types] メニューの「 」セクションで、配置タイプをクリックします。

   配置タイプは、配置に含めることができる広告タイプを決定します。

1. 次を入力します。 [配置設定](placement-settings.md):

   1. 次を指定： [!UICONTROL Basics] 設定。

   1. 内 [!UICONTROL Goals] セクションで、 [!UICONTROL Gross Budget] さらに、必要に応じて、追加の配置目標を指定します。

      一部のフィールドには、上書きできるデフォルト値が設定されています。

      配置が割り当てられるパッケージにパッケージレベルのペーシングがある場合、目標とペーシングの設定はパッケージ設定を反映します。

   1. （オプション） [!UICONTROL Geo-Targeting] 「 」セクションで、含めるまたは除外する場所を絞り込みます。

      特定の場所が特定されない場合は、すべての場所がターゲットになります。

      >[!NOTE]
      >
      >Roku プレースメントでは、市区町村と DMA の場所は使用できません。

   1. 内 [!UICONTROL Inventory Targeting] 「 」セクションで、含めるまたは除外する在庫ソースを絞り込みます。

      ほとんどの配置タイプでは、すべての在庫タイプと各タイプのすべてのソースがデフォルトで含まれます。 の場合 [!DNL Roku] 配置を使用する場合は、在庫のタイプとソースを指定する必要があります。

   1. （オプション） [!UICONTROL Site Targeting] 「 」セクションで、ターゲットにするサイトを絞り込み、除外するサイトを指定します。

   1. （オプション） [!UICONTROL Audience Targeting] セクション：

      1. オーディエンスを絞り込みます。 これには、配置内でターゲットにするオーディエンスセグメントの選択が含まれます。

         の場合 [!DNL] Roku プレースメントでは、 [と一致する一意のオーディエンスをDSP [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) 一致する 1 つ以上のオーディエンスセグメントを [!DNL Roku] （オプトイン）決定論的データセット。
   1. （ユーザーレベルのクロスデバイスターゲティングを使用するキャンペーンの場合）（オプション）配置が 1 つ以上の特定のオーディエンスをターゲットにする場合、配置のユーザーベースのクロスデバイスターゲティングを有効にします。

      ユーザーベースのクロスデバイスターゲティングは、次の方法で提供されます。 [!DNL LiveRamp] 米国のデータのみを使用する。 このサービスは、0.35 CPM のすべての広告主が、 [!DNL LiveRamp] デバイスグラフ（ターゲットとなるオーディエンスセグメント内に見つからないデバイスの場合）。

   1. （オプション） [!DNL Brand Safety and Media Targeting] 「 」セクションで、配置にブランドの安全性制限を適用します。

   1. （オプション） [!DNL Tracking] 「 」セクションで、配置する広告のサードパーティイベントピクセルまたはコンバージョンピクセルを入力します。

      >[!NOTE]
      >
      >([!DNL Roku] プレースメント ) によって承認されたサードパーティのピクセルベンダー [!DNL Roku] 含める [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]、および [!DNL Research Now].


1. クリック **[!UICONTROL Create Placement]**.

1. （オプション）プレースメントに広告を付加する：

   1. クリック **[!UICONTROL Attach an ad]**.

   1. 次のいずれかの操作を行います。
   * 新しい広告を作成するには：

      1. クリック **[!UICONTROL Create a New Ad].**

      1. 以下の広告設定を指定します。 [オーディオ広告](/help/dsp/campaign-management/ads/ad-settings-audio.md), [接続された TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [広告の表示](/help/dsp/campaign-management/ads/ad-settings-display.md), [モバイル広告](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [ネイティブ広告](/help/dsp/campaign-management/ads/ad-settings-native.md)または [プリロール広告](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md).

      1. クリック **[!UICONTROL Save & Submit for Review]**.

      1. （オプション）プレースメントに作成する追加の広告ごとに、 **[!UICONTROL Attach Another Ad]**&#x200B;をクリックし、手順 1 ～ 3 を繰り返します。

      1. 既存の広告を添付しない場合は、 **[!UICONTROL I'm done for now]**.
   * キャンペーンに既存の広告を添付するには：

      1. クリック **[!UICONTROL Select an Ad]**.
      1. 次のいずれかの操作を行います。
         * 一度に 1 つの広告を追加するには：
            1. 広告名の横にある **[!UICONTROL Select].**
            1. （オプション）添付する追加の広告ごとに、 **[!UICONTROL Attach Another Ad]**&#x200B;をクリックし、この処理を繰り返します。
         * 一度に最大 20 個の広告を追加するには：
            1. 広告リストの上にあるチェックボックスを選択します。
            1. 追加する各広告の横にあるチェックボックスを選択します。
            1. クリック **[!UICONTROL Attach]**.
            1. 広告名の横にある **[!UICONTROL Select]**.
      1. （オプション）プレースメント内の特定の広告に対して、デフォルトのフライト期間と広告のローテーションを上書きするには、次の手順を実行します。
         1. クリック **[!UICONTROL Custom Schedule Ads]**.

         1. 次のいずれかの操作を行います。

            * フライトを追加するには、 **[!UICONTROL Add Flight]**&#x200B;をクリックし、開始日と終了日を指定します。

            * 広告に既存のフライトを追加するには、 **[!UICONTROL +]** （「flight」列の広告行）

            * 広告から既存のフライトを削除するには、 **[!UICONTROL x]** （「flight」列の広告行）

            * （複数の広告が同じフライトを持つ場合）広告を不均等に回転させるには、 **[!UICONTROL Even Rotation]** フライト情報を入力し、各広告を回転させる相対的な重みをパーセンテージで入力します。

               重みの合計は 100 にする必要があります。
         1. 右上で、 **[!UICONTROL Continue]**.

         1. フライトの詳細を確認し、 **[!UICONTROL Save & Finish]**.




>[!MORELIKETHIS]
>
>* [配置管理について](placement-about.md)
>* [配置の編集](placement-edit.md)
>* [プレースメントの広告スケジュールの編集](placement-edit-ad-schedule.md)
>* [配置の一時停止またはアクティブ化](placement-pause-activate.md)
>* [配置の変更ログの表示](placement-change-log.md)
>* [配置設定](placement-settings.md)
>* [キーボードショートカット](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[パフォーマンスのトラブルシューティング](/help/dsp/optimization/troubleshooting-performance.md)
>* [ビデオ：標準の表示配置を作成する方法](https://video.tv.adobe.com/v/340454)

