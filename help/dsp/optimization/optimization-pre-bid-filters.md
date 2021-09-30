---
title: 配置レベルの事前入札フィルターとその使用方法
description: 使用可能な配置レベルの入札前フィルターを参照し、その使用方法を確認します。
feature: DSP Optimization
exl-id: c699e970-84ca-429b-8062-81804e6c9f21
source-git-commit: 75ec6f54271542d56e0d16fbb7aa92ebcf00d765
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# 配置レベルの事前入札フィルターとその使用方法

| 入札前フィルター | 説明 | このフィルターを使用するタイミング |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | オークションでクリックスルーが発生する確率の最小予測しきい値を設定します。 例えば、しきい値を 0.1%に設定した場合、クリックの予測確率が 0.1%以上でない限り、オークションでの入札はおこなわれません。<br><br><b>注意：</b> フィルターは、最適化目標の前に適用されます。その結果、非常に厳密なフィルターは支出を防ぐことができます。 | クリックスルー率 (CTR) の最小 KPI 目標があり、CTR がしきい値を下回る場合に予算を使用しない場合に使用します。 このフィルターは非常に制限が厳しい場合があるので、現実的な目標を設定することが重要です。 配置に関する他の制限によっては、通常 0.03～0.07%の目標が良い出発点です。 指標の改善に役立つように、必要に応じてサイトレベルで最適化できます。<br><br>目標が CTR を最小限に抑え、可能な限り最高の CPM を達成することである場合、推奨される設定は、フィルターを最適化目標「 [!UICONTROL Click Through Rate] 」と組み合わせることで[!UICONTROL Lowest CPM]す。目標が、達成度を超える利点がない最大の CPM と最小の CTR の場合は、[!UICONTROL Click Through Rate] フィルターと最適化目標「[!UICONTROL Always Max Bid + Highest CTR]」をペアリングする方が適切な場合があります。 |
| [!UICONTROL 100% Completion Rate] | インプレッションに入札する前に満たす必要がある、必要な最小完了率を設定します。 | キャンペーンの主な目標が完了率の場合に、このフィルターを使用します。 他のターゲティングパラメーターの要因。ただし、開始率は 65%が推奨されます。 |
| [!UICONTROL Player Size - Adobe] | Advertising Cloud DSPのデータを使用して、必要な最小プレーヤーサイズを設定します。 [!UICONTROL Player Size] しきい値を満たすと、インプレッションに入札します。 | DSPのデータを使用して、エピソード全体のプレーヤーインベントリで配信する場合に使用します。 |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | [!DNL Moat] または [!DNL Integral Ad Science]([!DNL IAS]) のデータを使用して、必要な最小プレーヤーサイズを設定します。 [!UICONTROL Player Size] しきい値を満たすと、インプレッションに入札します。 | プラットフォーム全体の [!DNL Moat] または [!DNL IAS] データを使用して、エピソード全体のプレーヤーインベントリで配信する場合に、を使用します。<br><br><b>注意：</b> このフィルターは、キャンペーンでまたはデータを使用するように設定されている場合に [!DNL Moat] のみ使 [!DNL IAS] 用します。 |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Advertising Cloud DSPの視認性の数値と測定値を使用して、視認性の最低必要な割合を設定します。 指定したしきい値に達すると、インプレッションに入札します。<br><br><b>注意：</b><ul><li>キャンペーンの [!UICONTROL Viewability Sensitivity] 設定が「[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]」の場合は、[!DNL Media Rating Council](MRC) 視認性の測定標準がキャンペーンに使用されます。 [!UICONTROL Viewability Sensitivity] 設定が「[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]」の場合は、 [!DNL GroupM] 視認性の測定標準がキャンペーンに使用されます。</li><li>Adobe測定の定義はサードパーティの定義とは異なるので、サードパーティのデータとの間に若干の相違が生じる可能性があります。</li></ul> | 最適化の目標と入札前のフィルター設定を、キャンペーンの [!UICONTROL Viewability Sensitivity] 設定と一致させることをお勧めします。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [キャンペーンの最適化方法](optimization-how-dsp-optimizes-campaigns.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [キャンペーンの設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [最適化の目標とその使用方法](optimization-goals.md)

