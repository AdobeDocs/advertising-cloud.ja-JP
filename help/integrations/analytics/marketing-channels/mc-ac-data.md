---
title: 使用 [!DNL Marketing Channels] とAdobe広告データ
description: でのAdobe広告データの使用方法 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: c9403a03-58aa-4633-bb97-51afc30843ad
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---

# 使用 [!DNL Analytics Marketing Channels] とAdobe広告データ

*Advertising とAdobe AnalyticsのAdobeの統合のみの広告主*

Adobe広告と [!DNL Analytics Marketing Channels] レポートを使用すると、デジタルメディアがサイトのアクティビティに与える影響について、有益なインサイトを得ることができます。

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

以下の図は、Adobe広告と [!DNL Marketing Channels] 1 人の訪問者のジャーニーを構成する個々の訪問を追跡します。 のAdobe広告レポート [!DNL Analytics] は、AMO ID を使用して、Adobe広告を通じて配信される有料ディスプレイ、検索、ソーシャルおよびコマースチャネルの広告のみに制限されます。 しかし、 [!DNL Marketing Channels] は、 [!DNL Marketing Channels] 処理ルールを参照してください。

![Adobe広告と [!DNL Marketing Channels] 訪問者のジャーニーにおける個々の訪問の追跡](/help/integrations/assets/a4adc-mc-sample-journey2.png)

最初の訪問では、ユーザーは電子メールキャンペーンを通じて Web サイトに入り、10 ページビューを実行してから離れました。 2 回目の訪問では、ユーザーはディスプレイ広告を使用してサイトに入り、10 回のページビューを実行してからサイトを離れました。 3 回目の訪問では、ユーザーは自然検索でサイトに入り、5 回のページビュー、250 ドルのコンバージョンを実行し、その後左に入りました。 トラッキングの違いは次のとおりです。 [!DNL Marketing Channels] およびAdobe広告。 このジャーニーでAdobe広告が追跡するチャネルは 1 つだけです。 [!UICONTROL Display]. Adobe広告は、 [!UICONTROL Display] チャネル訪問とは、後続のエンゲージメントデータ（ページビュー数など）やコンバージョンを、広告の影響を元にしたものにします。 [!DNL Marketing Channels]一方、は、すべてのチャネルの全体像を提供します。

AMO ID は訪問者のジャーニーを通じて保持されるので、AMO ID データを使用して、Adobe広告が他のマーケティングチャネルに与える影響を確認できます。 AMO ID [デフォルトで 60 日間保持されます](/help/integrations/analytics/overview.md)永続性は必要に応じて設定できます。

## Adobe広告とマーケティングチャネルのデータを組み合わせてメディアのパフォーマンスを分析する方法

内 [!DNL Analytics]を使用すると、Adobe広告を持続する有料広告データと [!DNL Marketing Channels] 包括的な訪問データを使用してメディアのパフォーマンスをよりよく分析し、カスタマージャーニーに対する影響を改善できます。

次の分析では、Adobe広告データを使用して、ディスプレイ広告がサイトコンバージョンに与える影響の様々なバージョンを示します。 3 つの列すべてで同じコンバージョン指標を使用しますが、各列は異なるストーリーを示しています。

* 列 1 では、訪問者のジャーニー全体で持続する AMO ID データを確認します。 列 1 は、641 のアプリ開始が、ある時点で、ビュースルーまたはクリックスルーイベントを通じて、Adobe広告とリンクされていたことを示します。 このビューは他のビューを取りません [!DNL Marketing Channels] 考慮する属性。

* 内 [!DNL Marketing Channels] ただし、641 のアプリ開始は、他のマーケティングチャネルに関連付けられます。 最後の 2 つの列は 641 のアプリケーション開始を取り、データを [!UICONTROL Display Click-Through] および [!UICONTROL Display View-Through] チャネルを表示し、ラストタッチアトリビューションモデルで発生したコンバージョンを示します。

![ディスプレイ広告がサイトコンバージョンに与える影響の例](/help/integrations/assets/a4adc-mc-display-impact.png)

この分析は、さらに 1 つ進めることができます。 マーケティングチャネル別にAdobe広告行をさらに分類し、Adobe広告コンバージョンが 641 アプリケーション開始に関連付けられている場所を確認できます。 これらのコンバージョンの 5 つは、ラストタッチディスプレイクリックスルーに関連付けられ、19 はラストタッチディスプレイビュースルーに関連付けられることは、既にご存じです。 それでも、他のマーケティングチャネルに関連する 617 件のアプリ開始が残ります。 Advertising DSPの行項目の上にラストタッチチャネルディメンションをドラッグ&amp;ドロップすると、残りのアプリケーション開始のチャネルアトリビューションを表示し、ディスプレイチャネルのクロスチャネルの影響を示すことができます。

![ラストタッチチャネルディメンションの追加方法](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

これで、残りの「アプリケーション開始」の属性を確認できます。 電子メールには、AMO ID が持続する 357 件のラストタッチアプリケーション開始のクレジットが与えられます。 このタイプの分析を使用すると、Adobe広告のディスプレイ広告がすべてのチャネルに及ぼす影響を確認できます。 データセットとアトリビューションモデルが 1 つだけの場合、このタイプのインサイトは使用できません。

![ディスプレイチャネルがチャネル間で及ぼす影響の例](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

「100%の積み重ね」に設定したスタックグラフを使用して経時的にトレンドデータを表示することで、分析をさらに改善できます。 このビジュアライゼーションを使用すると、ディスプレイマーケティングキャンペーンの影響を受けやすくなっているラストタッチマーケティングチャネルを監視しやすくなります。

![ディスプレイチャネルのクロスチャネルに対するトレンドの影響の例](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [の基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Adobe広告 ID を使用した作成 [!DNL Marketing Channels] 処理ルール](mc-ids.md)
>* [チャネル広告とチャネル広告でチャネルデータが異なるAdobeを使用する理由 [!DNL Marketing Channels]](mc-data-variances.md)
>* [ビデオ：使用 [!DNL Marketing Channels] (Adobe広告レポート用 )](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [の概要 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

