---
title: について [!UICONTROL CCPA Opt-out-of-Sale] セグメントとレポート
description: CCPA オプトアウトオブセールのリクエストから ID を追跡するセグメントの作成方法と、ID のレポートを取得する方法について説明します。
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: e9d9d51302d32b06af805917db2f46e5f6daee62
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# について [!UICONTROL CCPA Opt-out-of-Sale] セグメントとレポート

カリフォルニア州消費者プライバシー法 (CCPA) に従って、Web サイト上の消費者によるオプトアウトオブセールスリクエストからユーザー ID を追跡できます。その際、 [CCPA オプトアウトオブセールセグメントの作成と実装](ccpa-opt-out-segment-create.md). ユーザーは、無期限に CCPA オプトアウトオブセールセグメントに残ります。

セグメントピクセルタグが実装されると、Adobe広告は、広告主に代わって ID のプールの収集を開始します。

## 消費者のオプトアウトオブセールレポート

Adobe広告は、顧客がアカウントのオプトアウトオブセールのリクエストのために送信した ID の月別レポートを生成します。 このデータは、DSPで作成された CCPA オプトアウトオブセールセグメントと、Privacy ServiceAPI を介しておこなわれた送信を使用してキャプチャされたリクエストを統合します。  レポートは、前月の各月の最初に生成されます。 例えば、6 月の月別ユーザーリストは 7 月 1 日に公開されます。

各レポートは、GZIP 形式に圧縮されたタブ区切りテキストファイルとして使用できます。 CCPA オプトアウトオブセールセグメントでキャプチャされたユーザー ID は、セグメントおよび広告主によって識別されます。

以下が可能です。 [月別レポートへのリンクの取得](ccpa-opt-out-segment-report-retrieve.md) DSP内から、またはDSP [!DNL Trafficking API]. 各リンクは 7 日間有効ですが、顧客がリンクを取得しようとするたびに更新されます。

>[!MORELIKETHIS]
>
>* [カリフォルニア州消費者プライバシー法に対するAdobe広告のサポート：消費者のオプトアウトのサポート](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [の作成と実装 [!UICONTROL CCPA Opt-Out-of-Sale] セグメント](ccpa-opt-out-segment-create.md)
>* [消費者オプトアウトオブセールレポートの取得](ccpa-opt-out-segment-report-retrieve.md)
>* [Audience Management について](audience-about.md)

