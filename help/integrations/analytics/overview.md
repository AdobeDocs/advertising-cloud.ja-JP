---
title: の概要 [!DNL Analytics for Advertising]
description: の概要 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# の概要 [!DNL Analytics for Advertising]

*Advertising DSPおよび[!DNL Advertising Search]*

[!DNL Analytics for Advertising] は、Adobe AnalyticsとAdobe広告を統合して、各製品の機能を拡張および強化します。

この統合により、広告主は、 [!DNL Analytics] インスタンスを使用して、ブランドは広告の支出がサイトのエンゲージメントと重要なビジネス目標にどのように結び付いているかを確認できます。

さらに、Adobe広告は、 [!DNL Analytics] を使用して収集 [!DNL Analytics] タグが既にサイトに存在します。 これにより、より堅牢なジャーニー管理、ファーストパーティリマーケティング、有料メディアサイトのレポートを実現します。 Adobe広告では、 [!DNL Analytics] 支出と入札の最適化のデータ。

適切に使用されれば [!DNL Analytics for Advertising] 2 つの従来の役割の間の線をぼかします。advertising journey management（広告を通じてユーザーをサイトに送信する）と、web 分析を通じてそのサイトへのエンゲージメントを把握します。

プライマリの利点：

* 送信 [!DNL Analytics] セグメントをAdobe広告に直接追加し、ファーストパーティのサイトリマーケティングをおこなうことができます。
* 用途 [!DNL Analytics] 有料メディア広告を最適化するためのコンバージョンシグナルとしてのカスタムおよび標準イベント。
* を活用する [!DNL Analytics] Analysis Workspaceを使用して、サイトのエントリポイントと訪問の行動をより深く把握できます。
* Web アナリストと有料メディアチーム間の緊密なコラボレーションを可能にします。
* 内での永続的なAdobe広告ビュースルーおよびクリックスルー ID の使用 [!DNL Analytics] サイトのエンゲージメントを理解する。
* データやピクセルを広告サーバーやその他のDSPにエクスポートする場合に、カスタム指標、カスタムディメンション、サイトアクティビティでAnalysis Workspaceの従来の有料メディアレポートを強化できません。
* を活用する [!DNL Analytics] Adobe広告内での追跡と最適化のために、既に Web サイト上にコードが存在している。

