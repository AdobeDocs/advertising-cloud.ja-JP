---
title: の概要 [!DNL Analytics for Advertising Cloud]
description: の概要 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: bfbfc293ad04b294c813ce7c8a11200e70fc812f
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# の概要 [!DNL Analytics for Advertising Cloud]

*Advertising Cloud DSPとAdvertising Cloud Searchの広告主*

[!DNL Analytics for Advertising Cloud] は、Adobe AnalyticsとAdobe Advertising Cloudを統合して、各製品の機能を拡張および強化します。

この統合により、広告主は、 [!DNL Analytics] インスタンス。ブランドは、広告費用がサイトのエンゲージメントと重要なビジネス目標にどのようにつながるかを確認できます。

さらに、Advertising Cloudは、 [!DNL Analytics] を使用して収集 [!DNL Analytics] タグが既にサイトに存在している。 これにより、より堅牢なジャーニー管理、ファーストパーティリマーケティング、有料メディアサイトのレポートが可能になります。 Advertising Cloudは [!DNL Analytics] 支出および入札の最適化のデータ。

適切に使用されれば [!DNL Analytics for Advertising Cloud] 2 つの従来の役割の間の線をぼかします。advertising journey management（広告を通じてユーザーをサイトに送信する行為）と、web 分析を通じてそのサイトのエンゲージメントを把握します。

プライマリの利点：

* 送信 [!DNL Analytics] セグメントを直接Advertising Cloudに送信して、ファーストパーティサイトのリマーケティングをおこなう。
* 用途 [!DNL Analytics] カスタムイベントと標準イベントを、有料メディア広告を最適化するためのコンバージョンシグナルとして使用できます。
* を活用する [!DNL Analytics] Analysis Workspaceを参照してください。
* Web アナリストと有料メディアチーム間の緊密なコラボレーションを可能にします。
* 内で永続的なAdvertising Cloudビュースルーおよびクリックスルー ID を使用する [!DNL Analytics] サイトのエンゲージメントを理解する。
* データやピクセルを広告サーバーやその他のDSPにエクスポートする際に、カスタム指標、カスタムディメンション、サイトアクティビティでAnalysis Workspaceの従来の有料メディアレポートを強化できません。
* を活用する [!DNL Analytics] コードを既に Web サイト上に作成し、Advertising Cloud内でのトラッキングと最適化をおこなうことができます。

