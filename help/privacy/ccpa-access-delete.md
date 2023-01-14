---
title: カリフォルニア州消費者プライバシー法に対するAdobe広告のサポート：消費者データのアクセスと削除のサポート
description: サポートされるデータリクエストの種類、必須セットアップとフィールド値、および従来の製品 ID と返されたデータフィールドを使用した API アクセスリクエストの例について説明します。
feature: CCPA
exl-id: 1330da6c-a944-4bb5-8539-488d97f56175
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# カリフォルニア州消費者プライバシー法に対するAdobe広告のサポート：消費者データのアクセスと削除のサポート

*の場合 [!DNL Adobe Advertising Search];Adobe広告DSPAdobe広告クリエイティブおよびAdobe広告 DCO*

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 カリフォルニア州消費者プライバシー法に関するアドバイスについては、弁護士に相談してください。

カリフォルニア州消費者プライバシー法 (CCPA) は、2020 年 1 月 1 日に施行されるカリフォルニア州の新しいプライバシー法です。 CCPA は、カリフォルニア州の住民に対して個人情報に関する新しい権利を提供し、カリフォルニア州でビジネスをおこなう特定の事業者に対してデータ保護の責任を課します。 CCPA は、消費者に対し、自分の個人情報にアクセスし削除する権利と、第三者への個人情報の「販売」と見なされる特定の活動をオプトアウトする権利を提供します。

お客様は、ビジネスとして、Adobe Experience Cloudに処理および保管を委任する個人データを決定します。

Adobe広告は、Adobe広告の製品およびサービスの使用に適用される CCPA に基づく義務を果たすためのサポートを提供します。これには、個人情報のアクセスおよび削除の要求の管理や、個人情報の販売のオプトアウトに対する要求の管理などが含まれます。

このドキュメントでは、 [!DNL Advertising Search];Advertising Creative、Advertising DSP (Demand Side Platform)および [!DNL Advertising DCO]  — サービス・プロバイダとして —Adobeを使用して個人情報にアクセスし、削除する消費者の権利をサポート [!DNL Experience Platform Privacy Service API] および [!DNL Privacy Service UI].

個人情報の販売のオプトアウトに対する消費者権利を Advertising DSPがどのようにサポートしているかについて詳しくは、 [カリフォルニア州消費者プライバシー法に対するAdobe広告のサポート：消費者のオプトアウトのサポート](/help/privacy/ccpa-opt-out-of-sale.md).

