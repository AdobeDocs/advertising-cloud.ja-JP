---
title: Adobe Advertising Cloud州消費者プライバシー法(&#58)のサポート消費者データのアクセスおよび削除のサポート
description: サポートされるデータリクエストのタイプ、必須設定値とフィールド値、および従来の製品IDと返されたデータフィールドを使用したAPIアクセスリクエストの例について説明します。
feature: CCPA
exl-id: 1330da6c-a944-4bb5-8539-488d97f56175
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Adobe Advertising Cloud州消費者プライバシー法のサポート：消費者データのアクセスおよび削除のサポート

*Adobe Advertising Cloud Search、Adobe Advertising Cloud Creative、Adobe Advertising Cloud DSP、Adobe[!DNL Media Optimizer DCO]*

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 カリフォルニア州消費者プライバシー法に関するアドバイスについては、弁護士に相談してください。

カリフォルニア州消費者プライバシー法(CCPA)は、2020年1月1日に施行されるカリフォルニア州の新しいプライバシー法です。 CCPAは、カリフォルニア州民に個人情報に関する新しい権利を提供し、カリフォルニア州でビジネスをおこなう特定の事業者に対してデータ保護の責任を課します。 CCPAは、消費者に対し、自分の個人情報にアクセスし削除する権利と、第三者に対して個人情報を「販売」すると見なされる特定の活動をオプトアウトする権利を提供します。

お客様は、ビジネスとして、Adobe Experience Cloudに処理および保管を委任する個人データを決定します。

Adobe Advertising Cloudは、サービスプロバイダーとして、Advertising Cloudの製品およびサービスの使用に適用されるCCPAに基づく義務を果たすためのサポートを提供します。これには、個人情報のアクセスおよび削除の要求の管理、個人情報の販売のオプトアウトの要求の管理などが含まれます。

このドキュメントでは、Advertising Cloud Search、Advertising Cloud Creative、Advertising Cloud DSP(Demand Side Platform)、[!DNL Media Optimizer DCO]（サービスプロバイダー）が、Adobe[!DNL Experience Platform Privacy Service API]と[!DNL Privacy Service UI]を使用して、消費者の個人情報へのアクセス権と削除権をどのようにサポートするかを説明します。

Advertising Cloud DSPが、個人情報の販売のオプトアウトに対する消費者権利をどのようにサポートしているかについて詳しくは、カリフォルニア州消費者プライバシー法(CPI)の[Adobe Advertising Cloudサポートを参照してください。消費者のオプトアウトのサポート](/help/privacy/ad-cloud-ccpa-opt-out-of-sale.md)。

CCPAのAdobeプライバシーサービスについて詳しくは、[Adobeプライバシーセンター](https://www.adobe.com/privacy/ccpa.html)を参照してください。

## Advertising Cloudでサポートされているデータリクエストタイプ

Adobe Experience Platformは、企業が次のタスクを実行する機能を提供します。

* [!DNL Search]、[!DNL Creative]、[!DNL DSP]または[!DNL DCO]内で、消費者のCookieレベルのデータまたはデバイスIDレベルのデータ（モバイルアプリの広告用）にアクセスします。
* ブラウザーを使用している消費者向けに、[!DNL Search]、[!DNL Creative]、[!DNL DSP]または[!DNL DCO]に保存されているCookieレベルのデータを削除する。または、モバイルデバイスでアプリを使用する消費者向けに[!DNL DSP]に保存されたIDレベルのデータを削除します。
* 1つまたはすべての既存のリクエストのステータスを確認します。

## Advertising Cloud用のリクエストを送信するために必要な設定

Advertising Cloudから消費者の個人情報にアクセスして削除するようにリクエストするには、次の操作が必要です。

1. JavaScriptライブラリをデプロイして、顧客のCookieを取得および削除します。 同じライブラリ`AdobePrivacy.js`がすべてのAdobe Experience Cloudソリューションで使用されます。

   >[!IMPORTANT]
   >
   >一部のAdobe Experience CloudソリューションへのリクエストにはJavaScriptライブラリが必要ないが、Advertising Cloudへのリクエストには必要である。

   ライブラリは、お客様がアクセス要求や削除要求（会社のプライバシーポータルなど）を送信できるWebページにデプロイする必要があります。 ライブラリを使用すると、AdobeCookie(名前空間ID:`gsurferID`)を送信して、[!DNL  Adobe Experience Platform Privacy Service API]を介してこれらのIDをアクセス要求および削除要求の一部として送信できるようにします。

   顧客が個人データの削除を要求すると、ライブラリは顧客のブラウザーから顧客のCookieも削除します。

   >[!NOTE]
   >
   >個人データの削除は、オーディエンスセグメントを持つエンドユーザーのターゲティングを停止するオプトアウトとは異なります。 ただし、消費者が[!DNL Creative]、[!DNL DSP]または[!DNL DCO]からの個人データの削除を要求すると、ライブラリはAdvertising Cloudに対しても、顧客に対してセグメントのターゲティングからのオプトアウトの要求を送信します。 [!DNL Search]を持つ広告主の場合は、オーディエンスセグメントのターゲティングをオプトアウトする方法について、 [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)へのリンクをお客様に提供することをお勧めします。

1. IMS Org IDを特定し、Advertising Cloudアカウントにリンクされていることを確認します。

   IMS Org IDは、24文字の英数字と共に使用される文字列で、末尾に「@AdobeOrg」が付きます。 ほとんどのAdobe Experience Cloudのお客様には、IMS Org IDが割り当てられています。 マーケティングチームまたは内部Adobeシステム管理者が組織のIMS Org IDを把握していない場合、またはIMS Org IDがプロビジョニングされているかどうかが不明な場合は、Adobeカスタマーケア(gdprsupport@adobe.com)にお問い合わせください。 プライバシーAPIにリクエストを送信するには、IMS Org IDが必要です。

   >[!IMPORTANT]
   >
   >会社のAdvertising Cloud担当者に連絡して、組織のAdvertising Cloudアカウント（[!DNL DSP]アカウントまたは広告主、[!DNL Search]アカウント、[!DNL Creative]または[!DNL DCO]アカウントを含む）がIMS Org IDにリンクされていることを確認してください。

1. [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html)（自動リクエストの場合）または[Privacy ServiceUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html)（アドホックリクエストの場合）を使用して、消費者に代わってAdvertising Cloudにアクセスおよび削除のリクエストを送信し、既存のリクエストのステータスを確認します。

   モバイルアプリを持つ広告主が顧客とやり取りし、[!DNL DSP]とキャンペーンを開始する場合は、Experience Cloud用にプライバシー対応のMobile SDKをダウンロードする必要があります。 モバイルSDKを使用すると、企業はオプトアウトステータスフラグを設定し、消費者のデバイスID(名前空間ID:`deviceID`)を送信し、Privacy ServiceAPIに要求を送信します。 モバイルアプリには、SDKバージョン4.15.0以降が必要です。

   消費者アクセス要求を送信すると、Privacy ServiceAPIは指定されたCookieまたはデバイスIDに基づいて消費者の情報を返します。この情報は消費者に返す必要があります。

   消費者削除リクエストを送信すると、そのcookieに関連付けられたcookie IDまたはデバイスIDとすべてのコスト、クリック数、売上高のデータがサーバーから削除されます。

   >[!NOTE]
   ビジネスに複数のAdobe Experience Cloud Identity Management Service組織ID(IMS Org ID)がある場合は、それぞれに対して個別のAPIリクエストを送信する必要があります。 ただし、1つのサブソリューションにつき1つのアカウントを使用して、複数のAdvertising Cloudサブソリューション([!DNL Search]、[!DNL Creative]、[!DNL DSP]、[!DNL DCO])に対して1つのAPIリクエストを送信できます。

これらの手順はすべて、Advertising Cloudからサポートを受けるために必要です。 Adobe Experience Platform Privacy Serviceを使用して実行する必要があるこれらのタスクやその他の関連タスクの詳細、および必要な項目の見つけ方については、[https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)を参照してください。

## Advertising Cloud JSONリクエストの必須フィールド値

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;>IMS Org ID値&#x200B;*>*

&quot;users&quot;:

* `"key":` &lt;>通常は顧客の名前&#x200B;*>*

* `"action":` どちらか `**access**` または  `**delete**`

* `"user IDs":`

   * `"namespace": **411**` （adcloudのcookie領域を示します）。

   * `"value":` &lt;>>から取得した実際の顧客のCookie ID値 `AdobePrivacy.js`*。*

* `"include": **adCloud**` (リクエストに適用されるAdobe製品)

* `"regulation": **ccpa**` （リクエストに適用されるプライバシー規則）

## AdobePrivacy.jsから取得したAdvertising CloudユーザーIDを使用して消費者が送信した要求の例

```
{
"companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
  "userIDs":[
      {
         "namespace":"411",
         "value":"Wqersioejr-wdg",
         "type":"namespaceId",
         "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
}
```

## アクセス要求に対して返されるデータフィールド

以下は、Advertising Cloudの個人情報アクセスに対する応答の例です。

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
