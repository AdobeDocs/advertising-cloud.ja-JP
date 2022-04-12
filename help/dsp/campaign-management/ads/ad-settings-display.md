---
title: ディスプレイ広告の設定
description: ディスプレイ広告に使用可能な広告設定の説明を参照してください。
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ディスプレイ広告の設定

以下の設定は、標準のディスプレイ広告に使用します。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。 デフォルトはです。 *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前は変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を、 [!UICONTROL Ads] レポートで、およびを表示します。 たとえば、ユニット・タイプといくつかの主要属性（Holiday Product Preview など）を説明します。300x250 Gamer&quot;) で表示されます。

**\[ 広告ソース\]**:（読み取り専用） *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** （サードパーティ広告のみ）広告が拡大可能なバナー広告であることを示します。 関連する展開設定は、購入する在庫を決定するので、広告の動作を反映するようにします。

**[!UICONTROL Expansion Method]:** （サードパーティの拡大可能なバナー広告のみ）バナーが次の場所に拡大するかどうか *[!UICONTROL Click]* または *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** （サードパーティの拡大可能なバナー広告のみ）広告が展開される方向。 *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]*&#x200B;または *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** （サードパーティの拡大可能なバナー広告のみ）広告が利用可能な認定ベンダー： *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]*&#x200B;または *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** （サードパーティ広告のみ）サードパーティのクリエイティブアセットの URL。 任意 [timestamp] および [[timestamp]] パラメーターは実際の値に置き換えられます。

**[!UICONTROL Final Display Code]:** （サードパーティ広告のみ）サードパーティのクリエイティブアセットの URL で、必要なもの [Advertising Cloud DSPトラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入されています（該当する場合）。

**[!UICONTROL Ad Size]:** 広告の幅と高さ。 これは、 [サポートされる標準のディスプレイ広告サイズ](ad-specs.md). 広告をアップロードする前に、広告のサイズを手動で入力するか、 [!UICONTROL Display Code]. 広告サイズを入力しない場合、アップロードされた広告または広告タグのサイズは、自動的に読み取り専用として入力されます。 ディメンションが標準ディスプレイ内にサイズ（例：300x250 の広告サイズではなく 301x250）がない場合、ディスプレイ広告は保存されません。

>[!IMPORTANT]
>
> 「幅」フィールドと「高さ」フィールドで宣言されている広告サイズは、受信する入札リクエストと一致します。 広告のディメンションが宣言された広告サイズと一致しない場合、配信の問題が発生する可能性があります。

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
>* [広告に関連付けられた配置のリスト](ad-list-placements.md)
>* [広告の仕様](ad-specs.md)
>* [Advertising Cloud DSPマクロ](/help/dsp/campaign-management/macros.md)

