---
title: Advertising Cloud DSPマクロ
description: 一般的な追跡に使用可能なマクロを参照し、サードパーティのディスプレイ広告のクリックを追跡します。
feature: DSP Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: fbadd81a34c375f00fa3e420ea3c46fc9143daf8
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Advertising Cloud DSPマクロ

マクロは、命令の短いコマンドまたは略記法で、通常は形式に従います `${MACRO_NAME}`. クリエイティブコードまたはクリックスルー URL に含まれるマクロは、広告サーバーが理解できる長いコード文字列に展開されます。 Advertising Cloud DSP広告サーバーは、広告が提供またはクリックされると、マクロを実行します。

広告サーバーマクロは、重要な情報をDSPまたはサードパーティの広告サーバーに渡すのに役立ちます。 マクロは、サードパーティとカスタムのクリエイティブコードまたはメタデータ（サードパーティのピクセルなど）のトラフィック指定時に最も一般的に使用されます。

マクロは、VAST タグ、URL、DSPまたはサードパーティのイベントピクセルなど、任意の場所に手動で挿入できます。 ただし、DSPクライアントとパートナーは広告タグの形式が異なるので、それに応じてタグ内の別の場所にマクロを挿入する必要があります。 新しいクライアントまたはパートナーと連携するたびに、DSPトラフィックの広告タグにマクロを挿入する場所に関するドキュメントをユーザーに問い合わせます。

## 一般的なトラッキングマクロ

必要に応じて、すべての広告およびタグタイプで一般的なトラッキングマクロを使用して、特定のデータを返します。

| マクロ | 置換の説明 | タイプ |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | アカウント ID。 | 整数 |
| `${TM_AD_ID}` | 広告キー (adKey)。 | 文字列 |
| `${TM_AD_ID_NUM}` | 広告 ID。 | 整数 |
| `${TM_ADVERTISER_ID}` | 広告主 ID。 | 整数 |
| `${TM_CAMPAIGN_ID}` | キャンペーンキー。 | 文字列 |
| `${TM_CAMPAIGN_ID_NUM}` | キャンペーン ID。 | 整数 |
| ` ${TM_CLICK_URL}` | リダイレクト URL。広告サーバーは、広告のクリックを追跡し、カウントできます。 広告が提供される際に、ユーザーが広告をクリックすると、マクロが有効化され、クリックが記録され、レポート目的でカウントされます。 | 文字列 |
| ` ${TM_CLICK_URL_URLENC}` | エンコードされたリダイレクト URL。広告サーバーは、広告クリックの追跡とカウントを可能にします。 広告が提供される際に、ユーザーが広告をクリックすると、マクロが有効化され、クリックが記録され、レポート目的でカウントされます。 サードパーティの広告を作成し、ベンダーが URL エンコーディングを必要とする場合を除き、このマクロは使用しないでください。 | 文字列 |
| `${TM_FEED_ID}` | メディア配置のキー (feedKey)。 | 文字列 |
| `${TM_FEED_ID_NUM}` | メディア配置の ID。 | 整数 |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | プレースメントのサイトキー。 必須 [!DNL AppsFlyer] モバイルアプリインストール広告用のトラッカーをクリックします。<!-- should map to placement_site_key column of placement_site table --> | 文字列 |
| `${TM_PLACEMENT_ID}` | 配置キー (cpKey)。 | 文字列 |
| `${TM_PLACEMENT_ID_NUM}` | プレースメント ID。 | 整数 |
| `${TM_RANDOM}` | Cachebuster:1 ～ 1000000の乱数。 | long |
| `${TM_SESSION_ID}` | 広告タグの単一の取得に対応するセッションの ID。 | 文字列 |
| `${TM_SITE_DOMAIN_URLENC}` | 入札リクエストの URL から解析されたページサブドメイン。URL エンコード済み。 バナー内、クリックトゥプレイ広告はサポートされていません。 | 文字列 |
| ` ${TM_SITE_NAME}` | 配置のサイト名。 | 文字列 |
| `${TM_SITE_URL_URLENC}` | 入札リクエストで渡された URL。URL エンコード済み。 バナー内、クリックトゥプレイ広告はサポートされていません。 | 文字列 |
| `${TM_SITE_ID_NUM}` | プレースメントのサイト ID。 | 整数 |
| `${TM_TIMESTAMP}` | 1970 年 1 月 1 日の午前 0 時 (00:00 UTC) 以降の経過秒数を示す Unix タイムスタンプ。 | long |
| ` ${TM_VIDEO_DURATION}` | 広告ビデオの長さ（秒）。 | 整数 |

