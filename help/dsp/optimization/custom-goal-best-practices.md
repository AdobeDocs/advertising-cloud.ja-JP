---
title: カスタム目標を構築するためのベストプラクティス
description: 成功イベントを定義するためのカスタム目標を構築するためのベストプラクティスを学びます。
feature: DSP Optimization, DSP Best Practices
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# カスタム目標を構築するためのベストプラクティス

## 単一のプロパティを持つカスタム目標

次の例は、単一のプロパティ（指標）をターゲットに設定する目標の設定方法を示しています。

### 「[!UICONTROL Highest ROAS - Custom Goal]»最適化目標

キャンペーンの目標が売上高 ([!UICONTROL Highest ROAS - Custom Goal]) の場合、カスタム目標（目標）には、「[!UICONTROL Revenue]」プロパティの重みが 1(1) である。

![単一のプロパティを持つ ROAS カスタム目標の例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] の値は、追跡される売上高の$1 ごとに 1 と等しくなります。
>
> 例えば、重みが 1 の$250 のコンバージョンは、$250 とレポートされます。 コンバージョン指標に 0.5 の重みが割り当てられている場合、Adobe広告（$250 コンバージョン* 0.5）では、$250 のコンバージョンが$125 としてレポートされます。 [!UICONTROL Property Weight] = 125 ドル )。

### 「[!UICONTROL Lowest CPA - Custom Goal]»最適化目標

キャンペーンの目標が最も低い獲得単価 (CPA) で、成功イベントが 1 つだけ必要な場合は、その 1 つの指標（次の例では「アプリケーション送信」）を含めます。 ベストプラクティスは、重み付けを 1(1) に設定することです。

![単一のプロパティを持つ CPA カスタム目標の例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] の値は、トラッキングされるコンバージョンごとに 1 と等しくなります。
>
> 例えば、10 件の「アプリケーション送信」コンバージョンが追跡される場合、10 件の「アプリケーション送信」コンバージョンがレポートされます。  コンバージョン指標に 0.5 の重みが割り当てられている場合、Adobe広告（10 コンバージョン* 0.5）では、10 のコンバージョンが 5 としてレポートされます。 [!UICONTROL Property Weight] = 5)。

## 複数のプロパティを持つカスタム目標

カスタム目標で複数のプロパティを使用する場合、次の 2 つのシナリオがあります。

* キャンペーンの目標に複数の成功イベントがあります。 例えば、複数のオンサイトアクションの広告をしていて、すべてが CPA 目標に関連付けられているとします。 次の目的の例には、3 つの異なるプロパティ (PDFのダウンロード、お問い合わせ、電子メールのサインアップ ) が含まれ、それぞれ重み付けが 1(1) で、 [!DNL Adobe Sensei] 各プロパティの重要度が等しいアルゴリズム。 様々なコストや重要度を持つプロパティを含める場合は、それに応じて相対的な重みを調整できます。

   ![複数のプロパティを持つカスタム目標の例](/help/dsp/assets/custom-goal-multiple-properties.png)

* カスタム目標の単一のプロパティでは、最適化されたパフォーマンスに必要な 1 日あたりのコンバージョン数は 10 個とはなりません。 これは、日々のパッケージの支出が最小限か、自然なコンバージョンの数が限られているために発生する可能性があります。 カスタム目標にサポートプロパティを追加すると、1 日あたりのコンバージョン数のしきい値を 10 個にするのに役立ちます。 10 個のサポートイベントを使用すると、各重みが 1 個 (1) を下回っている場合でも、パッケージが 10 日/しきい値を満たすのに役立ちます。 しかし、その多くのイベントを追加する必要がない場合があります。

   カスタム目標にサポートプロパティを追加する場合、主な成功イベントに対する相対的な重要度に従ってプロパティの重みを付け、データポイントの数に注意してください。 これにより、Adobe Senseiアルゴリズムは複数のプロパティのバランスを取り、目標に向けて最適化をおこなうことができます。

   次の目的の例には、3 つのプロパティが含まれ、それぞれに異なる重み付けが設定されます。アプリケーション送信= 1、アプリケーション開始= 0.1、広告主ランディングページ= 0.01 です。つまり、各アプリケーション送信コンバージョンは、平均で 10 件のアプリケーション開始コンバージョンおよび 100 件の広告主ランディングページコンバージョンと同じ値を持ちます。

   ![複数のプロパティを持つカスタム目標の例](/help/dsp/assets/custom-goal-multiple-properties2.png)

   代わりに、ランディングページの訪問数を「アプリケーションの送信数」と同じように重み付けした場合、自然に多数のランディングページの訪問数が目標を圧倒し、ランディングページの訪問数にゆがむ可能性があります。<!--reword-->

>[!MORELIKETHIS]
>
>* [カスタム目標について](custom-goal-about.md)
>* [カスタム目標の作成](custom-goal-create.md)
>* [最適化目標とその使用方法](optimization-goals.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [キャンペーンの最適化方法](optimization-how-dsp-optimizes-campaigns.md)

