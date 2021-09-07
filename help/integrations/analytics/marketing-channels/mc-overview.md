---
title: ' [!DNL Marketing Channels]の基本'
description: ' [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising Cloud] ユーザーが理解する必要がある主な情報を説明します。'
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# [!DNL Analytics Marketing Channels]の基本

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

このページでは、[!DNL Analytics for Advertising Cloud]ユーザーが理解する必要がある[!DNL Analytics Marketing Channels]に関する主な情報を説明します。

[!DNL Marketing Channels]に関する完全なドキュメントについては、「[ [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html)で始める」を参照してください。

## [!DNL Marketing Channels]の概要

[!DNL Marketing Channels] は、Adobe Analyticsの主な機能です。[!DNL Marketing Channels] レポートは、レポートウィンドウを使用して顧客がwebサイトに到達した方法と、各チャネルが売上高やオンサイト行動に及ぼす影響を示します。

次に、クロス訪問のジャーニーの例を示します。 Webサイトへの各訪問は、訪問者が入ったマーケティングチャネルによって示されます。 最初の訪問は、ファーストタッチチャネルとも呼ばれ、電子メールです。 「訪問時に表示」 2つは参加チャネルで、「自然検索」はラストタッチチャネルと見なされます。 [!UICONTROL Attribution IQ]内で[!UICONTROL Last Touch Attribution]を使用すると、自然検索は$250のコンバージョンイベントのフルクレジットを受け取ります。 Experience CloudIDサービスを使用すると、これらの個々の訪問を結び付けて、1人の訪問者が1つのジャーニーを表示できます。

![マーケティングチャネルでのクロス訪問コンバージョンジャーニーの例](/help/integrations/assets/a4adc-mc-sample-journey.png)

[!UICONTROL Marketing Channels]処理ルールを使用すると、トラフィックを駆動するチャネルを決定するロジックのセットを作成し、ユーザーがサイトに来訪したときに各チャネルを追跡できます。 例えば、[!UICONTROL Email]チャネルは、Adobe Analyticsが訪問者を電子メールマーケティングキャンペーンからの訪問として分類するクリック時に生成される一意のトラッキングコードで示されます。

## 処理ルールとマーケティングチャネルの設定方法

ユーザーがWebサイトにアクセスするたびに、アドレスバーをクリックするか直接入力するURLを使用します。 ユーザーがWebサイトに入ると、[!DNL Analytics]は、訪問の原因となったチャネルを特定するために使用できる情報を追跡します。

多くの場合、マーケターは、チャネルがサイトに与える影響を追跡するのに役立つように、クエリー文字列パラメーターのトラッキングコードをチャネルURLに追加します。 [!DNL Marketing Channels]処理ルールを設定して、特定のトラッキングパラメーターと値をリッスンし、追加のトラッキングをおこなわずにチャネルを決定できます。 例えば、すべての電子メールキャンペーンURLが`www.adobe.com?cid=email…`（URLにクエリー文字列パラメーターと値`cid=email`が含まれる）の形式に従う場合、このトラッキングコードをリッスンし、[!UICONTROL Email]チャネルで訪問をバケット化するルールを作成できます。

その他のチャネルにはトラッキング可能なURLパスがなく、識別のための追加ロジックが必要です。 例えば、ユーザーがソーシャルネットワーク上で別のユーザーが有機的に共有したリンクをクリックする[!UICONTROL Earned Social]は、追跡する重要なチャネルです。 ただし、マーケターは、共有されているURLにクエリー文字列パラメータートラッキングコードを追加する方法はありません。 この場合、関心のあるソーシャルネットワークの参照ドメインと、有料トラッキングコードのないことをリッスンしてチャネルを決定する処理ルールを作成できます。 これらの要件を満たす訪問は、マーケティングチャネルレポート内で獲得ソーシャルとして追跡されます。

Adobeは、分析チームと協力して、[!DNL Marketing Channels]処理ルールの包括的なセットを作成し、ビジネスに関連するすべてのチャネルを追跡することをお勧めします。 これにより、強力なアトリビューションレポートを作成できます。

Advertising Cloudがカスタムマーケティングチャネルの作成に必要なシグナルにどのように貢献できるかについて詳しくは、「[広告IDを使用した [!DNL Marketing Channels] ルール](mc-ids.md)の作成」を参照してください。

>[!MORELIKETHIS]
>
>* [Advertising Cloud IDを使用した処 [!DNL Marketing Channels] 理ルールの作成](mc-ids.md)
>* [Advertising Cloudと [!DNL Marketing Channels]](mc-data-variances.md)
>* [ [!DNL Analytics Marketing Channels] Advertising Cloudデータの使用](mc-ac-data.md)
>* [ビデオ：Advertising Cloudを使用したレポート [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [の概要 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

