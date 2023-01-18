---
title: Analysis WorkspaceのAdobe広告指標
description: Analysis WorkspaceのAdobe広告指標
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Analysis WorkspaceのAdobe広告指標

*Advertising とAdobe AnalyticsのAdobeの統合のみの広告主*

>[!NOTE]
>
>* Adobe広告がトラフィック指標およびディメンションをに渡します。 [!DNL Analytics] 毎日
>* [!DNL Analytics] は、Adobe広告のクリックスルー数とビュースルー数をリアルタイムでキャプチャします。


## Adobe広告のトラフィック指標

>[!NOTE]
>
>のすべてのAdobe広告トラフィック指標 [!DNL Analytics] 「AMO」で始まる

| トラフィック指標 | 説明 |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Adobe広告インプレッション数。 |
| [!UICONTROL AMO Clicks] | Adobe広告のクリック総数。 |
| [!UICONTROL AMO Cost] | Adobe広告は、レポートスイートの通貨での支出です。 |
| [!UICONTROL AMO ID Instance] | Adobe広告 ID が設定された回数。 |
| [!UICONTROL AMO Minutes Viewed] | Adobe広告ビデオが表示された時間（分）。 |
| [!UICONTROL AMO Views] | 広告の視聴回数。 ビューアが広告ビデオのAdobeを開始すると、ビューがカウントされます。 |
| [!UICONTROL AMO Views 25% Complete] | Adobe広告ビデオの少なくとも 25%が視聴された視聴回数。 |
| [!UICONTROL AMO Views 50% Complete] | Adobe広告ビデオの少なくとも 50%が視聴された視聴回数。 |
| [!UICONTROL AMO Views 75% Complete] | Adobe広告ビデオの少なくとも 75%が視聴された視聴回数。 |
| [!UICONTROL AMO Views 100% Complete] | Adobe広告ビデオの 100%が視聴された視聴回数。 |
| [!UICONTROL AMO Viewable Impressions] | 配置設定に従って表示可能と測定されたインプレッション数。 |
| [!UICONTROL AMO Not Viewable Impressions] | 表示不可と判断されたインプレッションの数。 この値は ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ]) をクリックします。 |
| [!UICONTROL AMO Measurable Impressions] | 視認性計測が正常に初期化された、提供されたインプレッション数。 この値は、 （計測されたインプレッション数 — 測定できないインプレッション数）として計算されます。 |

## Adobe広告に役立つカスタム計算指標

Adobe広告データ用に次の指標を作成することを検討します。

* ランディングページインスタンスに対するクリック数 ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]):これは、広告をクリックしてランディングページに表示したユーザーの割合です。
* 測定可能な率 ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* 表示可能なインプレッション率 ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* ビュー単価 ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* クリック単価 ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Adobe広告Dimension

>[!NOTE]
>
>のすべてのAdobe広告ディメンション [!DNL Analytics] の後に「(AMO ID)」が続きます。

| Dimension | 該当するAdobe広告データ | 説明 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] および [!DNL Search] データ | Advertising DSPまたは検索エンジン名 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] および [!DNL Search] データ | アカウント名。 |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] および [!DNL Search] データ | RTB ([!DNL DSP]) または広告ネットワーク名 ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] および [!DNL Search] データ | キャンペーン名。 |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] および [!DNL Search] データ | パッケージ ([!DNL DSP]) またはポートフォリオ ([!DNL Search]) 名を入力します。 |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] データ | 配置名。 |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] データ | 広告グループ名。 |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] データ | キーワード。 |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] データ | 検索一致タイプ。 |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] データ | キーワードと一致のタイプ。 |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] および [!DNL Search] データ | 広告のタイプ（例： ） `text`, `video`, `display`または `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] および [!DNL Search] データ | 広告タイプ ([!DNL DSP]) または広告タイトル ([!DNL Search]) をクリックします。 |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] および [!DNL Search] データ | 広告の説明 ([!DNL DSP]) または広告本文 ([!DNL Search]) をクリックします。 |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] データ | 広告に表示される URL。 |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] データ | 広告のリンク先 URL。 |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] および [!DNL Search] データ | ランディングページのエントリがビュースルーかクリックスルーか。 |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] データ | 製品リスト広告の製品ターゲット。 |

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Adobe広告のデータ](/help/integrations/analytics/analytics-data-in-advertising.md)

