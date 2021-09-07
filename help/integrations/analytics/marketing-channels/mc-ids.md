---
title: Advertising Cloud IDを使用した [!DNL Marketing Channels] ルールの作成
description: Advertising Cloud IDを使用して [!DNL Analytics Marketing Channels]の処理ルールを作成する方法を説明します。
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 5224d891d665b901d076ff6a203e9ff3bab80f85
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Advertising Cloud IDを使用した[!DNL Marketing Channels]処理ルールの作成

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

Advertising Cloud ID（[AMO IDとEF ID](../ids.md)）を使用して、Adobe Analyticsで[!DNL Marketing Channels]処理ルールを設定できます。 Advertising Cloud IDは、Advertising Cloudキャンペーンに固有のルールに使用します。

## 処理ルールのAMO ID

AMO IDは、[!DNL Analytics]内でAdvertising Cloudデータをレポートするために使用される主なトラッキングコードです。 AMO IDは、[!DNL Analytics]内で詳細なレポートを提供するために、Adobeが管理する動的な値を連結したものです。 これは[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)またはrVarディメンション(AMO ID)に保存されます。 AMO IDは、次の2つの方法で[!DNL Analytics]に設定できます。

* クリックスルーの追跡：Advertising Cloudはリンクに`s_kwcid`クエリー文字列パラメーターを設定し、クリックスルーが発生すると、[!DNL Analytics]はランディングページのURLからパラメーターを取得します。
* ビュースルートラッキング（[!DNL DSP]のみ）:最後のイベントサービスは、サーバー側のビュースルーを検出し、AMO IDを[!DNL Analytics]に送信します。 この場合、URLには`s_kwcid`パラメーターは含まれません。

AMO ID内の動的な値は、追跡されたマーケティングチャネルを示します。

* AMO IDのプレフィックスは、[!DNL Marketing Channels]内のトップレベルチャネルを識別するために使用できます。

* AMO IDの本文の文字フレーズは、より具体的なキャンペーンタイプを示します。

* [!DNL DSP]ビュースルートラフィックにはサフィックス「vt」が付き、別々のクリックスルーチャネルとビュースルー[!DNL DSP]チャネルを作成するために使用できます。

残りのAMO IDは無視できます。

| AMO ID | チャネル | ルールロジック |
|--------|---------|--------------------|
| アル！ （プレフィックス） | [!UICONTROL Paid Search] | 次の語句で始まる |
| 交通！ （プレフィックス） | [!UICONTROL DSP] | 次の語句で始まる |
| !g! （本文） | [!UICONTROL Google Search] | 次を含む |
| !s! （本文） | [!UICONTROL Search Partner] | 次を含む |
| !d! （本文） | [!UICONTROL Display Network] | 次を含む |
| !u! （本文） | [!UICONTROL Smart Shopping Campaign] | 次を含む |
| !ytv! （本文） | [!UICONTROL YouTube Video Ad] | 次を含む |
| !yts! （本文） | [!UICONTROL YouTube Search Ad] | 次を含む |
| !vp! （本文） | [!UICONTROL Google Video Partners] | 次を含む |
| !vt （サフィックス） | [!UICONTROL DSP View-through] | 次の語句で終わる |

### AMO IDを使用する処理ルールの例

[!UICONTROL Paid Search]チャネルの[!DNL Marketing Channels]処理ルールは次のようになります。

![ルールの [!UICONTROL Paid Search] 例](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

[!UICONTROL YouTube Video Ads]チャネルの[!DNL Marketing Channels]処理ルールは次のようになります。

![ルールの [!UICONTROL YouTube Video Ads] 例](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> ルールは必ず特異性の順に実行してください。 上記の2つのルールが順番に実行された場合、AMO IDは「AL!」で始まるので、 [!DNL YouTube]ビデオ広告トラフィックはすべて[!UICONTROL Paid Search]チャネルに分類されます。 「!ytv!」を含める必要があります。

## 処理ルール内のEF ID

AMO EF ID(EF ID)は、[!DNL Analytics for Advertising Cloud]統合で使用される2番目のトラッキングコードです。 主な目的は、[!DNL Analytics]イベントデータを追跡し、Advertising Cloudに渡すことです。 同じ訪問者に対してまったく同じ広告であっても、クリックスルーまたはビュースルーが発生するたびに、一意のEF IDが生成されます。 EF IDは、[!DNL Analytics]レポートのユーザーインターフェイスでは使用されません。通常、[!DNL Analytics]の変数制限あたりの500,000個の一意の値を超えているので、レポートで使用できなくなります。 Advertising Cloudの指標とメタデータは、EF IDには適用されません。これらはAMO IDにのみ適用されます。 Advertising Cloudでのキャンペーンの最適化には、追跡の精度を追加する必要があるので、両方のIDが必要です。

EF IDディメンションは[!DNL Analytics]レポートでは直接使用されませんが、EF IDはマーケティングチャネルの作成に役立ちます。 EF IDサフィックスは、チャネル（表示または検索）と、訪問がクリックスルーまたはビュースルーによって実行されたかどうかを示します。 EF IDの区切り文字は、AMO IDの感嘆符ではなく、コロンです。

| EF IDサフィックス | チャネル |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### EF IDを使用する処理ルールの例

#### クリックスルールの表示

クリックスルーのみを取り込んで、ディスプレイ用のクリックスルーマーケティングチャネルを作成します。 AMO IDは、クリックスルーとビュースルーの両方で同じなので、このルールではEF ID変数と`ef_id`クエリー文字列パラメーターを使用します。

クリックスルーは、URL（デフォルト）で追跡される場合があります。 その他の場合は、クリックスルーはサーバー側の「最後のイベントサービス」で追跡されるので、URLに`ef_id`パラメーターは含まれません。 したがって、このルールは、EF ID変数または`ef_id`クエリー文字列パラメーターが「:d」で終わる条件を確認します。 どちらの条件でもこのルールをトリガーする場合は、「`Any`」演算子を使用します。

![表示のクリックスルールールの例](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### ビュースルールを表示

表示ビュースルーチャネルを作成するには、EF IDが「:i」で終わるルールを作成します。 訪問者が広告をクリックしなかったので、ビュースルートラッキングのURLには`ef_id`または`s_kwcid`が含まれません。 したがって、必要な条件は1つだけです。

![表示ビュースルールの例](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [の基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Advertising Cloudと [!DNL Marketing Channels]](mc-data-variances.md)
>* [ [!DNL Analytics Marketing Channels] Advertising Cloudデータの使用](mc-ac-data.md)
>* [ビデオ：Advertising Cloudを使用したレポート [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Advertising Cloudで使用されるID [!DNL Analytics]](/help/integrations/analytics/ids.md)

