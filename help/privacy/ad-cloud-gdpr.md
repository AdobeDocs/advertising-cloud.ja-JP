---
title: Adobe Advertising Cloud EU一般データ保護規則のサポート
description: サポートされるデータリクエストのタイプ、必須設定値とフィールド値、および従来の製品IDと返されたデータフィールドを使用したAPIアクセスリクエストの例について説明します
feature: GDPR
exl-id: 304d88d0-d63d-4b32-8d4d-c61ba2409adc
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 0%

---

# Adobe Advertising Cloud EU一般データ保護規則のサポート

*Adobe Advertising Cloud Search、Adobe Advertising Cloud Creative、Adobe Advertising Cloud DSP、Adobe Media Optimizer DCO*

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 EU一般データ保護規則に関するアドバイスについては、弁護士に相談してください。

2018年5月25日施行の法律であるGDPR(General Data Protection Regulation)は、欧州連合(EU)圏内にあるすべての個人（データ主体）に対して個人データの制御を提供し、国際ビジネスの規制環境を簡素化します。 この法律は、データ管理者の事業所に関係なく、個人データの処理時にEU圏内の個人に対して商品やサービスを提供、監視、収集するすべての企業（データ管理者）に適用されます。

Adobe Experience Cloudは、顧客に代わって受信および保存する個人データのデータ処理者としての役割を果たします。 データ管理者であるお客様は、Adobe Experience Cloudに処理および保管を委任する個人データを決めます。

このドキュメントでは、Advertising Cloud Search、Advertising Cloud Creative、Advertising Cloud DSP(Demand Side Platform)、Media Manager DCOが、Adobe Experience Platform Privacy Service APIとPrivacy ServiceUIを使用して、データ主体のGDPRデータアクセスおよび削除権をどのようにサポートするかについて説明します。

