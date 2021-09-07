---
title: 接続されたテレビ広告の設定
description: 接続されているテレビ広告で使用可能な広告設定の説明を参照してください。
feature: Ads
exl-id: 4daae9e4-27eb-4496-9186-f33aebd8daae
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# 接続されたテレビ広告の設定

## [!UICONTROL Upload or Select Creative]

*新しい広告のみ*

**[!UICONTROL Upload Audio]:** 生のアセットをDSPにアップロードします。これを選択したら、次の操作を行います。

1. **[!UICONTROL Choose File]**&#x200B;をクリックし、デバイスまたはネットワーク上でファイルを探します。
1. [!UICONTROL Ads]ビューとレポートで使用するファイルのタイトルを入力します。
1. クリック **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** アカウント内で、以前にアップロードしたクリエイティブを正しい形式で選択します。

**[!UICONTROL Advanced: VAST Tag URL]:** （一部の広告タイプ）クリエイティブアセットとトラッキングピクセルを含むサードパーティのVASTタグを入力するには：

1. ![**[!UICONTROL Advanced: VAST Tag URL]**&#x200B;の横にある矢印](/help/dsp/assets/compressed.png)をクリックします。
1. **[!UICONTROL URL]**&#x200B;フィールドに、VASTタグのURLを入力します。
1. 広告ビューとレポートで使用するファイルの&#x200B;**[!UICONTROL Title]**&#x200B;を入力します。

>[!TIP]
>
> VASTタグの有効性を確認するには、VASTタグをブラウザーに貼り付けて&#x200B;**[!UICONTROL Enter]**&#x200B;キーを押します。 タグが有効な場合は、上部に`<VAST>`を含むXMLファイルが表示されます。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。アセットのタイトルはデフォルトで使用されますが、名前は変更できます。

>[!TIP]
>
> 配置、[!UICONTROL Ads]ビューおよびレポートで広告を添付する際に見つけやすい名前を使用します。 例えば、単位タイプといくつかの主要属性（休日の製品プレビューなど）を説明します。30秒CTV&quot;)。

**[!UICONTROL Width | Ad Unit Width]:** 広告ユニット全体の幅。このオプションは、選択した広告ユニットのタイプに応じてロックされます。

**[!UICONTROL Height | Ad Unit Height]:** 広告ユニット全体の高さ。このオプションは、選択した広告ユニットのタイプに応じてロックされます。

**[!UICONTROL Player X]:** 広告ユニットのX座標。デフォルト設定のままにします。

**[!UICONTROL Player Y]:** 広告ユニットのY座標。デフォルト設定のままにします。

**[!UICONTROL Player Width]:** 広告ユニット全体の幅。このオプションは、選択した広告ユニットのタイプに応じてロックされます。

これは&#x200B;**[!UICONTROL Width]**&#x200B;フィールドと同じです。

**[!UICONTROL Player Height]:** 広告ユニット全体の高さ。このオプションは、選択した広告ユニットのタイプに応じてロックされます。

これは&#x200B;**[!UICONTROL Height]**&#x200B;フィールドと同じです。

**[!UICONTROL Show Controls]:** 広告のビデオコントロールを含める場所： *[!UICONTROL Under]*、 *[!UICONTROL Over]*、 *[!UICONTROL Bottom]*&#x200B;または(デ *[!UICONTROL None]* フォルト)。

**[!UICONTROL Preserve Aspect Ratio]:** ビデオの幅と高さの比率を維持するか(*[!UICONTROL Yes]*)、ビデオを拡大して使用可能な領域を埋めるか(*[!UICONTROL No]*)。

**[!UICONTROL Click URL]:** (Adobe提供の広告のみ)ビューアが広告をクリックしたときに表示されるURL。

**[!UICONTROL Final Click URL]:** (Adobe提供の広告のみ；読み取り専用)必要な [!UICONTROL Click URL] Advertising Cloud DSPトラッキングマ [クロが挿](/help/dsp/campaign-management/macros.md) 入されている（該当する場合）。

**[!UICONTROL VAST Tag]:** (VASTタグのみを使用する広告。読み取り専用)広告ソースとして入力したサードパーティのVASTタグ。

**[!UICONTROL Final VAST Tag]:** (VASTタグのみを使用する広告。読み取り専用)必要な [Advertising Cloud DSPトラッキングマクロを挿入した、広告ソースとして入力したサードパーティのVAST](/help/dsp/campaign-management/macros.md) タグ（該当する場合）。

**[!UICONTROL Clock Number]**:(英国でのみ使用。（権限を持つユーザーのみが使用可能）正しい広告が確実にブロードキャストされるようにするために使用される一意の識別子。この設定を適用できない場合は、空白のままにします。

### [!UICONTROL Pixel]

配置の既存のイベントトラッキングピクセルは、すべて自動的に添付されます。 必要に応じて、既存のピクセルを分離し、トラッキングのニーズに応じて新しいピクセルを作成できます。

作成または編集する各ピクセルには、次の設定が適用されます。

**[!UICONTROL Integration Event]:** 実行するピクセルをトリガー化するイベント。この広告タイプでは、*[!UICONTROL Impression]*&#x200B;または&#x200B;*[!UICONTROL Click-through]*&#x200B;で実行されるピクセルを使用します。

**[!UICONTROL Pixel Type]:** ピクセルが(1 x  *[!UICONTROL IMG URL]* 1ピクセルの画像ファイル)、またはの *[!UICONTROL HTML]*&#x200B;どちらであるか。 *[!UICONTROL JavaScript URL]*

**[!UICONTROL Pixel URL or Code]:** 指定したピクセルタイプに適した形式のピクセル画像のURL。

**[!UICONTROL Pixel Name]:** ピクセル名。ピクセルを簡単に識別できる名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー： *[!UICONTROL None]*、 *[!UICONTROL Nielsen]*&#x200B;または *[!UICONTROL Comscore]*。

>[!MORELIKETHIS]
>
>* [広告管理について](ad-about.md)
>* [広告の作成](ad-create.md)
>* [広告に関連付けられている配置のリスト](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [使用可能な広告タイプ](ad-types.md)
>* [広告の仕様](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSPマクロ](/help/dsp/campaign-management/macros.md)

