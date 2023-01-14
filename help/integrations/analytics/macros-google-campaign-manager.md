---
title: 追加 [!DNL Analytics for Advertising] マクロ先 [!DNL Google Campaign Manager 360] 広告タグ
description: 理由と追加方法を説明します [!DNL Analytics for Advertising] マクロを [!DNL Google Campaign Manager 360] 広告タグ
feature: Integration with Adobe Analytics
exl-id: 05084a85-5890-4a82-b3eb-4520f44f9d66
source-git-commit: 7c467f7a6eb2522fb998539ba01ceef8c89c3853
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# 追加 [!DNL Analytics for Advertising] マクロ先 [!DNL Google Campaign Manager 360] 広告タグ

*Advertising とAdobe AnalyticsのAdobeの統合のみの広告主*

*Advertising DSPのみに適用*

の広告タグを使用する場合 [!DNL Google Campaign Manager 360] Advertising DSP広告に、 [!DNL Analytics for Advertising] パラメーターをランディングページの URL に追加する場合は、 [`%p` マクロ](https://support.google.com/campaignmanager/table/6096962). パラメーターレコード `s_kwcid` および `ef_id` ランディングページ URL のクエリー文字列パラメーター。Adobe広告は、広告のクリックデータをAdobe Analyticsに送信できます。

マクロの使用対象 [!DNL Campaign Manager 360] 次のタイプのディスプレイ広告とビデオ広告 [!DNL Analytics for Advertising] 実装：

* **次を持つ広告主 [!DNL Adobe] [!DNL Analytics for Advertising] Web サイトに実装された JavaScript コード**:JavaScript コードは既に `s_kwcid` および `ef_id` クエリー文字列パラメーター。 ただし、マクロを使用すると、サードパーティ cookie がサポートされていない場合に、クリックベースのコンバージョンを追跡に含めるようになります。 ベストプラクティスは、JavaScript コードで取り込まれていない追加のクリックスルーデータを取り込むために、以降のセクションのマクロを広告タグに追加することです。

>[!NOTE]
>
>JavaScript コードは、cookie が引き続き使用可能な間にのみクリック追跡をおこなうためのソリューションです。 Cookie が廃止されたら、次のマクロの実装が必要になります。

* **Web サイトが [!DNL Analytics for Advertising] JavaScript コードを使用し、代わりにを使用します。 [!DNL Analytics] クリックスルーデータ専用のサーバー側転送** （ビュースルーデータを含まない）:Adobe広告を通じて購入した広告に基づくオンサイトクリックアクティビティをレポートするには、次のマクロが必要です。

## にマクロを追加する [!DNL Google Campaign Manager 360] 広告

内 [!DNL Google Campaign Manager 360]を、ディスプレイ広告およびビデオ広告の各ランディングページ URL に追加します。 `%pamo=!;`

ランディングページの URL は、複数の方法で指定できます。 各オプションの手順は、以下のサブセクションに記載されています。

次に、サフィックス付きのランディングページ URL の例を示します。

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>
>* ランディングページの URL に一般的でないハッシュ記号 (#) が含まれている場合は、 `amo` パラメーターをハッシュ記号の前に追加します。
>* 他のパラメーターが `amo` パラメーターを追加し、その後にパラメーター（&amp;a=b など）を追加します。 例：`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`


### 広告主レベルのランディングページの URL サフィックスの設定

1. 詳しくは、 [広告主プロパティを開く手順](https://support.google.com/campaignmanager/answer/2829344).
1. 内 [!UICONTROL Landing page URL suffix] 設定、含む `%pamo!;` 内 [!UICONTROL URL suffix] フィールドに入力します。

### キャンペーンレベルのランディングページ URL サフィックスの設定

1. 詳しくは、 [キャンペーンプロパティを開く手順](https://support.google.com/campaignmanager/answer/2838056#set).
1. 内 [!UICONTROL Landing page URL suffix] 設定、含む `%pamo!;` 内 [!UICONTROL URL suffix] フィールドに入力します。

### クリエイティブレベルのランディングページ URL サフィックスの設定

1. クリエイティブのプロパティを開きます。
1. 内 [!UICONTROL Click tags] 設定、含む `%pamo!;` 内 [!UICONTROL Landing page] 列をクリックします。

## 方法 [!DNL Analytics for Advertising] マクロはDSPで展開されます

DSPで、 [!DNL Analytics for Advertising] パラメータ (`amo`)、 `ef_id` および `s_kwcid` マクロはクリック URL に自動的に追加されます。 ベストプラクティスは、DSPでタグをチェックして、 `ef_id` および `s_kwcid` マクロが存在する。

次に、 [!DNL Google Campaign Manager 360] [ins タグ](https://support.google.com/campaignmanager/answer/6080468) DSPで表示されるように

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

ユーザーが広告をクリックしたとき、 [!DNL Google Campaign Manager 360] sees `%pamo` を指定し、 `amo` パラメーターを URL に追加します。

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe広告 ID が [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [追加 [!DNL Analytics for Advertising] マクロ先 [!DNL Flashtalking] 広告タグ](macros-flashtalking.md)

