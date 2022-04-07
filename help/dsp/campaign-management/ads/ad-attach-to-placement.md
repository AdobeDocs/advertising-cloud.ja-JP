---
title: プレースメントへの広告の添付
description: プレースメントに広告を添付する方法を説明します。
feature: DSP Ads
exl-id: 4d85b89b-217f-46eb-a8b2-27da4c220be7
source-git-commit: af5e9449802c98b92a3d0107a00c47fe2b2031ca
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# プレースメントへの広告の添付

## から新しい広告を添付 [!UICONTROL Ads] 表示

1. メインメニューで、 **[!UICONTROL Campaigns]**.
1. キャンペーンの名前をクリックします。
1. サブメニューで、 **[!UICONTROL Ads]**.
1. 広告名の横にある  **... >[!UICONTROL Add to Placements]**.
1. 広告を配置画面で、次のいずれかの操作をおこないます。
   * 広告の新しいプレースメントを作成するには：
      1. クリック **[!UICONTROL Create New Placement]**.
      1. 次を入力します。 [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)をクリックし、 **[!UICONTROL Create Placement]**.
   * 広告を 1 つ以上の既存のプレースメントに追加するには：
      1. クリック **[!UICONTROL Select a Placement].**
      1. 次のいずれかの操作を行います。
         * 一度に 1 つの広告を追加するには：
            1. 広告名の横にある **[!UICONTROL Select].**
            1. （オプション）添付する追加の広告ごとに、 **[!UICONTROL Attach to Other Placement]**. 広告名の横にある **[!UICONTROL Select].**
         * 一度に最大 20 個のプレースメントに広告を添付するには：
            1. 「一括選択」の横にあるチェッ**ックボックスを選択します。
            1. 広告を添付する各配置の横にあるチェックボックスを選択します。
            1. クリック **[!UICONTROL Attach]**.
      1. 「完了とレビュー」タブで、次のいずれかを選択します。
         * 広告ビューに戻るには、 **[!UICONTROL I'm done for now]**.
         * 広告を別のプレースメントに添付するには、 **[!UICONTROL Attach To Other Placement]**.

## 新しい広告または既存の広告を [!UICONTROL Placements] 表示

1. メインメニューで、 **[!UICONTROL Campaigns]**.
1. キャンペーンの名前をクリックします。
1. サブメニューで、 **[!UICONTROL Placements]**.
1. 配置名の横にある  **... > [!UICONTROL Attach Ads].**
1. 内 [!UICONTROL Add Ad to Placement] 画面で、次のいずれかの操作を行います。
   * 新しい広告を作成するには：
      1. クリック **[!UICONTROL Create a New Ad]**.
      1. 次の広告設定を入力 [オーディオ広告](ad-settings-audio.md), [接続された TV](ad-settings-connected-tv.md), [広告の表示](ad-settings-display.md), [モバイル広告](ad-settings-mobile.md), [ネイティブ広告](ad-settings-native.md)または [プリロール広告](ad-settings-pre-roll.md).
      1. クリック **[!UICONTROL Save & Submit for Review]**.

         この [広告レビュー](ad-about.md) 新しい広告の場合は 24 ～ 48 時間がかかり、機密カテゴリのチェック、URL 機能のクリック、プレビューレンダリングが含まれます。 この [!UICONTROL Status] 列は、DSPが広告を承認したかどうかを示します。 壊れた広告のステータスが 24 ～ 48 時間以上保留になる場合があるので、却下される前にエラーを修正する時間があります。

         >[!NOTE]
         >
         >広告は、DSPと SSP の両方がクリエイティブを承認した場合にのみ提供されます。 各 SSP には独自の承認要件とプロセスがあります。
   * 既存の広告を選択するには：
      1. クリック **[!UICONTROL Select an Ad].**
      1. 広告を指定します。
         * 一度に 1 つの広告を追加するには：
            1. 広告名の横にある **[!UICONTROL Select].**
            1. （オプション）添付する追加の広告ごとに、 **[!UICONTROL Add Another Ad]**. 広告名の横にある **[!UICONTROL Select].**
         * 一度に最大 20 個の広告を追加するには：
            1. の横にあるチェックボックスを選択します。 **[!UICONTROL Bulk Select]**.&quot;
            1. 追加する各広告の横にあるチェックボックスを選択します。
            1. クリック **[!UICONTROL Attach]**.
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
      1. クリック **[!UICONTROL I'm done for now]**.


>[!MORELIKETHIS]
>
>* [広告管理について](ad-about.md)
>* [単一の広告の作成](ad-create.md)
>* [複数のサードパーティ広告の作成](ad-create-multiple.md)
>* [広告の編集](ad-edit.md)
>* [広告に関連付けられた配置のリスト](ad-list-placements.md)
>* [プレースメントの広告スケジュールの編集](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)

