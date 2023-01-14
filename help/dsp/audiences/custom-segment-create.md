---
title: カスタムセグメントの作成と実装
description: Web ページを訪問した広告やユーザーにさらされるユーザーを追跡するカスタムセグメントを作成および実装する方法について説明します。
feature: DSP Segments
exl-id: 691903e2-773e-4205-837e-822f435f57a7
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# カスタムセグメントの作成と実装

カスタムDSPセグメントを作成して実装することで、独自のファーストパーティオーディエンスデータを収集できます。 セグメントを使用すると、a) デスクトップ、モバイル、CTV デバイスから広告を受けるユーザー、および b) 特定の Web ページを訪問するユーザーを追跡できます。 後で、セグメント内のユーザーを追加の広告で再ターゲット化したり、セグメント内のユーザーが追加の広告を受け取らないようにしたりできます。

>[!NOTE]
>
>カリフォルニア州消費者プライバシー法 (CCPA) に従って、Web サイト上の消費者オプトアウトオブセールスリクエストからのユーザー ID を追跡するには、 [CCPA オプトアウトオブセールセグメント](ccpa-opt-out-segment-create.md).

1. セグメントの作成：

   1. メインメニューで、 **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. データテーブルの上にある **[!UICONTROL Create]**.

   1. 一意の **[!UICONTROL Segment Name]**.

   1. の **[!UICONTROL Segment Type]**&#x200B;を選択します。 *[!UICONTROL Custom]*.

   1. 次を入力します。 **[!UICONTROL Segment Window]**：ユーザーの Cookie がセグメントに残る日数です。

      デフォルトの期間は 45 日です。 1 ～ 365 の値を入力します。

   1. クリック **[!UICONTROL Save]**.

1. 必要に応じて、タグをコピーして実装し、セグメントを追跡します。

   1. 戻る **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   2. セグメント行の上にカーソルを置き、 **[!UICONTROL Get Pixel]**.

      * Web ページのデスクトップ訪問者とモバイル訪問者を追跡するには：

         1. ページビュートラッキングタグ (「[!UICONTROL Desktop or mobile websites].&quot;

         1. タグを、導入用の広告主または Web サイトの連絡先に提供します。

            広告主の IT 部門やその他のグループは、タグの導入をスケジュールしたり、通知を受けたりする必要がある場合があります。
      * デスクトップ、モバイルまたは CTV デバイスで広告ユニットに公開されたユーザーを追跡するには：

         1. インプレッショントラッキングタグ (「[!UICONTROL Desktop or mobile ads].&quot;


1. タグを [!UICONTROL Pixel] タブをクリックします。 [!UICONTROL Event Pixels] セクション [[!UICONTROL Tracking] 関連する各配置の設定](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

トラッキングタグを実装すると、そのセグメントをオーディエンスのターゲットまたは除外で任意の配置に使用できます。

>[!TIP]
>
>ユーザーが追跡されるたびに、セグメントのサイズを追跡します。

>[!MORELIKETHIS]
>
>* [Audience Management について](audience-about.md)
>* [セグメント情報の編集](segment-edit.md)
>* [セグメントの削除](segment-delete.md)
>* [セグメントの表示追跡ピクセル](segment-view-pixels.md)
>* [セグメントの共有または共有の停止](segment-share.md)
>* [の作成と実装 [!UICONTROL CCPA Opt-Out-of-Sale] セグメント](ccpa-opt-out-segment-create.md)
>* [再利用可能なオーディエンスを作成](reusable-audience-create.md)
>* [利用可能なサードパーティデータプロバイダー](third-party-data-providers.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

