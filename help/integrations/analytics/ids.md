---
title: Advertising Cloud IDが [!DNL Analytics]で使用されている
description: Advertising Cloud IDが [!DNL Analytics]で使用されている
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# [!DNL Analytics]で使用されるAdvertising Cloud ID

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

*Advertising Cloud DSPおよびAdvertising Cloud Searchに適用*

Advertising Cloudは、オンサイトパフォーマンストラッキングに2つのIDを使用します。 EF IDとAMO ID。

広告インプレッションが発生すると、Advertising CloudはAMO IDとEF IDの値を作成して保存します。 広告を表示した訪問者が広告をクリックせずにサイトに入ると、[!DNL Analytics]は[!DNL Analytics for Advertising Cloud] JavaScriptコードを通じてこれらの値をAdvertising Cloudから呼び出します。 ビュースルートラフィックの場合、[!DNL Analytics]は追加のID(`SDID`)を生成します。このIDは、EF IDとAMO IDを[!DNL Analytics]にステッチするために使用されます。 クリックスルートラフィックの場合、 `s_kwcid`および`ef_id`クエリ文字列パラメーターを使用して、これらのIDがランディングページのURLに含まれます。

Advertising Cloudは、次の条件を使用して、Webサイトへのクリックスルーエントリとビュースルーエントリを区別します。

