---
title: 最適化の目標とその使用方法
description: 利用可能な最適化目標を参照し、それらをいつ使用するかを確認します。
feature: DSP Optimization
exl-id: 9bca09b5-9aa7-4009-a576-9b30cfddfd55
source-git-commit: 75ec6f54271542d56e0d16fbb7aa92ebcf00d765
workflow-type: tm+mt
source-wordcount: '1605'
ht-degree: 0%

---

# 最適化の目標とその使用方法

| 最適化目標 | 説明 | この目標を使用するタイミング |
| -----------| ---------- | ---------- |
| [!UICONTROL Always Max Bid & Highest Clickthrough Rate] | パッケージレベルの最適化では、予算配分は、クリックスルー率が最も高い配置に優先順位を付けます。<br><br>オークション評価では、支出目標が満たされている場合に CTR が優先されます。送信された入札額は常に [!UICONTROL Max Bid] に設定されますが、配置が順調に行われれば、予測される CTR しきい値はより厳しくなります。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：最高のクリックスルー率 <br><br> 広告タイプ：プリロール、ディスプレイ <br><br><b> 注意：</b> 超える必要のない固定 CPM 目標と、最大化する必要のある CTR 目標がある場合は、この目標を使用します。 「最大入札額」を目的の CPM 目標に設定すると、DSPは最高の CTR を達成しながら、予算を最大限に使用します。 |
| [!UICONTROL Always Max Bid & Highest Completion Rate] | パッケージレベルの最適化では、予算配分は、最も高い完了率の配置に優先順位を付けます。<br><br>オークション評価では、支出目標が満たされている場合に完了率が優先されます。送信される入札額は常に「最高入札額」に設定されますが、配置が優れている場合は、予測される完了率しきい値がより厳しくなります。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：最も高い完了率 <br><br> 広告タイプ：プリロールのみ <br><br><b> 注意：</b> この目標は、超える必要のない固定の CPM 目標と、最大化する必要のある完了率目標がある場合に使用します。 「最大入札額」を目的の CPM 目標に設定すると、DSPは予算全体を費やしながら、可能な限り最高の完了率を達成します。 |
| [!UICONTROL Always Max Bid & Highest Engagement Rate] | パッケージレベルの最適化では、予算配分は、最もエンゲージメント率の高い配置に優先順位を付けます。<br><br>オークション評価では、支出目標が満たされている場合に、エンゲージメント率が優先されます。送信される入札額は常に「最高入札額」に設定されますが、プレースメントが優れている場合は、予測されるエンゲージメント率のしきい値がより厳しくなります。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：最も高いエンゲージメント率 <br><br> 広告タイプ：モバイルインタースティシャルのみ <br><br><b> 注意：</b> 超える必要のない固定 CPM 目標と、最大化する必要のあるエンゲージメント目標がある場合に、この目標を使用します。 「最大入札額」を目的の CPM 目標に設定すると、DSPは予算を最大限に使用しながら、可能な限り最高のエンゲージメント率を達成します。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe – GroupM)] | パッケージレベルの最適化では、予算配分は、視認性が最も高い配置に優先順位を付けます。<br><br>オークション評価では、支出目標が満たされている場合に、視認性率が優先されます。送信される入札額は常に「最高入札額」に設定されますが、配置が優れている場合は、予測される視認性のしきい値がより厳しくなります。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：最も高い視認性率 <br><br> 広告タイプ：インタラクティブプリロールのみ <br><br><b> 注意：</b> この目標は、常にプレースメントレベルの最大入札額を使用します。<br><br>キャンペーンの「視認性の感度」設定が「標準（連続して 2 秒間表示される広告の 50%）」に設定されている場合は、メディア評価評議会 (MRC) の視認性の測定標準がキャンペーンに使用されます。キャンペーンが「厳密（視聴とオーディオで 100%、50%継続）」に設定されている場合は、GroupM の視認性測定標準がキャンペーンに使用されます。 理想的には、キャンペーン設定を最適化目標および入札前のフィルター設定と一致させる必要があります。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe – MRC)] | パッケージレベルの最適化では、予算配分は、視認性が最も高い配置に優先順位を付けます。<br><br>オークション評価では、支出目標が満たされている場合に、視認性率が優先されます。送信される入札額は常に「最高入札額」に設定されますが、配置が優れている場合は、予測される視認性のしきい値がより厳しくなります。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：最も高い視認性率 <br><br> 広告タイプ：インタラクティブプリロールのみ <br><br><b> 注意：</b> この目標は、常にプレースメントレベルの最大入札額を使用します。<br><br>キャンペーンの「視認性の感度」設定が「標準（連続して 2 秒間表示される広告の 50%）」に設定されている場合は、メディア評価評議会 (MRC) の視認性の測定標準がキャンペーンに使用されます。キャンペーンが「厳密（視聴とオーディオで 100%、50%継続）」に設定されている場合は、GroupM の視認性測定標準がキャンペーンに使用されます。 理想的には、キャンペーン設定を最適化目標および入札前のフィルター設定と一致させる必要があります。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (IAS – MRC)] | パッケージレベルの最適化では、予算配分は、視認性が最も高い配置に優先順位を付けます。<br><br>オークション評価では、支出目標が満たされている場合に、視認性率が優先されます。送信される入札額は常に「最高入札額」に設定されますが、配置が優れている場合は、予測される視認性のしきい値がより厳しくなります。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：最も高い視認性率 <br><br> 広告タイプ：インタラクティブプリロールのみ <br><br><b> 注意：</b> この目標は、常にプレースメントレベルの最大入札額を使用します。<br><br>この設定は、IAS からのサードパーティデータがアルゴリズムに通知する場合に最も適しています。この目標は、キャンペーンに対して IAS 統合を有効にした場合にのみ使用します。 |
| [!UICONTROL Highest ROAS – Custom Goal] | （パッケージレベルでのみ使用可能）予算配分は、最も高い広告費用対効果 (ROAS) を持つ配置に優先順位を付けます。<br><br>オークション評価は ROAS を優先します。支出目標が満たされている場合、DSPは CPM の削減と ROAS の向上のバランスを取ります。 | キャンペーンタイプ：パフォーマンス <br><br> ベンチマーク：最高の売上高 <br><br> 広告タイプ：ディスプレイ <br><br><b> 注意：</b> 詳しくは、「パフォーマンスキャンペーンの設定に関するベストプラクティス」を参照してください。 |
| [!UICONTROL Lowest CPA – Custom Goal] | （パッケージレベルでのみ使用可能）予算配分は、最も低い CPA を持つ配置に優先順位を付けます。<br><br>オークション評価は CPA を優先します。支出目標が達成されている場合、DSPは CPM の削減と CPA の削減のバランスを取ります。 | キャンペーンタイプ：パフォーマンス <br><br> ベンチマーク：最も低い CPA<br><br> 広告タイプ：ディスプレイ <br><br><b> 注意：</b> 詳しくは、「パフォーマンスキャンペーンの設定に関するベストプラクティス」を参照してください。 |
| [!UICONTROL Lowest Cost Per Click] | パッケージレベルの最適化では、予算配分は最も低い CPC の配置に優先順位を付けます。<br><br>オークション評価は CPC を優先します。支出目標が満たされている場合、DSPは CPM の削減と CTR の上昇のバランスを取って CPC を下げます。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：効率的な CPM と最高のクリックスルー率 <br><br> 広告タイプ：プリロール、ディスプレイ <br><br><b> 注意：</b> この目標を使用して、可能な限り最高の CPC を実現します。 最大 CPM を保証するには、配置の最大入札額として使用します。 |
| [!UICONTROL Lowest Cost Per Completion] | パッケージレベルの最適化では、予算配分は完了あたりのコストが最も低い配置を優先します。<br><br>オークション評価では、ビデオ完了率 (VCR) が優先されます。支出目標が満たされている場合、DSPは CPM の削減と VCR の増加のバランスを取り、完了あたりのコストを削減する試みを行います。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：効率的な CPM と最も高い完了率 <br><br> 広告タイプ：プリロールのみ |
| [!UICONTROL Lowest Cost Per Engagement] | パッケージレベルの最適化では、予算配分は、エンゲージメント率が最も低い配置に優先順位を付けます。<br><br>オークション評価では、エンゲージメント率が優先されます。支出目標が満たされている場合、DSPは CPM の削減とエンゲージメントあたりのコストの削減のバランスを取ろうとします。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：効率的な CPM と最高のエンゲージメント率 <br><br> 広告タイプ：モバイルインタースティシャルのみ |
| [!UICONTROL Lowest CPM] | パッケージレベルの最適化では、予算配分は最も低い CPM の配置に優先順位を付けます。<br><br>オークション評価では CPM が優先されます。支出目標が満たされている場合、DSPは CPM を徐々に減らします。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：効率的な CPM<br><br> 広告タイプ：プリロール、ディスプレイ、CTV、ネイティブ、オーディオ |
| [!UICONTROL Lowest Cost Per View] | 最も低い CPM と同じように動作します。 パッケージレベルの最適化では、予算配分は最も低い CPM の配置に優先順位を付けます。<br><br>オークション評価では CPM が優先されます。支出目標が満たされている場合、DSPは CPM を徐々に減らします。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：効率的な CPM と最高のクリックスルー率 <br><br> 広告タイプ：プリロール、ディスプレイ |
| [!UICONTROL Lowest vCPM (Adobe - GroupM)] | パッケージレベルの最適化では、予算配分は最も低い vCPM の配置に優先順位を付けます。<br><br>オークション評価では vCPM が優先されます。支出目標を満たしている場合、DSPは CPM の削減と視認性の向上のバランスを取ろうとします。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：効率的な CPM と最高の vCPM<br><br> 広告タイプ：プリロール、ディスプレイ <br><br><b> 注意：</b> この目標を使用して、vCPM を最高のものにします。<br><br>最大 CPM を保証するには、配置の最大入札額として使用します。 |
| [!UICONTROL Lowest vCPM (Adobe - MRC)] | パッケージレベルの最適化では、予算配分は最も低い vCPM の配置に優先順位を付けます。<br><br>オークション評価では vCPM が優先されます。支出目標を満たしている場合、DSPは CPM の削減と視認性の向上のバランスを取ろうとします。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：効率的な CPM と最高の vCPM<br><br> 広告タイプ：プリロール、ディスプレイ <br><br><b> 注意：</b> この目標を使用して、vCPM を最高のものにします。<br><br>最大 CPM を保証するには、配置の最大入札額として使用します。 |
| [!UICONTROL Lowest vCPM (IAS - MRC)] | パッケージレベルの最適化では、予算配分は最も低い vCPM の配置に優先順位を付けます。<br><br>オークション評価では vCPM が優先されます。支出目標を満たしている場合、DSPは CPM の削減と視認性の向上のバランスを取ろうとします。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：効率的な CPM と最高の vCPM<br><br> 広告タイプ：プリロール、ディスプレイ <br><br><b> 注意：</b> この目標を使用して、vCPM を最高のものにします。<br><br>最大 CPM を保証するには、配置の最大入札額として使用します。<br><br>この設定は、IAS からのサードパーティデータがアルゴリズムに通知する場合に最も適しています。この目標は、キャンペーンに対して IAS 統合を有効にした場合にのみ使用します。 |
| [!UICONTROL Lowest vCPM (Moat - GroupM)] | パッケージレベルの最適化では、予算配分は最も低い vCPM の配置に優先順位を付けます。<br><br>オークション評価では vCPM が優先されます。支出目標を満たしている場合、DSPは CPM の削減と視認性の向上のバランスを取ろうとします。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：効率的な CPM と最高の vCPM<br><br> 広告タイプ：プリロール、ディスプレイ <br><br><b> 注意：</b> この目標を使用して、vCPM を最高のものにします。<br><br>最大 CPM を保証するには、配置の最大入札額として使用します。<br><br>この設定は、からのサードパーティデータがアルゴリズムに通知す [!DNL Moat] る場合に最も適しています。この目標は、キャンペーンに対して [!DNL Moat] 統合を有効にした場合にのみ使用します。 |
| [!UICONTROL Lowest vCPM (Moat - MRC)] | パッケージレベルの最適化では、予算配分は最も低い vCPM の配置に優先順位を付けます。<br><br>オークション評価では vCPM が優先されます。支出目標を満たしている場合、DSPは CPM の削減と視認性の向上のバランスを取ろうとします。 | キャンペーンタイプ：ブランディング <br><br> ベンチマーク：効率的な CPM と最高の vCPM<br><br> 広告タイプ：プリロール、ディスプレイ <br><br><b> 注意：</b> この目標を使用して、vCPM を最高のものにします。<br><br>最大 CPM を保証するには、配置の最大入札額として使用します。<br><br>この設定は、からのサードパーティデータがアルゴリズムに通知す [!DNL Moat] る場合に最も適しています。この目標は、キャンペーンに対して [!DNL Moat] 統合を有効にした場合にのみ使用します。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [パフォーマンスキャンペーンの設定のベストプラクティス](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [配置レベルの事前入札フィルターとその使用方法](optimization-pre-bid-filters.md)
>* [キャンペーンの設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
