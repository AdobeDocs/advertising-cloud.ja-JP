---
title: オーディオ広告の設定
description: オーディオ広告で使用可能な広告設定の説明を参照してください。
feature: Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---

# オーディオ広告の設定

## [!UICONTROL Upload or Select Creative]

*新しい広告のみ*

**[!UICONTROL Upload Audio]:** 生のアセットをDSPにアップロードします。これを選択したら、次の操作を行います。

1. **[!UICONTROL Choose File]**&#x200B;をクリックし、デバイスまたはネットワーク上でファイルを探します。
1. [!UICONTROL Ads]ビューとレポートで使用するファイルのタイトルを入力します。
1. クリック **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** アカウント内で、以前にアップロードしたクリエイティブを正しい形式で選択します。

**[!UICONTROL Advanced: VAST Tag URL]:** クリエイティブアセットと追跡ピクセルを含むサードパーティのVASTタグを入力するには：

1. ![**[!UICONTROL Advanced: VAST Tag URL]**&#x200B;の横にある矢印](/help/dsp/assets/compressed.png)をクリックします。
1. **[!UICONTROL URL]**&#x200B;フィールドに、VASTタグのURLを入力します。
1. ファイルの&#x200B;**[!UICONTROL Title]**&#x200B;を入力します。このファイルは、[!UICONTROL Ads]ビューとレポートで使用されます。

>[!TIP]
>
> VASTタグの有効性を確認するには、VASTタグをブラウザーに貼り付けて&#x200B;**[!UICONTROL Enter]**&#x200B;キーを押します。 タグが有効な場合は、上部に`<VAST>`を含むXMLファイルが表示されます。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。デフォルトは&#x200B;*[!UICONTROL Audio]*&#x200B;です。

**[!UICONTROL Ad Name]:** 広告名。アセットのタイトルはデフォルトで使用されますが、名前は変更できます。

>[!TIP]
>
> 配置、[!UICONTROL Ads]ビューおよびレポートで広告を添付する際に見つけやすい名前を使用します。 例えば、単位タイプといくつかの主要属性（休日の製品プレビューなど）を説明します。30秒オーディオ&quot;)。

**[!UICONTROL Ad Duration]:** オーディオファイルの長さ。選択した広告ユニットに応じて、[!UICONTROL 15]または[!UICONTROL 30]に自動的に設定されます。

このフィールドは、アカウント権限に応じて表示される場合と表示されない場合があります。

**[!UICONTROL Click URL]:** (生のアセットを使用し、ディスプレイバナーのみを使用する広告。（オプション）広告に付属するディスプレイバナーをクリックしたときに表示されるURL。

**[!UICONTROL Final Click URL]:** (生のアセットを使用し、ディスプレイバナーのみを使用する広告。読み取り専用)必要な [!UICONTROL Click URL] Advertising Cloud DSPトラッキングマ [クロが挿](/help/dsp/campaign-management/macros.md) 入されている（該当する場合）。

**[!UICONTROL VAST Tag]:** （VASTタグを使用する広告のみ）サードパーティの広告ソースのURL。VASTタグにオーディオメディアファイルのみが含まれていることを確認します。

**[!UICONTROL Final VAST Tag]:** （VASTタグを使用する広告のみ）必要な [Advertising Cloud DSPトラッキングマクロを挿入したサードパーテ](/help/dsp/campaign-management/macros.md) ィ広告ソースのURL（該当する場合）

**[!UICONTROL Select Rate]:** （権限を持つユーザーのみ）Adobeを通じて請求される事前にネゴシエートされたレート、または自分がネゴシエートし、ベンダーを通じて請求されるレートの1つ。レートを追加するには、担当のAdobeアカウントマネージャーにお問い合わせください。

### [!UICONTROL Companion]

*DSP提供広告のみ*

オプションで、1つの広告に最大3つのコンパニオンバナーを添付できます。 ベストプラクティスは、可能な場合はコンパニオンバナーを添付することです。

>[!NOTE]
>
>* コンパニオンバナーを許可していないパブリッシャーもあります。 コンパニオンバナーを許可する発行者は、コンパニオンバナーのインプレッションを保証しません。
>* サードパーティの広告タグのコンパニオンバナーは、必ずしもプレビューできるとは限りません。


**\[チェックボックス\]:** 指定したコンパニオンバナーを広告に含めます。このチェックボックスをオフにすると、コンパニオンバナーは含まれません。

**\[バナーサイズ\]:** コンパニオンバナーのサイズ： *[!UICONTROL 300x250]* (、、、お [!DNL iHeartRadio]よびに使用)、 [!DNL Spotify]( [!DNL SoundCloud]*に使 [!DNL TuneIn]用) *[!UICONTROL 640x640]* に使用され [!DNL Spotify), or *1024x1024] [!DNL SoundCloud]ます。

**\[ソース\]:** コンパニオンバナーアセットのソース：

* *[!UICONTROL Upload My Own Asset]:* 独自のアセットをアップロードする場合。
* *[!UICONTROL Use a Third Party Tag]:* 認定を受けたサードパーティ広告サービングパートナーからiFrameまたはscriptタグを入力するには、以下を実行します。

サードパーティコンパニオンバナーのインプレッションを追跡する場合は、サードパーティタグを使用します。

**[!UICONTROL Asset]:** （Rawアセットのみ）コンパニオンバナーアセット（GIF、JPGまたはPNG形式）。**[!UICONTROL Browse]**&#x200B;をクリックし、デバイスまたはネットワーク上でファイルを探して、**[!UICONTROL Upload]**&#x200B;をクリックします。

**[!UICONTROL Click URL]:** （生アセットのみ）ビューアが広告のコンパニオンバナーをクリックしたときに表示されるURL。サードパーティのクリック追跡ピクセルを使用して、クリックリダイレクトを含めることができます。

**[!UICONTROL Final Click URL]:** (Rawアセットのみ。読み取り専用)必要な [Advertising Cloud DSPトラッキングマクロを挿入し](/help/dsp/campaign-management/macros.md) たクリックURL（該当する場合）。

**[!UICONTROL Ad Tag]:** （サードパーティの広告タグを使用する広告のみ）サードパーティのコンパニオンバナーソース用のiFrameまたはスクリプトのバナータグ。認定を受けたサードパーティの広告提供パートナーからのものである必要があります。

**[!UICONTROL Final Ad Tag]:** （サードパーティの広告タグを使用する広告のみ）必要な [](/help/dsp/campaign-management/macros.md) Advertising Cloud DSPトラッキングマクロを挿入した広告タグ（該当する場合）。

### ピクセル

配置の既存のイベントトラッキングピクセルは、すべて自動的に添付されます。 必要に応じて、既存のピクセルを分離し、トラッキングのニーズに応じて新しいピクセルを作成できます。

作成または編集する各ピクセルには、次の設定が適用されます。

**[!UICONTROL Integration Event]:** 実行するピクセルをトリガー化するイベント。この広告タイプでは、*[!UICONTROL Impression]*&#x200B;または&#x200B;*[!UICONTROL Click-through]*&#x200B;で実行されるピクセルを使用します。

**[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG UR]L* （1 x 1ピクセルの画像ファイル）か *[!UICONTROL HTML]*、またはのどちらか *[!UICONTROL JavaScript URL]*。

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

