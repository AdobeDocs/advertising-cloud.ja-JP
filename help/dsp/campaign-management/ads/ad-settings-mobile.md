---
title: モバイル広告の設定
description: モバイル広告で使用可能な広告設定の説明を参照してください。
feature: Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 0%

---

# モバイル広告の設定

## [!UICONTROL Upload or Select Creative]

*新しいモバイルビデオ広告の形式のみ*

**[!UICONTROL Vertical video]:** (が選択されている場合は [!UICONTROL Custom Transcode] 使用不可)ビデオが縦（縦長モード）であることを示します。

**[!UICONTROL Transcode to]:** (権限に応じて、一部のユーザー。（オプション）パブリッシャーが特定のクリエイティブファイル要件を持つ場合にVASTタグに含める形式。ほとんどの発行者が受け入れる形式は、デフォルトで選択されています。

**[!UICONTROL Custom Transcode]:** （ベータ版ユーザーのみ）「垂直方向のビデオ」が選択されている場合は使用できません)ビデオでカスタムトランスコードが使用されていることを示します。このオプションを選択した場合は、最大3つのカスタムトランスコードバージョンのファイル形式、ビデオビットレート、ズームおよびサイズを指定します。

**[!UICONTROL XTrader]:** （権限に応じて一部のユーザー）ビデオで1つ以上のフィードが使用されることを示 [!DNL X_TRADER] します。

**[!UICONTROL Upload Video]:** 生のアセットをDSPにアップロードします。これを選択したら、次の操作を行います。

1. **[!UICONTROL Choose File]**&#x200B;をクリックし、デバイスまたはネットワーク上でファイルを探します。
1. [!UICONTROL Ads]ビューとレポートで使用するファイルのタイトルを入力します。
1. クリック **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Video]:** アカウント内で、以前にアップロードしたクリエイティブを正しい形式で選択します。

**[!UICONTROL Advanced: VAST Tag URL]:** （一部の広告タイプ）クリエイティブアセットとトラッキングピクセルを含むサードパーティのVASTタグを入力するには：

