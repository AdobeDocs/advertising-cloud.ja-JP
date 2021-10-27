---
title: Advertising Cloud DSPの新機能
description: このページでは、Advertising Cloud DSPの新機能および最近変更された機能について説明します。
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: d4b67393-e8c5-4170-92eb-bcf643ba3ec3
source-git-commit: 07687a569ba9f24a944bd899524bb2a6a4070204
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 0%

---

# 新機能

以下の機能は、新機能または最近変更されました。

<!-- | 27  October 2021 | The [!UICONTROL Deal ID] settings and other places in the user interface reflect new branding for [!DNL Magnite] SSP:<ul><li>The SSP "[!DNL Tremor]" ([!DNL Telaria]) is now "[!DNL Magnite CTV]."</li><li>[!DNL Rubicon]" will soon change to "[!DNL Magnite DV+]," where [!DNL DV+] stands for display, video, and other formats such as audio.</li></ul> | See "[SSP Partners](/help/dsp/inventory/ssp-partners.md)." | -->

| 日付 | 機能 | 説明 | 詳細情報 |
| ---- | ------- | ----------- | -------------------- |
| 2021 年 10 月 8 日 | ヘルプ | すべて [DSPおよびその他のAdvertising Cloudドキュメント](https://experienceleague.adobe.com/docs/advertising-cloud.html) on [!DNL Experience League] は、使用可能なすべての言語に機械翻訳されるようになりました。 表示言語を変更するには、ページの左下にある「言語を変更」メニューを使用します。<br>![言語の変更](/help/dsp/assets/change-language.png) |
| 2021 年 9 月 30 日 | ブランドの安全性 | （9 月 23 日リリース） [!DNL DoubleVerify] ブランド安全性の事前入札製品を [!DNL Brand Suitability Tiers]：特定のトピックのすべてのインスタンスを避けることなく、特定のセグメントに対して 3 つのリスクレベル（低、中、高）の中から選択できます。 従来、セグメントには公差レベルは含まれていませんでした。<br><br>新しい [!DNL DoubleVerify] セグメント構造， DSPは、既存の Brand Safety セグメントを新しい、推奨される *medium* — レベルのセグメント。 必要に応じて、次のようにセグメント層を調整できます。 *low* または *high*.<br><br>**注意：** セグメントの一部には層はありませんが、「迷惑/スパイウェア/マルウェア、ウェアズ」/Incentivized/Malware/Clutter」などの新しい名前が付けられています。 | — |
|  | 最適化 | 次の最適化目標および入札前フィルターは非推奨（廃止予定）となりました。<ul><li>最適化目標：<ul><li>[!UICONTROL Always Max Bid & Highest Viewability Rate (Moat – GroupM)]</li><li>[!UICONTROL Always Max Bid & Highest Viewability Rate (Moat – MRC)]</li></ul><li>事前入札フィルターの目標：<ul><li>[!UICONTROL Viewability IAS]</li><li>[!UICONTROL Viewability Moat]</li></ul></ul> | 参照：[最適化の目標とその使用方法](/help/dsp/optimization/optimization-goals.md)&quot;と&quot;[配置レベルの事前入札フィルターとその使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md).」 |
| 2021 年 9 月 29 日 | キャンペーン管理ビュー | A &quot;[!UICONTROL Creation date]「 」列は、 [!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements]および [!UICONTROL Ads] ビュー。 また、 [!UICONTROL Placements] および [!UICONTROL Ads] 閲覧数 [!UICONTROL Creation date]. | 参照：[カスタム列表示の作成](/help/dsp/campaign-management/reports/column-view-create.md)&quot;と&quot;[キャンペーンデータのフィルター](/help/dsp/campaign-management/reports/campaign-data-filter.md).」 |
|  | プログラムで保証された取引 | （9 月リリース） [!UICONTROL Max Bid] プログラム保証 (PG) 取引のデフォルトの配置。 ただし、PG の取引には常に固定 CPM があるので、国際的なクライアントだけが [!UICONTROL Max Bid] 為替手数料を考慮する。 | — |
|  |  | （9 月リリース）[!DNL FreeWheel Programmatic Guaranteed]「権限は、 [!DNL FreeWheel Programmatic Creative API] から [!UICONTROL Ads] 表示または [!UICONTROL Placements] 表示 引き続き、 [!UICONTROL Deals] 表示 | —<!-- Add link to page on submitting ads to Freewheel once it's edited. --> |
| 2021 年 8 月 12 日 | 入札前の視認性 | 入札前の視認性フィルター [!DNL Oracle Advertising (Moat)] が配置に使用できるようになりました。 | 詳しくは、 [入札前の視認性のためのサードパーティ統合](/help/dsp/introduction/features/brand-safety-media-quality.md#pre-bid-viewability) および」[配置レベルの事前入札フィルターとその使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md).」 |
| 7 月 15 日 | ヘルプ | Advertising Cloud DSPがメディアやサービスを購入する際に、どのようにして顧客アカウントを調達したかに関する詳細が追加されました。 | 参照：[アカウントの資金調達](/help/dsp/introduction/billing/account-funding.md).」 |
| 2021 年 6 月 12 日 | ヘルプ | 広告ポリシーが更新されました。 | 参照：[Adobe Advertising Cloud広告要件ポリシー](/help/policies/ad-requirements-policy.md).」 |
| 2021 年 6 月 8 日 | ヘルプ | で、プログラム的に保証された取引を使用して広告を実行する際に、手順を使用できます。 [!DNL FreeWheel]. | 参照：[でのプログラム保証取引の設定の概要 [!DNL FreeWheel]](/help/dsp/inventory/freewheel-overview.md),&quot; &quot;[プログラム的に保証された取り引きの広告をに送信 [!DNL FreeWheel]](/help/dsp/inventory/freewheel-submit.md),&quot; &quot;[広告のステータスの確認 [!DNL Freewheel] プログラム保証取引](/help/dsp/inventory/freewheel-check-status.md)」と「[のエラーコード [!DNL FreeWheel] 広告送信](/help/dsp/inventory/freewheel-error-codes.md).」 |
| 2021 年 5 月 28 日 | ヘルプ | ヘルス関連のオーディエンスセグメントをターゲット設定する代わりに使用する、許容可能なヘルス関連のオーディエンスセグメントおよび戦術に関するガイドラインを利用できます。 | 参照：[許容可能なヘルスセグメントのガイドライン](/help/policies/health-segment-guidelines.md).」 |
| 2021 年 5 月 27 日 | ヘルプ | 「Adobe Experience Cloudとの統合」の章は、別のガイドになり、 [Advertising Cloudドキュメントのホームページ](https://experienceleague.adobe.com/docs/advertising-cloud.html). 新しいガイドでは、「 [!DNL Analytics Marketing Channels].」<br>このDSPガイドの目次には、新しいガイドへのリンクが含まれています。 | 参照：[Adobe Experience Cloudとの統合](/help/integrations/home.md).」 |
| 2021 年 5 月 25 日 | ヘルプ | 「キャンペーンの管理」の章では、Excel QA スプレッドシートを使用してキャンペーンの主要な配置設定を確認および編集する方法に関する新しいトピックを参照できます。 | 参照：[スプレッドシートを使用したキャンペーンの配置設定の修正について](/help/dsp/campaign-management/qa/qa-about.md), &quot;[キャンペーンのダウンロード配置設定](/help/dsp/campaign-management/qa/qa-sheet-download.md),&quot; &quot;[キャンペーンの配置設定のアップロード](/help/dsp/campaign-management/qa/qa-sheet-upload.md)、および[ダウンロード/アップロードされたスプレッドシートの列](/help/dsp/campaign-management/qa/qa-sheet-columns.md). |
| 2021 年 5 月 6 日 | パッケージ設定 | 新しい Pacing Fill Strategy オプション「Slightly Ahead」が利用可能で、新しいパッケージのデフォルトです。 この戦略により配信が加速され、飛行時間の途中で 55～65%完了します。 | 参照：[パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md).」 |
| 2021 年 3 月 18 日 | ヘルプ | 「キャンペーン管理」の章が拡張され、さらに多くの手順と参照が含まれるようになりました。 | 目次で、「キャンペーン管理」の章とサブセクションを開きます。 |
| 2021 年 3 月 11 日 | 在庫 | 現在は、 [!UICONTROL Smart Ad Serving] は VAST タグを使用して取引を行います。 代わりに、パブリッシャーに、取引 ID を使用して個人取引を実行できるかどうかを問い合わせます。 Deal ID は、 [!UICONTROL Deal ID inbox] または、取引の詳細を手動で入力します。<br><br>既存の Smart Ad Serving の契約は引き続き利用できますが、今年中に終了します。 | 参照：[について [!UICONTROL Deal ID inbox]](/help/dsp/inventory/deal-id-inbox-about.md)&quot;と&quot;[手動で作成 [!UICONTROL Deal ID] 詳細](/help/dsp/inventory/deal-id-create.md)&quot; |
| 2021 年 2 月 26 日 | ヘルプ | に関するドキュメント [!DNL Analytics for Advertising Cloud]は、Adobe AnalyticsとAdobe Advertising Cloudの統合機能です。 | 統合の概要については、[の概要 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md).」 完全なドキュメントについては、「Adobe Experience Cloudとの統合」の章を参照してください。[!DNL Analytics for Advertising Cloud].」 |
| 2020 年 10 月 28 日 | 新しいヘルプ | 従来のヘルプは更新されたページに置き換えられました。ページは、 [!DNL DSP] メインメニューおよびから常に利用可能 [https://experienceleague.adobe.com/docs/advertising-cloud/dsp/home.html](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/home.html). | — |
|  | Campaigns | 前の [!UICONTROL Campaigns Beta] ビューがデフォルトになりました。 [!UICONTROL Campaigns] ビューを使用して、より迅速なインサイト、シンプルなワークフロー、カスタマイズされたビューを実現<br><br>新しい [!UICONTROL Campaigns] 表示内容は次のとおりです。<ul><li>新しいナビゲーション。 アカウント内のすべてのキャンペーンのリストを表示できます。 キャンペーン内では、キャンペーンエンティティに基づいてデータをフィルタリングできます。 [!UICONTROL Packages], [!UICONTROL Placements]および [!UICONTROL Ads].<br><br>![キャンペーンエンティティタブ](/help/dsp/assets/campaign-subtabs.png)</li><li>データのビジュアライゼーションで最大 3 つの指標を比較できます。<br><br>![3 つの指標に関する個別のトレンドグラフ](/help/dsp/assets/trend-chart-separate.png)</li><li>カスタム列表示を作成および管理する機能（事前定義済み） [!UICONTROL Pacing] および [!UICONTROL Performance] ビュー。<br><br>![列表示セレクター](/help/dsp/assets/column-view-selector.png)</li><li>検索とフィルタリングのアップグレード</li></ul><br>レガシー [!UICONTROL Campaigns Classic] ビューは、右上のプロファイルメニューから引き続き使用できます。 を開くには、 [!UICONTROL Campaigns Classic] ビュー、クリック **[!UICONTROL Switch to Campaigns Classic]**.<br><br>![リンク [!UICONTROL Campaigns Classic]](/help/dsp/assets/switch-campaigns-classic.png)<br><br>に戻るには [!UICONTROL Campaigns] ホーム、クリック **[!UICONTROL Exit Classic]**. | 参照：[プラットフォーム内レポートについて](/help/dsp/campaign-management/reports/campaign-reports-about.md).」<br><br>関連項目[Campaign のデータビューについて](/help/dsp/campaign-management/reports/campaign-data-views-about.md).」 |
|  | 配置 | 手動入札ルールを含めるオプションが削除され、DSPの最適化で作業ができるようになりました。 最新性に基づく既存の最大入札額は、すべて自動的に最適化されるようになりました。 | — |
|  |  | 全体的なパフォーマンスを向上させるために、ビューアのタイムゾーンで時間帯区分のベースを設定できなくなりました。 代わりに、すべての時間帯区分がキャンペーンのタイムゾーンに基づいていま&#x200B;す。 | 参照：[配置設定](/help/dsp/campaign-management/placements/placement-settings.md).」 |
| 2020 年 10 月 16 日 | プライベート在庫 | すべてのユーザーが、新しい Deal ID フォームを使用して、Deal ID の詳細を設定および編集できるようになりました。これは、従来の [!UICONTROL Smart Ad Serving] フォーム。 新しい Deal ID の詳細を設定するには、 [!UICONTROL Inventory] > [!UICONTROL Deals]をクリックします。 [!UICONTROL Create]をクリックし、 [!UICONTROL Deal ID Beta]. | 参照：[Deal ID の詳細の手動作成](/help/dsp/inventory/deal-id-create.md)&quot;と&quot;[手動の Deal ID 設定](/help/dsp/inventory/deal-id-settings.md).」 |
|  | 配置の予測 | 配置レベルのペーシングを使用する配置の場合、 [!UICONTROL Forecast] 配置設定の「 」セクションには、新しい [!UICONTROL Estimated Maximums] 「 」セクションには、現在のターゲティング設定で使用可能な容量が表示されます。 | — |
| 2020 年 9 月 3 日 | レポート | 複数のDSPアカウントを持つ組織では、必要に応じて、カスタムレポートでクロスアカウントデータを有効にすることができます。 | 詳しくは、[カスタムレポートについて](/help/dsp/reports/report-about.md#cross-account-reporting).」 |
