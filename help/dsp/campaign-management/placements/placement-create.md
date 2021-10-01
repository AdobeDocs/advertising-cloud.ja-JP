---
title: プレースメントの作成
description: プレースメントの作成方法を説明します。
feature: DSP Placements
exl-id: 4e37b571-9af4-4897-bff2-035a5f2600a5
source-git-commit: 608774723f865c22bfdd5c911ac818600a495114
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 1%

---

# プレースメントの作成

>[!TIP]
>
>特定のキャンペーンの目標またはレポートのニーズに基づいて、プレースメントを作成します。

1. メインメニューで **[!UICONTROL Campaigns]** をクリックします。

1. 配置を含めるキャンペーンの名前をクリックします。

1. データテーブルの上で **[!UICONTROL Create]** をクリックします。 メニューの [!UICONTROL Placement Types] セクションで、配置タイプをクリックします。

   配置タイプは、配置に含めることができる広告のタイプを決定します。

1. [ 配置設定 ](placement-settings.md) を入力します。

   1. [!UICONTROL Basics] 設定を指定します。

   1. [!UICONTROL Goals] セクションで、[!UICONTROL Gross Budget] を指定し、必要に応じて追加の配置目標を指定します。

      一部のフィールドには、上書きできるデフォルト値が設定されています。

      配置が割り当てられるパッケージにパッケージレベルのペーシングがある場合、目標とペーシング設定はパッケージ設定を反映します。

   1. （オプション） [!UICONTROL Geo-Targeting] セクションで、含めるまたは除外する場所を絞り込みます。

      特定の場所を特定しない場合は、すべての場所がターゲットになります。

      >[!NOTE]
      >
      >市区町村と DMA の場所は、Roku プレースメントでは使用できません。

   1. [!UICONTROL Inventory Targeting] セクションで、在庫ソースを絞り込んで、含めるか除外するかを指定します。

      ほとんどの配置タイプでは、すべての在庫タイプと各タイプのすべてのソースがデフォルトで含まれます。 [!DNL Roku] 配置の場合、在庫のタイプとソースを指定する必要があります。

   1. （オプション） [!UICONTROL Site Targeting] セクションで、ターゲットにするサイトを絞り込み、除外するサイトを指定します。

   1. （オプション） [!UICONTROL Audience Targeting] セクションで、次の操作を行います。

      1. 観客を絞り込む。 これには、配置内でターゲットとするオーディエンスセグメントの選択も含まれます。

         [!DNL] Roku 配置の場合、[!DNL Roku]（オプトイン）決定論的データセットと一致するオーディエンスセグメントを 1 つ以上含めることで、 [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) と一致する [DSPの一意のオーディエンスを活用できます。
   1. （ユーザーレベルのクロスデバイスターゲティングを含むキャンペーンの場合）。（オプション）プレースメントのターゲットが 1 つ以上の特定のオーディエンスの場合、そのプレースメントに対してユーザーベースのクロスデバイスターゲティングを有効にします。

      ユーザーベースのクロスデバイスターゲティングは、[!DNL LiveRamp] が米国のデータのみを使用して提供します。 このサービスは、 [!DNL LiveRamp] デバイスグラフ（ターゲットのオーディエンスセグメント内に見つからないデバイス）を使用して配信されるインプレッションについて、0.35 CPM ですべての広告主が利用できます。

   1. （オプション） [!DNL Brand Safety and Media Targeting] セクションで、配置にブランドの安全性制限を適用します。

   1. （オプション） [!DNL Tracking] セクションで、配置する広告のサードパーティイベントピクセルまたはコンバージョンピクセルを入力します。

      >[!NOTE]
      >
      >（[!DNL Roku] 配置） [!DNL Roku] が承認したサードパーティのピクセルベンダーには、[!DNL Acxiom]、[!DNL comScore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL NinthDecimal]、[!DNL Nielsen Catalina Solutions] が含まれます 13/>、[!DNL Placed]、[!DNL Polk]、[!DNL Research Now]。[!DNL Oracle]


1. クリック **[!UICONTROL Create Placement]**.

1. （オプション）配置に広告を付加します。

   1. クリック **[!UICONTROL Attach an ad]**.

   1. 次のいずれかの操作を行います。
   * 新しい広告を作成するには：

      1. クリック **[!UICONTROL Create a New Ad].**

      1. [ オーディオ広告 ](/help/dsp/campaign-management/ads/ad-settings-audio.md)、[ 接続された TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)、[ ディスプレイ広告 ](/help/dsp/campaign-management/ads/ad-settings-display.md)、[ モバイル広告 ](/help/dsp/campaign-management/ads/ad-settings-mobile.md)、[ ネイティブ広告 ](/help/dsp/campaign-management/ads/ad-settings-native.md) または [ プリロール広告 ](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md) の広告設定を指定します。

      1. クリック **[!UICONTROL Save & Submit for Review]**.

      1. （オプション）配置用に作成する追加の広告ごとに、**[!UICONTROL Attach Another Ad]** をクリックし、手順 1 ～ 3 を繰り返します。

      1. 既存の広告を添付しない場合は、**[!UICONTROL I'm done for now]** をクリックします。
   * キャンペーンに既存の広告を関連付けるには：

      1. クリック **[!UICONTROL Select an Ad]**.
      1. 次のいずれかの操作を行います。
         * 一度に 1 つの広告を追加するには：
            1. 広告名の横にある **[!UICONTROL Select].** をクリックします。
            1. （オプション）添付する追加の広告ごとに、**[!UICONTROL Attach Another Ad]** をクリックし、この手順を繰り返します。
         * 一度に 20 個までの広告を追加するには：
            1. 広告リストの上にあるチェックボックスを選択します。
            1. 追加する各広告の横にあるチェックボックスを選択します。
            1. クリック **[!UICONTROL Attach]**.
            1. 広告名の横にある「**[!UICONTROL Select]**」をクリックします。
      1. （オプション）配置内の特定の広告に対して、デフォルトのフライト期間と広告のローテーションを上書きするには：
         1. クリック **[!UICONTROL Custom Schedule Ads]**.

         1. 次のいずれかの操作を行います。

            * フライトを追加するには、**[!UICONTROL Add Flight]** をクリックし、開始日と終了日を指定します。

            * 既存のフライトを広告に追加するには、フライト列の広告行で **[!UICONTROL +]** をクリックします。

            * 広告から既存のフライトを削除するには、フライト列の広告行で **[!UICONTROL x]** をクリックします。

            * （複数の広告が同じフライトを持つ場合）広告を均等に回転させるには、フライト情報の **[!UICONTROL Even Rotation]** をクリックし、各広告を回転させる相対的な重みをパーセントで入力します。

               重みの合計は 100 にする必要があります。
         1. 右上の **[!UICONTROL Continue]** をクリックします。

         1. フライトの詳細を確認し、[**[!UICONTROL Save & Finish]**] をクリックします。




>[!MORELIKETHIS]
>
>* [配置管理について](placement-about.md)
>* [プレースメントの編集](placement-edit.md)
>* [プレースメントの広告スケジュールの編集](placement-edit-ad-schedule.md)
>* [配置の一時停止またはアクティブ化](placement-pause-activate.md)
>* [配置設定](placement-settings.md)
>* [キーボードショートカット](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[ パフォーマンスのトラブルシューティング ](/help/dsp/optimization/troubleshooting-performance.md)

