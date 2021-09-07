---
title: Advertising Cloud DSPの広告管理について
description: 広告管理について説明します。
feature: Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Advertising Cloud DSPの広告管理について

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSPは、広告を提供する2つの方法を提供します。

* Advertising Cloud DSPでは、独自のアセット（ディスプレイバナー、ビデオアセット、オーディオファイル、URLなど）をDSPに直接アップロードする際に、広告を無料で提供します。 DSPが提供するアセットの場合は、オーバーレイなどの追加機能にアクセスできます。

* サードパーティの広告サーバー（Google、Flashtalking、Sizmekなど）を使用している場合は、サードパーティの広告配信タグをDSPに個別に、または一括でアップロードできます。 バルクアップロード機能を使用するには、a) DoubleClickおよびFlashtalkingタグシートをアップロードするか、b)テンプレートをダウンロードし、タグをテンプレートに入力してから、テンプレートを再度アップロードする必要があります。<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

広告を設定したら、各広告を配置に関連付ける必要があります。配置には、キャンペーンの配信方法を制御するターゲティングパラメーター（地域、オーディエンス、デバイス、在庫のターゲティングなど）が含まれます。 1つの広告を1つまたは複数のプレースメントに添付できます。

## 使用可能な広告タイプ

* オーディオ
* 接続済みテレビ
* 表示
* モバイル
* ネイティブ
* プリロール

これらの広告タイプについて詳しくは、[利用可能な広告タイプ](ad-types.md)および[広告仕様](/help/dsp/assets/ad-specs.pdf)を参照してください。

## 特別な広告機能

次の機能は、DSP-seved広告にのみ使用できます。

### コンパニオンバナー

コンパニオンバナーは、[プリロール広告](ad-settings-pre-roll.md)または（一部の発行者と共に）[オーディオ広告](ad-settings-audio.md)と共に提供され、ブランドとメッセージの関連付けを強化するのに役立ちます。

>[!NOTE]
>
>* コンパニオンバナーを許可していないパブリッシャーもあります。 コンパニオンバナーを許可する発行者は、コンパニオンバナーのインプレッションを保証しません。
>* サードパーティの広告タグのコンパニオンバナーは、必ずしもプレビューできるとは限りません。


独自のコンパニオンバナーアセットをアップロードするか、認定済みのサードパーティ広告サービングパートナーからサードパーティのiFrameまたはスクリプトバナータグをアップロードできます。

### オーバーレイ

オーバーレイは、ビデオ全体での永続的なブランディングに役立ち、追加のクリックを促進できます。 オーバーレイ機能は、[インタラクティブなプリロール広告](ad-settings-pre-roll.md)と、[インタラクティブでタップトゥプレイ形式のモバイル広告](ad-settings-mobile.md)で使用できます。

[オーバーレイのデザインのベストプラクティス](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)を参照してください。

### ティーザー

ティーザーは、視聴者に広告を再生するよう誘導する、目を引く画像です。 ティーザーは、モバイルのタップトゥプレイ広告形式にのみ適用されます。

## Advertising Cloud DSP Ad Approvals

広告を作成すると、Advertising Cloud DSPは、機密性の高いカテゴリについて広告をレビューし、URL機能をクリックして、レンダリングをプレビューします。

最初は、[!UICONTROL Status]列に赤い点が表示されます。 レビュープロセスには通常24～48時間かかります。 ただし、広告が拒否される前にエラーを修正する時間があるので、中断された広告のステータスが48時間を超える場合があります。 却下された広告には、却下の理由が含まれます。

DSPが広告を承認すると、ステータス列に緑の点が表示されます。

![列の承認インジケ [!UICONTROL Status] ーター](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>広告は、DSPとSSPの両方がクリエイティブを承認した場合にのみ表示されます。 各SSPには、独自の承認要件とプロセスがあります。

>[!MORELIKETHIS]
>
>* [広告の作成](ad-create.md)
>* [複数のサードパーティ広告の作成](ad-create-third-party.md)
>* [使用可能な広告タイプ](ad-types.md)
>* [広告の仕様](/help/dsp/assets/ad-specs.pdf)

