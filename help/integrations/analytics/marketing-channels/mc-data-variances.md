---
title: チャネル広告とチャネル広告でチャネルデータが異なるAdobeを使用する理由 [!DNL Marketing Channels]
description: AMO ID でトラッキングされるチャネルデータが、 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 4605dc7d-43d7-414f-a509-6096c6cf5fd2
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# チャネル広告とチャネル広告でチャネルデータが異なるAdobeを使用する理由 [!DNL Marketing Channels]

*Advertising とAdobe AnalyticsのAdobeの統合のみの広告主*

Adobe広告と [!DNL Marketing Channels] データセットは、「AMO ID との間でデータの相違が生じる原因 [!DNL Marketing Channels]?」 「データが壊れたのはなぜですか？ レポート全体で一致する指標がすべて必要です。」 幸いにも、不一致は、データが「壊れている」ことを示しておらず、不一致が予想され、さらには望ましいことも示していません。 統合がこのように設計された理由を見てみましょう。

2 つのデータセットの主な使用例は異なります。

* [!DNL Marketing Channels]:の主な使用例 [!DNL Marketing Channels] は、複数のチャネルをまたいだデータを共通のアトリビューションモデルと比較するためのものです。 アナリストは、 [!UICONTROL Marketing Channel] ディメンションを使用して、チャネルが相互にどのように関わっているかに関するインサイトを増やすことができます。 このインサイトは、各チャネルへの投資方法に関するマクロレベルの決定を促進し、各チャネルからの訪問者が Web サイトとどのようにやり取りするかに関するインサイトを導くのに役立ちます。

   この [!DNL Analytics] [!UICONTROL Marketing Channel] したがって、ディメンションは、すべてのチャネルをキャプチャして追跡するように設定されます。 [!DNL Marketing Channels] は、Advertising DSPビュースルーとクリックスルーを取り込むように設定することもでき、他のマーケティングチャネルとの関連で取り込むことができます。

* Adobe広告 AMO ID:Adobe広告 AMO ID データの主な使用例は、高度な [!DNL Adobe Sensei]-powered 入札アルゴリズム。 アルゴリズムは、広告費用を最大化し、 [!DNL DSP] キャンペーンまたは [!DNL Search] ポートフォリオ アルゴリズムがキャンペーンを結び付けることができるコンバージョンデータが多いほど、アルゴリズムがこれらの入札の決定を下すことができます。

   このデータを収集するには、 [!DNL Analytics for Advertising] 統合では、Adobe Analyticsの AMO ID ディメンションにクリックスルーおよびビュースルートラッキングコードとして変換できる生の AMO ID を渡します。これは、カスタム変数 (eVar) または予約変数 (rVar) として保存されます。 他のチャネルのクリックスルーは AMO ID ディメンションに設定されないので、AMO ID ディメンションは、これらの他のチャネルからのエントリを追跡できません。 その結果、AMO ID は [!DNL Marketing Channels] エントリポイント

Adobeの広告追跡データとのデータの相違について詳しくは、 [!DNL Analytics]-tracked データ：[A と B の間で予想されるデータの相違 [!DNL Analytics] およびAdobe広告](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [A と B の間で予想されるデータの相違 [!DNL Analytics] およびAdobe広告](/help/integrations/analytics/data-variances.md)
>* [の基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Adobe広告 ID を使用した作成 [!DNL Marketing Channels] 処理ルール](mc-ids.md)
>* [使用 [!DNL Analytics Marketing Channels] とAdobe広告データ](mc-ac-data.md)
>* [ビデオ：使用 [!DNL Marketing Channels] (Adobe広告レポート用 )](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

