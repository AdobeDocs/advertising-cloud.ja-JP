---
title: Adobe Advertising Cloud州消費者プライバシー法(&#58)のサポート消費者向けオプトアウトオブセールのサポート
description: 消費者のオプトアウトオブセールのリクエストをキャプチャするためのサポートについて説明します。
feature: CCPA
exl-id: 2c0cd4f5-798f-479a-99cd-f555cd676766
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 0%

---

# Adobe Advertising Cloud州消費者プライバシー法のサポート：消費者向けオプトアウトオブセールのサポート

*Adobe Advertising CloudDemand Side Platform*

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 カリフォルニア州消費者プライバシー法に関するアドバイスについては、弁護士に相談してください。

カリフォルニア州消費者プライバシー法(CCPA)は、2020年1月1日に施行されるカリフォルニア州の新しいプライバシー法です。 CCPAは、カリフォルニア州民に個人情報に関する新しい権利を提供し、カリフォルニア州でビジネスをおこなう特定の事業者に対してデータ保護の責任を課します。 CCPAは、消費者に対し、データにアクセスし削除する権利と、個人情報をサードパーティに「販売」すると見なされる特定のアクティビティをオプトアウトする権利を提供します。

お客様は、ビジネスとして、Adobe Experience Cloudに処理および保管を委任する個人データを決定します。

Adobe Advertising Cloudは、サービスプロバイダーとして、Advertising Cloudの製品およびサービスの使用に適用されるCCPAに基づく義務を果たすためのサポートを提供します。これには、個人情報のアクセスおよび削除に対する消費者要求の管理、個人情報の販売のオプトアウトの管理などが含まれます。

このドキュメントでは、Adobe Advertising CloudDemand Side Platform(DSP)が、CCPAによって各用語が定義されるので、「個人情報」の「販売」からオプトアウトする消費者権利を、サービスプロバイダーとしてどのようにサポートするかについて説明します。 これには、販売オプトアウトリクエストをAdvertising Cloudに伝える方法、および組織の販売オプトアウトリクエストのレポートを取得する方法に関する情報が含まれます。

Advertising Cloud Search、Advertising Cloud Creative、Advertising Cloud DSP(Demand Side Platform)、Media Manager DCOが消費者の個人情報のアクセスおよび削除権をどのようにサポートするかについて詳しくは、カリフォルニア州消費者プライバシー法(CPI)の[Adobe Advertising Cloudサポートを参照してください。消費者データのアクセスと削除のサポート](/help/privacy/ad-cloud-ccpa-access-delete.md)。

CCPAのAdobeプライバシーサービスについて詳しくは、[Adobeプライバシーセンター](https://www.adobe.com/privacy/ccpa.html)を参照してください。

## Advertising Cloudへの消費者のオプトアウトオブセール要求の伝達

次のいずれかを使用して、消費者のオプトアウトオブセール要求を伝えることができます。

* Advertising Cloud DSPで作成されたCCPAオプトアウトオブセールセグメント
* Adobe Experience Platform Privacy Service API

### 方法1:Advertising Cloud DSPの[!UICONTROL CCPA Opt-Out-of-Sale]セグメントを使用したCCPAオプトアウトオブセールのリクエストの伝達

>[!NOTE]
>
>ユーザーは、無期限にCCPAオプトアウトオブセールセグメントにとどまります。

1. Advertising Cloud DSP([https://advertising.adobe.com/](https://advertising.adobe.com/))の広告主のアカウントにログインします。
1. [CCPAオプトアウトオブセールセグメントを作成し、セグメントピクセルを実装してオプトアウトリクエストを取り込みます](/help/dsp/audiences/ccpa-opt-out-segment-create.md)。

### 方法2:Adobe Experience Platform Privacy Service APIを使用したCCPAオプトアウトオブセールのリクエストの伝達

*広告主がExperience Cloud組織ID(IMS Org ID)のみを割り当てた*

1. JavaScriptライブラリをデプロイして、顧客のCookieを取得します。 同じライブラリ`AdobePrivacy.js`がすべてのAdobe Experience Cloudソリューションで使用されます。

   >[!IMPORTANT]
   >
   >一部のAdobe Experience CloudソリューションへのリクエストにはJavaScriptライブラリが必要ないが、Advertising Cloudへのリクエストには必要である。

   ライブラリはWebページにデプロイします。このWebページから、会社のプライバシーポータルなど、販売のオプトアウトリクエストを送信できます。 ライブラリを使用すると、AdobeCookie(名前空間ID:`gsurferID`)を送信して、Adobe Experience Platform Privacy Service APIを介して販売のオプトアウトリクエストの一部としてこれらのIDを送信できるようにする必要があります。

1. IMS Org IDを特定し、Advertising Cloudアカウントにリンクされていることを確認します。

   IMS Org IDは、24文字の英数字と共に使用される文字列で、末尾に@AdobeOrgが付きます。 ほとんどのAdobe Experience Cloudのお客様には、IMS Org IDが割り当てられています。 マーケティングチームまたは内部Adobeシステム管理者が組織のIMS Org IDを把握していない場合、またはIMS Org IDがプロビジョニングされているかどうかが不明な場合は、Adobeカスタマーケア(gdprsupport@adobe.com)にお問い合わせください。 プライバシーAPIにリクエストを送信するには、IMS Org IDが必要です。

   >[!IMPORTANT]
   >
   >会社のAdvertising Cloud担当者に連絡して、組織のAdvertising Cloudアカウント（[!DNL DSP]アカウントまたは広告主、[!DNL Search]アカウント、[!DNL Creative]または[!DNL DCO]アカウントを含む）がIMS Org IDにリンクされていることを確認してください。

1. Adobe Experience Platform Privacy Service APIを使用して、消費者の代わりに販売オプトアウトリクエスト](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html)をAdvertising Cloudに送信し、既存のリクエストのステータスを確認します。[

   以下の付録では、販売オプトアウトリクエストの例を示します。

   >[!NOTE]
   ビジネスに複数のAdobe Experience Cloud Identity Management Service組織ID(IMS Org ID)がある場合は、それぞれに対して個別のAPIリクエストを送信する必要があります。 ただし、1つのサブソリューションにつき1つのアカウントを使用して、複数のAdvertising Cloudサブソリューション([!DNL Search]、[!DNL Creative]、[!DNL DSP]、[!DNL DCO])に対して1つのAPIリクエストを送信できます。

これらの手順はすべて、Advertising Cloudからサポートを受けるために必要です。 Adobe Experience Platform Privacy Serviceを使用して実行する必要があるこれらのタスクやその他の関連タスクの詳細、および必要な項目の見つけ方については、[https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)を参照してください。

## 販売オプトアウトオブリクエストを送信した消費者のレポートの取得

Advertising Cloudは、顧客がアカウントのオプトアウトオブセールの要求のために送信したIDの月別レポートを生成します。 各レポートは、GZIP形式に圧縮されたタブ区切りテキストファイルとして使用できます。 データは、Advertising Cloud DSPで作成されたCCPAオプトアウトオブセールセグメントと、Privacy ServiceAPIを介しておこなわれた送信を使用してキャプチャされたリクエストを統合します。 CCPAオプトアウトオブセールセグメントでキャプチャされたユーザーIDは、セグメントおよび広告主によって識別されます。 レポートは、前月の毎月1日に生成されます。 例えば、6月の月別ユーザーリストは7月1日に公開されます。

過去3か月間に作成された月別レポートへのリンクは、Advertising Cloud DSP内から、またはAdvertising Cloud [!DNL Trafficking API]を使用して取得できます。 各リンクは7日間有効ですが、顧客がリンクを取得しようとするたびに更新されます。

### 方法1:Advertising Cloud DSP内での消費者のオプトアウトオブセールレポートの取得

1. Advertising Cloud DSP([https://advertising.adobe.com/](https://advertising.adobe.com/))の広告主のアカウントにログインします。
1. [レポートを取得します](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md)。

### 方法2:Advertising Cloud [!DNL Trafficking API]を使用して消費者のオプトアウトオブセールレポートを取得する

この機能は、[!DNL Trafficking API]を使用する組織で使用できます。 詳しくは、 [!DNL Trafficking API]のドキュメントを参照してください。

[!DNL Trafficking API]を使用していないが、詳細を知りたい場合は、担当のAdobeアカウントマネージャーにお問い合わせください。

## 付録：例[!UICONTROL CCPA Opt-Out-of-Sale]Privacy ServiceAPIユーザーのリクエスト

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

* `"namespace": "AdCloud"` はcookie領 `AdCloud` 域を示し、対応する値はから取得された顧客のcookie IDです。  `AdobePrivacy.js`
* `"include": ["AdCloud"]` は、リクエストがAdvertising Cloudに適用されることを示します
