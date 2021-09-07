---
title: ' [!DNL Analytics for Advertising Cloud]の概要'
description: ' [!DNL Analytics for Advertising Cloud]の概要'
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 0%

---

# [!DNL Analytics for Advertising Cloud]の概要

*Advertising Cloud DSPとAdvertising Cloud Searchの広告主*

[!DNL Analytics for Advertising Cloud] は、Adobe AnalyticsとAdobe Advertising Cloudを統合して、各製品の機能を拡張および強化します。

この統合により、広告主は[!DNL Analytics]インスタンスでのクリックスルーおよびビュースルーのサイトのやり取りを追跡でき、ブランドは広告の支出がサイトのエンゲージメントと重要なビジネス目標にどのようにつながるかを確認できます。

さらに、Advertising Cloudは、既にサイトにある[!DNL Analytics]タグを使用して[!DNL Analytics]が収集した広大なファーストパーティデータにアクセスできます。 これにより、より堅牢なジャーニー管理、ファーストパーティリマーケティング、有料メディアサイトのレポートが可能になります。 Advertising Cloudは、支出と入札の最適化のために[!DNL Analytics]データをさらに使用できます。

[!DNL Analytics for Advertising Cloud]は、適切に使用されると、2つの従来の役割の間の線をぼかします。advertising journey management（広告を通じてユーザーをサイトに送信する行為）、およびweb分析を通じてそのサイトのエンゲージメントを把握します。

プライマリのメリット：

* ファーストパーティサイトのリマーケティングのために、[!DNL Analytics]セグメントをAdvertising Cloudに直接送信します。
* 有料メディア広告を最適化するためのコンバージョンシグナルとして、カスタムイベントと標準イベントを使用します。[!DNL Analytics]
* [!DNL Analytics] Analysis Workspaceを活用して、サイトのエントリポイントと訪問の行動をより深く理解します。
* Webアナリストと有料メディアチーム間の緊密なコラボレーションを実現
* [!DNL Analytics]内で永続的なAdvertising CloudビュースルーIDとクリックスルーIDを使用して、サイトのエンゲージメントを把握します。
* データやピクセルを広告サーバーやその他のDSPにエクスポートする場合に、カスタム指標、カスタムディメンション、サイトアクティビティでAnalysis Workspaceの従来の有料メディアレポートを強化できません。
* Advertising Cloud内で追跡と最適化を行うには、既にWebサイト上にある[!DNL Analytics]コードを利用してください。