* ビュースルーエントリは、広告を表示した後、広告をクリックせずにユーザーがサイトを訪問した場合に取り込まれます。 [!DNL Analytics] は、次の2つの条件を満たした場合にビュースルーを記録します。
   * 訪問者は、[クリックルックバックウィンドウ](#lookback-a4adc)の間、[!DNL DSP]または[!DNL Search]の広告のクリックスルーがありません。
   * 訪問者は、[インプレッションのルックバックウィンドウ](#lookback-a4adc)で、少なくとも1つの[!DNL DSP]広告を閲覧しました。 最後のインプレッションは、ビュースルーとして渡されます。
* クリックスルーエントリは、サイト訪問者がサイトに入る前に広告をクリックした場合にキャプチャされます。 [!DNL Analytics] は、次のいずれかの条件が発生した場合にクリックスルーをキャプチャします。
   * URLには、Advertising CloudによってランディングページURLに追加されたEF IDとAMO IDが含まれます。
   * URLにはトラッキングコードは含まれていませんが、Advertising Cloud JavaScriptコードが過去2分以内にクリックを検出しました。

![Advertising Cloudビューベースの [!DNL Analytics] 統合](/help/integrations/assets/a4adc-view-through-process.png)

*図1:Advertising Cloudビューベースの [!DNL Analytics] 統合*

![Advertising Cloud Click URLベースの [!DNL Analytics] 統合](/help/integrations/assets/a4adc-click-through-process.png)

*図2:Advertising Cloud Click URLベースの [!DNL Analytics] 統合*

## Advertising Cloud EF ID

EF IDは、Advertising Cloudがアクティビティをオンラインクリックまたは広告公開に関連付けるために使用する一意のトークンです。 EF IDは、 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)またはrVar(予約eVar)ディメンション(Advertising Cloud EF ID)に保存され、個々のブラウザーまたはデバイスレベルで各広告のクリックまたは露出を追跡します。 EF IDは主に、Advertising Cloud内でのレポートおよび入札の最適化のためにAdvertising Cloudに[!DNL Analytics]データを送信する際のキーとして機能します。

### EF ID形式

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

ここで、

* &lt;>Advertising Cloud訪問者ID *>は、訪問者ごとの一意のIDです（UhKVaAABCkJ0mDtなど）。**サーファーID*&#x200B;とも呼ばれます。

* &lt;>timestamp *>は、YYYYMMDDHHMMSSの形式の時間です（2019年、月08日、21日、19日など）:25:。*

* &lt;>チャネルタイプ&#x200B;*/は、クリックまたは露出を担当するチャネルタイプです。*

   * `d` DSPディスプレイ広告のクリック（クリックスルーを表示）
   * `i` (DSPディスプレイ広告のインプレッション)
   * `s` 検索広告のクリック（検索のクリックスルー）。

例： `EF `ID:WcmibgAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>EF IDでは大文字と小文字が区別されます。 [!DNL Analytics]実装によってURLの追跡が強制的に小文字に変換された場合、Advertising CloudはEF IDを認識しません。 これはAdvertising Cloudの入札とレポートに影響しますが、[!DNL Analytics]内のAdvertising Cloudのレポートには影響しません。

### [!DNL Analytics]のEF IDDimension

[!DNL Analytics]レポートでは、[!UICONTROL EF ID]ディメンションを検索し、[!UICONTROL EF ID Instance]指標を使用して、EF IDデータを見つけることができます。

`EF IDs` Analysis Workspaceでは、500,000個の一意の識別子の制限が適用されます。500,000個の値に達すると、すべての新しいトラッキングコードが1行項目のタイトル「[!UICONTROL Low Traffic]」でレポートされます。 レポートの正確性が欠落する可能性があるので、`EF IDs`は分類されないので、[!DNL Analytics]のセグメントやレポートには使用しないでください。

## Advertising Cloud AMO ID

AMO IDは、一意の広告の組み合わせをより詳細なレベルで追跡し、[!DNL Analytics]のデータ分類とAdvertising Cloudからの広告指標（インプレッション数、クリック数、コストなど）の取り込みに使用します。 AMO IDは、[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)またはrVarディメンション(AMO ID)に格納され、[!DNL Analytics]でのレポートにのみ使用されます。

AMO IDは`s_kwcid`とも呼ばれ、「squid」とも呼ばれます。

### [!DNL DSP]のAMO ID形式

```<Channel ID>!<Ad ID>!<Placement ID>```

ここで、

* &lt;>チャネルID *>は次のいずれかになります。*

   * `AC` = Advertising Cloud DSP
   * `AL` Advertising Cloud Search

* &lt;>広告ID *>は、Advertising Cloudで生成された広告の一意の識別子として使用されます。*&#x200B;これは、Advertising Cloudエンティティのメタデータを読み取り可能な[!DNL Analytics]ディメンションに変換するためのキーとして機能します。

* &lt;>プレースメントID *>は、Advertising Cloudで生成されたプレースメントの一意の識別子です。*&#x200B;これは、Advertising Cloudエンティティのメタデータを読み取り可能な[!DNL Analytics]ディメンションに変換するためのキーとして機能します。

<!-- <*Channel ID*>!<*Ad ID*>!<*Placement ID*>

where:

* <*Channel ID*> may be:

    * `AC` = Advertising Cloud DSP
    * `AL` for Advertising Cloud Search

* <*Ad ID*> is used an Advertising Cloud-generated unique identifier for an ad. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.

* <*Placement ID*> is an Advertising Cloud-generated unique identifier for an placement. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.
 -->

AMO IDの例：AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### [!DNL Search]のAMO ID形式

[!DNL Search]のAMO IDは、各検索エンジンに固有の形式に従います。 すべての検索エンジンの形式は、次の文字列で始まります。

```AL!{ef_userid}!{ef_sid}```

ここで、

* `AL` は、検索チャネルのチャネルIDです。
* `{ef_userid}` は、Advertising Cloudが広告主に割り当てる一意の数値ユーザーIDです。
* `{ef_sid}` は、 Advertising Cloudが指定した検索エンジンに使用する数値IDです(例え `3` ば、  [!DNL Google Ads] 、  `10` for ) [!DNL Microsoft Advertising]。

以下は、検索エンジンの完全なAMO ID形式です。 他の検索エンジンのAMO ID形式については、担当のAdobeアカウントマネージャーにお問い合わせください。

[!DNL Google Ads]のAMO ID形式：

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

ここで、

* `{creative}` は、ク [!DNL Google Ads] リエイティブの一意の数値IDです。
* `{matchtype}` は、広告をトリガーしたキーワードの一致タイプです。 `e` 正確に言えば、フレーズ `p` の場合は、部分一致の `b` 場合は。
* `{placement}` は、広告がクリックされたWebサイトのドメイン名です。値は、プレースメントターゲットキャンペーンの広告と、コンテンツサイトに表示されるキーワードターゲットキャンペーンの広告で使用できます。
* `{network}` クリックが発生したネットワークを示します。  `g` 検索(キ [!DNL Google] ーワードターゲット広告のみ)、検索パートナー（キーワードターゲット広告のみ）、または表示ネットワー `s`  `d` ク（キーワードターゲット広告またはプレースメントターゲット広告）の場合。
* `{keyword}` は、広告をトリガーした特定のキーワード（検索サイトの場合）または最も一致するキーワード（コンテンツサイトの場合）のいずれかです。

[!DNL Microsoft Advertising]のAMO ID形式：

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

ここで、

* `{AdId}` は、ク [!DNL Microsoft Advertising] リエイティブの一意の数値IDです。
* `{OrderItemId}` はキー [!DNL Microsoft Advertising] ワードの数値IDです。

### [!DNL Analytics]のAMO IDDimension

Analyticsレポートでは、[!UICONTROL AMO ID]ディメンションを検索し、[!UICONTROL AMO ID Instance]指標を使用して、AMO IDデータを見つけることができます。 [!UICONTROL AMO ID]ディメンションには、取り込まれたすべてのAMO ID値が格納されますが、[!UICONTROL AMO ID Instance]指標は、AMO ID値がサイトによって取り込まれた頻度を示します。 例えば、同じ検索広告が4回クリックされたが、Analyticsが7つのサイトエントリを追跡した場合、[!UICONTROL AMO ID Instance]は7、[!UICONTROL Clicks]は4になります。

[!DNL Analytics]内のレポートや監査に関しては、AMO IDを対応するインスタンスと共に使用することをお勧めします。 詳しくは、「[!DNL Analytics]とAdvertising Cloudの間で予想されるデータの相違」の「[ [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)のデータ検証」を参照してください。

## Analytics分類について

[!DNL Analytics]では、[分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html)は、アカウント、キャンペーン、広告など、特定のトラッキングコードのメタデータです。 Advertising Cloudでは、生のAdvertising Cloudデータが分類を使用して分類され、レポートの生成時に様々な方法（広告タイプやキャンペーン別など）でデータを表示できます。 分類は、[!DNL Analytics]のAdvertising Cloudレポートの基礎となり、[!UICONTROL AMO Cost]、[!UICONTROL AMO Impressions]、[!UICONTROL AMO Clicks]などのAMO指標や、[!UICONTROL Visits]、[!UICONTROL Leads]、[!UICONTROL Orders]、[!UICONTROL Revenue]などのカスタムおよび標準のオンサイトイベントで使用できます。

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [とAdvertising Cloudの間で予想され [!DNL Analytics] るデータの相違](data-variances.md)

