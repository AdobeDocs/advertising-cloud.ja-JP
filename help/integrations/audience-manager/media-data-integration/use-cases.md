---
title: 使用例
description: Advertising DSPのメディアデータをAudience Managerと共有する使用例について説明します
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Adobe Audience Managerでのメディア露出データのキャプチャの使用例

*Advertising DSPのみの広告主*

*Advertising とAdobe Audience ManagerのAdobeの統合のみの広告主*

Advertising DSPのメディア露出データをキャプチャすることでメリットが得られる方法を次に示します <!-- ad impression data? --> Audience Manager

## 最新性と頻度の管理

Audience Managerでインプレッションデータをキャプチャすると、特定の広告やキャンペーンに公開されたユーザーのセグメントを作成し、頻度管理を強化できます。 これらのセグメントは、頻度を増やす場合は広告ターゲティングに、頻度を制限する場合は広告抑制に使用できます。

また、Audience Manager [!DNL Segment Builder]を使用する場合、 [最新性と頻度の制御](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) 任意の [ルールベースの特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) アクションにつながるシグナルを含んだ これにより、例えば、メディアキャンペーン内でユーザーが特定のクリエイティブを表示する回数を制限できます。 「[Instant Cross-Device Suppression](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)」を参照してください。<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## 順次メッセージ

インプレッションデータをキャプチャすることで、キャンペーンや広告に公開されたユーザーのセグメントを作成し、このセグメントを順次メッセージや抑制に使用できます。 例えば、クリエイティブを閲覧したユーザーをリターゲティングできます `123` クリエイティブな画像を表示して、クリックまたは変換しなかった `456`.

この例をAudience Managerで実行するには、次の手順に従います。<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. クリエイティブを閲覧したユーザーを取り込むための特性を作成します。

   例えば、特性の名前を指定するには、 `Creative Trait 123`の場合は、次の特性ルールを使用します。

   `d_creative == 123 AND d_event == imp`

1. クリックまたはコンバージョンをおこなうユーザーを取得する特性を作成します。

   例えば、この特性の名前をに設定するには、次のようにします。 `Click and Converter`の場合は、次の特性ルールを使用します。

   `d_event == click OR d_event=conv`

1. という名前のセグメントを作成します。 `Retarget Users` クリエイティブを見たユーザーを生み出す `123` ただし、クリックや変換は行われませんでした。 次の特性ルールを使用します。

   `Creative Trait 123 AND NOT Click and Converter`

1. セグメントのマッピング `Retarget Users` を宛先に追加し、クリエイティブを使用して宛先のユーザーをターゲット化する `456`.

## [!DNL Adobe Audience Analytics] キャンペーン露出データ

キャンペーンのインプレッションとクリックデータがAudience Manager内で使用可能になったら、特定のキャンペーンまたは戦術にさらされた、または特定のキャンペーンや戦術に対してインタラクションがおこなわれたユーザーの特性およびセグメントを作成できます。 を使用 [[!DNL Audience Analytics] 統合](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)の場合、Audience Managerセグメントを [!DNL Analytics] を参照してください。 潜在的な使用例を次に示します。

* **DSPと [!DNL Adobe Advertising Search] 広告：** 標準 [[!DNL Analytics for Advertising] 統合](/help/integrations/analytics/overview.md) では、DSPと [!DNL] の間のやり取りに関するインサイトを提供しません。 [!DNL Search]] の場合は、両方のチャネルで AMO ID 属性ルールに従う AMO ID が使用され、検索クリックで表示ビュースルーが上書きされます。 Audience ManagerでDSP露出セグメントを作成すると、 [!DNL Audience Analytics] DSPと [!DNL] の間のインタラクションを分析するには、以下を実行します。 [!DNL Search]] 広告 [!DNL Analytics].

* **頻度分析：** 特定の広告またはキャンペーンに対するAudience Managerの表示回数に基づいて、ユーザーでセグメントを作成できます。 その後、Analytics で様々な露出セグメントを分析し、DSPの露出数に応じてユーザーの行動がどのように変化するかを確認できます。

## [!DNL Audience Optimization Reports]

以下を利用して、 [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) を使用して、キャンペーン全体のセグメントで潜在的なパフォーマンス向上の機会を特定します。 これらのレポートは、キャンペーンのインプレッション、クリック、コンバージョンの各データをセグメント指標と組み合わせて、セグメントを中心とした最適化および効果的なチャネルミックスを導き出します。

### 関連するAudience Optimizationレポートのタイプ

| レポート | 説明 |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] レポート](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | インプレッションおよびコンバージョン率を使用して、マッピングされたセグメントとマッピングされていないセグメントを比較します。 |
| [[!UICONTROL Trend Analysis and Volume Analysis] レポート ]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | 様々な広告ディメンションに対して、インプレッション数、クリックスルー率およびコンバージョンに関するデータを返します。 |
| [[!UICONTROL Optimal Frequency] レポート](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | 提供されたインプレッション数とコンバージョン数の最適なバランスを見つけるのに役立ちます。 収益減少の表示を開始する前に、表示するインプレッション数を調整できます。 |
| [[!UICONTROL Unique User Reach] レポート](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | バブルチャート。各バブルのサイズは、選択したディメンションのユニークユーザー数に正比例しています。 |

### 注意点

* If [!DNL Audience Optimization Reports] 次に、ユーザーには役割ベースのアクセス制御 (RBAC) が用意され、 [!DNL Adobe Customer Care] は、広告主 ID と組織の統合データソース統合コードの間のマッピングをAudience Managerする必要があります。 その後、管理者ユーザーは様々なユーザーに RBAC の権限を提供できます。

* でのコンバージョンレポート [!DNL Audience Optimization Reports] には、エンドユーザーによる設定が必要です。 ユーザーは、メタデータファイルに値を入力する必要があります。

* [!DNL Audience Optimization Reports] では、キャンペーンメタデータ（キャンペーン名やプレースメント名など）の変更はサポートされていません。

* 検索広告のクリック数は、 [!DNL Audience Optimization Reports] インプレッション数と関連がある場合にのみ有効です。 つまり、検索のクリックは、インプレッションに続くコンバージョンとして扱われます。 その結果、多くの検索クリックが [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [DSP Media Exposure データのAdobe Audience Managerへの送信の概要](overview.md)
>* [Advertising DSP Campaigns からクリックおよびインプレッションデータを収集](collect.md)

