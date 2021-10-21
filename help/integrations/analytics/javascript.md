---
title: 用 JavaScript コード [!DNL Analytics for Advertising Cloud]
description: 用 JavaScript コード [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 26709071be0fffb43bb3fa4666c6fa52229ad5be
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# 用 JavaScript コード [!DNL Analytics for Advertising Cloud]

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

*Advertising Cloud DSPのみの広告主*

Advertising Cloud DSPの場合、 [!DNL Analytics for Advertising Cloud] 統合は、ビュースルーおよびクリックスルーサイトのインタラクションを追跡します。 クリックスルー訪問は、Web ページ上の標準のAdobe Analyticsコードで追跡されます。ザ [!DNL Analytics] コードは、ランディングページ URL に AMO ID および EF ID パラメーターをキャプチャし、それぞれの予約済み eVar で追跡します。 Web ページに 2 行の JavaScript コードをデプロイすることで、ビュースルー訪問を追跡できます。

サイトへの訪問の最初のページビューで、Advertising Cloud JavaScript コードは、訪問者が以前に広告を表示またはクリックしたかどうかを確認します。 ユーザーが以前にクリックスルー経由でサイトに入ったことがある場合や、広告を表示していない場合、訪問者は無視されます。 訪問者が広告を閲覧したことがあり、 [ルックバックウィンドウをクリック](/help/integrations/analytics/prerequisites.md#lookback-a4adc) をAdvertising Cloud内で設定すると、Advertising Cloud JavaScript コードは [Experience CloudID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html) 追加の ID(`SDID`) と呼ばれ、Advertising Cloudから訪問者のAdobe Analyticsヒットにデータをステッチするのに使用されます。 次に、Advertising Cloudに対して、広告公開に関連付けられた AMO ID と EF ID を問い合わせます。 AMO ID と EF ID は、それぞれの eVar に設定されます。 これらの値は、指定された期間（デフォルトでは 60 日間）保持されます。

[!DNL Analytics] は、サイトトラフィック指標（ページビュー数、訪問回数、滞在時間など）と [!DNL Analytics] EF ID をキーとして使用し、Advertising Cloudに 1 時間ごとに追加したカスタムイベントまたは標準イベント。 これら [!DNL Analytics] 次に、指標はAdvertising Cloudアトリビューションシステムを通じて実行され、コンバージョンをクリック数および露出数の履歴と結び付けます。

>[!NOTE]
>
>Advertising Cloud JavaScript のトラッキングロジックはAdobe側で発生するので、ページの読み込み時間にはほとんど影響しません。
>
>これに対して、 [!DNL DCM] データコネクタ [!DNL Analytics] ( [!DNL Google Campaign Manager 360]) がAdvertising Cloud DSPに対して発生します。 クライアント側のステッチでは、ページの読み込みが遅くなり、データの損失のリスクが高まります。 これは、 [!DNL Analytics] JavaScript must ping [!DNL DoubleClick] そして待つ [!DNL DoubleClick] 最後のクリック/インプレッションデータをに渡すには [!DNL Analytics]. 使用する [!DNL DSP] チームが設立する [!DNL DCM] data connector の場合は、ページの遅延時間を指定する必要があります。

## JavaScript コードのデプロイ

JavaScript ライブラリは、 [!DNL Analytics] Advertising Cloudは互いにコミュニケーションを取る を [!DNL Analytics for Advertising Cloud] 統合は、Advertising Cloudの実装中に完了したので、このコードとデプロイ方法の説明を受け取っているはずです。

コードをまだお持ちでない場合は、Advertising Cloudサポートチームにお問い合わせください。

### コードの配置場所

10. [!DNL Analytics for Advertising Cloud] JavaScript 関数は、Experience CloudID サービスの後、追加の ID(`SDID`) を Analytics 呼び出しに含めることができます。

![コードの配置](/help/integrations/assets/a4adc-code-placement.png)

### コードのデプロイメントの検証

任意の種類のパケットスニファーツール ( [!DNL Charles], [!DNL Fiddler]または [!DNL Chrome Developer Tools]) を比較することで、Advertising Cloudに送信されるリクエストと [!DNL Analytics]以下に示すように。

#### でコードを確認する方法 [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. 開く [!DNL Chrome Developer Tools] をクリックし、 **ネットワーク** タブに移動します。
1. を含む Web サイトページを読み込みます。 [!DNL Analytics for Advertising Cloud] JavaScript。
1. フィルター [!UICONTROL Network] タブで `last` と 2 つの行を確認します。

   ![最後の](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 最初の行は JavaScript ライブラリの呼び出しで、タイトルは `last-event-tag-latest.min.js`.
   * 2 番目の行は、要求をAdvertising Cloudに送信する呼び出しです。 次のように始まります。 `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Advertising Cloudへの呼び出しが表示されない場合は、訪問の最初のページビューではない可能性があります。 テストの目的で、cookie を削除して、次の呼び出しが対応する訪問の最初のページビューになるようにできます。

      1. 「アプリケーション」タブで、 `adcloud` Cookie を設定し、Cookie に `_les_v` （最後の訪問）の値が `y` と、30 分で期限切れになる UTC エポックタイムスタンプ。
      1. を削除します。 `ad cloud` cookie を更新し、ページを更新します。
1. フィルター条件 `/b/ss` をクリックして、Analytics ヒットを確認します。

   ![に対するフィルター `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. 2 つのヒット間の ID 値を比較します。 すべての値は、Analytics ヒット内のレポートスイート ID（の直後の URL パス）を除く、クエリー文字列パラメーターに含まれます `/b/ss/`.

   | ID | Analytics パラメーター | Advertising Cloud Parameter |
   |--- |--- |--- |
   | Experience CloudIMS 組織 | `mcorgid` | `_les_imsOrgid` |
   | 追加データ ID | sdid | `_les_sdid` |
   | Analytics レポートスイート | の後の値 `/b/ss/` | `_les_rsid` |
   | Experience Cloud訪問者 ID | mid | `_les_mid` |

   ID 値が一致する場合、JavaScript の実装が確認されます。 Advertising Cloudが [!DNL Analytics] クリックスルーまたはビュースルーの追跡の詳細（存在する場合）がサーバーに送信されます。

#### でコードを確認する方法 [!DNL Adobe Experience Cloud Debugger]

1. を開きます。 [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) をホームページに貼り付けます。
1. に移動します。 [!UICONTROL Network] タブに表示されます。
1. の [!UICONTROL Solutions Filter] ツールバーで、 [!UICONTROL Advertising Cloud] および [!UICONTROL Analytics].
1. の [!UICONTROL Request URL – Hostname] パラメータ行、 `lasteventf-tm.everesttech.net`.
1. の [!UICONTROL Request – Parameters*] 行では、「[でコードを確認する方法 [!DNL Chrome Developer Tools]](#validate-js-chrome).」
   * を確認し、 `SDID` パラメータは `Supplemental Data ID` (Adobe Analyticsフィルター )。
   * コードが生成されない場合は、Advertising Cloud Cookie が [!UICONTROL Application] タブに移動します。 削除したら、ページを更新し、処理を繰り返します。

   ![監査 [!DNL Analytics for Advertising Cloud] の JavaScript コード [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [実装の前提条件と主な情報 [!DNL Analytics for Advertising Cloud]](prerequisites.md)

