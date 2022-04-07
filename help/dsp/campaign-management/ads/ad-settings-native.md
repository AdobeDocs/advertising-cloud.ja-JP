---
title: ネイティブディスプレイ広告設定
description: ネイティブディスプレイ広告で使用可能な広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 3ae59e63-ae64-41b2-8734-3df2da020c7c
source-git-commit: 68af6b1846a37689dce0ca13a05cc1611b1f35a9
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ネイティブディスプレイ広告設定

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。 広告タイプはデフォルトで使用されますが、名前は変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を、 [!UICONTROL Ads] レポートで、およびを表示します。 たとえば、ユニット・タイプといくつかの主要属性（Holiday Product Preview など）を説明します。15 秒ネイティブ」)。

**[!UICONTROL Native Creative]:** 1200 x 627 の画像で、モバイルインベントリでの配信を最大化します。 クリック **[!UICONTROL Browse]** お使いのデバイスまたはネットワーク上でファイルを探し、 **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** 視聴者を惹きつける目を引くタイトル。

**[!UICONTROL Description]:** 広告の本文。 最大長は 100 文字です。

**[!UICONTROL Landing Page]:** ユーザーが広告をクリックしたときに閲覧者が到着した URL。

**[!UICONTROL Final Landing Page]:** この [!UICONTROL Landing Page] 必要な [Advertising Cloud DSPトラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入されています（該当する場合）。

**[!UICONTROL Sponsored By (Advertiser Name)]:** 広告の広告主。

**[!UICONTROL Call to Action]:** （オプション）この広告が表示された後にビューアに実行させる手順です。

**[!UICONTROL Advertiser Logo]:** （オプション）ブランド認識を高めるために、広告に含める 1:1 の比率のロゴ。 クリック **[!UICONTROL Browse]** お使いのデバイスまたはネットワーク上でファイルを探し、 **[!UICONTROL Upload]**.

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
>* [広告の仕様](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSPマクロ](/help/dsp/campaign-management/macros.md)

