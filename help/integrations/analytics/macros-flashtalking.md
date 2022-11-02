---
title: 追加 [!DNL Analytics for Advertising Cloud] マクロ先 [!DNL Flashtalking] 広告タグ
description: 理由と追加方法を説明します [!DNL Analytics for Advertising Cloud] マクロを [!DNL Flashtalking] 広告タグ
feature: Integration with Adobe Analytics
exl-id: 4b060668-723c-4cd2-b70e-409501ec67de
source-git-commit: ae516c1947d2b163ebd97dd05fb4e2870a1450d2
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# 追加 [!DNL Analytics for Advertising Cloud] マクロ先 [!DNL Flashtalking] 広告タグ

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

*Advertising Cloud DSPのみに適用*

の広告タグを使用する場合 [!DNL Flashtalking] Advertising Cloud DSP広告の場合、ランディングページの URL にAdvertising Cloud用の Analytics パラメーターを追加します。 パラメーターレコード `s_kwcid` および `ef_id` ランディングページ URL のクエリー文字列パラメーター。Advertising Cloudは、広告のクリックデータをAdobe Analyticsに送信できます。

マクロの使用対象 [!DNL Flashtalking] 次のタイプのディスプレイ広告とビデオ広告 [!DNL Analytics for Advertising Cloud] 実装：

* **次を持つ広告主 [!DNL Adobe] [!DNL Analytics for Advertising Cloud] Web サイトに実装された JavaScript コード**:JavaScript コードは既に `s_kwcid` および `ef_id` クエリー文字列パラメーター。 ただし、マクロを使用すると、サードパーティ cookie がサポートされていない場合に、クリックベースのコンバージョンを追跡に含めるようになります。 ベストプラクティスは、JavaScript コードで取り込まれていない追加のクリックスルーデータを取り込むために、以降のセクションのマクロを広告タグに追加することです。

>[!NOTE]
>
>JavaScript コードは、cookie が引き続き使用可能な間にのみクリック追跡をおこなうためのソリューションです。 Cookie が廃止されたら、次のマクロの実装が必要になります。

* **Web サイトが [!DNL Analytics for Advertising Cloud] JavaScript コードを使用し、代わりにを使用します。 [!DNL Analytics] クリックスルーデータ専用のサーバー側転送** （ビュースルーデータを含まない）:Advertising Cloudで購入した広告に基づくオンサイトクリックアクティビティをレポートするには、次のマクロが必要です。

## ディスプレイ広告タグ

内 [!DNL Flashtalking] 広告タグ設定で、のクリックスルー URL の末尾に次のマクロを追加します。 `Clicktag` フィールド：

```html
?[ftqs:[AdobeAMO]]
```

例：  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

![の例 [!DNL Flashtalking] 広告タグ設定](/help/integrations/assets/macro-flashtalking-display-ad.png)

## ビデオ広告タグ

内 [!DNL Flashtalking] 広告タグ設定で、のクリックスルー URL の末尾に次のマクロを追加します。 `Clicktag` フィールド：

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

例：  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

![の例 [!DNL Flashtalking] 広告タグ設定](/help/integrations/assets/macro-flashtalking-video-ad.png)

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud ID 使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [追加 [!DNL Analytics for Advertising Cloud] マクロ先 [!DNL Google Campaign Manager 360] 広告タグ](/help/integrations/analytics/macros-google-campaign-manager.md)

