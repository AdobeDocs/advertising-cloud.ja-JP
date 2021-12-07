---
title: Advertising Cloud ID を使用した作成 [!DNL Marketing Channels] ルール
description: Advertising Cloud ID を使用しての処理ルールを作成する方法を説明します。 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Advertising Cloud ID を使用した作成 [!DNL Marketing Channels] 処理ルール

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

Advertising Cloud ID ([AMO ID と EF ID](../ids.md)) を設定します。 [!DNL Marketing Channels] Adobe Analyticsの処理ルール Advertising Cloud ID をAdvertising Cloudキャンペーンに固有のルールに使用します。

## 処理ルール内の AMO ID

AMO ID は、内でAdvertising Cloudデータをレポートするために使用される主なトラッキングコードです [!DNL Analytics]. AMO ID は、内で詳細なレポートを提供するために、Adobeが管理する動的な値を連結したものです。 [!DNL Analytics]. これは、 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または rVar ディメンション (AMO ID)。 AMO ID は、で設定できます。 [!DNL Analytics] 次の 2 つの方法で、

* クリックスルートラッキング：Advertising Cloudが `s_kwcid` リンク内のクエリー文字列パラメーター、および [!DNL Analytics] クリックスルーが発生した場合に、ランディングページ URL からパラメーターを取得します。
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

AMO EF ID(EF ID) は、 [!DNL Analytics for Advertising Cloud] 統合とも呼ばれます。 その主な目的は、トラッキングとパス [!DNL Analytics] イベントデータをAdvertising Cloudに送信します。 同じ訪問者に対してまったく同じ広告である場合でも、クリックスルーまたはビュースルーが発生するたびに、一意の EF ID が生成されます。 EF ID は、 [!DNL Analytics] の変数制限あたりのユニーク値が通常 500,000 個を超えるので、レポートユーザーインターフェイスを使用します。 [!DNL Analytics]レポートで使用できなくなります。 Advertising Cloudの指標とメタデータは、EF ID には適用されません。これらは AMO ID にのみ適用されます。 Advertising Cloudでキャンペーンを最適化するには、追加された精度のトラッキングが必要なので、両方の ID が必要です。

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

表示ビュースルーチャネルを作成するには、EF ID が「:i」で終わるルールを作成します。 訪問者が広告をクリックしなかったので、ビュースルートラッキングには `ef_id` または `s_kwcid` 」と入力します。 したがって、必要な条件は 1 つだけです。

![表示ビュースルールの例](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [の基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Advertising Cloudと [!DNL Marketing Channels]](mc-data-variances.md)
>* [使用 [!DNL Analytics Marketing Channels] Advertising Cloud Data を使用](mc-ac-data.md)
>* [ビデオ：Advertising Cloudを使用したレポート [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Advertising Cloud ID 使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)

