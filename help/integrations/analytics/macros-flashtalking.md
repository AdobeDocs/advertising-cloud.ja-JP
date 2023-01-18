---
title: 追加 [!DNL Analytics for Advertising] マクロ先 [!DNL Flashtalking] 広告タグ
description: 理由と追加方法を説明します [!DNL Analytics for Advertising] マクロを [!DNL Flashtalking] 広告タグ
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 追加 [!DNL Analytics for Advertising] マクロ先 [!DNL Flashtalking] 広告タグ

*Advertising とAdobe AnalyticsのAdobeの統合のみの広告主*

*Advertising DSPのみに適用*

の広告タグを使用する場合 [!DNL Flashtalking] Advertising DSP広告の場合、ランディングページの URL に Advertising 用の Analytics パラメーターを追加します。 パラメーターレコード `s_kwcid` および `ef_id` ランディングページ URL のクエリー文字列パラメーター。Adobe広告は、広告のクリックデータをAdobe Analyticsに送信できます。

マクロの使用対象 [!DNL Flashtalking] 次のタイプのディスプレイ広告とビデオ広告 [!DNL Analytics for Advertising] 実装：

* **次を持つ広告主 [!DNL Adobe] [!DNL Analytics for Advertising] Web サイトに実装された JavaScript コード**:JavaScript コードは既に `s_kwcid` および `ef_id` クエリー文字列パラメーター。 ただし、マクロを使用すると、サードパーティ cookie がサポートされていない場合に、クリックベースのコンバージョンを追跡に含めるようになります。 ベストプラクティスは、JavaScript コードで取り込まれていない追加のクリックスルーデータを取り込むために、以降のセクションのマクロを広告タグに追加することです。

>[!NOTE]
>
>JavaScript コードは、cookie が引き続き使用可能な間にのみクリック追跡をおこなうためのソリューションです。 Cookie が廃止されたら、次のマクロの実装が必要になります。

* **Web サイトが [!DNL Analytics for Advertising] JavaScript コードを使用し、代わりにを使用します。 [!DNL Analytics] クリックスルーデータ専用のサーバー側転送** （ビュースルーデータを含まない）:Adobe広告を通じて購入した広告に基づくオンサイトクリックアクティビティをレポートするには、次のマクロが必要です。

## ディスプレイ広告タグ

内 [!DNL Flashtalking] 広告タグ設定で、のクリックスルー URL の末尾に次のマクロを追加します。 `Clicktag` フィールド：

```html
?[ftqs:[AdobeAMO]]
```

例：  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## ビデオ広告タグ

内 [!DNL Flashtalking] 広告タグ設定で、のクリックスルー URL の末尾に次のマクロを追加します。 `Clicktag` フィールド：

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

例：  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe広告 ID が [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [追加 [!DNL Analytics for Advertising] マクロ先 [!DNL Google Campaign Manager 360] 広告タグ](/help/integrations/analytics/macros-google-campaign-manager.md)

