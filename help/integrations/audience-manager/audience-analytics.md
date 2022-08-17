---
title: '"[!DNL Adobe][!DNL Audience Analytics] Advertising Cloudのお客様向け»'
description: 使用方法を学ぶ [!DNL Adobe][!DNL Audience Analytics] 広告のユースケース
feature: Integration with Adobe Audience Manager
source-git-commit: d83e36847d0e14bc7e83106c0a221680060c2e58
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!DNL Adobe][!DNL Adobe] (Advertising Cloudのお客様向け )

[[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) は、Adobe Audience ManagerとAdobe Analyticsの統合で、Audience Managerのお客様がにセグメントを送信できるようにします。 [!DNL Analytics] サイトアクティビティに関するインサイトを強化します。

Advertising Cloudのお客様は、 [!DNL Audience Analytics]. 統合により、次のことが可能になります。

* Advertising Cloud露出データをに直接送信 [!DNL Analytics] 上部ファネルアクティビティが下流のサイトアクティビティに与える影響を判断するため。

* 上位ファネル露出広告からマーケティングチャネルとサイトエントリポイントを決定します。

* との統合をレイヤー化する [!DNL Analytics for Advertising Cloud] ～からサードパーティの人口統計セグメントを組み込む [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) と [!DNL Analytics for Advertising Cloud] データを参照してください。

   [!DNL Audience Marketplace] では、「Activation」サブスクリプションモデルを使用してサードパーティデータフィードにアクセスでき、購入者はこのモデルを使用して宛先にデータを送信できます。 データが [!DNL Analytics] の宛先に設定されている場合、アクティベーション料は適用されません。

* (Advertising Cloud DSPを使用した広告主 ) 総合的なジャーニー管理のインサイトを得るために、公開セグメントを追加します。

   Advertising Cloud DSPは、Adobe Experience PlatformまたはAudience Managerのインプレッショントラッキングピクセルの実装を通じて、露出データをAudience Managerに実用的なシグナルとして送信できます。 同じデータの転送先 [!DNL Analytics] アドバンスデータ分析を有効にします。 参照：[Advertising Cloud Media Data とAdobe Audience Managerの統合の概要](/help/integrations/audience-manager/media-data-integration/overview.md)」を参照してください。

詳しくは、 [!DNL Audience Analytics]（前提条件とワークフローを含む）。[Audience Analyticsの概要](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## 使用例 [!DNL Audience Analytics] Advertising Cloud Data を使用したデータ

次に、 [!DNL Analytics] [!DNL Analysis Workspace].

### 上部ファネルアクティビティがダウンストリームアクティビティに与える影響を確認する

Audience Manager露出セグメントを使用して、上部ファネルサイトのアクティビティがダウンストリームサイトのアクティビティに与える影響を確認します。 Advertising Cloudまたはサードパーティマクロ ID をトラッキングピクセルに含めて、キャンペーンレベルからユーザーに公開されたサイトのレベルまで、詳細レベルに対する影響を追跡します。

主なメリット：

* ファネル/広告タイプ別に露出を追跡し、を使用する [!DNL Audience Analytics] を使用して、カスタマージャーニーの次のフェーズとの入口率と重複を判断します。

* 上部ファネルアクティビティが下流のサイトアクティビティに与える影響を判断します。

* 接続 [!DNL Analytics for Advertising Cloud]<!-- which doesn't include the last exposure event --> および [!DNL Audience Analytics] データ <!-- (which includes the user's last exposure event) --> をクリックして、サイトへの全体的なジャーニーを判断します。

次に、 [!DNL Analysis Workspace].

![上部ファネルアクティビティがダウンストリームサイトのアクティビティに与える影響を確認する](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### 用途 [!DNL Audience Analytics] ユーザープロファイル分析用のサードパーティセグメントデータ

サードパーティのAudience Managerセグメントを使用して、ユーザーがサイトとどのようにやり取りしているかをより深く分析できます。 この情報を使用して、メディアをアクティブ化する新しいサードパーティオーディエンスを、サードパーティセグメントのプロファイルがメディアキャンペーンのサイトの主要業績評価指標とどのように関わっているかに基づいて決定できます。

>[!TIP]
> Audience Manager `Audiences ID` および `Audiences Name` 寸法 [!DNL Analytics]他のディメンションと同様に [!DNL Analytics] を収集します。

次に、 [!DNL Analysis Workspace].

![サードパーティセグメントを使用したユーザープロファイル分析の強化](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Advertising CloudとAdobe Audience Managerの統合](/help/integrations/audience-manager/overview.md)

