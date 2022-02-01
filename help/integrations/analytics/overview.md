---
title: の概要 [!DNL Analytics for Advertising Cloud]
description: の概要 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# の概要 [!DNL Analytics for Advertising Cloud]

*Advertising Cloud DSPとAdvertising Cloud Searchの広告主*

[!DNL Analytics for Advertising Cloud] は、Adobe AnalyticsとAdobe Advertising Cloudを統合して、各製品の機能を拡張および強化します。

この統合により、広告主は、 [!DNL Analytics] インスタンスを使用して、ブランドは広告の支出がサイトのエンゲージメントと重要なビジネス目標にどのように結び付いているかを確認できます。

さらに、Advertising Cloudは次のような広大なファーストパーティデータにアクセスできます。 [!DNL Analytics] を使用して収集 [!DNL Analytics] タグが既にサイトに存在します。 これにより、より堅牢なジャーニー管理、ファーストパーティリマーケティング、有料メディアサイトのレポートを実現します。 Advertising Cloudは [!DNL Analytics] 支出と入札の最適化のデータ。

適切に使用されれば [!DNL Analytics for Advertising Cloud] 2 つの従来の役割の間の線をぼかします。advertising journey management（広告を通じてユーザーをサイトに送信する）と、web 分析を通じてそのサイトへのエンゲージメントを把握します。

プライマリの利点：

* 送信 [!DNL Analytics] セグメントをAdvertising Cloudに直接送信して、ファーストパーティサイトのリマーケティングをおこなう。
* 用途 [!DNL Analytics] 有料メディア広告を最適化するためのコンバージョンシグナルとしてのカスタムおよび標準イベント。
* を活用する [!DNL Analytics] Analysis Workspaceを使用して、サイトのエントリポイントと訪問の行動をより深く把握できます。
* Web アナリストと有料メディアチーム間の緊密なコラボレーションを可能にします。
* 内での永続的なAdvertising Cloudビュースルーおよびクリックスルー ID の使用 [!DNL Analytics] サイトのエンゲージメントを理解する。
* データやピクセルを広告サーバーやその他のDSPにエクスポートする場合に、カスタム指標、カスタムディメンション、サイトアクティビティでAnalysis Workspaceの従来の有料メディアレポートを強化できません。
* を活用する [!DNL Analytics] Advertising Cloud内での追跡と最適化のために、既に web サイト上にコードが存在している。

