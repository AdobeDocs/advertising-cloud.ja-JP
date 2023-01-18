---
title: Adobe広告 ID が [!DNL Analytics]
description: Adobe広告 ID が [!DNL Analytics]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 0%

---

# Adobe広告 ID が [!DNL Analytics]

*Advertising とAdobe AnalyticsのAdobeの統合のみの広告主*

*Advertising DSPおよび[!DNL Advertising Search]*

Adobe広告は、オンサイトパフォーマンストラッキングに 2 つの ID を使用します。の *EF ID* そして *AMO ID*.

広告インプレッションが発生すると、Adobe広告は AMO ID と EF ID の値を作成して保存します。 広告を閲覧した訪問者が広告をクリックせずにサイトに入ったとき、 [!DNL Analytics] は、を通じてこれらの値をAdobe広告から呼び出します。 [!DNL Analytics for Advertising] JavaScript コード。 ビュースルートラフィックの場合、 [!DNL Analytics] は追加の ID(`SDID`) で始まり、EF ID と AMO ID をステッチするために使用されます。 [!DNL Analytics]. クリックスルートラフィックの場合、これらの ID は `s_kwcid` および `ef_id` クエリー文字列パラメーター。

Adobe広告は、次の条件を使用して、Web サイトへのクリックスルーエントリとビュースルーエントリを区別します。

