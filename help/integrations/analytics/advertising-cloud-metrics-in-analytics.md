---
title: Analysis WorkspaceのAdvertising Cloud指標
description: Analysis WorkspaceのAdvertising Cloud指標
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Analysis WorkspaceのAdvertising Cloud指標

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

>[!NOTE]
>
>* Advertising Cloudはトラフィック指標とディメンションを毎日[!DNL Analytics]に渡します。
>* [!DNL Analytics] はAdvertising Cloudのクリックスルー数とビュースルー数をリアルタイムで取り込みます。


## Advertising Cloudからのトラフィック指標

>[!NOTE]
>
>[!DNL Analytics]内のすべてのAdvertising Cloudトラフィック指標は「AMO」で始まります。

| トラフィック指標 | 説明 |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Advertising Cloudインプレッション数。 |
| [!UICONTROL AMO Clicks] | Advertising Cloudクリック総数。 |
| [!UICONTROL AMO Cost] | Advertising Cloudはレポートスイートの通貨で支出します。 |
| [!UICONTROL AMO ID Instance] | Advertising Cloud IDが設定された回数。 |
| [!UICONTROL AMO Minutes Viewed] | Advertising Cloudビデオが視聴された時間（分）。 |
| [!UICONTROL AMO Views] | 広告の視聴回数。 ビューアがAdvertising Cloudビデオを開始すると、ビューがカウントされます。 |
| [!UICONTROL AMO Views 25% Complete] | Advertising Cloudビデオの少なくとも25%が視聴された視聴回数。 |
| [!UICONTROL AMO Views 50% Complete] | Advertising Cloudビデオの少なくとも50%が視聴された視聴回数。 |
| [!UICONTROL AMO Views 75% Complete] | Advertising Cloudビデオの少なくとも75%が視聴された視聴回数。 |
| [!UICONTROL AMO Views 100% Complete] | Advertising Cloudビデオの100%が視聴された視聴回数。 |
| [!UICONTROL AMO Viewable Impressions] | 配置設定に従って表示可能と測定されたインプレッション数。 |
| [!UICONTROL AMO Not Viewable Impressions] | 表示できないと判断されたインプレッションの数。 この値は([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ])として計算されます。 |
| [!UICONTROL AMO Measurable Impressions] | 視認性インストルメンテーションが正常に初期化された、提供されたインプレッション数。 この値は、（計測されたインプレッション — 測定できないインプレッションの数）として計算されます。 |

## Advertising Cloudに役立つカスタム計算指標

Advertising Cloudデータ用の次の指標を作成することを検討します。

* ランディングページインスタンス([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks])へのクリック数：これは、広告をクリックしてランディングページに表示した訪問者の割合です。
* 測定可能な率([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* 表示可能なインプレッション率([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* ビューあたりのコスト([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* クリックあたりのコスト([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Advertising CloudDimension

>[!NOTE]
>
>[!DNL Analytics]内のすべてのAdvertising Cloudディメンションの後に「(AMO ID)」が続きます。

| Dimension | 適用可能なAdvertising Cloudデータ | 説明 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] とデ [!DNL Search] ータ | Advertising Cloud DSPまたは検索エンジン名 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] とデ [!DNL Search] ータ | アカウント名。 |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] とデ [!DNL Search] ータ | RTB([!DNL DSP])または広告ネットワーク名([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] とデ [!DNL Search] ータ | キャンペーン名。 |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] とデ [!DNL Search] ータ | パッケージ([!DNL DSP])またはポートフォリオ([!DNL Search])の名前。 |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | 配置名。 |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] data | 広告グループ名。 |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] data | キーワード。 |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] data | 検索一致タイプ。 |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] data | キーワードと一致タイプ。 |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] とデ [!DNL Search] ータ | `text`、`video`、`display`、`native`などの広告タイプ。 |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] とデ [!DNL Search] ータ | 広告のタイプ([!DNL DSP])または広告のタイトル([!DNL Search])。 |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] とデ [!DNL Search] ータ | 広告の説明([!DNL DSP])または広告本文([!DNL Search])。 |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] data | 広告に表示されるURL。 |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] data | 広告の表示先URL。 |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] とデ [!DNL Search] ータ | ランディングページエントリがビュースルーかクリックスルーか。 |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] data | 製品リスト広告の製品ターゲット。 |

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [[!DNL Analytics] Advertising Cloudのデータ](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

