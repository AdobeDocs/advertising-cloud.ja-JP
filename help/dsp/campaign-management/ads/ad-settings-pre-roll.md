---
title: プリロール広告の設定
description: プリロール広告に使用できる広告設定の説明を参照してください。
feature: Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 0%

---

# プリロール広告の設定

## [!UICONTROL Upload or Select Creative]

*新しい広告のみ*

**[!UICONTROL Transcode to]:** (権限に応じて、一部のユーザー。（オプション）パブリッシャーが特定のクリエイティブファイル要件を持つ場合にVASTタグに含める形式。ほとんどの発行者が受け入れる形式は、デフォルトで選択されています。

**[!UICONTROL Custom Transcode]:** （ベータ版ユーザーのみ）「垂直方向のビデオ」が選択されている場合は使用できません)ビデオでカスタムトランスコードが使用されていることを示します。このオプションを選択した場合は、最大3つのカスタムトランスコードバージョンのファイル形式、ビデオビットレート、ズームおよびサイズを指定します。

**[!UICONTROL XTrader]:** （権限に応じて一部のユーザー）ビデオが1つ以上のフィードを使用することを示 [!DNL X_TRADER] します。

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

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。アセットのタイトルはデフォルトで使用されますが、名前は変更できます。

>[!TIP]
>
> 配置、[!UICONTROL Ads]ビューおよびレポートで広告を添付する際に見つけやすい名前を使用します。 例えば、単位タイプといくつかの主要属性（休日の製品プレビューなど）を説明します。30秒プリロール」)。

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:** （標準およびスキップ可能なプリロール広告のみ）広告ユニット全体の幅。このオプションは、選択した広告ユニットのタイプに応じてロックされます。

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:** （標準およびスキップ可能なプリロール広告のみ）広告ユニット全体の高さ。このオプションは、選択した広告ユニットのタイプに応じてロックされます。

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

**[!UICONTROL Wmode]:** （インタラクティブプリロールのみ）ウィンドウモード： *[!UICONTROL window]*、 *[!UICONTROL transparent]*&#x200B;または *[!UICONTROL opaque]*。

**[!UICONTROL Video Format]:** （インタラクティブプリロールのみ）潜在的なインベントリ用の広告プレーヤーの形式： *[!UICONTROL VPAID]* または *[!UICONTROL VPAID & VAST]*。視認性は常にVPAIDで測定されますが、VPAIDおよびVASTには視認性の測定が許可されない在庫が含まれます。 キャンペーンで視認性指標が重要な場合は、次の点に注意してください。

**[!UICONTROL Clock Number]**:(インタラクティブなプリロールのみ。イギリスでのみ使われ、（権限を持つユーザーのみが使用可能）正しい広告が確実にブロードキャストされるようにするために使用される一意の識別子。この設定を適用できない場合は、空白のままにします。

### [!UICONTROL Companion]

*DSP提供広告のみ*

オプションで、1つの広告に最大3つのコンパニオンバナーを添付できます。 ベストプラクティスは、可能な場合はコンパニオンバナーを添付することです。

>[!NOTE]
>
> コンパニオンバナーを許可していないパブリッシャーもあります。 コンパニオンバナーを許可する発行者は、コンパニオンバナーのインプレッションを保証しません。
> サードパーティの広告タグのコンパニオンバナーは、必ずしもプレビューできるとは限りません。

**\[チェックボックス\]:** 指定したコンパニオンバナーを広告に含めます。このチェックボックスをオフにすると、コンパニオンバナーは含まれません。

**\[バナーサイズ\]:** コンパニオンバナーのサイズ： *[!UICONTROL 300x600 (Skyscraper)]*; *[!UICONTROL 300x250 (Medium Rectangle)]*：最も一般的な広告サイズで、すべての広告に推奨されます。 *[!UICONTROL 300x60 (Small Banner)]*;また *[!UICONTROL 728x90 (Leaderboard)]*&#x200B;は（より一般的でない広告サイズ）

**\[ソース\]:** 独自のコンパニオンバナーアセットをアップロードするか、サードパーティタグを使用するかを指定します。

**アセット：** （生のアセットのみ）コンパニオンバナーアセット。**[!UICONTROL Browse]**&#x200B;をクリックし、デバイスまたはネットワーク上でファイルを探して、**[!UICONTROL Upload]**&#x200B;をクリックします。

**広告タグ]:[!UICONTROL ** （VASTタグを使用する広告のみ）サードパーティのコンパニオンバナーソースへのURL。

**[!UICONTROL Final Ad Tag]:** （VASTタグを使用する広告のみ）必要な [](/help/dsp/campaign-management/macros.md) Advertising Cloud DSPトラッキングマクロを挿入した、サードパーティコンパニオンバナーソースへのURL（該当する場合）。

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

### [!UICONTROL Pixel]

配置の既存のイベントトラッキングピクセルは、すべて自動的に添付されます。 必要に応じて、既存のピクセルを分離し、トラッキングのニーズに応じて新しいピクセルを作成できます。

作成または編集する各ピクセルには、次の設定が適用されます。

**[!UICONTROL Integration Event]:** 実行するピクセルをトリガー化するイベント。この広告タイプでは、*[!UICONTROL Impression]*&#x200B;または&#x200B;*[!UICONTROL Click-through]*&#x200B;で実行されるピクセルを使用します。

**[!UICONTROL Pixel Type]:** ピクセルが(1 x  *[!UICONTROL IMG URL]* 1ピクセルの画像ファイル)、またはの *[!UICONTROL HTML]*&#x200B;どちらであるか。 *[!UICONTROL JavaScript URL]*

**[!UICONTROL Pixel URL or Code]:** ピクセル画像のURL（指定したに適した形式） [!UICONTROL Pixel Type]。

**[!UICONTROL Pixel Name]:** ピクセル名。ピクセルを簡単に識別できる名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー： *[!UICONTROL None]*、 *[!UICONTROL Nielsen]*&#x200B;または *[!UICONTROL Comscore]*。

>[!MORELIKETHIS]
>
>* [広告管理について](ad-about.md)
>* [広告の作成](ad-create.md)
>* [広告に関連付けられている配置のリスト](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [使用可能な広告タイプ](ad-types.md)
>* [広告の仕様](/help/dsp/assets/ad-specs.pdf)
>* [オーバーレイのデザインのベストプラクティス](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Advertising Cloud DSPマクロ](/help/dsp/campaign-management/macros.md)

