---
title: の基本 [!DNL Marketing Channels]
description: 以下に関する主な情報を学ぶ： [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising Cloud] ユーザーは理解する必要があります。
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# の基本 [!DNL Analytics Marketing Channels]

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

このページでは、 [!DNL Analytics Marketing Channels] その [!DNL Analytics for Advertising Cloud] ユーザーは理解する必要があります。

に関する完全なドキュメントについては、 [!DNL Marketing Channels]を参照してください。[使用の手引き [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## の概要 [!DNL Marketing Channels]

[!DNL Marketing Channels] はAdobe Analyticsの主要機能です。 [!DNL Marketing Channels] レポートは、レポートウィンドウを使用して顧客が web サイトに到達した方法と、各チャネルが売上高やオンサイト行動に与える影響を示します。

次に、クロス訪問のジャーニーの例を示します。 Web サイトへの各訪問は、訪問者が訪問したマーケティングチャネルによって示されます。 最初の訪問は、ファーストタッチチャネルとも呼ばれ、電子メールです。 訪問時に表示 2 は参加チャネルで、自然検索はラストタッチチャネルと見なされます。 次を使用する場合、 [!UICONTROL Last Touch Attribution] 範囲 [!UICONTROL Attribution IQ]に値を指定しない場合、自然検索は 250 ドルのコンバージョンイベントのフルクレジットを受け取ります。 Experience CloudID サービスを使用すると、これらの個々の訪問を結び付けて、1 人の訪問者が 1 つのジャーニーを示すことができます。

![マーケティングチャネルでのクロス訪問コンバージョンジャーニーの例](/help/integrations/assets/a4adc-mc-sample-journey.png)

次を使用： [!UICONTROL Marketing Channels] 処理ルールでは、トラフィックを促すチャネルを決定する一連のロジックを作成し、ユーザーがサイトに来訪したときに各チャネルを追跡することができます。 例えば、 [!UICONTROL Email] チャネルは、Adobe Analyticsが訪問の分類に使用し、クリック時に生成される一意のトラッキングコードによって示されます。このコードが電子メールマーケティングキャンペーンからの訪問として分類されます。

## 処理ルールとマーケティングチャネルの設定方法

ユーザーが Web サイトにアクセスするたびに、URL を使用して、アドレスバーをクリックするか直接入力します。 ユーザーが Web サイトに入ると、 [!DNL Analytics] は、訪問の原因となったチャネルを判断するために使用できる情報を追跡します。

多くの場合、マーケターは、チャネルがサイトに与える影響を追跡するのに役立つクエリー文字列パラメーターのトラッキングコードをチャネル URL に追加します。 次の項目を設定できます。 [!DNL Marketing Channels] 処理ルールを使用して、特定のトラッキングパラメーターと値をリッスンし、追加のトラッキングをおこなわずにチャネルを決定します。 例えば、すべての電子メールキャンペーン URL が次のフォーマットに従っている場合、 `www.adobe.com?cid=email…` （URL にはクエリー文字列パラメーターと値が含まれます） `cid=email`) が含まれている場合、このトラッキングコードをリッスンし、で訪問をグループ化するルールを作成できます。 [!UICONTROL Email] チャネル。

その他のチャネルには追跡可能な URL パスがないので、識別にさらにロジックが必要です。 例： [!UICONTROL Earned Social]は、ユーザーがソーシャルネットワーク上で別のユーザーが有機的に共有したリンクをクリックすることを、追跡するための重要なチャネルです。 ただし、マーケターは、共有されている URL にクエリー文字列パラメータートラッキングコードを追加する方法はありません。 この場合、関心のあるソーシャルネットワークの参照ドメインと有料トラッキングコードの不在をリッスンしてチャネルを決定する処理ルールを作成できます。 これらの要件を満たす訪問は、マーケティングチャネルレポート内で獲得ソーシャルとして追跡されます。

Adobeは、Analytics チームと協力して、 [!DNL Marketing Channels] 処理ルールを使用して、ビジネスに関連するすべてのチャネルを追跡します。 これにより、強力なアトリビューションレポートを作成できます。

Advertising Cloudがカスタムマーケティングチャネルの作成に必要なシグナルにどのように貢献できるかについては、[広告 ID を使用した作成 [!DNL Marketing Channels] ルール](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Advertising Cloud ID を使用した作成 [!DNL Marketing Channels] 処理ルール](mc-ids.md)
>* [Advertising Cloudと [!DNL Marketing Channels]](mc-data-variances.md)
>* [使用 [!DNL Analytics Marketing Channels] Advertising Cloud Data を使用](mc-ac-data.md)
>* [ビデオ：Advertising Cloudを使用したレポート [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [の概要 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

