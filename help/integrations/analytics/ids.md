---
title: Advertising Cloud ID で使用 [!DNL Analytics]
description: Advertising Cloud ID で使用 [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: bfbfc293ad04b294c813ce7c8a11200e70fc812f
workflow-type: tm+mt
source-wordcount: '1156'
ht-degree: 0%

---

# Advertising Cloud ID で使用 [!DNL Analytics]

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

*Advertising Cloud DSPおよびAdvertising Cloud Searchに適用*

Advertising Cloudは、オンサイトパフォーマンストラッキングに 2 つの ID を使用します。EF ID と AMO ID。

広告インプレッションが発生すると、Advertising Cloudは AMO ID と EF ID の値を作成して保存します。 広告を閲覧した訪問者が広告をクリックせずにサイトに入ったとき、 [!DNL Analytics] は、 [!DNL Analytics for Advertising Cloud] JavaScript コード。 ビュースルートラフィックの場合、 [!DNL Analytics] は追加の ID(`SDID`) を使用します。 [!DNL Analytics]. クリックスルートラフィックの場合、これらの ID は `s_kwcid` および `ef_id` クエリー文字列パラメーター。

Advertising Cloudでは、次の条件を使用して、Web サイトへのクリックスルーエントリとビュースルーエントリを区別します。

* ビュースルーエントリは、広告を表示した後、広告をクリックせずにユーザーがサイトを訪問した場合に取り込まれます。 [!DNL Analytics] は、次の 2 つの条件を満たした場合にビュースルーを記録します。
   * 訪問者に [!DNL DSP] または [!DNL Search] 広告 [ルックバックウィンドウをクリック](#lookback-a4adc).
   * 訪問者が少なくとも 1 つの [!DNL DSP] 広告 [インプレッションルックバックウィンドウ](#lookback-a4adc). 最後のインプレッションは、ビュースルーとして渡されます。
* クリックスルーエントリは、サイト訪問者がサイトに入る前に広告をクリックした場合にキャプチャされます。 [!DNL Analytics] は、次のいずれかの条件が発生した場合にクリックスルーを取り込みます。
   * URL には、Advertising Cloudによってランディングページ URL に追加された EF ID と AMO ID が含まれます。
   * URL にはトラッキングコードは含まれていませんが、Advertising Cloud JavaScript コードが過去 2 分以内にクリックを検出しました。

![Advertising Cloudビューベース [!DNL Analytics] 統合](/help/integrations/assets/a4adc-view-through-process.png)

*図 1:Advertising Cloudビューベース [!DNL Analytics] 統合*

![Advertising Cloudのクリック URL ベース [!DNL Analytics] 統合](/help/integrations/assets/a4adc-click-through-process.png)

*図 2:Advertising Cloudのクリック URL ベース [!DNL Analytics] 統合*

## Advertising Cloud EF ID

EF ID は、アクティビティをオンラインクリックまたは広告公開に関連付けるためにAdvertising Cloudが使用する一意のトークンです。 EF ID は、 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または rVar( 予約eVar) ディメンション (Advertising Cloud EF ID) は、個々のブラウザーまたはデバイスレベルで、各広告のクリックまたは露出を追跡します。 EF ID は主に送信のキーとして機能します [!DNL Analytics] Advertising Cloud内でのレポートおよび入札の最適化のためにAdvertising Cloudにデータを送信します。

### EF ID 形式

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

ここで、

* &lt;*Advertising Cloud visitor ID*> は、訪問者ごとの一意の ID です（UhKVaABCkJ0mDt など）。 「 *サーファー ID*.

* &lt;*timestamp*> は、YYYYMMDDHHMMSS の形式の時刻です (2019 年、月 08、日 21、時刻 19 の場合は20190821192533など )。:25:33)。

* &lt;*チャネルタイプ*> は、クリックまたは露出の原因となるチャネルタイプです。

   * `d` DSPディスプレイ広告のクリック（クリックスルーを表示）
   * `i` (DSPディスプレイ広告のインプレッション（表示ビュースルー）の場合 )
   * `s` 検索広告のクリック（検索のクリックスルー）。

例 `EF `ID:WcmibgAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>EF ID では大文字と小文字が区別されます。 の [!DNL Analytics] 実装により、URL トラッキングが強制的に小文字に変換され、Advertising Cloudは EF ID を認識しません。 これは、Advertising Cloudの入札とレポートに影響しますが、内のAdvertising Cloudレポートには影響しません [!DNL Analytics].

### の EF IDDimension [!DNL Analytics]

In [!DNL Analytics] レポートでは、 [!UICONTROL EF ID] ディメンションと使用 [!UICONTROL EF ID Instance] 指標を使用します。

`EF IDs` は、Analysis Workspaceでは 500,000 個の一意の識別子の制限を受けます。 500,000 個の値に達すると、すべての新しいトラッキングコードが 1 行項目のタイトル「[!UICONTROL Low Traffic].」 レポートの正確性が失われる可能性があるので、 `EF IDs` 分類されず、でのセグメントやレポートに使用しないでください。 [!DNL Analytics].

## Advertising Cloud AMO ID

AMO ID は、より詳細なレベルで各一意の広告の組み合わせを追跡し、 [!DNL Analytics] Advertising Cloudからの広告指標（インプレッション数、クリック数、コストなど）のデータ分類と取り込み AMO ID は、 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または rVar ディメンション (AMO ID)。 [!DNL Analytics].

AMO ID は、 `s_kwcid`「イカ」とも呼ばれる。

### の AMO ID 形式 [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

ここで、

* &lt;*チャネル ID*> は次の場合があります。

   * `AC` = Advertising Cloud DSP
   * `AL` Advertising Cloud Search

* &lt;*広告 ID*> は、Advertising Cloudで生成された広告の一意の識別子を使用します。 Advertising Cloudエンティティのメタデータを読み取り可能にするキーとして機能します [!DNL Analytics] 寸法。

* &lt;*プレースメント ID*> は、Advertising Cloudで生成された配置の一意の識別子です。 Advertising Cloudエンティティのメタデータを読み取り可能にするキーとして機能します [!DNL Analytics] 寸法。

<!-- <*Channel ID*>!<*Ad ID*>!<*Placement ID*>

where:

* <*Channel ID*> may be:

    * `AC` = Advertising Cloud DSP
    * `AL` for Advertising Cloud Search

* <*Ad ID*> is used an Advertising Cloud-generated unique identifier for an ad. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.

* <*Placement ID*> is an Advertising Cloud-generated unique identifier for an placement. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.
 -->

AMO ID の例：AC!iIMvXqlOa6Nia2lDvtgw!GrV6o2oV2qQLjQiXLC7

### の AMO ID 形式 [!DNL Search]

の AMO ID [!DNL Search] 各検索エンジンに固有の形式に従います。 すべての検索エンジンの形式は、次のように始まります。

```AL!{ef_userid}!{ef_sid}```

ここで、

* `AL` は、検索チャネルのチャネル ID です。
* `{ef_userid}` は、Advertising Cloudが広告主に割り当てる一意の数値ユーザー ID です。
* `{ef_sid}` は、Advertising Cloudが指定した検索エンジンに使用する数値 ID です ( 例： `3` for [!DNL Google Ads] または `10` for [!DNL Microsoft Advertising].

次に、2 つの検索エンジンの完全な AMO ID 形式を示します。 他の検索エンジンの AMO ID 形式については、 [!DNL Adobe] アカウントマネージャー

の AMO ID 形式 [!DNL Google Ads]:

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

ここで、

* `{creative}` は [!DNL Google Ads] クリエイティブの一意な数値 ID。
* `{matchtype}` は、広告をトリガーしたキーワードの一致タイプです。 `e` 正確には `p` ( フレーズの場合、または `b` 幅広く
* `{placement}` は、広告がクリックされた Web サイトのドメイン名です。 値は、プレースメントターゲットキャンペーンの広告と、コンテンツサイトに表示されるキーワードターゲットキャンペーンの広告で使用できます。
* `{network}` クリックの発生元のネットワークを示します。  `g` for [!DNL Google] 検索（キーワードターゲット広告のみ） `s` （キーワードターゲットの広告のみ）または `d` （キーワードターゲット広告またはプレースメントターゲット広告のいずれか）を設定します。
* `{keyword}` は、広告をトリガーした特定のキーワード（検索サイトの場合）または最も一致するキーワード（コンテンツサイトの場合）です。

の AMO ID 形式 [!DNL Microsoft Advertising]:

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

ここで、

* `{AdId}` は [!DNL Microsoft Advertising] クリエイティブの一意な数値 ID。
* `{OrderItemId}` は [!DNL Microsoft Advertising] キーワードの数値 ID。

### での AMO IDDimension [!DNL Analytics]

Analytics レポートで、 [!UICONTROL AMO ID] ディメンションと使用 [!UICONTROL AMO ID Instance] 指標を使用します。 10. [!UICONTROL AMO ID] ディメンションには、取り込まれたすべての AMO ID 値が格納されますが、 [!UICONTROL AMO ID Instance] 指標は、AMO ID 値がサイトによってキャプチャされた頻度を示します。 例えば、同じ検索広告が 4 回クリックされたが、Analytics が 7 つのサイトエントリを追跡した場合、 [!UICONTROL AMO ID Instance] 7 (7) で [!UICONTROL Clicks] は 4(4) になります。

内の任意のレポートまたは監査 [!DNL Analytics]を使用する場合、ベストプラクティスは、AMO ID を対応するインスタンスと共に使用することです。 詳しくは、[のデータ検証 [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)」(「 [!DNL Analytics] Advertising Cloud」

## Analytics 分類について

In [!DNL Analytics]、 [分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) は、アカウント、キャンペーン、広告など、特定のトラッキングコードのメタデータです。 Advertising Cloudは、分類を使用して生のAdvertising Cloudデータを分類し、レポートの生成時に様々な方法（広告タイプやキャンペーンなど）でデータを表示できるようにします。 分類は、 [!DNL Analytics] およびは、 [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]および [!UICONTROL AMO Clicks]と同様に、 [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]および [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [～間で予想されるデータの相違 [!DNL Analytics] とAdvertising Cloud](data-variances.md)

