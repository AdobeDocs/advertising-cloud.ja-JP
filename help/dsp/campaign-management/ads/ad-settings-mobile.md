---
title: モバイル広告設定
description: モバイル広告で使用可能な広告設定の説明を参照してください。
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# モバイル広告設定

## [!UICONTROL Insert Ad Tag]

*新しいモバイルビデオ広告の形式のみ*

**[!UICONTROL URL]** または **[!UICONTROL Ad Tag]**:クリエイティブアセットと追跡ピクセルを含むサードパーティの VAST 広告タグまたは広告タグ

**[!UICONTROL Ad Title]** または **[!UICONTROL Title]**:内で使用される広告の名前 [!UICONTROL Ads] 表示とレポート。

>[!TIP]
>
> VAST タグの有効性を確認するには、タグをブラウザーに貼り付け、 **[!UICONTROL Enter]** キー。 タグが有効な場合は、 `<VAST>` 一番上の近くに

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]:モバイルディスプレイ広告

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前は変更できます。

>[!TIP]
>
> 広告をプレースメント、広告ビューおよびレポートに付ける際に見つけやすい名前を使用します。 たとえば、ユニット・タイプといくつかの主要属性（Holiday Product Preview など）を説明します。300x250 Gamer&quot;) で表示されます。

**\[ 広告ソース\]**:（読み取り専用） *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** サードパーティのクリエイティブアセットの URL。 任意 [timestamp] および [[timestamp]] パラメーターは実際の値に置き換えられます。

**[!UICONTROL Final Display Code]:** サードパーティのクリエイティブアセットの URL（必要なもの） [Advertising DSPトラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入されています（該当する場合）。

### [!UICONTROL Basic]:ビデオ広告

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前は変更できます。

>[!TIP]
>
> 広告をプレースメント、広告ビューおよびレポートに付ける際に見つけやすい名前を使用します。 たとえば、ユニット・タイプといくつかの主要属性（Holiday Product Preview など）を説明します。30 秒 Phone Preroll&quot;)。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** 広告ユニット全体の幅。 このオプションは、選択した広告ユニットのタイプに応じてロックされる場合があります。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** 広告ユニット全体の高さ。 このオプションは、選択した広告ユニットのタイプに応じてロックされる場合があります。

**[!UICONTROL Player X]:** 広告ユニットの X 座標。 デフォルト設定のままにします。

**[!UICONTROL Player Y]:** 広告ユニットの Y 座標。 デフォルト設定のままにします。

**[!UICONTROL Player Width]:** 広告ユニット全体の幅。 このオプションは、選択した広告ユニットのタイプに応じてロックされる場合があります。

これは、 **[!UICONTROL Width]** フィールドに入力します。

**[!UICONTROL Player Height]:** 広告ユニット全体の高さ。 このオプションは、選択した広告ユニットのタイプに応じてロックされる場合があります。

これは、 **[!UICONTROL Height]** フィールドに入力します。

**[!UICONTROL Show Controls]:** 広告のビデオコントロールを含める場所： *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*&#x200B;または *[!UICONTROL None]* （デフォルト）。

**[!UICONTROL Preserve Aspect Ratio]:** ビデオの幅と高さの比率 (*[!UICONTROL Yes]*) またはビデオを拡大して使用可能な領域を埋めます (*[!UICONTROL No]*) をクリックします。

**[!UICONTROL Close Button Delay]:** （一部の広告タイプ）閉じるボタンの表示を遅らせる秒数。

**[!UICONTROL VAST Tag]:** (VAST タグのみを使用する広告。読み取り専用 ) クリエイティブアセットとして入力したサードパーティの VAST タグ。

**[!UICONTROL Final VAST Tag]:** (VAST タグのみを使用する広告。読み取り専用 ) クリエイティブアセットとして入力したサードパーティの VAST タグ ( 必要な [Advertising DSPトラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入されています（該当する場合）。

**[!UICONTROL Wmode]:** （一部の広告タイプ）ウィンドウモード： *[!UICONTROL window]*, *[!UICONTROL transparent]*&#x200B;または *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

配置の既存のイベントトラッキングピクセルはすべて自動的に添付されます。 個々の広告に対するトラッキングのニーズに応じて、必要に応じて、既存のピクセルを分離し、新しいピクセルを作成できます。

作成または編集する各ピクセルには、次の設定が適用されます。

**[!UICONTROL Integration Event]:** 実行するピクセルをトリガーにするイベント。 この広告タイプでは、 *[!UICONTROL Impression]* または *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG URL]* （1 x 1 ピクセルの画像ファイル）、 *[!UICONTROL HTML]*&#x200B;または *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 指定した [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを簡単に識別できる名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*&#x200B;または *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

非推奨

>[!MORELIKETHIS]
>
>* [広告管理について](ad-about.md)
>* [単一の広告の作成](ad-create.md)
>* [広告に関連付けられた配置のリスト](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [広告の仕様](ad-specs.md)
>* [DSPマクロ](/help/dsp/campaign-management/macros.md)

