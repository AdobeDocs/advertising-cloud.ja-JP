---
title: パッケージ設定
description: 使用可能なパッケージ設定の説明を参照してください。
feature: Packages
exl-id: b4d415d1-86a5-40bd-b645-1709b267c174
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# パッケージ設定

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** パッケージ名。最大長は60文字です。

**[!UICONTROL Description]:** （オプション）パッケージの説明。

**[!UICONTROL 3rd Party Billed Fees]:** （オプション）請求不可コストとして追跡される静的なサードパーティ料金：

>[!NOTE]
>
>請求可能な料金は[!UICONTROL Net CPM]指標に反映されます。
* **[!UICONTROL CPM]:** 1000件のインプレッション(CPM)あたりのコスト。

* **[!UICONTROL CPM Description]:** CPM費用の説明。

[配置レベル](/help/dsp/campaign-management/placements/placement-settings.md)で、パッケージレベルの設定を上書きできます。

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** （既存のパッケージの場合は読み取り専用）パッケージ内の配置のペースと制限のレベル：

* **[!UICONTROL Package level pacing]:** このペーシング戦略は、含まれるすべての配置をグループとしてペーシングおよびキャッピングするこ *とで動作します*。この戦略では、特定のパッケージ内のすべての配置を全体的に最適化し、パフォーマンスとスケールに基づいて支出を選択した主要業績評価指標(KPI)に配分します。

* **[!UICONTROL Placement level pacing]:**  このペーシング戦略は、含まれるすべての配置を個別にペーシングおよびキャップすることで *動作します*。ベストプラクティスは、この戦略を使用して、保証された民間市場取引を実行することです。

**[!UICONTROL Flight Dates]:** パッケージの開始日と終了日。

オプションで、パッケージに対して不均等にペーシング可能なフライトを作成するには、*[!UICONTROL *Activate Custom Flighting]**を選択し、下の[!UICONTROL Flighting]セクションでカスタムフライトを設定します。 カスタムフライティングを有効にしてパッケージを保存すると、カスタムフライティングを無効にすることはできません。

>[!NOTE]
>
>* フライト日は、キャンペーンのフライト日に含める必要があります。 さらに、このパッケージに割り当てられるすべてのプレースメントのフライト日をこれらの日付に含める必要があります。
> * カスタムフライティングが有効な場合は、パッケージの開始日を編集できません。


**[!UICONTROL Budget]:** （パッケージレベルのペーシングのみを含むパッケージ）総予算の上限と予算間隔。

カスタムフライティングを含むパッケージの場合、予算間隔は常に&#x200B;*[!UICONTROL All time]*&#x200B;です。 カスタムフライトのないパッケージの場合は、予算間隔を指定します。*[!UICONTROL All time]、* *[!UICONTROL Daily]、* *[!UICONTROL Monthly]、*&#x200B;または&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Gross Budget]:** （パッケージレベルのペーシングとDynamic Margin Managementのみを含むパッケージ）パッケージの期間中の総予算上限。

**[!UICONTROL Optimization Goal]:** （パッケージレベルのペーシングのみのパッケージ）パッケージの最適化目標です。各最適化目標の説明は、[最適化目標とその使い方](/help/dsp/optimization/optimization-goals.md)を参照してください。

**[!UICONTROL Custom Goals]:** （カスタム最適化目標を含むパッケージのみ）パッ [ケ](/help/dsp/optimization/custom-goal-about.md) ージのカスタム目標。カスタムの目標とそれを使用するキャンペーンのベストプラクティスについて詳しくは、「[カスタムの目標を作成するためのベストプラクティス](/help/dsp/optimization/custom-goal-best-practices.md)」と「[パフォーマンスキャンペーンを設定するためのベストプラクティス](/help/dsp/optimization/campaign-best-practices-performance.md)」を参照してください。

**[!UICONTROL Package Goal Type]:** （カスタム最適化目標を含むパッケージのみ）パッケージの目的。この設定は、パッケージの最適化方法を決定するのに役立ちます。

* *[!UICONTROL Prospecting]:* 新しい顧客の獲得に重点を置いたパッケージの予測

* *[!UICONTROL Retargeting]:* パッケージの再ターゲット化は、以前の訪問者または顧客を再公開することに重点を置いています。

* *[!UICONTROL Other]:* その他の目的。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** （カスタム最適化目標を含むパッケージのみ）履歴データがパッケージの最適化の入力として使用される別のパッケージ。

**[!UICONTROL Target]:** （パッケージレベルのペーシングのみを含むパッケージ）ターゲットの目標。パフォーマンスの追跡に使用されます。

>[!NOTE]
>
>このフィールドは、ベンチマークに過ぎず、判定には使用されません。

**[!UICONTROL Frequency Cap]:** （パッケージレベルのペーシングのみのパッケージ）一意のデバイスまたは人（指定したに応じて）がパッケージから広告を提供できる回数 [!UICONTROL Cross Device Level]。*[!UICONTROL Unlimited]*&#x200B;や、日、週、月ごとの特定の金額を選択できます。

>[!NOTE]
>
>* 頻度キャップは、キャンペーン、パッケージおよび配置レベルで設定できます。 DSPは、キャンペーン階層で最も厳格な頻度キャップに従います。
>* ベストプラクティスは、プロスペクティングとリターゲティングの両方に対して、パッケージレベルで頻度キャップを設定することです。
> * 頻度の上限が高いほど、支出とインプレッションは高くなりますが、リーチは低くなります。 頻度の上限が小さいと、支出とインプレッションは少なくなりますが、リーチは高くなります。


**[!UICONTROL Pace on]:** （パッケージレベルのペーシングのみを含むパッケージ）ペーシングの基礎は次のとおりです。

* *[!UICONTROL Budget]:* （デフォルト）割り当てられたパッケージ予算内で可能な限り多くのインプレッションを配信します。

* *[!UICONTROL Impressions]:* このオプションは、指定した数量が指定した期間内に達するまで、インプレッション数を配信します。このオプションを選択する場合は、インプレッション数と間隔を指定します。*常に、* *[!UICONTROL Daily]、* *[!UICONTROL Monthly]、*&#x200B;または&#x200B;*[!UICONTROL Weekly]*&#x200B;です。

**[!UICONTROL Pacing Fill Strategy]:** （パッケージレベルのペーシングのみを含むパッケージ）広告配信のペースを調整する方法：

* *[!UICONTROL Even]:* 各フライトを通して配信が均等に配置され、フライトの前半の配信のターゲットが50%になります。

* *[!UICONTROL Slightly Ahead]:* （デフォルト）飛行時間の途中で55～65%完了するように配信を加速します。

* *[!UICONTROL Frontload]:* 配信を加速し、飛行の途中で65～75%完了するようにします。

* *[!UICONTROL Aggressive Frontload]:* 配信を加速し、75～85%が飛行の途中で完了するようにします。

## [!UICONTROL Flighting]

（パッケージレベルのペーシングを有効にし、「[!UICONTROL Activate Custom Flighting]」を有効にしたパッケージ） [!UICONTROL Goals & Budget]セクションで指定された[!UICONTROL Flight Dates]全体内のカスタムフライト期間。

フライトごとに、開始日、終了日、およびインプレッションのターゲット数を入力します。 別のフライトを追加するには、**[!UICONTROL Add Flight]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [パッケージ管理について](package-about.md)
>* [パッケージの作成](package-create.md)
>* [パッケージの編集](package-edit.md)
>* [パッケージへの配置の添付](package-attach-placement.md)
>* [キャンペーン管理に関するFAQ](/help/dsp/campaign-management/campaign-management-faq.md)

