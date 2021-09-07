---
title: Advertising Cloudデータでの [!DNL Marketing Channels] の使用
description: ' [!DNL Analytics Marketing Channels]でのAdvertising Cloudデータの使用方法を説明します。'
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# Advertising Cloudデータでの[!DNL Analytics Marketing Channels]の使用

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

Advertising Cloudと[!DNL Marketing Channels]の両方のレポートを使用すると、デジタルメディアがサイトのアクティビティに与える影響に関する貴重なインサイトを得ることができます。

<!-- from video: By using Marketing Channels with your Advertising Cloud data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

次の図は、Advertising Cloudと[!DNL Marketing Channels]が、1人の訪問者のジャーニーを構成する個々の訪問を追跡する方法を示しています。 [!DNL Analytics]のAdvertising Cloudレポートは、Advertising Cloudを通じてトラフィックされる有料の表示および検索広告のみに制限され、AMO IDを使用します。 ただし、[!DNL Marketing Channels]は[!DNL Marketing Channels]処理ルールに設定されているすべてのチャネルを追跡します。

![Advertising Cloudと訪問 [!DNL Marketing Channels] 者のジャーニーにおける個々の訪問の追跡方法](/help/integrations/assets/a4adc-mc-sample-journey2.png)

最初の訪問では、ユーザーは電子メールキャンペーンを通じてWebサイトに入り、10ページビューを実行してから離れました。 2回目の訪問では、ユーザーはディスプレイ広告を使用してサイトに入り、10回のページビューを実行してからサイトを離れました。 3回目の訪問では、ユーザーは自然検索を使用してサイトに入り、5回のページビュー、250ドルのコンバージョンを実行し、その後左に移動しました。 [!DNL Marketing Channels]とAdvertising Cloudの間のトラッキングの違いに注意してください。 このジャーニーでAdvertising Cloudが追跡するチャネルは[!UICONTROL Display]のみです。 Advertising Cloudは、[!UICONTROL Display]チャネル訪問を追跡し、後続のエンゲージメントデータ（ページビューなど）とコンバージョンをその広告の影響にもどします。 [!DNL Marketing Channels]一方、は、すべてのチャネルを完全に表示します。

AMO IDは訪問者のジャーニーを通じて保持されるので、AMO IDデータを使用して、Advertising Cloudが他のマーケティングチャネルに与える影響を確認できます。 AMO ID [は、デフォルトで60日間](/help/integrations/analytics/overview.md)保持されますが、必要に応じて永続性を設定できます。

## Advertising Cloudとマーケティングチャネルのデータを組み合わせてメディアのパフォーマンスを分析する方法

[!DNL Analytics]内で、Advertising Cloudの持続的な有料広告データと[!DNL Marketing Channels]の包括的な訪問データを組み合わせて、メディアのパフォーマンスをより良く分析し、カスタマージャーニーにより良い影響を与えることができます。

次の分析では、Advertising Cloudのデータを使用して、ディスプレイ広告がサイトコンバージョンに与える影響を様々なバージョンで示します。 3つの列はすべて同じコンバージョン指標を使用しますが、各列は異なるストーリーを示します。

* 列1は、訪問者のジャーニー全体で持続するAMO IDデータを調べます。 列1は、ある時点で、641のアプリ開始が、ビュースルーまたはクリックスルーイベントを通じてAdvertising Cloud広告にリンクされたことを示します。 このビューでは、他の[!DNL Marketing Channels]属性は考慮されません。

* ただし、[!DNL Marketing Channels]データセットでは、「アプリケーション開始」は他のマーケティングチャネルに関連付けられます。 最後の2つの列は、「アプリケーション開始」641を取り、データを[!UICONTROL Display Click-Through]チャネルと[!UICONTROL Display View-Through]チャネルに制限し、ラストタッチアトリビューションモデルで発生したコンバージョンを示します。

![ディスプレイ広告がサイトコンバージョンに与える影響の例](/help/integrations/assets/a4adc-mc-display-impact.png)

この分析は、さらに1ステップ進めることができます。 Advertising Cloud行をマーケティングチャネル別にさらに分類し、Advertising Cloudコンバージョンが641アプリ開始に関連付けられる場所を確認できます。 これらの変換のうち5つがラストタッチディスプレイのクリックスルーと19がラストタッチディスプレイのビュースルーに関連付けられていることは、既にわかっています。 それでも、「アプリ開始」は他のマーケティングチャネルに関連付けられ、617件残ります。 ラストタッチチャネルディメンションをAdvertising Cloud DSP行項目の上にドラッグ&amp;ドロップして、残りのアプリケーション開始のチャネルアトリビューションを表示し、ディスプレイチャネルのクロスチャネルの影響を表示できます。

![ラストタッチチャネルディメンションの追加方法](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

これで、残りのアプリ開始がどのように関連付けられるかを確認できます。 AMO IDが持続する357のラストタッチアプリケーション開始に対して、電子メールにクレジットが与えられます。 このタイプの分析を使用すると、Advertising Cloudディスプレイ広告がすべてのチャネルに及ぼす影響を確認できます。 データセットとアトリビューションモデルが1つだけの場合、このタイプのインサイトは使用できません。

![ディスプレイチャネルのクロスチャネルの影響の例](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

「100%の積み重ね」に設定したスタックグラフを使用して経時的にトレンドデータを表示することで、分析をさらに改善できます。 このビジュアライゼーションを使用すると、ディスプレイマーケティングキャンペーンの影響を最も大きく受けるラストタッチマーケティングチャネルを監視しやすくなります。

![ディスプレイチャネルのクロスチャネルインパクトのトレンドの例](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [の基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Advertising Cloud IDを使用した処 [!DNL Marketing Channels] 理ルールの作成](mc-ids.md)
>* [Advertising Cloudと [!DNL Marketing Channels]](mc-data-variances.md)
>* [ビデオ：Advertising Cloudを使用したレポート [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [の概要 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

