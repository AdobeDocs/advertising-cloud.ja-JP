---
title: プレースメントへの広告の添付
description: プレースメントに広告を添付する方法を説明します。
feature: Ads
exl-id: 4d85b89b-217f-46eb-a8b2-27da4c220be7
source-git-commit: fcd55f882f56c9eacd82d554d30364400b99555c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# プレースメントへの広告の添付

## [!UICONTROL Ads]ビューからの新しい広告の付加

1. メインメニューで&#x200B;**[!UICONTROL Campaigns]**&#x200B;をクリックします。
1. キャンペーンの名前をクリックします。
1. サブメニューで&#x200B;**[!UICONTROL Ads]**&#x200B;をクリックします。
1. 広告名の横にある&#x200B;**... >[!UICONTROL Add to Placements]**&#x200B;をクリックします。
1. 広告を配置画面で、次のいずれかの操作を行います。
   * 広告の新しいプレースメントを作成するには：
      1. クリック **[!UICONTROL Create New Placement]**.
      1. [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)を入力し、**[!UICONTROL Create Placement]**&#x200B;をクリックします。
   * 1つ以上の既存の配置に広告を追加するには：
      1. クリック **[!UICONTROL Select a Placement].**
      1. 次のいずれかの操作を行います。
         * 一度に1つの広告を追加するには：
            1. 広告名の横にある「**[!UICONTROL Select].**」をクリックします。
            1. （オプション）追加する広告ごとに、「**[!UICONTROL Attach to Other Placement]**」をクリックします。 広告名の横にある「**[!UICONTROL Select].**」をクリックします。
         * 一度に最大20個の配置に広告をアタッチするには：
            1. 「一括選択」の横にあるチェックボ**ックスを選択します。」
            1. 広告を添付する各プレースメントの横にあるチェックボックスを選択します。
            1. クリック **[!UICONTROL Attach]**.
      1. 「完了とレビュー」タブで、次のいずれかを選択します。
         * 広告ビューに戻るには、**[!UICONTROL I'm done for now]**&#x200B;をクリックします。
         * 広告を別の配置に添付するには、**[!UICONTROL Attach To Other Placement]**&#x200B;をクリックします。

## [!UICONTROL Placements]ビューからの新しい広告または既存の広告の付加

1. メインメニューで&#x200B;**[!UICONTROL Campaigns]**&#x200B;をクリックします。
1. キャンペーンの名前をクリックします。
1. サブメニューで&#x200B;**[!UICONTROL Placements]**&#x200B;をクリックします。
1. 配置名の横にある&#x200B;**... > [!UICONTROL Attach Ads].**&#x200B;をクリックします。
1. [!UICONTROL Add Ad to Placement]画面で、次のいずれかの操作を行います。
   * 新しい広告を作成するには：
      1. クリック **[!UICONTROL Create a New Ad]**.
      1. [オーディオ広告](ad-settings-audio.md)、[接続されたTV](ad-settings-connected-tv.md)、[ディスプレイ広告](ad-settings-display.md)、[モバイル広告](ad-settings-mobile.md)、[ネイティブ広告](ad-settings-native.md)、または[プリロール広告](ad-settings-pre-roll.md)の広告設定を入力します。
      1. クリック **[!UICONTROL Save & Submit for Review]**.

         新しい広告の[広告レビュー](ad-about.md)には24～48時間かかり、機密性の高いカテゴリのチェック、URLの機能のクリック、レンダリングのプレビューが含まれます。 [!UICONTROL Status]列は、DSPが広告を承認したかどうかを示します。 壊れた広告のステータスが24 ～ 48時間を超える場合があるので、却下される前にエラーを修正する時間があります。

         >[!NOTE]
         >
         >広告は、DSPとSSPの両方がクリエイティブを承認した場合にのみ表示されます。 各SSPには、独自の承認要件とプロセスがあります。
   * 既存の広告を選択するには：
      1. クリック **[!UICONTROL Select an Ad].**
      1. 広告を指定します。
         * 一度に1つの広告を追加するには：
            1. 広告名の横にある「**[!UICONTROL Select].**」をクリックします。
            1. （オプション）追加する広告ごとに、「**[!UICONTROL Add Another Ad]**」をクリックします。 広告名の横にある「**[!UICONTROL Select].**」をクリックします。
         * 一度に最大20個の広告を追加するには：
            1. 「**[!UICONTROL Bulk Select]**」の横にあるチェックボックスをオンにします。
            1. 追加する各広告の横にあるチェックボックスを選択します。
            1. クリック **[!UICONTROL Attach]**.
      1. （オプション）配置内の特定の広告に対して、デフォルトのフライト期間と広告のローテーションを上書きするには：
         1. クリック **[!UICONTROL Custom Schedule Ads]**.
         1. 次のいずれかの操作を行います。
            * フライトを追加するには、**[!UICONTROL Add Flight]**&#x200B;をクリックし、開始日と終了日を指定します。
            * 既存のフライトを広告に追加するには、フライト列の広告行の&#x200B;**[!UICONTROL +]**&#x200B;をクリックします。
            * 広告から既存のフライトを削除するには、フライト列の広告行の&#x200B;**[!UICONTROL x]**&#x200B;をクリックします。
            * （複数の広告が同じフライトを持つ場合）広告を均等に回転させるには、フライト情報の&#x200B;**[!UICONTROL Even Rotation]**をクリックし、各広告を回転させる相対的な重みをパーセンテージで入力します。
重みの合計は100にする必要があります。
         1. 右上の「**[!UICONTROL Continue]**」をクリックします。
         1. フライトの詳細を確認し、[**[!UICONTROL Save & Finish]**]をクリックします。
      1. クリック **[!UICONTROL I'm done for now]**.


>[!MORELIKETHIS]
>
>* [広告管理について](ad-about.md)
>* [広告の作成](ad-create.md)
>* [広告の編集](ad-edit.md)
>* [広告に関連付けられている配置のリスト](ad-list-placements.md)
>* [プレースメントの広告スケジュールの編集](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)

