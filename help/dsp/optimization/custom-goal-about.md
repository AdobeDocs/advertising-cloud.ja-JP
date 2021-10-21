---
title: カスタム目標について
description: 最も低い CPA または最も高い ROAS に最適化されたパッケージで成功イベントを定義するためのカスタム目標について説明します。
feature: DSP Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: d2ad7d47d9cf13411fc831526a6fa4ff698b0a15
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# カスタム目標について

カスタム目標は、広告主がビジネス目標を満たすために必要とする成功イベントを定義します。 最適化目標を使用する各パッケージ[!UICONTROL Highest ROAS - Custom Goal]&quot;または&quot;[!UICONTROL Lowest CPA - Custom Goal]「 」には、全体的な最適化目標の達成に役立つカスタム目標を含める必要があります。 カスタム目標は、 *目標* Advertising Cloud Search

![カスタム目標](/help/dsp/assets/objective-goals.png)

各カスタム目標は、1 つ以上の指標、または *トランザクションプロパティ*、およびこれらのトランザクションプロパティの相対的な重み付け。 使用可能なトランザクションプロパティには、Advertising CloudのコンバージョンピクセルおよびAdobe Analyticsを使用して追跡されたすべての指標が含まれます。

>[!NOTE]
>
>* [!DNL Analytics] ディメンションとセグメントは、Advertising Cloudの最適化には使用できません。
>* DSPで Analytics イベントを使用するには、 [!DNL Adobe] アカウントマネージャーを使用して、広告主レベルの統合を設定します。
>* [!DNL Analytics] カスタムイベントは、次の命名規則に従います。 `custom_event_[*event #*]_[*Analytics report suite ID*]`. 例： `custom_event_16_examplersid`


例えば、3 つの指標（トランザクションプロパティ）がキャンペーンの 1 つの特定のパッケージに関連しているとします。「PDFのダウンロード」は 20 USD、「E メールのサインアップ」は 30 USD、「注文の確認」は 40 USD と評価されています。 顧客のアクションの 1 回限りの金額値に従って重み付けを指定する場合、プロパティの相対的な重み付けは 1、2、1.5 になります。

詳しくは、 [カスタム目標の作成に関するベストプラクティス](custom-goal-best-practices.md) カスタム目標の設定方法に関するヒントを参照してください。

一度 [カスタム目標の作成](custom-goal-create.md)を使用する場合、 [パッケージに割り当てる](/help/dsp/campaign-management/packages/package-settings.md) Adobe Senseiを使用したレポートおよびアルゴリズムの最適化。

>[!MORELIKETHIS]
>
>* [カスタム目標の作成](custom-goal-create.md)
>* [カスタム目標を作成するためのベストプラクティス](custom-goal-best-practices.md)
>* [最適化の目標とその使用方法](optimization-goals.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [キャンペーンの最適化方法](optimization-how-dsp-optimizes-campaigns.md)

