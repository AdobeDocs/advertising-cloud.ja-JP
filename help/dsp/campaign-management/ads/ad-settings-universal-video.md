---
title: ユニバーサルビデオ広告設定
description: ユニバーサルビデオ広告で使用可能な広告設定の説明を参照してください。
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ユニバーサルビデオ広告設定

*ベータ版機能を開く*

## [!UICONTROL Insert Ad Tag]

*新しい広告のみ*

**[!UICONTROL URL]:** VAST タグの URL。

**[!UICONTROL Title]:** ファイルのタイトル ( [!UICONTROL Ads] 表示とレポート。

>[!TIP]
>
> VAST タグの有効性を確認するには、タグをブラウザーに貼り付け、 **[!UICONTROL Enter]** キー。 タグが有効な場合は、 `<VAST>` 一番上の近くに

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前は変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を、 [!UICONTROL Ads] レポートで、およびを表示します。 たとえば、ユニット・タイプといくつかの主要属性（Holiday Product Preview など）を説明します。30 秒ユニバーサルビデオ&quot;)。

**[!UICONTROL Show Controls]:** 広告のビデオコントロールを含める場所： *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*&#x200B;または *[!UICONTROL None]* （デフォルト）。

**[!UICONTROL Preserve Aspect Ratio]:** ビデオの幅と高さの比率を維持するかどうか (*[!UICONTROL Yes]*) またはビデオを拡大して使用可能な領域を埋めます (*[!UICONTROL No]*) をクリックします。

**[!UICONTROL VAST Tag]:** (VAST タグのみを使用する広告。読み取り専用 ) 広告ソースとして入力したサードパーティの VAST タグ。

**[!UICONTROL Final VAST Tag]:** (VAST タグのみを使用する広告。読み取り専用 ) 広告ソースとして入力し、必要に応じて [Advertising DSPトラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入されています（該当する場合）。

**[!UICONTROL Wmode]:** ウィンドウモード： *[!UICONTROL window]*, *[!UICONTROL transparent]*&#x200B;または *[!UICONTROL opaque]*. この設定を適用できない場合は、空白のままにします。

**[!UICONTROL Video Format]:** 潜在的な在庫に関する広告プレーヤーの形式： *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]*&#x200B;または *[!UICONTROL VAST]*. の視認性は常に測定されます。 [!UICONTROL VPAID]ですが [!UICONTROL VPAID & VAST] には、視認性の測定を許可しない在庫が含まれています。 視認性指標がキャンペーンにとって重要な場合は、この違いを考慮します。

用途 *[!UICONTROL VAST]* VAST 形式のみを厳密に必要とする接続済みの TV や在庫をターゲットにする場合 ( 通常、Google Ad Manager、Appnexus、SpotX、Freewheel などの供給元から ) は、視認性測定を許可しません。

**[!UICONTROL Clock Number]**:( 英国でのみ使用。（権限を持つユーザーのみが使用できます）正しい広告が確実にブロードキャストされるようにするために使用される一意の識別子。 この設定を適用できない場合は、空白のままにします。

### [!UICONTROL Pixel]

配置の既存のイベントトラッキングピクセルはすべて自動的に添付されます。 個々の広告に対するトラッキングのニーズに応じて、必要に応じて、既存のピクセルを分離し、新しいピクセルを作成できます。

作成または編集する各ピクセルには、次の設定が適用されます。

**[!UICONTROL Integration Event]:** 実行するピクセルをトリガーにするイベント。 この広告タイプでは、 *[!UICONTROL Impression]* または *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG URL]* （1 x 1 ピクセルの画像ファイル）、 *[!UICONTROL HTML]*&#x200B;または *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 指定した [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを簡単に識別できる名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*&#x200B;または *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [広告管理について](ad-about.md)
>* [単一の広告の作成](ad-create.md)
>* [広告に関連付けられた配置のリスト](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [広告の仕様](ad-specs.md)
>* [DSPマクロ](/help/dsp/campaign-management/macros.md)