CCPA のAdobeプライバシーサービスについて詳しくは、 [Adobeプライバシーセンター](https://www.adobe.com/privacy/ccpa.html).

## Adobe広告でサポートされるデータリクエストタイプ

Adobe Experience Platformは、企業が次のタスクを実行する機能を提供します。

* 内で消費者の Cookie レベルのデータまたはデバイス ID レベルのデータ（モバイルアプリの広告用）にアクセスする [!DNL Search], [!DNL Creative], [!DNL DSP]または [!DNL DCO].
* に保存されている Cookie レベルのデータの削除 [!DNL Search], [!DNL Creative], [!DNL DSP]または [!DNL DCO] ブラウザーを使用する消費者向けまたは、に保存されている ID レベルのデータを削除します。 [!DNL DSP] モバイルデバイスでアプリを使用する消費者向けの機能です。
* 1 つまたはすべての既存のリクエストのステータスを確認します。

## Adobe広告のリクエストを送信するために必要な設定

消費者の個人情報に対するアクセスおよび削除をAdobe広告からリクエストするには、次の操作が必要です。

1. JavaScript ライブラリをデプロイして、顧客の Cookie を取得および削除します。 同じライブラリ `AdobePrivacy.js`は、すべてのAdobe Experience Cloudソリューションで使用されます。

   >[!IMPORTANT]
   >
   >一部のExperience Cloudソリューションへのリクエストには JavaScript ライブラリは必要ありませんが、Adobe広告へのリクエストには必要です。

   Web ページにライブラリをデプロイし、その Web ページから、会社のプライバシーポータルなどのアクセス要求や削除要求を送信できるようにする必要があります。 ライブラリを使用すると、AdobeCookie( 名前空間 ID: `gsurferID`) を使用して、これらの id をアクセスリクエストや削除リクエストの一部として送信できるようにするため、 [!DNL Adobe Experience Platform Privacy Service API].

   顧客が個人データの削除を要求すると、ライブラリは顧客のブラウザーから顧客の Cookie も削除します。

   >[!NOTE]
   >
   >個人データの削除は、オーディエンスセグメントを持つエンドユーザーのターゲティングを停止するオプトアウトとは異なります。 ただし、消費者が次の場所から個人データを削除するように要求した場合は、 [!DNL Creative], [!DNL DSP]または [!DNL DCO]また、ライブラリは、顧客に対してセグメントのターゲティングからAdobeをオプトアウトするリクエストを広告配信に送信します。 を持つ広告主の場合 [!DNL Search]を使用する場合、 [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)：オーディエンスセグメントターゲティングをオプトアウトする方法を説明します。

1. Experience Cloudの組織 ID を特定し、組織の Advertising アカウントにリンクされていることを確認します。

   Experience Cloud組織 ID は、24 文字の英数字から成る文字列で、末尾に「@AdobeOrg」が付きます。 ほとんどのExperience Cloudのお客様には、組織 ID が割り当てられています。 マーケティングチームまたは内部Adobeシステム管理者が組織 ID を把握していない場合や、組織 ID がプロビジョニングされているかどうかが不明な場合は、Adobeカスタマーケア (gdprsupport@adobe.com) にお問い合わせください。 プライバシー API に要求を送信するには、組織 ID が、 `imsOrgID` 名前空間。

   >[!IMPORTANT]
   >
   >貴社のAdobe広告担当者に連絡して、組織のすべてのAdobe広告アカウント ( [!DNL DSP] アカウントまたは広告主 [!DNL Search] アカウントおよび [!DNL Creative] または [!DNL DCO] アカウント — がExperience Cloud組織 ID にリンクされている。

1. 次のいずれかを使用します。 [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （自動リクエストの場合）または [Privacy ServiceUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) （アドホックリクエストの場合）個人情報に対するアクセスおよび削除のリクエストをAdobe広告に送信し、消費者に代わって送信し、既存のリクエストのステータスを確認します。

   モバイルアプリを持つ広告主が顧客とやり取りし、キャンペーンを開始する [!DNL DSP]を使用する場合は、プライバシー対応のモバイル SDK をダウンロードしてExperience Cloudする必要があります。 Mobile SDK を使用すると、企業はオプトアウトステータスフラグを設定し、消費者のデバイス ID( 名前空間 ID: `deviceID`) をクリックし、リクエストをPrivacy ServiceAPI に送信します。 モバイルアプリには、SDK バージョン4.15.0以降が必要です。

   消費者のアクセス要求を送信すると、Privacy ServiceAPI は指定された Cookie またはデバイス ID に基づいて消費者の情報を返します。この情報は消費者に返す必要があります。

   消費者削除リクエストを送信すると、cookie ID またはデバイス ID と、その cookie に関連するすべてのコスト、クリック数、売上高のデータがサーバーから削除されます。

   >[!NOTE]
   ビジネスに複数のExperience Cloud組織 ID がある場合は、それぞれに対して個別の API リクエストを送信する必要があります。 ただし、複数のAdobe広告サブソリューション ([!DNL Search], [!DNL Creative], [!DNL DSP]、および [!DNL DCO]) の代わりに、サブソリューションごとに 1 つのアカウントを使用します。

これらの手順はすべて、Adobe広告からサポートを受けるために必要です。 Adobe Experience Platform Privacy Serviceを使用して実行する必要があるこれらのタスクやその他の関連タスクの詳細、および必要な項目の見つけ方については、 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Adobe広告 JSON リクエストの必須フィールド値

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*Experience Cloud組織 ID*>

&quot;users&quot;:

* `"key":` &lt;*通常、顧客の名前*>

* `"action":` どちらか `**access**` または `**delete**`

* `"user IDs":`

   * `"namespace": **411**` （adcloud の cookie 領域を示します）

   * `"value":` &lt;*から取得された実際の顧客の Cookie ID 値`AdobePrivacy.js`*>

* `"include": **adCloud**` ( リクエストに適用されるAdobe製品 )

* `"regulation": **ccpa**` （リクエストに適用されるプライバシー規則）

## AdobePrivacy.js から取得したAdobe広告ユーザー ID を使用して消費者が送信した要求の例

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

以下は、Adobe広告に対する個人情報アクセスの応答の例です。

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
