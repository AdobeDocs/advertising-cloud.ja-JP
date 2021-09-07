---
title: Advertising Cloud DSPマクロ
description: 一般的な追跡に使用できるマクロを参照し、サードパーティのディスプレイ広告のクリックを追跡します。
feature: Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Advertising Cloud DSPマクロ

マクロは、命令の短いコマンドまたは略記法で、通常は`${MACRO_NAME}`の形式に従います。 Advertising Cloud DSP広告サーバーは、広告が提供またはクリックされるとマクロを実行します。

マクロは、サードパーティおよびカスタムのクリエイティブコードまたはメタデータ（サードパーティのピクセルなど）のトラフィック指定時に最も一般的に使用されます。

## 一般的な追跡マクロ

必要に応じて、すべての広告およびタグタイプで一般的なトラッキングマクロを使用し、特定のデータを渡します。

| マクロ | 説明 |
| --------------- | ---------------------- |
| `${USER_ID}` | すべてのデバイスタイプのユーザー識別子。 |
| `${TM_RANDOM}` | Cachebuster:1 ～ 1000000の乱数 |
| `${TM_PLACEMENT_ID_NUM}` | プレースメントID |
| `${TM_SITE_URL_URLENC}` | 入札リクエストで渡されたURL。URLエンコード |
| `${TM_SITE_DOMAIN_URLENC}` | 入札リクエストのURLから解析されたページサブドメイン。URLエンコード |

{style=&quot;table-layout:auto&quot;}

## サードパーティディスプレイ広告のマクロをクリックする

サードパーティの表示タグを使用して広告のクリックを正確に追跡するには、DSPにディスプレイクリックマクロが必要です。 必要なマクロのバージョンは1つだけです。関連するマクロは、タグのタイプによって異なります。

| マクロ | 説明 |
| --------------- | ---------------------- |
| `${TM_CLICK_URL}` | プラットフォームで広告サーバーが広告クリックを追跡およびカウントできるリダイレクトURL |
| `${TM_CLICK_URL_URLENC}` | URLエンコーディングが必要な広告サーバーがプラットフォームで広告クリックを追跡してカウントできるようにするリダイレクトURL |

{style=&quot;table-layout:auto&quot;}

DSPは、次の場合に、表示タグに表示クリックマクロを自動的に挿入します。

* Advertising Cloud広告サーバーパートナー<!-- [Needs PM confirmation.] -->から広告タグを書き出す
* DSPで[!DNL Flashtalking]広告タグまたは[!DNL Google DoubleClick for Advertisers]広告タグを直接一括アップロードします

ディスプレイ広告の作成時にクリックマクロが見つからない場合は、適切なディスプレイクリックマクロをタグの正しい領域に手動で挿入するよう求める警告メッセージがDSPに表示されます。

>[!MORELIKETHIS]
>
>* [オーディオ広告の設定](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [オーディオ広告の設定](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [オーディオ広告の設定](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [オーディオ広告の設定](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [オーディオ広告の設定](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [オーディオ広告の設定](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)

