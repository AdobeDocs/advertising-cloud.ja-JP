---
title: Advertising Cloudと [!DNL Marketing Channels]
description: AMO ID でトラッキングされるチャネルデータが、 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 4605dc7d-43d7-414f-a509-6096c6cf5fd2
source-git-commit: b99d0ce78dc2adc16e555ef618393ef2fc11067d
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Advertising Cloudと [!DNL Marketing Channels]

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

Advertising Cloudと [!DNL Marketing Channels] データセットは、「AMO ID との間でデータの相違が生じる原因 [!DNL Marketing Channels]?」 「データが壊れたのはなぜですか？ レポート全体で一致する指標がすべて必要です。」 幸いにも、不一致は、データが「壊れている」ことを示しておらず、不一致が予想され、さらには望ましいことも示していません。 統合がこのように設計された理由を見てみましょう。

2 つのデータセットの主な使用例は異なります。

* [!DNL Marketing Channels]:の主な使用例 [!DNL Marketing Channels] は、複数のチャネルをまたいだデータを共通のアトリビューションモデルと比較するためのものです。 アナリストは、 [!UICONTROL Marketing Channel] ディメンションを使用して、チャネルが相互にどのように関わっているかに関するインサイトを増やすことができます。 このインサイトは、各チャネルへの投資方法に関するマクロレベルの決定を促進し、各チャネルからの訪問者が Web サイトとどのようにやり取りするかに関するインサイトを導くのに役立ちます。

   この [!DNL Analytics] [!UICONTROL Marketing Channel] したがって、ディメンションは、すべてのチャネルをキャプチャして追跡するように設定されます。 [!DNL Marketing Channels] は、Advertising Cloud DSPビュースルー数およびクリックスルー数を取り込むように設定することもできます。他のマーケティングチャネルとの関連で取り込みます。

* Advertising Cloud AMO ID :Advertising Cloud AMO ID データの主な使用例は、Advertising Cloud の詳細設定をフィードすることです [!DNL Adobe Sensei]-powered 入札アルゴリズム。 アルゴリズムは、広告費用を最大化し、 [!DNL DSP] キャンペーンまたは [!DNL Search] ポートフォリオ アルゴリズムがキャンペーンを結び付けることができるコンバージョンデータが多いほど、アルゴリズムがこれらの入札の決定を下すことができます。

   このデータを収集するには、 [!DNL Analytics for Advertising Cloud] 統合では、Adobe Analyticsの AMO ID ディメンションにクリックスルーおよびビュースルートラッキングコードとして変換できる生の AMO ID を渡します。これは、カスタム変数 (eVar) または予約変数 (rVar) として保存されます。 他のチャネルのクリックスルーは AMO ID ディメンションに設定されないので、AMO ID ディメンションは、これらの他のチャネルからのエントリを追跡できません。 その結果、AMO ID は [!DNL Marketing Channels] エントリポイント

Advertising Cloud追跡データとのデータの相違について詳しくは、 [!DNL Analytics]-tracked データ：[A と B の間で予想されるデータの相違 [!DNL Analytics] とAdvertising Cloud](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [A と B の間で予想されるデータの相違 [!DNL Analytics] とAdvertising Cloud](/help/integrations/analytics/data-variances.md)
>* [の基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Advertising Cloud ID を使用した作成 [!DNL Marketing Channels] 処理ルール](mc-ids.md)
>* [使用 [!DNL Analytics Marketing Channels] Advertising Cloud Data を使用](mc-ac-data.md)
>* [ビデオ：Advertising Cloudを使用したレポート [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

