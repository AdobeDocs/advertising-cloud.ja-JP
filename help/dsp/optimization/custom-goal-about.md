---
title: カスタム目標について
description: 最も低いCPAまたは最も高いROASに最適化されたパッケージで成功イベントを定義するためのカスタム目標について説明します。
feature: Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# カスタム目標について

カスタム目標は、広告主がビジネス目標を達成するために必要な成功イベントを定義します。 最適化目標「[!UICONTROL Highest ROAS - Custom Goal]」または「[!UICONTROL Lowest CPA - Custom Goal]」を使用する各パッケージには、全体的な最適化目標の達成に役立つカスタム目標を含める必要があります。 Advertising Cloud Searchでは、*目標*&#x200B;というカスタム目標を作成できます。

![カスタム目標](/help/dsp/assets/objective-goals.png)

各カスタム目標は、1つ以上の指標（*トランザクションプロパティ*）と、それらのトランザクションプロパティの相対的な重み付けで構成されます。 使用可能なトランザクションプロパティには、Advertising Cloudコンバージョンピクセルを使用して、またはAdobe Analyticsを通じて追跡されたすべての指標が含まれます。

>[!NOTE]
>
>* [!DNL Analytics] ディメンションとセグメントは、Advertising Cloudの最適化には使用できません。
>* DSPでAnalyticsイベントを使用するには、Adobeのアカウントマネージャーと協力して、広告主レベルの統合を設定します。
>* [!DNL Analytics] カスタムイベントは、次の命名規則に従います。 `custom_event_[*event #*]_[*Analytics report suite ID*]`.例：`custom_event_16_examplersid`


例えば、3つの指標（トランザクションプロパティ）がキャンペーンの1つの特定のパッケージに関連するとします。「PDFのダウンロード」は20米ドル、「Eメールのサインアップ」は30米ドル、「注文の確認」は40米ドルと評価されます。 顧客アクションの1回限りの金額値に従って重み付けを指定する場合、プロパティの相対的な重み付けは1、2、1.5になります。

カスタム目標の設定方法に関するヒントについては、[カスタム目標の作成のベストプラクティス](custom-goal-best-practices.md)を参照してください。

[カスタム目標](custom-goal-create.md)を作成したら、Adobe Senseiを使用してレポートやアルゴリズムを最適化するために、[パッケージ](/help/dsp/campaign-management/packages/package-settings.md)に割り当てることができます。

>[!MORELIKETHIS]
>
>* [カスタム目標の作成](custom-goal-create.md)
>* [カスタム目標を作成するためのベストプラクティス](custom-goal-best-practices.md)
>* [最適化目標とその使用方法](optimization-goals.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [キャンペーンの最適化方法](optimization-how-dsp-optimizes-campaigns.md)

