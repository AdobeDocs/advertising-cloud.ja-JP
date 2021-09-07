---
title: ' [!DNL Analytics for Advertising Cloud]のJavaScriptコード'
description: ' [!DNL Analytics for Advertising Cloud]のJavaScriptコード'
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# [!DNL Analytics for Advertising Cloud]のJavaScriptコード

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

*Advertising Cloud DSPのみの広告主*

Advertising Cloud DSPの場合、[!DNL Analytics for Advertising Cloud]統合は、ビュースルーおよびクリックスルーサイトでのインタラクションを追跡します。 クリックスルー訪問は、Webページ上の標準のAdobe Analyticsコードで追跡されます。[!DNL Analytics]コードは、ランディングページURLにAMO IDおよびEF IDパラメーターをキャプチャし、それぞれの予約済みeVarで追跡します。 Webページに2行のJavaScriptコードをデプロイすることで、ビュースルー訪問を追跡できます。

サイトへの訪問の最初のページビューで、Advertising Cloud JavaScriptコードは、訪問者が以前に広告を表示またはクリックしたことがあるかどうかを確認します。 ユーザーが以前にクリックスルー経由でサイトに入ったことがある場合、または広告を表示していない場合、訪問者は無視されます。 Advertising Cloud内で設定された[クリックルックバックウィンドウ](/help/integrations/analytics/prerequisites.md#lookback-a4adc)で、Experience Cloudを閲覧したことがあり、クリックスルーでサイトに入らない場合、Advertising Cloud JavaScriptコードは[広告IDサービス](https://experienceleague.adobe.com/docs/id-service/using/home.html)を使用して追加のID(`SDID`)を生成します。 次に、Adobe Analyticsは、広告公開に関連付けられたAMO IDとEF IDについてAdvertising Cloudを照会します。 AMO IDとEF IDは、それぞれのeVarに設定されます。 これらの値は、指定された期間（デフォルトでは60日）保持されます。

[!DNL Analytics] は、EF IDをキーとして使用して、サイトトラフィック指標（ページビュー、訪問、滞在時間など）とカスタムイベントまたは標準イベントを1時間ごと [!DNL Analytics]  にAdvertising Cloudに送信します。その後、これらの[!DNL Analytics]指標は、Advertising Cloudアトリビューションシステムを通じて実行され、コンバージョンをクリック数および露出数の履歴に結び付けます。

>[!NOTE]
>
>Advertising Cloud JavaScriptのトラッキングロジックはAdobe側で発生するので、ページの読み込み時間にはほとんど影響しません。
>
>これに対し、Advertising Cloud DSPの[!DNL DCM]データコネクタと[!DNL Analytics]（[!DNL Google Campaign Manager 360]を使用）のロジックは、クライアント側で発生します。 クライアント側のステッチでは、ページの読み込みが遅くなり、データの損失のリスクが高まります。 これは、[!DNL Analytics] JavaScriptが[!DNL DoubleClick]にpingを送信し、[!DNL DoubleClick]が最後のクリック/インプレッションデータを[!DNL Analytics]に返すのを待つ必要があるためです。 [!DNL DSP]チームが[!DNL DCM]データコネクタを設定する際に、ページの遅延時間を指定する必要があります。

## JavaScriptコードのデプロイ

JavaScriptライブラリは、[!DNL Analytics]とAdvertising Cloudが互いに通信する2つの行で構成されています。 Advertising Cloudの実装中に[!DNL Analytics for Advertising Cloud]統合が完了した場合は、このコードとデプロイ方法の説明を受け取っているはずです。

コードをまだお持ちでない場合は、Advertising Cloudサポートチームにお問い合わせください。

### コードの配置場所

追加のID(`SDID`)をAnalytics呼び出しに含めるには、 [!DNL Analytics for Advertising Cloud] JavaScript関数は、Experience CloudIDサービスの後で、Analytics App Measurementコードの前にある必要があります。

![コードの配置](/help/integrations/assets/a4adc-code-placement.png)

### コードデプロイメントの検証

以下に示すように、Advertising Cloudへのリクエストと[!DNL Analytics]へのリクエストの4つのIDの値を比較することで、任意のパケットスニッファータイプのツール（[!DNL Charles]、[!DNL Fiddler]、[!DNL Chrome Developer Tools]など）を使用して検証を実行できます。

#### [!DNL Chrome Developer Tools]でコードを確認する方法 {#validate-js-chrome}

1. [!DNL Chrome Developer Tools]を開き、「**ネットワーク**」タブをクリックします。
1. [!DNL Analytics for Advertising Cloud] JavaScriptを含むWebサイトページを読み込みます。
1. [!UICONTROL Network]タブを`last`でフィルターし、2行を確認します。

   ![最後の](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 最初の行はJavaScriptライブラリへの呼び出しで、タイトルは`last-event-tag-latest.min.js`です。
   * 2番目の行は、リクエストをAdvertising Cloudに送信する呼び出しです。 次のように始まります。`_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Advertising Cloudへの呼び出しが表示されない場合は、訪問の最初のページビューではない可能性があります。 テストの目的で、cookieを削除して、次の呼び出しが対応する訪問の最初のページビューになるようにできます。

      1. 「アプリケーション」タブで`adcloud` cookieを探し、そのcookieに`y`の値を持つ`_les_v` （最後の訪問）と、30分で期限切れになるUTCエポックタイムスタンプが含まれていることを確認します。
      1. `ad cloud` cookieを削除し、ページを更新します。
1. `/b/ss`でフィルターし、Analyticsヒットを確認します。

   ![に対するフィルター  `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. 2つのヒット間のID値を比較します。 すべての値は、Analyticsヒット内のレポートスイートID（`/b/ss/`の直後のURLパス）を除く、クエリー文字列パラメーターに含まれます。

   | ID | Analyticsパラメーター | Advertising Cloudパラメーター |
   |--- |--- |--- |
   | Experience CloudIMS組織 | `mcorgid` | `_les_imsOrgid` |
   | 追加データID | sdid | `_les_sdid` |
   | Analyticsレポートスイート | `/b/ss/`の後の値 | `_les_rsid` |
   | Experience Cloud訪問者ID | mid | `_les_mid` |

   ID値が一致する場合、JavaScriptの実装が確認されます。 Advertising Cloudは、クリックスルーまたはビュースルーの追跡の詳細が存在する場合、[!DNL Analytics]サーバーに送信します。

#### [!DNL Adobe Experience Cloud Debugger]でコードを確認する方法

1. ホームページで[[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html)を開きます。
1. 「[!UICONTROL Network]」タブに移動します。
1. [!UICONTROL Solutions Filter]ツールバーで、[!UICONTROL Advertising Cloud]と[!UICONTROL Analytics]をクリックします。
1. [!UICONTROL Request URL – Hostname]パラメーターの行で、 `lasteventf-tm.everesttech.net`を見つけます。
1. [!UICONTROL Request – Parameters*]行で、「[How to Confirm the Code with [!DNL Chrome Developer Tools]](#validate-js-chrome)」の手順3と同様に、生成されたシグナルを監査します。
   * `SDID`パラメーターがAdobe Analyticsフィルターの`Supplemental Data ID`と一致することを確認します。
   * コードが生成されない場合は、「[!UICONTROL Application]」タブでAdvertising Cloud Cookieが削除されていることを確認します。 削除したら、ページを更新し、処理を繰り返します。

   ![でのJavaScript [!DNL Analytics for Advertising Cloud] コードの監査  [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [実装の前提条件と主な情報 [!DNL Analytics for Advertising Cloud]](prerequisites.md)

