---
title: 使用 [!DNL Marketing Channels] Advertising Cloud Data を使用
description: でのAdvertising Cloudデータの使用方法を説明します。 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# 使用 [!DNL Analytics Marketing Channels] Advertising Cloud Data を使用

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

Advertising Cloudと [!DNL Marketing Channels] レポートを使用すると、デジタルメディアがサイトのアクティビティに与える影響について、有益なインサイトを得ることができます。

<!-- from video: By using Marketing Channels with your Advertising Cloud data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

次の図は、Advertising Cloudと [!DNL Marketing Channels] 1 人の訪問者のジャーニーを構成する個々の訪問を追跡します。 Advertising Cloudレポート [!DNL Analytics] は、AMO ID を使用して、Advertising Cloudを通じて配信される有料ディスプレイおよび検索広告にのみ制限されます。 しかし、 [!DNL Marketing Channels] は、 [!DNL Marketing Channels] 処理ルールを参照してください。

![Advertising Cloudと [!DNL Marketing Channels] 訪問者のジャーニーにおける個々の訪問の追跡](/help/integrations/assets/a4adc-mc-sample-journey2.png)

最初の訪問では、ユーザーは電子メールキャンペーンを通じて Web サイトに入り、10 ページビューを実行してから離れました。 2 回目の訪問では、ユーザーはディスプレイ広告を使用してサイトに入り、10 回のページビューを実行してからサイトを離れました。 3 回目の訪問では、ユーザーは自然検索でサイトに入り、5 回のページビュー、250 ドルのコンバージョンを実行し、その後左に入りました。 トラッキングの違いは次のとおりです。 [!DNL Marketing Channels] Advertising Cloud このジャーニーでAdvertising Cloudが追跡するチャネルは 1 つだけです。 [!UICONTROL Display]. Advertising Cloudは、 [!UICONTROL Display] チャネル訪問とは、後続のエンゲージメントデータ（ページビュー数など）やコンバージョンを、広告の影響を元にしたものにします。 [!DNL Marketing Channels]一方、は、すべてのチャネルの全体像を提供します。

AMO ID は訪問者のジャーニーを通じて保持されるので、AMO ID データを使用して、Advertising Cloudが他のマーケティングチャネルに与える影響を確認できます。 AMO ID [デフォルトで 60 日間保持されます](/help/integrations/analytics/overview.md)永続性は必要に応じて設定できます。

## Advertising Cloudとマーケティングチャネルのデータを組み合わせてメディアのパフォーマンスを分析する方法

内 [!DNL Analytics]を使用すると、Advertising Cloudの永続的な有料広告データと [!DNL Marketing Channels] 包括的な訪問データを使用してメディアのパフォーマンスをよりよく分析し、カスタマージャーニーに対する影響を改善できます。

次の分析では、Advertising Cloudのデータを使用して、ディスプレイ広告がサイトコンバージョンに与える影響を様々なバージョンで示します。 3 つの列すべてで同じコンバージョン指標を使用しますが、各列は異なるストーリーを示しています。

* 列 1 では、訪問者のジャーニー全体で持続する AMO ID データを確認します。 列 1 は、ある時点で、641 件のアプリ開始が、ビュースルーまたはクリックスルーイベントを通じてAdvertising Cloud広告とリンクされたことを示します。 このビューは他のビューを取りません [!DNL Marketing Channels] 考慮する属性。

* 内 [!DNL Marketing Channels] ただし、641 のアプリ開始は、他のマーケティングチャネルに関連付けられます。 最後の 2 つの列は 641 のアプリケーション開始を取り、データを [!UICONTROL Display Click-Through] および [!UICONTROL Display View-Through] チャネルを表示し、ラストタッチアトリビューションモデルで発生したコンバージョンを示します。

![ディスプレイ広告がサイトコンバージョンに与える影響の例](/help/integrations/assets/a4adc-mc-display-impact.png)

この分析は、さらに 1 つ進めることができます。 Advertising Cloud行をマーケティングチャネル別にさらに分類し、Advertising Cloudコンバージョンが 641 のアプリ開始に関連付けられる場所を確認できます。 これらのコンバージョンの 5 つは、ラストタッチディスプレイクリックスルーに関連付けられ、19 はラストタッチディスプレイビュースルーに関連付けられることは、既にご存じです。 それでも、他のマーケティングチャネルに関連する 617 件のアプリ開始が残ります。 ラストタッチチャネルディメンションをAdvertising Cloud DSP行項目の上にドラッグ&amp;ドロップすると、残りのアプリケーション開始のチャネルアトリビューションが表示され、ディスプレイチャネルのクロスチャネルの影響が示されます。

![ラストタッチチャネルディメンションの追加方法](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

これで、残りの「アプリケーション開始」の属性を確認できます。 電子メールには、AMO ID が持続する 357 件のラストタッチアプリケーション開始のクレジットが与えられます。 このタイプの分析を使用すると、すべてのチャネルにわたってAdvertising Cloudディスプレイ広告が及ぼす影響を確認できます。 データセットとアトリビューションモデルが 1 つだけの場合、このタイプのインサイトは使用できません。

![ディスプレイチャネルがチャネル間で及ぼす影響の例](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

「100%の積み重ね」に設定したスタックグラフを使用して経時的にトレンドデータを表示することで、分析をさらに改善できます。 このビジュアライゼーションを使用すると、ディスプレイマーケティングキャンペーンの影響を受けやすくなっているラストタッチマーケティングチャネルを監視しやすくなります。

![ディスプレイチャネルのクロスチャネルに対するトレンドの影響の例](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [の基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Advertising Cloud ID を使用した作成 [!DNL Marketing Channels] 処理ルール](mc-ids.md)
>* [Advertising Cloudと [!DNL Marketing Channels]](mc-data-variances.md)
>* [ビデオ：Advertising Cloudを使用したレポート [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [の概要 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

