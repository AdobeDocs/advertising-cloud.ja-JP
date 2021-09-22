---
title: ディスプレイ広告の設定
description: ディスプレイ広告に使用可能な広告設定の説明を参照してください。
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# ディスプレイ広告の設定

次の設定は、標準のディスプレイ広告用です。 また、ディスプレイ広告用にクリックトゥプレイビデオ広告を提供することもできますが、多くのパブリッシャーがビデオ広告をサポートしていないので、提供しないことをお勧めします。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。デフォルトは&#x200B;*[!UICONTROL Display]*&#x200B;です。

**[!UICONTROL Ad Name]:** 広告名。アセットのタイトルはデフォルトで使用されますが、名前は変更できます。

>[!TIP]
>
> 配置、[!UICONTROL Ads]ビューおよびレポートで広告を添付する際に見つけやすい名前を使用します。 例えば、単位タイプといくつかの主要属性（休日の製品プレビューなど）を説明します。300 x 250 Gamer&quot;)。

**\[広告ソース\]**:Advertising Cloud DSPが広告を提供しているか(*[!UICONTROL Adobe served]*)、サードパーティの広告サーバーを使用しているか(*[!UICONTROL 3rd party]*)。

**[!UICONTROL This is an expandable Banner]:** （サードパーティ広告のみ）広告が拡大可能なバナー広告であることを示します。関連する拡張設定は、購入する在庫を決定するので、広告の動作を反映するようにします。

**[!UICONTROL Expansion Method]:** （サードパーティ製の拡大可能なバナー広告のみ）バナーが拡大されるか、または *[!UICONTROL Click]* 拡大されま *[!UICONTROL Rollover]*&#x200B;す。

**[!UICONTROL Expansion Directions]:** （サードパーティの拡大可能なバナー広告のみ）広告の展開方向。 *[!UICONTROL Up]*、 *[!UICONTROL Down]*、 *[!UICONTROL Left]*&#x200B;または *[!UICONTROL Right]*。

**[!UICONTROL Certified Vendors]:** （サードパーティで拡張可能なバナー広告のみ）広告が利用可能な認定ベンダー。 *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers])、 *[!UICONTROL Flashtalking]*、 *[!UICONTROL Sizmek]*&#x200B;または *[!UICONTROL Jivox]*。

**[!UICONTROL Display Code]:** （サードパーティ広告のみ）サードパーティのクリエイティブアセットのURL。[timestamp]および[[timestamp]]パラメーターは、実際の値に置き換えられます。

**[!UICONTROL Final Display Code]:** （サードパーティ広告のみ）サードパーティのクリエイティブアセットのURL。必要な [Advertising Cloud DSPトラッキングマ](/help/dsp/campaign-management/macros.md) クロが挿入されています（該当する場合）。

**[!UICONTROL Creative type]:** (Adobe提供の広告のみ)アセットがアセットかアセッ *[!UICONTROL Image]* トか *[!UICONTROL HTML5]* を示す。

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:** (Adobe提供の広告のみ)クリエイティブタイプに応じて、アップロードする画像ファイルまたは圧縮されたHTML5アセット。**[!UICONTROL Browse]**&#x200B;をクリックし、デバイスまたはネットワーク上でファイルを探して、**[!UICONTROL Upload]**&#x200B;または&#x200B;**[!UICONTROL Upload Image]**&#x200B;をクリックします。

**[!UICONTROL Ad Size]:** 広告の幅と高さ。[サポートされている標準のディスプレイ広告サイズ](/help/dsp/assets/ad-specs.pdf)である必要があります。 広告をアップロードする前に、または[!UICONTROL Display Code]を入力する前に、広告サイズを手動で入力できます。 広告サイズを入力しない場合、アップロードされた広告または広告タグのサイズは、自動的に読み取り専用として入力されます。 ディメンションが標準ディスプレイ内にサイズ（例：300x250の代わりに301x250）がない場合、ディスプレイ広告は保存されません。

>[!IMPORTANT]
>
> 「幅」フィールドと「高さ」フィールドで宣言されている広告サイズは、受信する入札リクエストと一致します。 広告のディメンションが宣言された広告サイズと一致しない場合、配信の問題が発生する可能性があります。

**[!UICONTROL Click URL]:** (Adobe提供の広告のみ)ビューアが広告をクリックしたときに表示されるURL。

**[!UICONTROL Final Click URL]:** (Adobe提供の広告のみ；読み取り専用)必要な [!UICONTROL Click URL] Advertising Cloud DSPトラッキングマ [クロが挿](/help/dsp/campaign-management/macros.md) 入されている（該当する場合）。

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
>* [広告に関連付けられている配置のリスト](ad-list-placements.md)
>* [使用可能な広告タイプ](ad-types.md)
>* [広告の仕様](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSPマクロ](/help/dsp/campaign-management/macros.md)