>[!TIP]
>
> 所要時間 [のビデオ紹介 [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Analytics を使用した有料メディアレポート

[!DNL Analytics for Advertising Cloud] では、次の機能を使用して、広告がサイトの行動を促進する方法についてのレポートおよびインサイトを強化できます。

* 内での永続的なAdvertising Cloudビュースルーおよびクリックスルー ID の使用 [!DNL Analytics] サイトのエンゲージメントを理解する。
* Analysis Workspaceを活用して、サイトのエントリポイントと訪問の行動をより深く理解します。 有料メディアのディメンションおよびイベントデータにアクセスできます。これには、Advertising Cloudキャンペーンエンティティ名（配置や広告に至るまで）と、それに関連する指標（クリック数、インプレッション数、コストなど）が含まれます。

使用する [!DNL Analytics] 有料メディアレポートツールとして、組織はAnalysis Workspaceへのアクセス権を持つExperience Cloudログインが必要です。 Advertising Cloudのチームが、Analysis WorkspaceでAdvertising Cloudデータを個々のレポートスイートにマッピングするお手伝いをします。 Advertising Cloudのデータを任意のレポートスイートに送信できますが、Advertising Cloudにマッピングされたレポートスイートと、それまでにマッピングされていないレポートスイートについて把握しておく必要があります。レポートスイートに応じて、レポートされるデータが変わる場合があります。

[Advertising Cloud ID 内 [!DNL Analytics]](ids.md) は、他の eVar と同様に機能し、カスタムの永続的な有効期限が設定されます。 デフォルトでは、Advertising Cloudの実装時に、アトリビューションルックバックウィンドウは 60 日に設定されています。 この設定を変更するには、 [!DNL Adobe] アカウントチーム。

Advertising Cloudディメンションには、「(AMO ID)」というサフィックスが付きます (「広告タイプ (AMO ID)」など )。 参照：[Analysis WorkspaceのAdvertising Cloud指標](advertising-cloud-metrics-in-analytics.md)」をクリックします。

>[!NOTE]
>
> 内でAdvertising Cloudデータ（または任意のデータセット）を表示する場合 [!DNL Analytics]を使用する場合、指標とレポートは、 [!DNL Analytics]. データは、広告サーバーレポートなど、他のレポートシステム内に表示されるものとは異なる場合があります。 [!DNL DSP] レポート、または検索エンジンレポート。 のデータの違いを理解するには、以下を実行します。 [!DNL Analytics]を使用する場合は、eVarデータの有効期限、訪問の定義、ラストタッチアトリビューションと見なされるもの、永続アトリビューションの合計と見なされるもの、その他の要因を把握する必要があります。 詳しくは、 [A と B の間で予想されるデータの相違 [!DNL Analytics] とAdvertising Cloud](data-variances.md).

## Analytics を使用したAdvertising CloudキャンペーンおよびPortfolioの強化

追加のピクセルを必要とせずに、 [!DNL Analytics for Advertising Cloud] は、2 つの主要なシグナルをAdvertising Cloudに送信することで、より最適化がおこなわれ、オーディエンスのセグメント化が容易になります。

* 入札シグナルとして使用するコンバージョン指標：
   * 標準指標 ( 例： [!UICONTROL Revenue] および [!UICONTROL Cart Views].
   * サイトエンゲージメント指標（ページビュー数、訪問指標など）。
   * カスタム売上高指標。
   * 予約済みの売上高指標。
* で作成されたセグメント [!DNL Analytics] Experience Cloud

   以下を使用できます。 [!DNL Analytics] でのファーストパーティサイトリターゲティングのためのセグメント [!DNL DSP] 有料検索広告。

   (Advertising Cloud Searchのみ ) [!DNL Analytics] ただし、Audience Managerは、Google web サイトのタグベースのオーディエンス（リマーケティングリスト）や顧客一致オーディエンス（顧客リスト）を [!DNL Analytics] セグメントを共有するExperience Cloud。

### 入札シグナルとしてのサイトコンバージョン指標

標準のイベントとカスタムイベントは、 [!DNL Analytics] Advertising Cloudで重み付けされた目標を作成する 目標は、お客様の入札決定に役立ちます [!DNL DSP] パッケージ化し、ポートフォリオを検索します。

>[!NOTE]
>
> 以下から計算指標をマッピングすることはできません： [!DNL Analytics] Advertising Cloudに

Advertising Cloudのチームが、有料メディアのパフォーマンスに適したイベントを特定し、Advertising Cloud( [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

参照：[Advertising Cloudの Analytics 指標](analytics-data-in-advertising-cloud.md)」をクリックします。

### サイトリターゲティングのための Analytics セグメント

Advertising Cloudが取り込み可能 [!DNL Analytics] Advertising Cloud DSPおよび [!DNL Search] 広告で、 [!DNL Analytics] とExperience Cloud。

次の手順で [!DNL Analytics] セグメントの場合は、広告主アカウントに [Experience CloudID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html) 有効。 ID サービスが有効な場合、すべてのExperience Cloudセグメント ( [!DNL Analytics] Experience Cloudに公開されたセグメント、Adobe Audience Managerで作成されたセグメント、Experience Cloudで作成されたセグメント ( [!DNL People core service]や、Adobe Experience Platformで作成され、Audience Managerを使用してAdvertising Cloudに送信されたセグメントは、処理が完了するとすぐにAdvertising Cloud内で使用できるようになります。

[!DNL Analytics] セグメントは 24 時間以内に使用でき、毎日更新されます。

Audiences サービスについて詳しくは、「Experience Cloud」を参照してください。 [Experience Cloudオーディエンス](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## 統合の使用例

### Analysis WorkspaceでのAdvertising Cloud Data の使用

Advertising Cloudのデータを使用してAnalysis Workspaceで視覚的なレポートを作成する方法については、ビデオ「[Workspace とレポートの概要](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Advertising Cloudダッシュボードの作成

Analysis Workspaceで目標に合わせてAdvertising Cloudデータを追跡する方法については、ビデオ「[Adobe AnalyticsでのAdvertising Cloudダッシュボードの作成](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### サイト入口分析でのAdvertising Cloud ID の使用

曜日、時間帯、ブラウザー、および地理的な影響を監視するAdvertising Cloudのサイト入口レポートの作成方法については、ビデオ「[Advertising Cloudサイト入口レポートの作成](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [ビデオ：の概要 [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [実装の前提条件と主な情報 [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Analytics で使用されるAdvertising Cloud ID](ids.md)
>* [Advertising Cloud向け Analytics 用 JavaScript コード](/help/integrations/analytics/javascript.md)
>* [A と B の間で予想されるデータの相違 [!DNL Analytics] とAdvertising Cloud](data-variances.md)
>* [Analysis WorkspaceのAdvertising Cloud指標](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloudのデータ](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

