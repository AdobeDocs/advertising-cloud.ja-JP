---
title: Advertising Cloudと [!DNL Marketing Channels]でチャネルデータが異なる理由
description: AMO IDで追跡されるチャネルデータが、 [!DNL Analytics Marketing Channels]で追跡されるチャネルデータと異なる可能性がある理由を説明します。
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Advertising Cloudと[!DNL Marketing Channels]でチャネルデータが異なる理由

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

Advertising Cloudと[!DNL Marketing Channels]データセットの統合について学習するユーザーからの一般的な質問は、「AMO IDと[!DNL Marketing Channels]の間のデータの相違の原因は何ですか？」です。 「データが壊れた理由は？ レポート全体で一致する指標がすべて必要です。」 幸いなことに、不一致は、データが「壊れている」ことを示しておらず、不一致が予想され、さらには望ましい場合もあります。 統合がこのように設計された理由を見てみましょう。

2つのデータセットの主な使用例は次のとおりです。

* [!DNL Marketing Channels]:の主な使用例は、複数のチ [!DNL Marketing Channels] ャネルにわたるデータを共通のアトリビューションモデルと比較することです。アナリストは、[!UICONTROL Marketing Channel]ディメンションを使用して、チャネルが相互にどのように関わっているかに関するインサイトを得ることができます。 このインサイトは、各チャネルへの投資方法に関するマクロレベルの決定に役立ち、各チャネルからの訪問者がWebサイトとどのようにやり取りするかに関するインサイトを得ることができます。

   したがって、 [!DNL Analytics] [!UICONTROL Marketing Channel]ディメンションは、すべてのチャネルをキャプチャして追跡するように設定されます。 [!DNL Marketing Channels] は、Advertising Cloud DSPビュースルー数とクリックスルー数を取り込むように設定することもできます。他のマーケティングチャネルとの関係でも同様です。

* Advertising Cloud AMO ID:Advertising Cloud AMO IDデータの主な使用例は、Advertising Cloudの高度な[!DNL Adobe Sensei]を利用した入札アルゴリズムをフィードすることです。 このアルゴリズムは、広告費用を最大化し、[!DNL DSP]キャンペーンまたは[!DNL Search]ポートフォリオの目標を達成するために、毎日おこなわれる数千のマイクロレベル入札決定を自動的に行います。 アルゴリズムがキャンペーンを結び付けるコンバージョンデータが多いほど、アルゴリズムがこれらの入札に関する意思決定を行うことができます。

   このデータを収集するために、[!DNL Analytics for Advertising Cloud]統合は、Adobe AnalyticsのAMO IDディメンションに、クリックスルーおよびビュースルートラッキングコードとして変換できる生のAMO IDを渡します。このコードは、カスタム変数(eVar)または予約変数(rVar)として保存されます。 他のチャネルのクリックスルーはAMO IDディメンションに設定されないので、AMO IDディメンションは、これらの他のチャネルからのエントリを追跡できません。 その結果、AMO IDは[!DNL Marketing Channes]lエントリポイントを通じて保持されます。

Advertising Cloudで追跡されたデータと[!DNL Analytics]で追跡されたデータのデータの相違について詳しくは、「[ [!DNL Analytics] とAdvertising Cloud](../data-variances.md)で予想されるデータの相違」を参照してください。

>[!MORELIKETHIS]
>
>* [とAdvertising Cloudの間で予想され [!DNL Analytics] るデータの相違](/help/integrations/analytics/data-variances.md)
>* [の基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Advertising Cloud IDを使用した処 [!DNL Marketing Channels] 理ルールの作成](mc-ids.md)
>* [ [!DNL Analytics Marketing Channels] Advertising Cloudデータの使用](mc-ac-data.md)
>* [ビデオ：Advertising Cloudを使用したレポート [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

