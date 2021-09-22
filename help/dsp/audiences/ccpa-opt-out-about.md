---
title: '[!UICONTROL CCPA Opt-out-of-Sale]セグメントとレポートについて'
description: CCPAオプトアウトオブセールのリクエストからIDを追跡するセグメントの作成と、IDのレポートを取得する方法について説明します。
feature: CCPA, DSP Segments
exl-id: 9256d34e-d0dd-4abf-bc96-2b599caf2a8e
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# [!UICONTROL CCPA Opt-out-of-Sale]セグメントとレポートについて

カリフォルニア州消費者プライバシー法(CCPA)に従って、Webサイト上の消費者のオプトアウトオブセールのリクエストからのユーザーIDを追跡できます。そのためには、[CCPAオプトアウトオブセールセグメント](ccpa-opt-out-segment-create.md)を作成して実装します。 ユーザーは、無期限にCCPAオプトアウトオブセールセグメントにとどまります。

セグメントピクセルタグが実装されると、Advertising Cloudは広告主に代わってIDのプールの収集を開始します。

## 消費者向けオプトアウトオブセールレポート

Advertising Cloudは、顧客がアカウントのオプトアウトオブセールの要求のために送信したIDの月別レポートを生成します。 データは、Advertising Cloud DSPで作成されたCCPAオプトアウトオブセールセグメントと、Privacy ServiceAPIを介しておこなわれた送信を使用してキャプチャされたリクエストを統合します。  レポートは、前月の毎月1日に生成されます。 例えば、6月の月別ユーザーリストは7月1日に公開されます。

各レポートは、GZIP形式に圧縮されたタブ区切りテキストファイルとして使用できます。 CCPAオプトアウトオブセールセグメントでキャプチャされたユーザーIDは、セグメントおよび広告主によって識別されます。

過去3か月間に作成された月別レポート](ccpa-opt-out-segment-report-retrieve.md)へのリンクを、Advertising Cloud DSP内から、またはAdvertising Cloud [!DNL Trafficking API]を使用して、[取得できます。 各リンクは7日間有効ですが、顧客がリンクを取得しようとするたびに更新されます。

>[!MORELIKETHIS]
>
>* [Adobe Advertising Cloud州消費者プライバシー法のサポート：消費者のオプトアウトのサポート](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [セグメントの作成と [!UICONTROL CCPA Opt-Out-of-Sale] 実装](ccpa-opt-out-segment-create.md)
>* [消費者向けオプトアウトオブセールレポートの取得](ccpa-opt-out-segment-report-retrieve.md)
>* [Audience Managementについて](audience-about.md)