>[!TIP]
>
>  [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics)の[ビデオの紹介をご覧ください。

## Analyticsを使用した有料メディアレポート

[!DNL Analytics for Advertising Cloud] は、次のことを可能にし、広告がサイトの行動を促進する方法に関するレポートとインサイトを強化します。

* [!DNL Analytics]内で永続的なAdvertising CloudビュースルーIDとクリックスルーIDを使用して、サイトのエンゲージメントを把握します。
* Analysis Workspaceを活用して、サイトのエントリポイントと訪問の行動をより深く理解します。 有料メディアのディメンションおよびイベントデータにアクセスできます。これには、Advertising Cloudキャンペーンエンティティ名（配置や広告まで）と、その関連指標（クリック数、インプレッション数、コストなど）が含まれます。

[!DNL Analytics]を有料メディアレポートツールとして使用するには、Analysis Workspaceへのアクセス権を持つExperience Cloudログインが必要です。 Advertising Cloudチームが、Advertising CloudのデータをAnalysis Workspaceの個々のレポートスイートにマッピングするお手伝いをします。 Advertising Cloudのデータは任意のレポートスイートに送信できますが、Advertising Cloudにマッピングされているレポートスイートと、マッピングされていないレポートスイートを認識しておく必要があります。レポートスイートによっては、レポートされるデータが変わる場合があります。

[Advertising Cloud IDは [!DNL Analytics]](ids.md) 他のeVarと同様に機能し、カスタムの永続的な有効期限を設定します。Advertising Cloudの実装時には、デフォルトで、アトリビューションルックバックウィンドウが60日に設定されています。 この設定を変更するには、Adobeのアカウントマネージャーに問い合わせてください。

Advertising Cloudディメンションには、「(AMO ID)」というサフィックスが付きます(「広告タイプ(AMO ID)」など)。 使用可能なディメンションのリストについては、「Analysis WorkspaceのAdvertising Cloud指標](advertising-cloud-metrics-in-analytics.md)」を参照してください。[

>[!NOTE]
>
> [!DNL Analytics]内でAdvertising Cloudデータ（または任意のデータセット）を表示する場合、指標とレポートは[!DNL Analytics]内に設定されたルールに基づいていることに注意してください。 データは、広告サーバーレポート、[!DNL DSP]レポート、検索エンジンレポートなど、他のレポートシステム内で表示される内容とは異なる場合があります。 [!DNL Analytics]のeVarの違いを理解するには、データデータの有効期限、訪問の定義、合計持続アトリビューションに対するラストタッチアトリビューションと見なされるもの、その他の要因を把握する必要があります。 詳しくは、[ [!DNL Analytics] とAdvertising Cloud](data-variances.md)の間で予想されるデータの相違を参照してください。

## Analyticsを使用したAdvertising CloudのキャンペーンおよびPortfolioの強化

追加のピクセルを必要とせずに[!DNL Analytics for Advertising Cloud]を使用すると、2つの主要なシグナルをAdvertising Cloudに送信することで、より最適化とオーディエンスのセグメント化を容易に行うことができます。

* 入札シグナルとして使用するコンバージョン指標：
   * 標準指標（[!UICONTROL Revenue]や[!UICONTROL Cart Views]など）。
   * ページビュー数や訪問指標などのサイトエンゲージメント指標。
   * カスタム売上高指標。
   * 予約売上高指標。
* [!DNL Analytics]で作成され、Experience Cloudに公開されたセグメント。

   [!DNL Analytics]セグメントは、[!DNL DSP]および有料検索広告でのファーストパーティサイトのリターゲティングに使用できます。

   (Advertising Cloud Searchのみ)Audience Managerが[!DNL Analytics]でない広告主は、Experience Cloudと共有される[!DNL Analytics]セグメントから、Google Webサイトのタグベースのオーディエンス（リマーケティングリスト）と顧客一致のオーディエンス（顧客リスト）を作成することもできます。

### 入札シグナルとしてのサイトコンバージョン指標

[!DNL Analytics]の標準イベントとカスタムイベントを使用して、Advertising Cloudで重み付けされた目標を作成できます。 目標は、[!DNL DSP]パッケージと検索ポートフォリオの入札決定に役立ちます。

>[!NOTE]
>
> [!DNL Analytics]からAdvertising Cloudに計算指標をマッピングすることはできません。

Advertising Cloudチームが、有料メディアのパフォーマンスに適用できるイベントを特定し、Advertising Cloudにマッピングします。このイベントは[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties]に表示されます。

使用可能な指標のリストについては、「Advertising CloudのAnalytics指標](analytics-data-in-advertising-cloud.md)」を参照してください。[

### サイトリターゲティングのためのAnalyticsセグメント

Advertising Cloudは、[!DNL Analytics]とExperience Cloudの間のネイティブExperience Cloudオーディエンス統合を使用して、Advertising Cloud DSPおよび[!DNL Search]広告のリマーケティング用に[!DNL Analytics]セグメントを取り込むことができます。

[!DNL Analytics]セグメントにアクセスするには、Experience Cloud主アカウントで[広告主IDサービス](https://experienceleague.adobe.com/docs/id-service/using/home.html)を有効にする必要があります。 IDサービスを有効にすると、すべてのExperience Cloudセグメント([!DNL Analytics]で作成されExperience Cloudに公開されたセグメント、Adobe Audience Managerで作成されたセグメント、[!DNL People core service]でExperience Cloudで作成されたセグメント、Adobe Experience Platformで作成され、Audience Manager経由でAdvertising Cloudに送信されたセグメントを含む)がAdvertising Cloud内で使用可能になります。

[!DNL Analytics] セグメントは24時間以内に利用でき、毎日更新されます。

Experience Cloudオーディエンスサービスについて詳しくは、[Experience Cloudオーディエンス](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html)を参照してください。

## 統合の使用例

### Analysis WorkspaceでのAdvertising Cloudデータの使用

Advertising Cloudデータを使用してAnalysis Workspaceで視覚的なレポートを作成する方法については、ビデオ「[Workspaceとレポートの概要](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)」を参照してください。

### Advertising Cloudダッシュボードの作成

Analysis Workspaceでの目標に合わせてAdvertising Cloudデータを追跡する方法については、ビデオ「[Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html)でAdvertising Cloudダッシュボードを作成する」を参照してください。

### Advertising Cloud IDをサイト入口分析に使用する

曜日、時間帯、ブラウザー、地理的な影響を監視するAdvertising Cloudサイトエントリレポートの作成方法については、ビデオ「[Advertising Cloudサイトエントリレポートの作成](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html)」を参照してください。

>[!MORELIKETHIS]
>
>* [ビデオ：の概要 [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [実装の前提条件と主な情報 [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Analyticsで使用されるAdvertising Cloud ID](ids.md)
>* [Advertising Cloud用AnalyticsのJavaScriptコード](/help/integrations/analytics/javascript.md)
>* [とAdvertising Cloudの間で予想され [!DNL Analytics] るデータの相違](data-variances.md)
>* [Analysis WorkspaceのAdvertising Cloud指標](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloudのデータ](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

