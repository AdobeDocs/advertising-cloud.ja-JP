---
title: Adobe Advertising Cloud州消費者プライバシー法のサポート：消費者向けのオプトアウトオブセールのサポート
description: 消費者のオプトアウトオブセールのリクエストをキャプチャするためのサポートについて説明します。
feature: CCPA
exl-id: 2c0cd4f5-798f-479a-99cd-f555cd676766
source-git-commit: e00f87009fb36a057069caa53f30c7414a2ee444
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 0%

---

# Adobe Advertising Cloud州消費者プライバシー法のサポート：消費者による販売オプトアウトのサポート

*Adobe Advertising CloudDemand Side Platform*

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 カリフォルニア州消費者プライバシー法に関するアドバイスについては、弁護士に相談してください。

カリフォルニア州消費者プライバシー法 (CCPA) は、2020 年 1 月 1 日に施行されるカリフォルニア州の新しいプライバシー法です。 CCPA は、カリフォルニア州民に対し、自分の個人情報に関する新しい権利を提供し、カリフォルニア州でビジネスをおこなう特定の事業者に対してデータ保護の責任を課します。 CCPA は、消費者に対し、データにアクセスし削除する権利と、個人情報をサードパーティに「販売」すると見なされる特定のアクティビティをオプトアウトする権利を提供します。

お客様は、ビジネスとして、Adobe Experience Cloudに処理および保管を委任する個人データを決定します。

Adobe Advertising Cloudは、CCPA に基づく義務を果たすためのサポートを提供します。この義務は、個人情報にアクセスして削除する消費者要求の管理や、個人情報の販売をオプトアウトする消費者要求の管理など、Advertising Cloud製品およびサービスの使用に適用されます。

このドキュメントでは、Adobe Advertising CloudDemand Side Platform(DSP) が、CCPA で定義されている「個人情報」の「販売」からオプトアウトする消費者権利を、サービスプロバイダーとしてどのようにサポートするかについて説明します。 このレポートには、販売オプトアウトリクエストをAdvertising Cloudに伝える方法、および組織の販売オプトアウトリクエストのレポートを取得する方法に関する情報が含まれています。

Advertising Cloud Search、Advertising Cloud Creative、Advertising Cloud DSP(Demand Side Platform)、Media Manager の各 DCO が消費者の個人情報アクセス権と削除権をどのようにサポートするかについては、 [Adobe Advertising Cloud州消費者プライバシー法のサポート：消費者データのアクセスおよび削除のサポート](/help/privacy/ad-cloud-ccpa-access-delete.md).

