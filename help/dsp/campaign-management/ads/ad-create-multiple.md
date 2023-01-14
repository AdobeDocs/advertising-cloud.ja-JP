---
title: 複数のサードパーティ広告の作成
description: 一度に複数のサードパーティ広告を作成する方法を説明します。
feature: DSP Ads
exl-id: 83d35d27-1ab6-4fcf-877f-650a2dc6975a
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# 複数のサードパーティ広告の作成

サードパーティの広告サーバーでホストされるクリエイティブアセットを指すタグをアップロードすることで、一度に最大 500 個のサードパーティ広告を作成できます。 広告のトラッキングピクセルを含めることができます。<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

次のいずれかをアップロードできます。 [!DNL DoubleClick] および [!DNL Flashtalking] タグシート、または提供されたテンプレートを使用して手動で入力したファイル。

>[!TIP]
>
> ベストプラクティスは、HTTPS を使用して安全に提供されるサードパーティの広告を使用することです。 HTTPS を使用して提供された URL は、「https」で始まります。

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. 広告を含めるキャンペーンの名前をクリックします。

1. データテーブルの上にある **[!UICONTROL Create]**. メニューの「広告タイプ」セクションで、 **[!UICONTROL Bulk upload ads]**.

1. 広告がホストされている広告サーバーを選択します。 *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]*&#x200B;または *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] および [!DNL Flashtalking] ads) 各ビデオアセットおよび各ディスプレイアセットに使用するタグタイプを選択します。 使用可能なオプションは、広告サーバーによって異なります。

1. ( 以下を除くすべての広告サーバーの広告 [!DNL DoubleClick] および [!DNL Flashtalking]) クリック **[!UICONTROL Download this template]** テンプレートを [!DNL Microsoft Excel] スプレッドシート (XLSX) 形式。広告データを入力し、ローカルに保存できます。 必要な列は次のとおりです。 [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag]、および [!UICONTROL Ad Types].

1. クリック **[!UICONTROL Upload]** お使いのデバイスまたはネットワークから.xlsx 形式または.xls 形式のファイルを選択します。

   の場合 [!DNL DoubleClick] および [!DNL Flashtalking] 広告を開き、編集されていないタグシートを広告サーバーからアップロードします。 その他の広告サーバーの場合は、手順 3 でダウンロードしたテンプレートを使用します。

1. アップロードが完了したら、 **[!UICONTROL Start Building Ads]**.

1. 各広告の詳細とステータスを確認します。

   1. 各広告のステータスを確認します。これは、アップロードされたタグに対する検証チェックに基づいています。

   1. （オプション）各広告に対して、次のいずれかの操作を実行します。

      * 広告をプレビューするには、 ![play](/help/dsp/assets/play.png) 広告行に表示されます。

      * 広告の詳細を編集するには、 ![編集](/help/dsp/assets/edit.png)、詳細を編集し、 **保存**.

      * 広告を削除するには、 **[!UICONTROL X]** 広告行に表示されます。

1. クリック **[!UICONTROL Create *N *広告]**.

1. 次のいずれかの操作を行います。

   * クリック **[!UICONTROL Done]**.

   * ( 広告が拒否された場合。（オプション）広告レコードを編集し、レビュー用に広告を再送信するには、次の手順に従います。

      1. 広告名をクリックします。

      1. 広告設定を編集します。

      1. クリック **[!UICONTROL Save & submit for review]**.

>[!MORELIKETHIS]
>
>* [広告管理について](ad-about.md)
>* [広告の仕様](ad-specs.md)
>* [単一の広告の作成](ad-create.md)
>* [ビデオ：サードパーティの広告タグの一括アップロード方法](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)