GDPRがお客様のビジネスに与える意味について詳しくは、「[GDPRとお客様のビジネス](https://www.adobe.com/privacy/general-data-protection-regulation.html)」を参照してください。

## Advertising Cloudでサポートされているデータリクエストタイプ

Adobe Experience Platformは、企業が次のタスクを実行する機能を提供します。

* [!DNL Search]、[!DNL Creative]、[!DNL DSP]または[!DNL DCO]内で、データ主体のCookieレベルのデータまたは（モバイルアプリの広告の）デバイスIDレベルのデータにアクセスします。
* ブラウザーを使用して、データ主体の[!DNL Search]、[!DNL Creative]、[!DNL DSP]、または[!DNL DCO]に保存されているcookieレベルのデータを削除する。モバイルデバイスでアプリを使用するデータ主体向けに[!DNL DSP]に保存されているIDレベルのデータを削除する。
* 1つまたはすべての既存のリクエストのステータスを確認します。

## Advertising Cloud用のリクエストを送信するために必要な設定

Advertising Cloudのデータへのアクセスおよび削除をリクエストするには、次の操作が必要です。

1. JavaScriptライブラリをデプロイして、データ主体のCookieを取得および削除します。 同じライブラリ`AdobePrivacy.js`がすべてのAdobe Experience Cloudソリューションで使用されます。

   >[!IMPORTANT]
   >
   >一部のAdobe Experience CloudソリューションへのリクエストにはJavaScriptライブラリが必要ないが、Advertising Cloudへのリクエストには必要である。

   ライブラリは、会社のプライバシーポータルなど、データ主体がアクセス要求や削除要求を送信できるWebページにデプロイする必要があります。 ライブラリを使用すると、AdobeCookie(名前空間ID:`gsurferID`)を送信して、Adobe Experience Platform Privacy Service APIを介してこれらのIDをアクセス要求および削除要求の一部として送信できるようにする必要があります。

   データ主体が個人データの削除を要求すると、ライブラリはデータ主体のブラウザーからデータ主体のCookieも削除します。

   >[!NOTE]
   >
   >個人データの削除は、オプトアウトとは異なります。オプトアウトは、オーディエンスセグメントを持つエンドユーザーのターゲティングを停止します。 ただし、データ主体が[!DNL Creative]、[!DNL DSP]または[!DNL DCO]からの個人データの削除を要求すると、ライブラリはAdvertising Cloudに対しても、セグメントターゲティングからデータ主体をオプトアウトするよう要求します。 [!DNL Search]を持つ広告主の場合は、オーディエンスセグメントのターゲティングをオプトアウトする方法を説明する、[https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)へのリンクをデータ主体に提供することをお勧めします。

1. IMS Org IDを特定し、Advertising Cloudアカウントにリンクされていることを確認します。

   IMS Org IDは、24文字の英数字と共に使用される文字列で、末尾に@AdobeOrgが付きます。 ほとんどのAdobe Experience Cloudのお客様には、IMS Org IDが割り当てられています。 マーケティングチームまたは内部Adobeシステム管理者が組織のIMS Org IDを把握していない場合、またはIMS Org IDがプロビジョニングされているかどうかが不明な場合は、Adobeカスタマーケア(gdprsupport@adobe.com)にお問い合わせください。 プライバシーAPIにリクエストを送信するには、IMS Org IDが必要です。

   >[!IMPORTANT]
   >
   >会社のAdvertising Cloud担当者に連絡して、組織のAdvertising Cloudアカウント（[!DNL DSP]アカウントまたは広告主、[!DNL Search]アカウント、[!DNL Creative]または[!DNL DCO]アカウントを含む）がIMS Org IDにリンクされていることを確認してください。

1. [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html)（自動リクエストの場合）または[Privacy ServiceUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html)（アドホックリクエストの場合）を使用して、データサブジェクトに代わってAdvertising Cloudにアクセス要求と削除要求を送信し、既存の要求のステータスを確認します。

   モバイルアプリを持つ広告主がデータ主体とやり取りし、DSPでキャンペーンを開始する場合は、Experience Cloud用にプライバシー対応のMobile SDKをダウンロードする必要があります。 Mobile SDKを使用すると、データ管理者はオプトアウトステータスフラグの設定、データ主体のデバイスID(名前空間ID:deviceID)を使用して、要求をPrivacy ServiceAPIに送信します。 モバイルアプリには、SDKバージョン4.15.0以降が必要です。

   データ主体のアクセスリクエストを送信すると、Privacy ServiceAPIは指定されたCookieまたはデバイスIDに基づいてデータ主体の情報を返します。この情報はデータ主体に返す必要があります。

   データ主体の削除リクエストを送信すると、Cookie IDまたはデバイスIDと、そのCookieに関連するすべてのコスト、クリック、売上高のデータがサーバーから削除されます。

   >[!NOTE]
   会社に複数のAdobe Experience Cloud Identity Management Service組織ID(IMS Org ID)がある場合は、それぞれに対して個別のAPIリクエストを送信する必要があります。 ただし、1つのサブソリューションにつき1つのアカウントを使用して、複数のAdvertising Cloudサブソリューション([!DNL Search]、[!DNL Creative]、[!DNL DSP]、[!DNL DCO])に対して1つのAPIリクエストを送信できます。

これらの手順はすべてAdvertising Cloudに必要です。 Adobe Experience Platform Privacy Serviceを使用して実行する必要があるこれらのタスクやその他の関連タスクの詳細、および必要な項目の見つけ方については、[www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html)を参照してください。

## Advertising Cloud JSONリクエストの必須フィールド値

&quot;&quot;会社コンテキスト&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;>IMS Org ID値&#x200B;*>*

`"users":`

* `"key":` &lt;>通常はデータ主体の名前&#x200B;*>*

* `"action":` どちらか `**access**` または  `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (cookie領域を示 [!DNL adcloud] します)

   * `"value":` &lt;>>から取得した実際のデータ主体のCookie ID値 `AdobePrivacy.js`*。*

* `"include": **adCloud**` (リクエストに適用されるAdobe製品)

* `"regulation": **gdpr**` （リクエストに適用されるプライバシー規則）

## `AdobePrivacy.js`から取得したAdvertising CloudユーザーIDを使用してデータ主体から送信された要求の例

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
    "regulation":"gdpr"
}
}
```

## アクセス要求に対して返されるデータフィールド

Advertising Cloudのアクセス応答の例を次に示します。

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
