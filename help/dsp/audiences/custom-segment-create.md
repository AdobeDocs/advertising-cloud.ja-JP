---
title: カスタムセグメントの作成と実装
description: Webページを訪問する広告やユーザーに公開されたユーザーを追跡するためのカスタムセグメントの作成および実装方法について説明します。
feature: DSP Segments
exl-id: 691903e2-773e-4205-837e-822f435f57a7
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# カスタムセグメントの作成と実装

カスタムのAdvertising Cloudセグメントを作成して実装することで、独自のファーストパーティオーディエンスデータを収集できます。 セグメントを使用して、a)デスクトップ、モバイル、CTVデバイスから広告を受けたユーザー、およびb)特定のWebページを訪問したユーザーを追跡できます。 後で、セグメント内のユーザーを追加の広告で再ターゲット化したり、セグメント内のユーザーが追加の広告を受け取るのを防ぐことができます。

>[!NOTE]
>
>Webサイト上の消費者オプトアウトオブセールのリクエストからのユーザーIDを追跡するには、カリフォルニア州消費者プライバシー法(CCPA)に従って、[CCPAオプトアウトオブセールセグメント](ccpa-opt-out-segment-create.md)を作成します。

1. セグメントの作成：

   1. メインメニューで、**[!UICONTROL Audiences]>[!UICONTROL Segments]**&#x200B;をクリックします。

   1. データテーブルの上にある&#x200B;**[!UICONTROL Create]**&#x200B;をクリックします。

   1. 一意の&#x200B;**[!UICONTROL Segment Name]**&#x200B;を入力します。

   1. [!UICONTROL Segment Type]に対して、**[!UICONTROL Custom]**&#x200B;を選択します。

   1. セグメントウィンドウを入力します。このウィンドウは、ユーザーのCookieがセグメントに残る日数です。

      デフォルトの期間は45日です。 1 ～ 365の値を入力します。

   1. クリック **[!UICONTROL Save]**.

1. 必要に応じて、タグをコピーし、セグメントを追跡します。

   1. **[!UICONTROL Audiences]>[!UICONTROL Segments]**&#x200B;に戻ります。

   2. セグメント行の上にカーソルを置き、**[!UICONTROL Get pixel]**&#x200B;をクリックします。

      * Webページへのデスクトップ訪問者とモバイル訪問者を追跡するには：

         1. ページビュートラッキングタグ（「[!UICONTROL Desktop or mobile websites]」というラベル）をコピーします。

         1. タグは、導入用に広告主またはWebサイトの連絡先に提供します。

            広告主のIT部門やその他のグループは、タグの導入をスケジュールしたり、通知を受けたりする必要がある場合があります。
      * デスクトップ、モバイルまたはCTVデバイスで広告ユニットに公開されたユーザーを追跡するには：

         1. インプレッショントラッキングタグ（「[!UICONTROL Desktop or mobile ads]」というラベルが付いたタグ）をコピーします。

         1. 任意の広告の[!UICONTROL Pixel]タブにタグを追加します。<!-- I'll add cross-reference to ad settings later. -->


トラッキングタグを実装すると、そのセグメントをオーディエンスターゲットまたは除外で任意の配置に使用できます。

>[!TIP]
>
>ユーザーが追跡されるたびに、セグメントのサイズを追跡します。

>[!MORELIKETHIS]
>
>* [Audience Managementについて](audience-about.md)
>* [セグメントの作成と [!UICONTROL CCPA Opt-Out-of-Sale] 実装](ccpa-opt-out-segment-create.md)
>* [再利用可能なオーディエンスの作成](reusable-audience-create.md)
>* [オーディエンス設定](audience-settings.md)
>* [使用可能なサードパーティデータプロバイダー](third-party-data-providers.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- I'll add x-ref to ad settings later.-->
