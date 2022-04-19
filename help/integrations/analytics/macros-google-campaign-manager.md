---
title: 追加 [!DNL Analytics for Advertising Cloud] マクロ先 [!DNL Google Campaign Manager 360] 広告タグ
description: 理由と追加方法を説明します [!DNL Analytics for Advertising Cloud] マクロを [!DNL Google Campaign Manager 360] 広告タグ
feature: Integration with Adobe Analytics
source-git-commit: 3c2dc9337794ca1a6d57ca76642f5a5e05ecbe9a
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# 追加 [!DNL Analytics for Advertising Cloud] マクロ先 [!DNL Google Campaign Manager 360] 広告タグ

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

*Advertising Cloud DSPのみに適用*

の広告タグを使用する場合 [!DNL Google Campaign Manager 360] Advertising Cloud DSP広告で、 [`%p` マクロ](https://support.google.com/campaignmanager/table/6096962). パラメーターを使用することで、Advertising Cloudは広告のクリックデータをAdobe Analyticsに送信できます。

マクロの使用対象 [!DNL Campaign Manager 360] 次のタイプのディスプレイ広告とビデオ広告 [!DNL Analytics for Advertising Cloud] 実装：

* **次を持つ広告主 [!DNL Adobe] [!DNL Analytics for Advertising Cloud] Web サイトに実装された JavaScript コード**:Advertising Cloudを通じて購入した広告のクリックスルーデータが、追加のマクロなしでAdobe Analyticsに表示されます。 ただし、サードパーティ Cookie をサポートせず、したがって JavaScript コードで取り込まれないブラウザーでクリックスルーデータを取り込むには、次の節のマクロを [!DNL Campaign Manager 360] 広告タグ。

>[!NOTE]
>
>JavaScript コードは、cookie が引き続き使用可能な間にのみクリック追跡をおこなうためのソリューションです。 Advertising Cloudが Cookie を中断したら、次のマクロの実装が必要になります。

* **Web サイトが [!DNL Analytics for Advertising Cloud] JavaScript コードを使用し、代わりにを使用します。 [!DNL Analytics] クリックスルーデータ専用のサーバー側転送** （ビュースルーデータを含まない）:Advertising Cloudで購入した広告に基づくオンサイトクリックアクティビティをレポートするには、次のマクロが必要です。

## にマクロを追加する [!DNL Google Campaign Manager 360] 広告

内 [!DNL Google Campaign Manager 360]を次のパラメーターに追加して、ランディングページの URL に追加します。 `%pamo=!;`

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


## 広告主レベルのランディングページの URL サフィックスの設定

1. メインメニューで、 [!UICONTROL Advertisers] タブをクリックします。
1. 広告主名をクリックします。
1. 内 [!UICONTROL Landing page URL suffix] 設定、含む `%pamo!;` 内 [!UICONTROL URL suffix] フィールドに入力します。

## キャンペーンレベルのランディングページ URL サフィックスの設定

1. メインメニューで、 [!UICONTROL Campaigns] タブをクリックします。
1. キャンペーン名をクリックします。
1. クリック [!UICONTROL Properties].
1. 内 [!UICONTROL Landing page URL suffix] 設定、含む `%pamo!;` 内 [!UICONTROL URL suffix] フィールドに入力します。

## クリエイティブレベルのランディングページ URL サフィックスの設定

1. メインメニューで、 [!UICONTROL Campaigns] タブをクリックします。
1. キャンペーン名をクリックします。
1. 内 [!UICONTROL Views] メニュー、選択 [!UICONTROL Creatives].
1. クリエイティブ名をクリックします。
1. 内 [!UICONTROL Click tags] 設定、含む `%pamo!;` 内 [!UICONTROL Landing page] 列をクリックします。

## 方法 [!DNL Analytics for Advertising Cloud] マクロはDSPで展開されます

DSPで、 [!DNL Analytics for Advertising Cloud] パラメータ (`amo`)、 `ef_id` および `s_kwcid` マクロはクリック URL に自動的に追加されます。 ベストプラクティスは、DSPでタグをチェックして、 `ef_id` および `s_kwcid` マクロが存在する。

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
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [追加 [!DNL Analytics for Advertising Cloud] マクロ先 [!DNL Flashtalking] 広告タグ](macros-flashtalking.md)
