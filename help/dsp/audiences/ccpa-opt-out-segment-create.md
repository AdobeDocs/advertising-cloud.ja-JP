---
title: CCPAオプトアウトオブセールセグメントの作成と実装
description: 消費者のオプトアウトオブセールのリクエストからユーザーIDを追跡するセグメントを作成および実装する方法について説明します。
feature: CCPA, DSP Segments
exl-id: aebe0c5b-382f-4e4a-b145-c32f32d216ca
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# CCPAオプトアウトオブセールセグメントの作成と実装

カリフォルニア州消費者プライバシー法(CCPA)に従って、Webサイト上の消費者のオプトアウトオブセール要求からユーザーIDを追跡するセグメントを作成できます。 ユーザーは、無期限にCCPAオプトアウトオブセールセグメントにとどまります。

セグメントピクセルタグが実装されると、Advertising Cloudは広告主に代わってIDのプールの収集を開始します。

>[!NOTE]
>
>* Adobe Experience Platform Privacy Service APIを使用してCCPAオプトアウトオブセールのリクエストをAdvertising Cloudに伝える方法について詳しくは、 [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)を参照してください。
>* CCPAの販売オプトアウトイベントの追跡に関係のない目的でWebページを訪問したユーザーや、デスクトップ、モバイル、CTVデバイスから広告を受けるユーザーを追跡するには、[カスタムセグメント](/help/dsp/audiences/custom-segment-create.md)を作成します。


1. セグメントの作成：

   1. メインメニューで、**オーディエンス/セグメント**&#x200B;をクリックします。

   1. データテーブルの上にある&#x200B;**[!UICONTROL Create]**&#x200B;をクリックします。

   1. 一意の&#x200B;**[!UICONTROL Segment Name]**&#x200B;を入力します。

      推奨セグメント名：&quot;&lt;*広告主名*> - CCPA Opt Out of Sale&quot;（「Acme - CCPA Opt Out of Sale」など）

   1. [!UICONTROL Segment Type]に対して、**[!UICONTROL CCPA Opt-out of sale]**&#x200B;を選択します。

   1. クリック **[!UICONTROL Save]**.

1. セグメントを追跡するピクセルタグをコピーして実装します。

   1. **[!UICONTROL Audiences]>[!UICONTROL Segments]**&#x200B;に戻ります。

   1. セグメントの行で、新しいセグメントの上にカーソルを置き、**[!UICONTROL Get pixel]**&#x200B;をクリックします。

   1. 画像ピクセル（`<img src="https://rtd-tm.everesttech.net"`で始まる）をコピーして、Webページにアクセスするデスクトップおよびモバイル訪問者のユーザーIDを収集します。

   1. 会社がCCPAオプトアウトオブセールのリクエスト（同意管理プラットフォームの使用など）を追跡するために使用するメカニズムを使用して、導入用に広告主またはWebサイトの連絡先にタグを提供します。

      広告主のIT部門やその他のグループは、タグの導入をスケジュールしたり、通知を受けたりする必要がある場合があります。

      ピクセルが実装されると、Advertising Cloudは広告主に代わってIDのプールの収集を開始します。

      実装の選択とロジックは広告主次第ですが、次に、広告主がピクセルを実行する方法の例を示します。

      1. 消費者は、広告主のホームページにランディングします。
      1. 消費者は、広告主の「CCPAオプトアウトオプトオブセール」ボタンを見つけ、クリックします。
      1. 消費者には、広告主が機能するサービスプロバイダーのリストが表示されます。
      1. 消費者は、Adobe Advertising Cloudへのデータの販売をオプトアウトするために、ボックスをオンにします。

         このアクションは、実行するピクセルをトリガーし、指定された「[!UICONTROL CCPA Opt-out of sale]」セグメント内で消費者のCookie IDを収集します。

>[!MORELIKETHIS]
>
>* [Adobe Advertising Cloud州消費者プライバシー法のサポート：消費者のオプトアウトのサポート](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [セグメン [!UICONTROL CCPA Opt-out-of-Sale] トとレポートについて](ccpa-opt-out-about.md)
>* [消費者向けオプトアウトオブセールレポートの取得](ccpa-opt-out-segment-report-retrieve.md)
>* [カスタムセグメントの作成と実装](custom-segment-create.md)
>* [Audience Managementについて](audience-about.md)

