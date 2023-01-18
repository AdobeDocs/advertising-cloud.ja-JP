---
title: CCPA オプトアウトオブセールセグメントの作成と実装
description: セグメントを作成および実装して、消費者のオプトアウトオブセールのリクエストからユーザー ID を追跡する方法について説明します。
feature: CCPA, DSP Segments
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# CCPA オプトアウトオブセールセグメントの作成と実装

セグメントを作成して、カリフォルニア州消費者プライバシー法 (CCPA) に従って、Web サイト上の消費者によるオプトアウトオブセールス要求からのユーザー ID を追跡できます。 ユーザーは、無期限に CCPA オプトアウトオブセールセグメントに残ります。

セグメントピクセルタグが実装されると、Adobe広告は、広告主に代わって ID のプールの収集を開始します。

>[!NOTE]
>
>* Adobe Experience Platform Privacy Service API を使用してAdobe広告に CCPA オプトアウトオブセールのリクエストを伝える方法について詳しくは、 [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa-opt-out-of-sale.html).
>* CCPA オプトアウトオブセールイベントの追跡に関係なく、Web ページを訪問したユーザーや、デスクトップ、モバイル、CTV デバイスから広告を受け取るユーザーを追跡するには、 [カスタムセグメント](/help/dsp/audiences/custom-segment-create.md).


1. セグメントの作成：

   1. メインメニューで、 **オーディエンス/セグメント**.

   1. データテーブルの上にある **[!UICONTROL Create]**.

   1. 一意の **[!UICONTROL Segment Name]**.

      推奨セグメント名：&quot;&lt;*広告主名*> - CCPA Opt Out of Sale（ACME - CCPA Opt Of Sale など）

   1. の [!UICONTROL Segment Type]を選択します。 **[!UICONTROL CCPA Opt-out of sale]**.

   1. クリック **[!UICONTROL Save]**.

1. セグメントを追跡するピクセルタグをコピーして実装します。

   1. 戻る **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. セグメント行で、新しいセグメントの上にカーソルを置き、 **[!UICONTROL Get pixel]**.

   1. 画像ピクセルをコピーします ( `<img src="https://rtd-tm.everesttech.net"`) を使用して、Web ページへのデスクトップおよびモバイル訪問者のユーザー ID を収集します。

   1. 会社が CCPA オプトアウトオブセールのリクエスト（同意管理プラットフォームの使用など）を追跡するために使用するメカニズムを使用して、デプロイメント用のタグを広告主または Web サイトの連絡先に提供します。

      広告主の IT 部門やその他のグループは、タグの導入をスケジュールしたり、通知を受けたりする必要がある場合があります。

      ピクセルが実装されると、Adobe広告は、広告主に代わって ID のプールの収集を開始します。

      実装の選択とロジックは広告主次第ですが、次に、広告主がピクセルを実行する方法の例を示します。

      1. 消費者が広告主のホームページにランディングします。
      1. 消費者は、広告主の「CCPA オプトアウトオブセール」ボタンを見つけてクリックします。
      1. 消費者には、広告主が働くサービスプロバイダーのリストが表示されます。
      1. 消費者は、データをAdobe広告に販売することをオプトアウトするために、ボックスをオンにします。

         このアクションは、実行するピクセルをトリガー化し、指定した「[!UICONTROL CCPA Opt-out of sale]」セグメント内に存在します。

>[!MORELIKETHIS]
>
>* [カリフォルニア州消費者プライバシー法に対するAdobe広告のサポート：消費者のオプトアウトのサポート](/help/privacy/ccpa-opt-out-of-sale.md)
>* [について [!UICONTROL CCPA Opt-out-of-Sale] セグメントとレポート](ccpa-opt-out-about.md)
>* [消費者オプトアウトオブセールレポートの取得](ccpa-opt-out-segment-report-retrieve.md)
>* [カスタムセグメントの作成と実装](custom-segment-create.md)
>* [Audience Management について](audience-about.md)