>[!TIP]
>
> 所要時間 [ビデオの紹介 [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Analytics を使用した有料メディアレポート

[!DNL Analytics for Advertising Cloud] では、次の機能を利用して、広告がサイトの行動を促進する方法に関するレポートとインサイトを強化できます。

* 内で永続的なAdvertising Cloudビュースルーおよびクリックスルー ID を使用する [!DNL Analytics] サイトのエンゲージメントを理解する。
* Analysis Workspaceを活用して、サイトのエントリポイントと訪問の行動をより深く理解します。 有料メディアのディメンションおよびイベントデータにアクセスできます。これには、Advertising Cloudキャンペーンエンティティ名（配置や広告まで）と、それに関連する指標（クリック数、インプレッション数、コストなど）が含まれます。

使用する [!DNL Analytics] 有料メディアレポートツールとして、組織はAnalysis Workspaceへのアクセス権を持つExperience Cloudログインが必要です。 Advertising Cloudチームが、Advertising CloudのデータをAnalysis Workspaceの個々のレポートスイートにマッピングします。 Advertising Cloudのデータは任意のレポートスイートに送信できますが、Advertising Cloudにマッピングされたレポートスイートと、マッピングされていないレポートスイートを認識しておく必要があります。レポートスイートによっては、レポートされるデータが変わる場合があります。

[Advertising Cloud ID( [!DNL Analytics]](ids.md) は、他の eVar と同様に機能し、カスタムの永続的な有効期限を設定します。 デフォルトでは、Advertising Cloudの実装時に、アトリビューションルックバックウィンドウは 60 日に設定されています。 この設定を変更するには、 [!DNL Adobe] アカウントマネージャー

Advertising Cloudのディメンションには、「(AMO ID)」というサフィックスが付きます (「広告タイプ (AMO ID)」など )。 参照：[Analysis WorkspaceのAdvertising Cloud指標](advertising-cloud-metrics-in-analytics.md)」をクリックします。

>[!NOTE]
>
> 内でAdvertising Cloudデータ（または任意のデータセット）を表示する場合 [!DNL Analytics]を使用する場合、指標とレポートは、 [!DNL Analytics]. データは、広告サーバーレポートなど、他のレポートシステム内で表示される内容とは異なる場合があります。 [!DNL DSP] レポート、または検索エンジンレポート。 のデータの違いを理解するには [!DNL Analytics]を使用する場合は、eVarデータの有効期限、訪問の定義、ラストタッチ属性と見なされるもの、永続化アトリビューションの合計などの要因を把握する必要があります。 詳しくは、 [～間で予想されるデータの相違 [!DNL Analytics] とAdvertising Cloud](data-variances.md).

## Analytics を使用したAdvertising CloudキャンペーンおよびPortfolioの強化

追加のピクセルが不要な場合、 [!DNL Analytics for Advertising Cloud] では、2 つの主要なシグナルをAdvertising Cloudに送信することで、最適化とオーディエンスのセグメント化をより簡単におこなえます。

* 入札シグナルとして使用するコンバージョン指標：
   * 標準指標 [!UICONTROL Revenue] および [!UICONTROL Cart Views].
   * ページビュー数や訪問指標などのサイトエンゲージメント指標。
   * カスタム売上高指標。
   * 予約売上高指標。
* で作成されたセグメント [!DNL Analytics] Experience Cloud

   以下の [!DNL Analytics] でのファーストパーティサイトリターゲティングのセグメント [!DNL DSP] 有料検索広告。

   (Advertising Cloud Searchのみ ) [!DNL Analytics] ただし、Audience Managerは、Googleの web サイトタグベースのオーディエンス（リマーケティングリスト）や顧客一致オーディエンス（顧客リスト）を [!DNL Analytics] セグメントを共有するExperience Cloud

### 入札シグナルとしてのサイトコンバージョン指標

標準イベントとカスタムイベントは、 [!DNL Analytics] 重み付けされた目標をAdvertising Cloudで構築する 目標は、お客様の入札決定に役立ちます。 [!DNL DSP] パッケージ化および検索ポートフォリオ。

>[!NOTE]
>
> 計算指標を [!DNL Analytics] Advertising Cloudに

Advertising Cloudチームが、有料メディアのパフォーマンスに適用できるイベントを特定し、Advertising Cloud( [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

参照：[Advertising Cloudの Analytics 指標](analytics-data-in-advertising-cloud.md)」をクリックします。

### サイトのリターゲティングのための Analytics セグメント

Advertising Cloudは取り込み可能 [!DNL Analytics] Advertising Cloud DSPおよび [!DNL Search] 広告で、 [!DNL Analytics] とExperience Cloud。

次の手順で、 [!DNL Analytics] セグメントの場合、広告主アカウントに [Experience CloudID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html) 有効。 ID サービスを有効にすると、すべてのExperience Cloudセグメント ( [!DNL Analytics] Experience Cloudに公開、Adobe Audience Managerで作成されたセグメント、Experience Cloudで作成されたセグメント ( [!DNL People core service]や、 Adobe Experience Platformで作成され、Audience Manager経由でAdvertising Cloudに送信されたセグメントは、処理されるとすぐにAdvertising Cloud内で使用できるようになります。

[!DNL Analytics] セグメントは 24 時間以内に利用でき、毎日更新されます。

Audiences サービスについて詳しくは、「Experience Cloudオーディエンス」サービスについて [Experience Cloudオーディエンス](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## 統合の使用例

### Analysis WorkspaceでのAdvertising Cloudデータの使用

Analysis WorkspaceでAdvertising Cloudデータを使用して視覚的なレポートを作成する方法については、ビデオ「[Workspace とレポートの概要](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).」

### Advertising Cloudダッシュボードの作成

Analysis Workspaceでの目標に合わせてAdvertising Cloudデータを追跡する方法については、ビデオ「[Adobe AnalyticsでのAdvertising Cloudダッシュボードの作成](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).」

### サイト入口分析でのAdvertising Cloud ID の使用

曜日、時間帯、ブラウザー、地理的な影響を監視するAdvertising Cloudのサイトエントリレポートの作成方法については、ビデオ「[Advertising Cloudサイト入口レポートの作成](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).」

>[!MORELIKETHIS]
>
>* [ビデオ：の概要 [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [実装の前提条件と主な情報 [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Analytics で使用されるAdvertising Cloud ID](ids.md)
>* [Advertising Cloud用 Analytics の JavaScript コード](/help/integrations/analytics/javascript.md)
>* [～間で予想されるデータの相違 [!DNL Analytics] とAdvertising Cloud](data-variances.md)
>* [Analysis WorkspaceのAdvertising Cloud指標](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloudのデータ](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