* ビュースルーエントリは、広告を表示した後、広告をクリックせずにユーザーがサイトを訪問した場合にキャプチャされます。 [!DNL Analytics] は、次の 2 つの条件を満たした場合にビュースルーを記録します。
   * 訪問者には、 [!DNL DSP] または [!DNL Search] 広告 [ルックバックウィンドウをクリック](#lookback-a4adc).
   * 訪問者が少なくとも 1 つを閲覧しました [!DNL DSP] 広告 [インプレッションのルックバックウィンドウ](#lookback-a4adc). 最後のインプレッションは、ビュースルーとして渡されます。
* クリックスルーエントリは、サイト訪問者がサイトに入る前に広告をクリックするとキャプチャされます。 [!DNL Analytics] は、次のいずれかの条件が発生した場合にクリックスルーをキャプチャします。
   * この URL には、Adobe広告によってランディングページ URL に追加された EF ID と AMO ID が含まれます。
   * URL にトラッキングコードは含まれていませんが、Adobe広告の JavaScript コードが過去 2 分以内にクリックを検出しました。

![Adobe広告ビューベース [!DNL Analytics] 統合](/help/integrations/assets/a4adc-view-through-process.png)

*図 1:Adobe広告ビューベース [!DNL Analytics] 統合*

![Adobe広告のクリック URL ベース [!DNL Analytics] 統合](/help/integrations/assets/a4adc-click-through-process.png)

*図 2:Adobe広告のクリック URL ベース [!DNL Analytics] 統合*

## Adobe広告 EF ID

EF ID は、Adobe広告がアクティビティをオンラインクリックまたは広告露出に関連付けるために使用する一意のトークンです。 EF ID は、 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または rVar( 予約eVar) ディメンション (Adobe広告 EF ID) を使用して、個々のブラウザーまたはデバイスレベルで各広告のクリックまたは露出を追跡します。 EF ID は主に送信のキーとして機能します [!DNL Analytics] データをAdobe広告に変換し、Adobe広告内でのレポートおよび入札の最適化を行います。

### EF ID 形式

>[!NOTE]
>
>EF ID では大文字と小文字が区別されます。 次の場合、 [!DNL Analytics] 実装により、URL トラッキングが強制的に小文字に変換され、Adobe広告は EF ID を認識しません。 これは、Adobe広告の入札とレポートに影響しますが、内のAdobe広告レポートには影響しません [!DNL Analytics].

#### [!DNL Google Ads] 広告を検索

```{gclid}:G:s```

場所：

* `gclid` が [!DNL Google Click ID] (GCLID) を使用します。
* `s` はネットワークタイプです（「s」は検索用）。

#### Microsoft Advertising 検索広告

```{msclkid}:G:s```

場所：

* `msclkid` が [!DNL Microsoft Click ID] (MSCLKID)。
* `s` はネットワークタイプです（「s」は検索用）。

#### 他の検索エンジンでの広告と検索広告の表示

```<Adobe Advertising visitor ID>:<timestamp>:<channel type>```

場所：

* &lt;*Adobe広告訪問者 ID*> は、訪問者ごとの一意の ID です（UhKVaAABCkJ0mDt など）。 「 *サーファー ID*.

* &lt;*timestamp*> は、YYYYMMDDHHMMSS という形式の時刻です (2019 年の場合は20190821192533、08 月の場合は 21 日、19 時など )。:25:33).

* &lt;*チャネルタイプ*> は、クリックまたは露出の原因となるチャネルタイプです。

   * `d` DSPディスプレイ広告のクリック（クリックスルーを表示）
   * `i` DSPディスプレイ広告のインプレッション（表示ビュースルー）の場合
   * `s` 検索広告のクリック（検索クリックスルー）。

例 `EF `ID:WcmibgAAHJK1RyY:1551968087687:d

### の EF IDDimension [!DNL Analytics]

In [!DNL Analytics] レポートでは、EF ID データを検索するには、 [!UICONTROL EF ID] ディメンションと使用 [!UICONTROL EF ID Instance] 指標。

EF ID には、Analysis Workspaceでの 500,000 個の一意の ID 制限が適用されます。 500,000 個の値に達すると、すべての新しいトラッキングコードが 1 行項目のタイトル「[!UICONTROL Low Traffic].&quot; レポートの正確性が欠落する可能性があるので、EF ID は分類されず、でのセグメントやレポートに使用しないでください [!DNL Analytics].

## Adobe広告 AMO ID

AMO ID は、より詳細なレベルで一意の広告の組み合わせを追跡し、 [!DNL Analytics] 広告指標（インプレッション数、クリック数、コストなど）のデータ分類とAdobe広告からの取り込み AMO ID は、 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または rVar ディメンション (AMO ID)。でのレポートにのみ使用されます。 [!DNL Analytics].

AMO ID は、 `s_kwcid`(「[!DNL the squid].&quot;

### の AMO ID フォーマット [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

場所：

* &lt;*チャネル ID*> は次のいずれかになります。

   * `AC` = Advertising DSP
   * `AL` 対象 [!DNL Advertising Search]

* &lt;*広告 ID*> は、広告に対してAdobe広告で生成された一意の識別子を使用します。 AdobeAdvertising エンティティのメタデータを読み取り可能に変換するためのキーとして機能します [!DNL Analytics] ディメンション。

* &lt;*プレースメント ID*> は、Adobe広告で生成されたプレースメントの一意の識別子です。 AdobeAdvertising エンティティのメタデータを読み取り可能に変換するためのキーとして機能します [!DNL Analytics] ディメンション。

AMO ID の例：AC!iIMvXqlOa6Nia2lDvtgw!GrV6o2oV2qQLjQiXLC7

### の AMO ID フォーマット [!DNL Search]

の AMO ID [!DNL Search] 各検索エンジンで異なる形式に従います。 すべての検索エンジンの形式は、次のように始まります。

```AL!{userid}!{sid}```

場所：

* `AL` は、広告ネットワークのチャネル ID です。
* `{userid}` は、広告主に割り当てられる一意の数値AdobeID です。
* `{sid}` は、Adobe広告が指定した広告ネットワークに使用する数値 ID です（例： ）。 `3` 対象 [!DNL Google Ads] または `10` 対象 [!DNL Microsoft Advertising].

以下は、いくつかの広告ネットワークの完全な AMO ID 形式です。 その他の広告ネットワーク向けの AMO ID の形式については、 [!DNL Adobe] アカウントチーム。

の AMO ID フォーマット [!DNL Google Ads]:

```AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

場所：

* `{creative}` が [!DNL Google Ads] クリエイティブの一意の数値 ID。
* `{matchtype}` は、広告をトリガーしたキーワードの一致タイプです。 `e` 正確には `p` ( フレーズの場合は、 `b` 幅の広い
* `{placement}` は、広告がクリックされた Web サイトのドメイン名です。 値は、配置ターゲットキャンペーンの広告と、コンテンツサイトに表示されるキーワードターゲットキャンペーンの広告で使用できます。
* `{network}` クリック元のネットワークを示します。  `g` 対象 [!DNL Google] 検索（キーワードターゲット広告のみ） `s` 検索パートナー（キーワードターゲット広告のみ）、または `d` ディスプレイネットワーク用（キーワードターゲット広告またはプレースメントターゲット広告用）。
* `{keyword}` は、（検索サイトで）広告をトリガーした特定のキーワードか、（コンテンツサイトで）最適なキーワードのどちらかです。

の AMO ID フォーマット [!DNL Microsoft Advertising]:

```AL!{userid}!{sid}!{AdId}!{OrderItemId}```

場所：

* `{AdId}` が [!DNL Microsoft Advertising] クリエイティブの一意の数値 ID。
* `{OrderItemId}` が [!DNL Microsoft Advertising] キーワードの数値 ID。

### AMO IDDimension（内） [!DNL Analytics]

Analytics レポートでは、 [!UICONTROL AMO ID] ディメンションと使用 [!UICONTROL AMO ID Instance] 指標。 この [!UICONTROL AMO ID] ディメンションには、取得されたすべての AMO ID 値が格納されますが、 [!UICONTROL AMO ID Instance] 指標は、AMO ID 値がサイトによってキャプチャされた頻度を示します。 例えば、同じ検索広告が 4 回クリックされたが、Analytics が 7 つのサイトエントリを追跡した場合、 [!UICONTROL AMO ID Instance] 7 歳で [!UICONTROL Clicks] は 4(4) です。

内の任意のレポートまたは監査 [!DNL Analytics]を使用する場合、ベストプラクティスは、AMO ID を対応するインスタンスと共に使用することです。 詳しくは、[のデータ検証 [!DNL Analytics for Advertising]](data-variances.md#data-validation)」(「 [!DNL Analytics] Adobe広告」

## Analytics 分類について

In [!DNL Analytics], a [分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) は、アカウント、キャンペーン、広告など、特定のトラッキングコードのメタデータの一部です。 Adobe広告は、レポートを生成する際に様々な方法（広告タイプやキャンペーン別など）でデータを表示できるように、分類を使用して生のAdobe広告データを分類します。 分類は、 [!DNL Analytics] とは、AMO 指標と共に使用できます。例： [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]、および [!UICONTROL AMO Clicks]、およびのようなカスタムおよび標準のオンサイトイベント [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]、および [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [A と B の間で予想されるデータの相違 [!DNL Analytics] およびAdobe広告](data-variances.md)

