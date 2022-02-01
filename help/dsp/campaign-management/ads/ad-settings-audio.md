---
title: オーディオ広告設定
description: オーディオ広告で使用可能な広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# オーディオ広告設定

## [!UICONTROL Upload or Select Creative]

*新しい広告のみ*

**[!UICONTROL Upload Audio]:** 生のアセットをDSPにアップロードする場合。 これを選択した場合は、次の操作を行います。

1. クリック **[!UICONTROL Choose File]** お使いのデバイスまたはネットワーク上でファイルを探します。
1. ファイルのタイトルを入力します。このタイトルは、 [!UICONTROL Ads] 表示とレポート。
1. クリック **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** アカウント内で、以前にアップロードしたクリエイティブを正しい形式で選択する場合。

**[!UICONTROL Advanced: VAST Tag URL]:** クリエイティブアセットと追跡ピクセルを含むサードパーティの VAST タグを入力するには：

1. クリック ![矢印](/help/dsp/assets/compressed.png) 次の **[!UICONTROL Advanced: VAST Tag URL]**.
1. 内 **[!UICONTROL URL]** フィールドに、VAST タグ URL を入力します。
1. を入力します。 **[!UICONTROL Title]** ファイルに対して ( [!UICONTROL Ads] 表示とレポート。

>[!TIP]
>
> VAST タグの有効性を確認するには、タグをブラウザーに貼り付け、 **[!UICONTROL Enter]** キー。 タグが有効な場合は、 `<VAST>` 一番上の近くに

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できる配置タイプに対応します。 デフォルトはです。 *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前は変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を、 [!UICONTROL Ads] レポートで、およびを表示します。 たとえば、ユニット・タイプといくつかの主要属性（Holiday Product Preview など）を説明します。30 秒オーディオ&quot;)。

**[!UICONTROL Ad Duration]:** オーディオファイルの長さ。 自動的に [!UICONTROL 15] または [!UICONTROL 30]（選択した広告ユニットに応じる）

このフィールドは、アカウント権限に応じて、表示される場合と表示されない場合があります。

**[!UICONTROL Click URL]:** ( 生のアセットを使用する広告とディスプレイバナーのみ。（オプション）広告に付随するディスプレイバナーをクリックしたときに表示される URL。

**[!UICONTROL Final Click URL]:** ( 生のアセットを使用する広告とディスプレイバナーのみ。読み取り専用 ) [!UICONTROL Click URL] 必要に応じて [Advertising Cloud DSPトラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入されています（該当する場合）。

**[!UICONTROL VAST Tag]:** （VAST タグのみを使用する広告）サードパーティの広告ソースの URL。 VAST タグにオーディオメディアファイルのみが含まれていることを確認します。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用する広告のみ）必要な [Advertising Cloud DSPトラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入されています（該当する場合）。

**[!UICONTROL Select Rate]:** （権限を持つユーザーのみ）Adobeを通じて請求される事前にネゴシエートされた料金、またはネゴシエートした料金の 1 つで、ベンダーを通じて請求されます。 料金を追加するには、 [!DNL Adobe] アカウントチーム。

### [!UICONTROL Companion]

*DSP提供広告のみ*

オプションで、広告付きのコンパニオンバナーを 3 つまでアタッチできます。 可能な限りコンパニオンバナーを添付するのがベストプラクティスです。

>[!NOTE]
>
>* コンパニオンバナーを許可していないパブリッシャーもあります。 コンパニオンバナーを許可する発行者は、コンパニオンバナーのインプレッションを保証しません。
>* サードパーティの広告タグのコンパニオンバナーが、必ずしもプレビューに使用できるとは限りません。


**\[ チェックボックス\]:** 広告と共に指定したコンパニオンバナーを含めます。 このチェックボックスを無効にすると、コンパニオンバナーは含まれません。

**\[ バナーサイズ\]:** コンパニオンバナーのサイズ： *[!UICONTROL 300x250]* ( [!DNL iHeartRadio], [!DNL Spotify], [!DNL SoundCloud]、および [!DNL TuneIn]), *[!UICONTROL 640x640]* ( [!DNL Spotify), or *1024x1024]* （に使用） [!DNL SoundCloud]) をクリックします。

**\[ ソース\]:** コンパニオンバナーアセットのソース：

* *[!UICONTROL Upload My Own Asset]:* 独自のアセットをアップロードする場合。
* *[!UICONTROL Use a Third Party Tag]:* 認定を受けたサードパーティ広告サービングパートナーから iFrame または script タグを入力するには

サードパーティコンパニオンバナーのインプレッションを追跡する場合は、サードパーティのタグを使用します。

**[!UICONTROL Asset]:** （生のアセットのみ）コンパニオンバナーアセット (GIF、JPGまたは PNG 形式 )。 クリック **[!UICONTROL Browse]** お使いのデバイスまたはネットワーク上でファイルを探し、 **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:** （生のアセットのみ）広告のコンパニオンバナーをクリックしたときに閲覧者が到着する URL。 サードパーティのクリック追跡ピクセルを使用して、クリックリダイレクトを含めることができます。

**[!UICONTROL Final Click URL]:** ( 未加工資産のみ。読み取り専用 ) 必要な [Advertising Cloud DSPトラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入されています（該当する場合）。

**[!UICONTROL Ad Tag]:** （サードパーティの広告タグのみを使用する広告）サードパーティのコンパニオンバナーソース用の iFrame またはスクリプトバナータグ。 認定されたサードパーティの広告配信パートナーからのものである必要があります。

**[!UICONTROL Final Ad Tag]:** （サードパーティの広告タグのみを使用する広告）必要に応じて広告タグ [Advertising Cloud DSPトラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入されています（該当する場合）。

### ピクセル

配置の既存のイベントトラッキングピクセルはすべて自動的に添付されます。 必要に応じて、既存のピクセルを分離し、必要に応じて新しいピクセルを作成できます。

作成または編集する各ピクセルには、次の設定が適用されます。

**[!UICONTROL Integration Event]:** 実行するピクセルをトリガーにするイベント。 この広告タイプでは、 *[!UICONTROL Impression]* または *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG UR]L* （1 x 1 ピクセルの画像ファイル）、 *[!UICONTROL HTML]*&#x200B;または *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 指定したピクセルタイプに適した形式のピクセルイメージの URL。

**[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを簡単に識別できる名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*&#x200B;または *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [広告管理について](ad-about.md)
>* [広告の作成](ad-create.md)
>* [広告に関連付けられた配置のリスト](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [利用可能な広告タイプ](ad-types.md)
>* [広告の仕様](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSPマクロ](/help/dsp/campaign-management/macros.md)