CCPA のAdobeプライバシーサービスについて詳しくは、 [Adobeプライバシーセンター](https://www.adobe.com/privacy/ccpa.html).

## 消費者向けオプトアウトオブセール要求のAdvertising Cloudへの通信

次のいずれかを使用して、消費者のオプトアウトオブセールのリクエストを伝えることができます。

* Advertising Cloud DSPで作成された CCPA オプトアウトオブセールセグメント
* Adobe Experience Platform Privacy Service API

### 方法 1:CCPA の販売オプトアウトリクエストの伝達 ( [!UICONTROL CCPA Opt-Out-of-Sale] Advertising Cloud DSPでのセグメント

>[!NOTE]
>
>ユーザーは、無期限に CCPA オプトアウトオブセールセグメントにとどまります。

1. Advertising Cloud DSP( ) で広告主のアカウントにログインします。 [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [CCPA オプトアウトオブセールセグメントを作成し、セグメントピクセルを実装してオプトアウトリクエストを取り込む](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### 方法 2:Adobe Experience Platform Privacy Service API を使用した CCPA オプトアウトオブセールのリクエストの伝達

*広告主がExperience Cloud組織 ID(IMS Org ID) のみを割り当てた*

1. JavaScript ライブラリをデプロイして、顧客の Cookie を取得します。 同じ図書館 `AdobePrivacy.js`は、すべてのAdobe Experience Cloudソリューションで使用されます。

   >[!IMPORTANT]
   >
   >一部のAdobe Experience Cloudソリューションへのリクエストには JavaScript ライブラリが必要ないものの、Advertising Cloudへのリクエストには JavaScript ライブラリが必要なものもあります。

   ライブラリは Web ページにデプロイします。この Web ページから、お客様のプライバシーポータルなど、販売のオプトアウトリクエストを送信できます。 ライブラリを使用すると、AdobeCookie( 名前空間 ID: `gsurferID`) を使用して、Adobe Experience Platform Privacy Service API を介して販売のオプトアウトリクエストの一部としてこれらの id を送信できます。

1. IMS Org ID を特定し、自分のAdvertising Cloudアカウントにリンクされていることを確認します。

   IMS Org ID は、24 文字の英数字と共に使用される文字列で、末尾に@AdobeOrgが付きます。 ほとんどのAdobe Experience Cloudのお客様には、IMS Org ID が割り当てられています。 マーケティングチームまたは内部Adobeシステムの管理者が、組織の IMS Org ID を把握していない場合、またはプロビジョニングされているかどうかが不明な場合は、Adobeカスタマーケア (gdprsupport@adobe.com) にお問い合わせください。 プライバシー API にリクエストを送信するには、IMS Org ID が必要です。

   >[!IMPORTANT]
   >
   >貴社のAdvertising Cloud担当者に問い合わせて、組織のAdvertising Cloudアカウント ( [!DNL DSP] アカウントまたは広告主 [!DNL Search] アカウントおよび [!DNL Creative] または [!DNL DCO] アカウント — は、IMS Org ID にリンクされます。

1. Adobe Experience Platform Privacy Service API を使用して [販売オプトアウトリクエストの送信](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) をAdvertising Cloudに送信し、既存のリクエストのステータスを確認します。

   販売オプトアウトリクエストの例については、以下の付録を参照してください。

   >[!NOTE]
   ビジネスに複数のAdobe Experience Cloud Identity Management Service 組織 ID(IMS Org ID) がある場合は、それぞれに対して個別の API リクエストを送信する必要があります。 ただし、複数のAdvertising Cloudサブソリューション ([!DNL Search], [!DNL Creative], [!DNL DSP]および [!DNL DCO]) に割り当てられ、サブソリューションごとに 1 つのアカウントが使用されます。

これらの手順はすべて、Advertising Cloudからサポートを受けるために必要です。 Adobe Experience Platform Privacy Serviceを使用して実行する必要があるこれらのタスクやその他の関連タスクの詳細、および必要な項目の見つけ方については、 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## 販売オプトアウトリクエストを送信した消費者のレポートの取得

Advertising Cloudは、顧客がアカウントのオプトアウトオブセールの要求のために送信した ID の月別レポートを生成します。 各レポートは、GZIP 形式に圧縮されたタブ区切りのテキストファイルとして使用できます。 データは、Advertising Cloud DSPで作成された CCPA オプトアウトオブセールセグメントと、Privacy ServiceAPI を介しておこなわれた送信を使用して取得されたリクエストを統合します。 CCPA オプトアウトオブセールセグメントでキャプチャされたユーザー ID は、セグメントおよび広告主によって識別されます。 レポートは、前月の各月の最初に生成されます。 例えば、6 月の月別ユーザーリストは 7 月 1 日に公開されます。

過去 3 か月間に作成された月別レポートへのリンクを、Advertising Cloud DSP内から、またはAdvertising Cloudを使用して取得できます [!DNL Trafficking API]. 各リンクは 7 日間有効ですが、お客様がリンクを取得しようとするたびに更新されます。

### 方法 1:Advertising Cloud DSP内での消費者のオプトアウトオブセールレポートの取得

1. Advertising Cloud DSP( ) で広告主のアカウントにログインします。 [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [レポートの取得](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### 方法 2:Advertising Cloud [!DNL Trafficking API]

この機能は、 [!DNL Trafficking API]. 詳しくは、 [!DNL Trafficking API] を参照してください。

組織が [!DNL Trafficking API] しかし、より多くの情報に興味がある場合は、 [!DNL Adobe] アカウントマネージャー

## 付録：例 [!UICONTROL CCPA Opt-Out-of-Sale] Privacy ServiceAPI ユーザーのリクエスト

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

ここで、

* `"namespace": "AdCloud"` は、 `AdCloud` Cookie 領域に格納され、対応する値は、 `AdobePrivacy.js`
* `"include": ["AdCloud"]` は、要求がAdvertising Cloudに適用されることを示します
