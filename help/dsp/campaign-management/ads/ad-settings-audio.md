---
title: オーディオ広告設定
description: オーディオ広告で使用可能な広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# オーディオ広告設定

## [!UICONTROL Insert Ad Tag]

*新しい広告のみ*

**[!UICONTROL URL]**:VAST タグの URL。

**[!UICONTROL Title]**:ファイルの名前 ( [!UICONTROL Ads] 表示とレポート。

>[!TIP]
>
> VAST タグの有効性を確認するには、タグをブラウザーに貼り付け、 **[!UICONTROL Enter]** キー。 タグが有効な場合は、 `<VAST>` 一番上の近くに

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。 デフォルトはです。 *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前は変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を、 [!UICONTROL Ads] レポートで、およびを表示します。 たとえば、ユニット・タイプといくつかの主要属性（Holiday Product Preview など）を説明します。30 秒オーディオ&quot;)。

**[!UICONTROL Ad Duration]:** オーディオファイルの長さ。 自動的に [!UICONTROL 15] または [!UICONTROL 30]（選択した広告ユニットに応じる）

このフィールドは、アカウント権限に応じて、表示される場合と表示されない場合があります。

**[!UICONTROL VAST Tag]:** （VAST タグのみを使用する広告）サードパーティの広告ソースの URL。 VAST タグにオーディオメディアファイルのみが含まれていることを確認します。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用する広告のみ）必要な [Advertising DSPトラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入されています（該当する場合）。

**[!UICONTROL Select Rate]:** （権限を持つユーザーのみ）Adobeを通じて請求される事前にネゴシエートされた料金、またはネゴシエートした料金の 1 つで、ベンダーを通じて請求されます。 料金を追加するには、 [!DNL Adobe] アカウントチーム。

### ピクセル

配置の既存のイベントトラッキングピクセルはすべて自動的に添付されます。 個々の広告に対するトラッキングのニーズに応じて、必要に応じて、既存のピクセルを分離し、新しいピクセルを作成できます。

作成または編集する各ピクセルには、次の設定が適用されます。

**[!UICONTROL Integration Event]:** 実行するピクセルをトリガーにするイベント。 この広告タイプでは、 *[!UICONTROL Impression]* または *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG UR]L* （1 x 1 ピクセルの画像ファイル）、 *[!UICONTROL HTML]*&#x200B;または *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 指定したピクセルタイプに適した形式のピクセルイメージの URL。

**[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを簡単に識別できる名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*&#x200B;または *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [広告管理について](ad-about.md)
>* [単一の広告の作成](ad-create.md)
>* [広告に関連付けられた配置のリスト](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [広告の仕様](ad-specs.md)
>* [DSPマクロ](/help/dsp/campaign-management/macros.md)

