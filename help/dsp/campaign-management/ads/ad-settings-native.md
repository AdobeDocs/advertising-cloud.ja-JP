---
title: ネイティブ広告設定
description: ネイティブ広告に使用できる広告設定の説明を参照してください。
feature: Ads
exl-id: 3ae59e63-ae64-41b2-8734-3df2da020c7c
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# ネイティブ広告設定

## [!UICONTROL Upload or Select Creative]

*新しいビデオ（ただし、表示は除く）広告のみ*

**[!UICONTROL Upload Audio]:** 生のアセットをDSPにアップロードします。これを選択したら、次の操作を行います。

1. **[!UICONTROL Choose File]**&#x200B;をクリックし、デバイスまたはネットワーク上でファイルを探します。
1. [!UICONTROL Ads]ビューとレポートで使用するファイルのタイトルを入力します。
1. クリック **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** アカウント内で、以前にアップロードしたクリエイティブを正しい形式で選択します。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。デフォルトでは、広告タイプ（表示ネイティブ）またはビデオタイトル（ビデオ形式）が使用されますが、名前は変更できます。

>[!TIP]
>
> 配置、[!UICONTROL Ads]ビューおよびレポートで広告を添付する際に見つけやすい名前を使用します。 例えば、単位タイプといくつかの主要属性（休日の製品プレビューなど）を説明します。15秒ネイティブ」)。

**[!UICONTROL Native Creative]:** 1200 x 627の画像を使用して、モバイルインベントリでの配信を最大化します。ビデオ広告の場合、これはネイティブビデオが再生される前に表示される画像です。 **[!UICONTROL Browse]**&#x200B;をクリックし、デバイスまたはネットワーク上でファイルを探して、**[!UICONTROL Upload]**&#x200B;をクリックします。

**[!UICONTROL Title]:** 視聴者を引き付ける、目を引くタイトル。

**[!UICONTROL Description]:** ビデオ広告の場合、広告の短い概要です。ディスプレイ広告の場合、これは広告の本文です。 最大長は100文字です。

**[!UICONTROL Landing Page]:** ビューアが広告をクリックしたときに表示されるURL。

**[!UICONTROL Final Landing Page]:** 必要な [!UICONTROL Landing Page] Advertising Cloud DSPトラッキングマクロ [が挿入](/help/dsp/campaign-management/macros.md) されたURL（該当する場合）。

**[!UICONTROL Sponsored By (Advertiser Name)]:** 広告の広告主。

**[!UICONTROL Call to Action]:** （オプション）この広告を表示した後に閲覧者が実行する手順。

**[!UICONTROL Advertiser Logo]:** （オプション）ブランド認知度を高めるため、広告に含める1:1の比率のロゴ。**[!UICONTROL Browse]**&#x200B;をクリックし、デバイスまたはネットワーク上でファイルを探して、**[!UICONTROL Upload]**&#x200B;をクリックします。

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
>* [Advertising Cloud DSPマクロ](/help/dsp/campaign-management/macros.md)