1. ![**[!UICONTROL Advanced: VAST Tag URL]**&#x200B;の横にある矢印](/help/dsp/assets/compressed.png)をクリックします。
1. **[!UICONTROL URL]**&#x200B;フィールドに、VASTタグのURLを入力します。
1. ファイルの&#x200B;**[!UICONTROL Title]**&#x200B;を入力します。このファイルは、[!UICONTROL Ads]ビューとレポートで使用されます。

>[!TIP]
>
> VASTタグの有効性を確認するには、VASTタグをブラウザーに貼り付けて&#x200B;**[!UICONTROL Enter]**&#x200B;キーを押します。 タグが有効な場合は、上部に`<VAST>`を含むXMLファイルが表示されます。

**[!UICONTROL Advanced: 3rd party Ad Tag]:** （一部の広告タイプ）クリエイティブアセットと追跡ピクセルを含むサードパーティの広告タグを入力するには：

1. ![**[!UICONTROL Advanced: #3rd party Ad Tag]**&#x200B;の横にある矢印](/help/dsp/assets/compressed.png)をクリックします。
1. ファイルの&#x200B;**[!UICONTROL Ad Title]**&#x200B;を入力します。このファイルは、[!UICONTROL Ads]ビューとレポートで使用されます。
1. **[!UICONTROL Ad Tag]**&#x200B;フィールドに広告タグを入力します。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]:モバイルディスプレイ広告

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。アセットのタイトルはデフォルトで使用されますが、名前は変更できます。

>[!TIP]
>
> 広告を配置、広告ビューおよびレポートに付加する際に見つけやすい名前を使用します。 例えば、単位タイプといくつかの主要属性（休日の製品プレビューなど）を説明します。300 x 250 Gamer&quot;)。

**\[広告ソース\]**:Advertising Cloud DSPが広告を提供しているか(*[!UICONTROL Adobe served]*)、サードパーティの広告サーバーを使用しているか(*[!UICONTROL 3rd party]*)。

**[!UICONTROL Creative type]:** (Adobe提供の広告のみ)アセットがアセットかアセッ *[!UICONTROL Image]* トか *[!UICONTROL HTML5]* を示す。

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:** (Adobe提供の広告のみ)クリエイティブタイプに応じて、アップロードする画像ファイルまたは圧縮されたHTML5アセット。**[!UICONTROL Browse]**&#x200B;をクリックし、デバイスまたはネットワーク上でファイルを探して、**[!UICONTROL Upload]**&#x200B;をクリックします。

**[!UICONTROL Click URL]:** (Adobe提供の広告のみ)ビューアが広告をクリックしたときに表示されるURL。

**[!UICONTROL Final Click URL]:** (Adobe提供の広告のみ；読み取り専用)必要な [Advertising Cloud DSPトラッキングマクロを挿入し](/help/dsp/campaign-management/macros.md) たクリックURL（該当する場合）。

**[!UICONTROL Display Code]:** （サードパーティ広告のみ）サードパーティのクリエイティブアセットのURL。[timestamp]および[[timestamp]]パラメーターは、実際の値に置き換えられます。

**[!UICONTROL Final Display Code]:** （サードパーティ広告のみ）サードパーティのクリエイティブアセットのURL。必要な [Advertising Cloud DSPトラッキングマ](/help/dsp/campaign-management/macros.md) クロが挿入されています（該当する場合）。

### [!UICONTROL Basic]:ビデオ広告

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。アセットのタイトルはデフォルトで使用されますが、名前は変更できます。

>[!TIP]
>
> 広告を配置、広告ビューおよびレポートに付加する際に見つけやすい名前を使用します。 例えば、単位タイプといくつかの主要属性（休日の製品プレビューなど）を説明します。30秒電話プリロール」)。

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:** 広告ユニット全体の幅。このオプションは、選択した広告ユニットのタイプに応じてロックされます。

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:** 広告ユニット全体の高さ。このオプションは、選択した広告ユニットのタイプに応じてロックされます。

**[!UICONTROL Player X]:** 広告ユニットのX座標。デフォルト設定のままにします。

**[!UICONTROL Player Y]:** 広告ユニットのY座標。デフォルト設定のままにします。

**[!UICONTROL Player Width]:** 広告ユニット全体の幅。このオプションは、選択した広告ユニットのタイプに応じてロックされます。

これは&#x200B;**[!UICONTROL Width]**&#x200B;フィールドと同じです。

**[!UICONTROL Player Height]:** 広告ユニット全体の高さ。このオプションは、選択した広告ユニットのタイプに応じてロックされます。

これは&#x200B;**[!UICONTROL Height]**&#x200B;フィールドと同じです。

**[!UICONTROL Show Controls]:** 広告のビデオコントロールを含める場所： *[!UICONTROL Under]*、 *[!UICONTROL Over]*、 *[!UICONTROL Bottom]*&#x200B;または(デ *[!UICONTROL None]* フォルト)。

**[!UICONTROL Preserve Aspect Ratio]:** ビデオの幅と高さの比率を維持するか(*[!UICONTROL Yes]*)、ビデオを拡大して使用可能な領域を埋めるか(*[!UICONTROL No]*)。

**[!UICONTROL Close Button Delay]:** （一部の広告タイプ）閉じるボタンの表示を遅らせる秒数。

**[!UICONTROL Click URL]:** (Adobe提供の広告のみ)ビューアが広告をクリックしたときに表示されるURL。

**[!UICONTROL Final Click URL]:** (Adobe提供の広告のみ；読み取り専用)必要な [!UICONTROL Click URL] Advertising Cloud DSPトラッキングマ [クロが挿](/help/dsp/campaign-management/macros.md) 入されている（該当する場合）。

**[!UICONTROL VAST Tag]:** (VASTタグのみを使用する広告。読み取り専用)クリエイティブアセットとして入力したサードパーティのVASTタグ。

**[!UICONTROL Final VAST Tag]:** (VASTタグのみを使用する広告。読み取り専用)クリエイティブアセットとして入力し、必要な [Advertising Cloud DSPトラッキングマクロを挿入したサー](/help/dsp/campaign-management/macros.md) ドパーティのVASTタグ（該当する場合）。

**[!UICONTROL Wmode]:** （一部の広告タイプ）ウィンドウモード： *[!UICONTROL window]*、 *[!UICONTROL transparent]*&#x200B;または *[!UICONTROL opaque]*。

### [!UICONTROL Teaser]

*DSP提供広告のモバイルタップトゥプレイ形式*

**[!UICONTROL Asset]:** ティーザー画像またはビデオアセット：

* 独自の画像を選択するには、**[!UICONTROL Choose File]をクリックし、**&#x200B;をクリックしてデバイスまたはネットワーク上でファイルを探し、**[!UICONTROL Upload Image]**&#x200B;をクリックします。

   ベストプラクティスは、広告ユニットと同じサイズの画像を使用することです。

* クリエイティブから画像を選択するには、**[!UICONTROL Choose Thumbnail]**&#x200B;をクリックします。

静的画像ティーザーの要件：

* 形式：GIF、JPEG、PNG
* 画像サイズ：300 x 250
* ファイルサイズ：50 KB以下
* 推奨：行動への呼びかけ，認識可能な画像，ブランドロゴ

ビデオティーザーの要件：

* ファイルタイプ：MOV、MP4
* ファイルサイズ：2 MB未満
* 期間：7 ～ 10秒
* 推奨：認識可能な画像、顔、クイックカット

### [!UICONTROL Overlays]

*DSP提供広告用のインタラクティブなプリロールおよびモバイルインタラクティブなタップトゥプレイ形式*

次の設定は、作成または編集する各オーバーレイに適用されます。

**[!UICONTROL Asset]:** （生のアセットのみ）オーバーレイ画像アセット。ファイルの形式は1フレームGIF、JPGまたはPNGで、最大画像サイズは2 MB未満である必要があります。 アセットをアップロードするには、「**[!UICONTROL Browse]**」をクリックし、デバイスまたはネットワーク上でファイルを探して「**[!UICONTROL Upload]**」をクリックします。

>[!TIP]
>
>[オーバーレイのデザインのベストプラクティス](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)を参照してください。

**[!UICONTROL Click URL]:**  広告のオーバーレイをクリックしたときに表示されるURL。

**[!UICONTROL X]:** オーバーレイのX座標。オーバーレイの開始位置を選択し、開始位置からピクセル数（「中央から10ピクセル」など）を入力します。 ベストプラクティスは、「*中央から*」を使用することです。これは、オーバーレイが投稿サイト上で異なるプレーヤーサイズで移動するのを防ぎます。

**[!UICONTROL Y]:** オーバーレイのY座標。オーバーレイの開始位置を選択し、開始位置からピクセル数（「上から10ピクセル」など）を入力します。 広告上でオーバーレイを表示する位置に応じて、座標&#x200B;*[!UICONTROL From Bottom]*&#x200B;または&#x200B;*[!UICONTROL From Top]、*&#x200B;を指定することをお勧めします。

**[!UICONTROL Layer]:** オーバーレイを表示するレイヤー。ビデオと各オーバーレイは別々のレイヤーに表示されます。

* *[!UICONTROL 2 through 5]:* ビデオの前（他のオーバーレイの後）。

* *[!UICONTROL 1]:* ビデオの前に表示されます。

* *[!UICONTROL 0]:* ビデオと同じレイヤー内。残りの領域を埋めるためにビデオが縮小されます。 インタラクティブプリロールにはお勧めしません。

* *[!UICONTROL -1]:* ビデオの背後。

* *[!UICONTROL -2 through -5]:* ビデオの背後（他のオーバーレイの前）

* *[!UICONTROL Background]:* ビデオやその他のオーバーレイの背後。オーバーレイはビデオの幅と高さに合わせて拡大/縮小され、縦横比は維持されません。

### [!UICONTROL Endcap]

非推奨

### [!UICONTROL Pixel]

配置の既存のイベントトラッキングピクセルは、すべて自動的に添付されます。 必要に応じて、既存のピクセルを分離し、トラッキングのニーズに応じて新しいピクセルを作成できます。

作成または編集する各ピクセルには、次の設定が適用されます。

**[!UICONTROL Integration Event]:** 実行するピクセルをトリガー化するイベント。この広告タイプでは、*[!UICONTROL Impression]*&#x200B;または&#x200B;*[!UICONTROL Click-through]*&#x200B;で実行されるピクセルを使用します。

**[!UICONTROL Pixel Type]:** ピクセルが(1 x  *[!UICONTROL IMG URL]* 1ピクセルの画像ファイル)、またはの *[!UICONTROL HTML]*&#x200B;どちらであるか。 *[!UICONTROL JavaScript URL]*

**[!UICONTROL Pixel URL or Code]:** ピクセル画像のURL（指定したに適した形式） [!UICONTROL Pixel Type]。

**[!UICONTROL Pixel Name]:** ピクセル名。ピクセルを簡単に識別できる名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー： *[!UICONTROL None]*、 *[!UICONTROL Nielsen]*&#x200B;または *[!UICONTROL Comscore]*。

### [!UICONTROL Sharing]

非推奨

>[!MORELIKETHIS]
>
>* [広告管理について](ad-about.md)
>* [広告の作成](ad-create.md)
>* [広告に関連付けられている配置のリスト](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [使用可能な広告タイプ](ad-types.md)
>* [広告の仕様](/help/dsp/assets/ad-specs.pdf)
>* [オーバーレイのデザインのベストプラクティス](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Advertising Cloud DSPマクロ](/help/dsp/campaign-management/macros.md)

