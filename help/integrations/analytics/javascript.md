---
title: 用 JavaScript コード [!DNL Analytics for Advertising]
description: 用 JavaScript コード [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 用 JavaScript コード [!DNL Analytics for Advertising]

*Advertising とAdobe AnalyticsのAdobeの統合のみの広告主*

*Advertising DSPのみの広告主*

Advertising DSPの場合、 [!DNL Analytics for Advertising] 統合は、ビュースルーおよびクリックスルーサイトのインタラクションを追跡します。 クリックスルー訪問は、Web ページ上の標準のAdobe Analyticsコードで追跡されます。の [!DNL Analytics] コードはランディングページ URL に AMO ID および EF ID パラメーターをキャプチャし、それぞれの予約済み eVar で追跡します。 Web ページに JavaScript スニペットをデプロイすることで、ビュースルー訪問を追跡できます。

サイトへの訪問の最初のページビューで、Adobe広告の JavaScript コードは、訪問者が以前に広告を閲覧またはクリックしたかどうかを確認します。 ユーザーが以前にクリックスルーでサイトに入ったことがある場合や、広告を表示していない場合、訪問者は無視されます。 訪問者が広告を閲覧した後、 [ルックバックウィンドウをクリック](/help/integrations/analytics/prerequisites.md#lookback-a4adc) をAdobe広告内に設定すると、Adobe広告 JavaScript コード a) は、 [Experience CloudID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html) 追加の ID(`SDID`) または b) Adobe Experience Platformを使用 [!DNL Web SDK] `generateRandomID` メソッドを使用して `[!DNL StitchID]`. どちらの ID を使用しても、Adobe広告から訪問者のAdobe Analyticsヒットにデータをステッチできます。 次に、Adobe Analyticsは、Adobe露出に関連付けられた AMO ID および EF ID に対して広告をクエリします。 AMO ID と EF ID は、それぞれの eVar に入力されます。 これらの値は、指定された期間（デフォルトでは 60 日）保持されます。

[!DNL Analytics] サイトトラフィック指標（ページビュー数、訪問回数、滞在時間など）と [!DNL Analytics] EF ID をキーとして使用し、Adobe広告に対するカスタムイベントまたは標準イベントを 1 時間ごとに追加します。 これら [!DNL Analytics] 指標を使用してから、Adobe広告アトリビューションシステムを実行し、コンバージョンをクリック数および露出数の履歴に接続します。

>[!NOTE]
>
>Adobe広告の JavaScript トラッキングロジックはAdobe側で発生するので、ページの読み込み時間にほとんど影響しません。
>
>これに対し、 [!DNL DCM] データコネクタ [!DNL Analytics] ( [!DNL Google Campaign Manager 360])Advertising DSPの場合は、クライアント側で発生します。 クライアント側のステッチでは、ページの読み込みが遅くなり、データの損失のリスクが高まります。 これは、 [!DNL Analytics] JavaScript は ping が必要 [!DNL DoubleClick] 待つ [!DNL DoubleClick] を呼び出して、最後のクリック/インプレッションデータを [!DNL Analytics]. 次の場合、 [!DNL DSP] チームが設定 [!DNL DCM] data connector を使用する場合は、ページの遅延時間を指定する必要があります。

## JavaScript コードのデプロイ

JavaScript ライブラリは、 [!DNL Analytics] およびAdobe広告を使用して相互に通信を行います。 この [!DNL Analytics for Advertising] の統合は、Adobe広告の実装中に完了したので、このコードとデプロイ方法の手順を既に受け取っているはずです。

### コード

#### Experience CloudID サービスを使用する実装 `visitorAPI.js` コード

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

#### Experience Platform [!DNL Web SDK] `alloy.js`コード

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### コードの配置場所

この [!DNL Analytics for Advertising] 追加の ID(`SDID`) または `[!DNL StitchID]` を Analytics 呼び出しに含めることができます。

![コードの配置](/help/integrations/assets/a4adc-code-placement.png)

### コードのデプロイメントの検証

任意の種類のパケットスニファー ( [!DNL Charles], [!DNL Fiddler]または [!DNL Chrome Developer Tools]) を比較することで、Adobe広告を表示するリクエストと [!DNL Analytics]（以下に概要を示します）

#### を使用してコードを確認する方法 [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. 開く [!DNL Chrome Developer Tools] をクリックし、 **ネットワーク** タブをクリックします。

1. を含む Web サイトページを読み込みます [!DNL Analytics for Advertising] JavaScript。

1. フィルター [!UICONTROL Network] タブの基準 `last` とで、2 つの行を確認します。

   ![最後のフィルター](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 最初の行は JavaScript ライブラリへの呼び出しで、タイトルは `last-event-tag-latest.min.js`.
   * 2 番目の行は、リクエストをAdobe広告に送信する呼び出しです。 最初は次のようになります。 `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Adobe広告への呼び出しが表示されない場合は、訪問の最初のページビューでない可能性があります。 テストの目的で、cookie を削除して、次の呼び出しが対応する訪問の最初のページビューになるようにできます。

      1. 「アプリケーション」タブで、 `adcloud` cookie を確認し、cookie に `_les_v` （最後の訪問）の値が `y` と、30 分で期限切れになる UTC エポックタイムスタンプ。
      1. を削除します。 `ad cloud` cookie を更新し、ページを更新します。

1. (Experience CloudID サービスを使用する実装 ) `visitorAPI.js` コード ) フィルター `/b/ss` をクリックして Analytics ヒットを確認します。

   ![フィルター `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Experience Platform [!DNL Web SDK] `alloy.js`コード ) フィルター `/interact` を使用して、Edge ネットワークへのリクエストペイロードにが含まれていることを確認します。 `advertisingStitchID`.

   ![フィルター `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. 2 つのヒット間で ID 値を比較します。 すべての値は、Analytics ヒット内のレポートスイート ID（の直後の URL パス）を除く、クエリー文字列パラメーターに含まれます `/b/ss/`.

   | ID | Analytics パラメーター | Edge Network | Adobe広告パラメーター |
   | --- | --- | --- | --- |
   | Experience CloudIMS Org | `mcorgid` |  | `_les_imsOrgid` |
   | 追加データ ID | sdid |  | `_les_sdid` |
   | ステッチ ID | stitchId | `advertisingStitchID` の下に `_adcloud` プロパティ |  |
   | Analytics レポートスイート | 次の後の値 `/b/ss/` |  | `_les_rsid` |
   | Experience Cloud訪問者 ID | mid |  | `_les_mid` |

   ID 値が一致する場合、JavaScript の実装が確認されます。 Adobe広告が [!DNL Analytics] クリックスルーまたはビュースルートラッキングの詳細（存在する場合）をサーバーに送信します。

#### を使用してコードを確認する方法 [!DNL Adobe Experience Cloud Debugger]

1. を開きます。 [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) をホームページに追加します。
1. 次に移動： [!UICONTROL Network] タブをクリックします。
1. 内 [!UICONTROL Solutions Filter] ツールバー、クリック [!UICONTROL Adobe Advertising] および [!UICONTROL Analytics].
1. 内 [!UICONTROL Request URL – Hostname] パラメータ行、を見つけます。 `lasteventf-tm.everesttech.net`.
1. 内 [!UICONTROL Request – Parameters] 行で、生成されたシグナルを監査します。「[を使用してコードを確認する方法 [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Experience CloudID サービスを使用する実装 ) `visitorAPI.js` コード ) `Sdid` パラメーターは `Supplemental Data ID` (Adobe Analyticsフィルター )
   * (Experience Platform [!DNL Web SDK] `alloy.js`コード ) `advertisingStitchID` パラメーターは `Sdid` をExperience PlatformEdge ネットワークに送信しました。
   * コードが生成されない場合は、Adobe広告 cookie が [!UICONTROL Application] タブをクリックします。 削除したら、ページを更新し、処理を繰り返します。

   ![監査 [!DNL Analytics for Advertising] の JavaScript コード [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [実装の前提条件と主な情報 [!DNL Analytics for Advertising]](prerequisites.md)

