---
title: Adobe広告 ID を使用した作成 [!DNL Marketing Channels] ルール
description: Adobe広告 ID を使用しての処理ルールを作成する方法を説明します。 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 4fcdd586-e9c5-4405-a6dc-7799d2bac93e
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Adobe広告 ID を使用した作成 [!DNL Marketing Channels] 処理ルール

*Advertising とAdobe AnalyticsのAdobeの統合のみの広告主*

Adobe広告 ID ([AMO ID と EF ID](../ids.md)) を設定します。 [!DNL Marketing Channels] Adobe Analyticsの処理ルール Adobe広告 ID は、Adobe広告キャンペーンに固有のルールに使用します。

## 処理ルール内の AMO ID

AMO ID は、内で広告データをレポートするために使用される主なAdobeコードです [!DNL Analytics]. AMO ID は、内で詳細なレポートを提供するために、Adobeが管理する動的な値を連結したものです。 [!DNL Analytics]. これは、 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または rVar ディメンション (AMO ID)。 AMO ID は、で設定できます。 [!DNL Analytics] 次の 2 つの方法で、

* クリックスルートラッキング：Adobe広告は `s_kwcid` リンク内のクエリー文字列パラメーター、および [!DNL Analytics] クリックスルーが発生した場合に、ランディングページ URL からパラメーターを取得します。
* ビュースルートラッキング ([!DNL DSP] ):最後のイベントサービスは、サーバー側のビュースルーを検出し、AMO ID をに送信します。 [!DNL Analytics]. この場合、URL には `s_kwcid` パラメーター。

AMO ID 内の動的な値は、追跡されたマーケティングチャネルを示します。

* AMO ID のプレフィックスは、内の最上位チャネルを識別するために使用できます [!DNL Marketing Channels].

* AMO ID の本文の文字フレーズは、より具体的なキャンペーンタイプを示します。

* サフィックス「vt」が [!DNL DSP] ビュースルートラフィックに関連付けられ、別々のクリックスルーとビュースルーの作成に使用できます。 [!DNL DSP] チャネル。

残りの AMO ID は無視できます。

| AMO ID | チャネル | ルールロジック |
|--------|---------|--------------------|
| アル！ （プレフィックス） | [!UICONTROL Paid Search] | 次で始まる |
| 交通！ （プレフィックス） | [!UICONTROL DSP] | 次で始まる |
| !g! （本文） | [!UICONTROL Google Search] | 次を含む |
| !s! （本文） | [!UICONTROL Search Partner] | 次を含む |
| !d! （本文） | [!UICONTROL Display Network] | 次を含む |
| !u! （本文） | [!UICONTROL Smart Shopping Campaign] | 次を含む |
| !ytv! （本文） | [!UICONTROL YouTube Video Ad] | 次を含む |
| !yts! （本文） | [!UICONTROL YouTube Search Ad] | 次を含む |
| !vp! （本文） | [!UICONTROL Google Video Partners] | 次を含む |
| !vt （サフィックス） | [!UICONTROL DSP View-through] | 次で終わる |

### AMO ID を使用する処理ルールの例

この [!DNL Marketing Channels] 処理ルール [!UICONTROL Paid Search] チャネルは次のようになります。

![の例 [!UICONTROL Paid Search] ルール](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

この [!DNL Marketing Channels] 処理ルール [!UICONTROL YouTube Video Ads] チャネルは次のようになります。

![の例 [!UICONTROL YouTube Video Ads] ルール](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> ルールは、特異性の順に実行するようにしてください。 上記の 2 つのルールが順番に実行された場合、 [!DNL YouTube] ビデオ広告トラフィックは、すべて [!UICONTROL Paid Search] チャネルを設定する必要があります。AMO ID は共に「AL!」で始まるからです。 「!ytv!」が含まれている必要があります。

## 処理ルール内の EF ID

AMO EF ID(EF ID) は、 [!DNL Analytics for Advertising] 統合とも呼ばれます。 その主な目的は、トラッキングとパス [!DNL Analytics] イベントデータからAdobe広告。 同じ訪問者に対してまったく同じ広告である場合でも、クリックスルーまたはビュースルーが発生するたびに、一意の EF ID が生成されます。 EF ID は、 [!DNL Analytics] の変数制限あたりのユニーク値が通常 500,000 個を超えるので、レポートユーザーインターフェイスを使用します。 [!DNL Analytics]レポートで使用できなくなります。 Adobe広告の指標とメタデータは、EF ID には適用されません。これらは AMO ID にのみ適用されます。 Adobe広告でキャンペーンを最適化するには、追跡に追加された精度が必要なので、両方の ID が必要です。

ただし、EF ID ディメンションは [!DNL Analytics] レポートの場合、EF ID はマーケティングチャネルの作成に役立ちます。 EF ID サフィックスは、チャネル（表示または検索）と、訪問がクリックスルーまたはビュースルーによって駆動されたかどうかを示します。 EF ID の区切り文字は、AMO ID 内の感嘆符ではなくコロンです。

| EF ID サフィックス | チャネル |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### EF ID を使用する処理ルールの例

#### クリックスルールを表示

クリックスルーのみを取り込んで、ディスプレイクリックスルーマーケティングチャネルを作成します。 AMO ID はクリックスルー数とビュースルー数の両方で同じなので、このルールでは EF ID 変数と `ef_id` クエリー文字列パラメーター。

クリックスルーは、URL（デフォルト）で追跡される場合があります。 その他の場合は、クリックスルーはサーバー側の最後のイベントサービスで追跡されるので、URL には `ef_id` パラメーター。 したがって、EF ID 変数または `ef_id` クエリー文字列パラメーターが「:d」で終わる。 「`Any`」演算子を使用する必要があります。

![表示のクリックスルールールの例](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### ビュースルールを表示

表示ビュースルーチャネルを作成するには、EF ID が「:i」で終わるルールを作成します。 訪問者が広告をクリックしなかったので、ビュースルートラッキングには `ef_id` または `s_kwcid` 」と入力する必要があるので、ルールに必要な条件は 1 つだけです。

![表示ビュースルールの例](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [の基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [チャネル広告とチャネル広告でチャネルデータが異なるAdobeを使用する理由 [!DNL Marketing Channels]](mc-data-variances.md)
>* [使用 [!DNL Analytics Marketing Channels] とAdobe広告データ](mc-ac-data.md)
>* [ビデオ：使用 [!DNL Marketing Channels] (Adobe広告レポート用 )](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe広告 ID が [!DNL Analytics]](/help/integrations/analytics/ids.md)