>[!TIP]
>
> 所要時間 [のビデオ紹介 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Analytics を使用した有料メディアレポート

[!DNL Analytics for Advertising] では、次の機能を使用して、広告がサイトの行動を促進する方法についてのレポートおよびインサイトを強化できます。

* 内での永続的なAdobe広告ビュースルーおよびクリックスルー ID の使用 [!DNL Analytics] サイトのエンゲージメントを理解する。
* Analysis Workspaceを活用して、サイトのエントリポイントと訪問の行動をより深く理解します。 有料メディアのディメンションおよびイベントデータにアクセスできます。これには、Adobe広告キャンペーンエンティティ名（配置や広告まで）と、それに関連する指標（クリック数、インプレッション数、コストなど）が含まれます。

使用する [!DNL Analytics] 有料メディアレポートツールとして、組織はAnalysis Workspaceへのアクセス権を持つExperience Cloudログインが必要です。 Adobe広告チームが、Analysis Workspaceの個々のレポートスイートにAdobe広告データをマッピングするのを支援します。 Adobe広告データは任意のレポートスイートに送信できますが、Adobe広告にマッピングされたレポートスイートと、それまでにマッピングされていないレポートスイートについて認識しておく必要があります。レポートスイートに応じて、レポートされるデータが変わる場合があります。

[Adobe広告 ID （内） [!DNL Analytics]](ids.md) は、他の eVar と同様に機能し、カスタムの永続的な有効期限が設定されます。 デフォルトでは、Adobe広告の実装時に、アトリビューションルックバックウィンドウは 60 日に設定されています。 この設定を変更するには、 [!DNL Adobe] アカウントチーム。

Adobe広告ディメンションには、サフィックス「(AMO ID)」が付きます (「広告タイプ (AMO ID)」など )。 参照：[Analysis WorkspaceのAdobe広告指標](advertising-cloud-metrics-in-analytics.md)」をクリックします。

>[!NOTE]
>
> 内でAdobe広告データ（または任意のデータセット）を表示する場合 [!DNL Analytics]を使用する場合、指標とレポートは、 [!DNL Analytics]. データは、広告サーバーレポートなど、他のレポートシステム内に表示されるものとは異なる場合があります。 [!DNL DSP] レポート、または検索エンジンレポート。 のデータの違いを理解するには、以下を実行します。 [!DNL Analytics]を使用する場合は、eVarデータの有効期限、訪問の定義、ラストタッチアトリビューションと見なされるもの、永続アトリビューションの合計と見なされるもの、その他の要因を把握する必要があります。 詳しくは、 [A と B の間で予想されるデータの相違 [!DNL Analytics] およびAdobe広告](data-variances.md).

## Analytics を使用したAdobe広告キャンペーンおよびPortfolioの強化

追加のピクセルを必要とせずに、 [!DNL Analytics for Advertising] は、2 つの主要シグナルをAdobe広告に送信することで、より最適化がおこなわれ、オーディエンスのセグメント化が容易になります。

* 入札シグナルとして使用するコンバージョン指標：
   * 標準指標 ( 例： [!UICONTROL Revenue] および [!UICONTROL Cart Views].
   * サイトエンゲージメント指標（ページビュー数、訪問指標など）。
   * カスタム売上高指標。
   * 予約済みの売上高指標。
* で作成されたセグメント [!DNL Analytics] Experience Cloud

   以下を使用できます。 [!DNL Analytics] でのファーストパーティサイトリターゲティングのためのセグメント [!DNL DSP] 有料検索広告。

   ([!DNL Search] （専用） [!DNL Analytics] ただし、Audience Managerは、Google web サイトのタグベースのオーディエンス（リマーケティングリスト）や顧客一致オーディエンス（顧客リスト）を [!DNL Analytics] セグメントを共有するExperience Cloud。

### 入札シグナルとしてのサイトコンバージョン指標

標準のイベントとカスタムイベントは、 [!DNL Analytics] :Adobe広告で重み付けされた目標を構築します。 目標は、お客様の入札決定に役立ちます [!DNL DSP] パッケージ化し、ポートフォリオを検索します。

>[!NOTE]
>
> 以下から計算指標をマッピングすることはできません： [!DNL Analytics] をAdobe広告に追加します。

Adobe広告チームが、有料メディアのパフォーマンスに適したイベントを特定し、Adobe広告 ( [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

参照：[Analytics の指標 (Adobe広告 )](analytics-data-in-advertising-cloud.md)」をクリックします。

### サイトリターゲティングのための Analytics セグメント

Adobe広告が取り込み可能 [!DNL Analytics] Advertising DSPおよび [!DNL Search] 広告で、 [!DNL Analytics] とExperience Cloud。

次の手順で [!DNL Analytics] セグメントの場合は、広告主アカウントに [Experience CloudID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html) 有効。 ID サービスが有効な場合、すべてのExperience Cloudセグメント ( [!DNL Analytics] Experience Cloudに公開されたセグメント、Adobe Audience Managerで作成されたセグメント、Experience Cloudで作成されたセグメント ( [!DNL People core service]や、Adobe Experience Platformで作成され、Audience Managerを介してAdobe広告に送信されたセグメントは、処理されるとすぐにAdobe広告内で使用できるようになります。

[!DNL Analytics] セグメントは 24 時間以内に使用でき、毎日更新されます。

Audiences サービスについて詳しくは、「Experience Cloud」を参照してください。 [Experience Cloudオーディエンス](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## 統合の使用例

### Analysis WorkspaceでのAdobe広告データの使用

Analysis WorkspaceでAdobe広告データを使用して視覚的なレポートを作成する方法については、ビデオを参照してください。[Workspace とレポートの概要](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Adobe広告ダッシュボードの作成

Analysis Workspaceで目標に合わせてAdobe広告データを追跡する方法については、ビデオ「[Adobe AnalyticsでのAdobe広告ダッシュボードの作成](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### サイト入口分析にAdobe広告 ID を使用する

曜日、時間帯、ブラウザー、地理的な影響を監視するAdobe広告サイトエントリレポートを作成する方法については、ビデオ「[Adobe広告サイト入口レポートの作成](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [ビデオ：の概要 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [実装の前提条件と主な情報 [!DNL Analytics for Advertising]](prerequisites.md)
>* [Analytics で使用されるAdobe広告 ID](ids.md)
>* [広告用 Analytics の JavaScript コード](/help/integrations/analytics/javascript.md)
>* [A と B の間で予想されるデータの相違 [!DNL Analytics] およびAdobe広告](data-variances.md)
>* [Analysis WorkspaceのAdobe広告指標](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe広告のデータ](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