{style=&quot;table-layout:auto&quot;}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## モバイル固有のマクロ

| マクロ | 置換の説明 | タイプ |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) デバイスのオペレーティングシステムに対応するプラットフォーム ID。<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` プラットフォームが上記のいずれでもない場合</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) デバイスモデル名（URL エンコード済み）。 | 文字列 |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) 広告が提供された環境：<ul><li>`a` =モバイルアプリケーション</li><li>`b` =モバイル web サイト</li></ul> | 文字列 (`a` または `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) デバイスのオペレーティングシステムに対応するプラットフォーム ID。<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` プラットフォームが上記のいずれでもない場合</li></ul> | 文字列 |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) 広告が閲覧されたデバイスのタイプ。<ul><li>`TAB` =タブレット</li><li>`PHN` =モバイル</li><li>`computer` =コンピュータ</li></ul> | 文字列 |
| `${UOO}` | ([!DNL Nielsen]) ユーザーが広告トラッキングをオプトアウトしたかどうかを示します。<ul><li>`1` （DNT フラグ= 1） =ユーザーが広告トラッキングをオプトアウトしました</li><li>`0` （DNT フラグ= 0） =ユーザーが広告トラッキングをオプトインした</li></ul> | 整数 (`0` または `1`) |
| `${TM_BUNDLE}` | この [!DNL iOS] または [!DNL Android] app store バンドル ID。 例：com.zynga.wwf2.free またはid804379658 | 文字列 |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` 入札者が、入札リクエストが欧州連合 (EU) の起源から送信され、GDPR の実施を必要とすると判断するかどうかを示します。<ul><li>`1` = GDPR を適用する必要がある</li><li>`0` = GDPR は適用しない</li></ul>`gdpr_consent=${GDPR_CONSENT}` は、インバウンド入札リクエストで供給パートナーから渡される同意値です。<ul><li>ほとんどの場合、これは base64URL でエンコードされたコンセントストリング、または daisybit です ( 例：BN5lERiMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` =同意なし</li><li>`1` =同意</li></ul> | dasybit または integer |

{style=&quot;table-layout:auto&quot;}

## サードパーティのディスプレイ広告のマクロをクリックする

サードパーティの表示タグを使用して広告のクリックを正確に追跡するには、DSPにディスプレイクリックマクロが必要です。 必要なマクロのバージョンは 1 つだけです。関連するマクロは、タグのタイプによって異なります。

| マクロ | 置換の説明 | タイプ |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | 広告サーバーがプラットフォームで広告クリックを追跡し、カウントできるようにするリダイレクト URL です。 | 文字列 |
| `${TM_CLICK_URL_URLENC}` | URL エンコーディングが必要な広告サーバーがプラットフォームでの広告クリックを追跡し、カウントできるようにするリダイレクト URL です。 | 文字列 |

{style=&quot;table-layout:auto&quot;}

DSPは、次の場合に、サードパーティの表示タグにディスプレイクリックマクロを自動的に挿入します。

* Advertising Cloud広告サーバーパートナーからの広告タグのエクスポート <!-- [Needs PM confirmation.] -->
* バルクアップロード [!DNL Flashtalking] または [!DNL Google DoubleClick for Advertisers] DSPで直接タグを追加

ディスプレイ広告の作成時にクリックマクロが見つからない場合は、DSPに警告メッセージが表示され、適切なディスプレイクリックマクロをタグの正しい領域に手動で挿入するよう求められます。

## マクロエラーのトラブルシューティング

コードにマクロを追加する場合は、マクロの構文を正確に使用する必要があります。 マクロを検証する際に、DSPはマクロが有効なマクロの 1 つと完全に一致していることを確認します。

マクロ名の先頭または末尾に文字がない場合は、エラーが生成されます。 例えば、次の場合にエラーメッセージが表示されます。

* マクロ名の先頭に 1 つ以上の文字 ( 例： `${`. 完全な構文を含めない場合、エントリは有効なマクロとして認識されません。
* マクロは、次のような有効な文字セットで終わりません。 `}`.

>[!MORELIKETHIS]
>
>* [オーディオ広告設定](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [接続済み TV 広告設定](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [ディスプレイ広告の設定](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [モバイル広告設定](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [ネイティブ広告設定](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [プリロール広告の設定](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)

