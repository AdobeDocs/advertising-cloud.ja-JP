---
title: 配置レベルの事前入札フィルターとその使用方法
description: 使用可能な配置レベルの入札前フィルターを参照し、その使用方法を確認します。
feature: DSP Optimization
exl-id: c699e970-84ca-429b-8062-81804e6c9f21
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# 配置レベルの事前入札フィルターとその使用方法

| 入札前フィルター | 説明 | このフィルターを使用するタイミング |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | オークションがクリックスルーを引き起こす確率の最小予測しきい値を設定します。 例えば、しきい値を 0.1%に設定した場合、クリックの予測確率が 0.1%以上でない限り、オークションでの入札はおこなわれません。<br><br><b>注意：</b> 最適化目標の前にフィルターが適用されます。 その結果、非常に厳密なフィルターが支出を防ぐことができます。 | クリックスルー率 (CTR) の最小 KPI 目標があり、CTR がしきい値を下回った場合に予算を使用しない場合に使用します。 このフィルターは非常に制限が厳しい場合があるので、現実的な目標を設定することが重要です。 配置に関する他の制限に応じて、一般に 0.03～07%の目標は、出発点として適切です。 指標の改善に役立つように、必要に応じてサイトレベルで最適化できます。<br><br>最小限の CTR と最高の CPM を達成することを目的としている場合、推奨される設定は、 [!UICONTROL Click Through Rate] 最適化目標「 」でフィルター[!UICONTROL Lowest CPM].&quot; 目標が、達成度を超える実際のメリットがない最大の CPM で、最小の CTR を持つ場合は、 [!UICONTROL Click Through Rate] 最適化目標「 」でフィルター[!UICONTROL Always Max Bid + Highest CTR]」の方が適している可能性があります。 |
| [!UICONTROL 100% Completion Rate] | インプレッションに入札する前に満たす必要がある、必要な最小完了率を設定します。 | キャンペーンの主な目標が完了率の場合に、このフィルターを使用します。 他のターゲティングパラメーターでの要因。ただし、開始率は 65%が推奨されます。 |
| [!UICONTROL Player Size - Adobe] | DSPのデータを使用して、必要な最小プレーヤーサイズを設定します。 インプレッションに入札する際に、 [!UICONTROL Player Size] しきい値を満たした。 | DSPのデータを使用して、エピソード全体のプレーヤーインベントリで配信していることを確認する場合に使用します。 |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | 以下のデータを使用して、必要な最小プレーヤーサイズを設定します。 [!DNL Moat] または [!DNL Integral Ad Science] ([!DNL IAS]) をクリックします。 インプレッションに入札する際に、 [!UICONTROL Player Size] しきい値を満たした。 | プラットフォーム全体を使用して、エピソード全体のプレーヤーインベントリでを提供する場合に使用します。 [!DNL Moat] または [!DNL IAS] データ。<br><br><b>注意：</b> このフィルターは、キャンペーンが [!DNL Moat] または [!DNL IAS] データ。 |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | DSPの視認性の数値と測定値を使用して、必要最小限の視認性の割合を設定します。 指定したしきい値に達すると、インプレッションで入札が行われます。<br><br><b>メモ：</b><ul><li>キャンペーンの [!UICONTROL Viewability Sensitivity] の設定は&quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]、」 [!DNL Media Rating Council] (MRC) 視認性の測定標準は、キャンペーンに使用されます。 この [!UICONTROL Viewability Sensitivity] の設定は&quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]、」 [!DNL GroupM] ビューアビリティ測定標準は、キャンペーンに使用されます。</li><li>Adobe測定の定義はサードパーティの定義とは異なるので、サードパーティのデータとの間に若干の相違が生じる場合があります。</li></ul> | 最適化目標と入札前のフィルター設定を、キャンペーンの [!UICONTROL Viewability Sensitivity] 設定。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [キャンペーンの最適化方法](optimization-how-dsp-optimizes-campaigns.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [キャンペーン設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [最適化目標とその使用方法](optimization-goals.md)

