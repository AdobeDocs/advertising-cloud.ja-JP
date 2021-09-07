---
title: 複数のサードパーティ広告の作成
description: 一度に複数のサードパーティ広告を作成する方法を説明します。
feature: Ads
exl-id: 83d35d27-1ab6-4fcf-877f-650a2dc6975a
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# 複数のサードパーティ広告の作成

サードパーティの広告サーバーでホストされるクリエイティブアセットを指すタグをアップロードすることで、一度に最大500個のサードパーティ広告を作成できます。 広告の追跡ピクセルを含めることができます。<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

[!DNL DoubleClick]タグシートと[!DNL Flashtalking]タグシート、または提供されたテンプレートを使用して手動で入力したファイルをアップロードできます。

サードパーティ広告を1つ作成するには、[広告の作成](ad-create.md)を参照してください。

>[!TIP]
>
> ベストプラクティスは、HTTPSを使用して安全に提供されるサードパーティの広告を使用することです。 HTTPSを使用して提供されるURLは「https」で始まります。

1. メインメニューで&#x200B;**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 広告を含めるキャンペーンの名前をクリックします。

1. データテーブルの上にある&#x200B;**[!UICONTROL Create]**&#x200B;をクリックします。 メニューの「広告タイプ」セクションで、「**[!UICONTROL Bulk upload ads]**」をクリックします。

1. 広告がホストされている広告サーバーを選択します。*[!UICONTROL DoubleClick]*、*[!UICONTROL Flashtalking]*、または&#x200B;*[!UICONTROL Other]*。

1. （[!DNL DoubleClick]および[!DNL Flashtalking]広告）各ビデオアセットと各表示アセットに使用するタグタイプを選択します。 使用可能なオプションは、広告サーバーによって異なります。

1. （[!DNL DoubleClick]と[!DNL Flashtalking]を除くすべての広告サーバーで広告）**[!UICONTROL Download this template]**&#x200B;をクリックして、テンプレートを[!DNL Microsoft Excel]スプレッドシート(XLSX)形式でダウンロードし、広告データを入力してローカルに保存できます。 必要な列は、[!UICONTROL Ad Name]、[!UICONTROL VAST/VPAID URL or Ad Tag]、[!UICONTROL Ad Types]です。

1. **[!UICONTROL Upload]**&#x200B;をクリックし、デバイスまたはネットワークから.xlsx形式または.xls形式のファイルを選択します。

   [!DNL DoubleClick]および[!DNL Flashtalking]広告の場合は、編集されていないタグシートを広告サーバーからアップロードします。 その他の広告サーバーの場合は、手順3でダウンロードしたテンプレートを使用します。

1. アップロードが完了したら、「**[!UICONTROL Start Building Ads]**」をクリックします。

1. 各広告の詳細とステータスを確認します。

   1. 各広告のステータスを確認します。これは、アップロードされたタグの検証チェックに基づいています。
   1. （オプション）各広告に対して、次のいずれかの操作を実行します。
      * 広告をプレビューするには、広告行の「![play](/help/dsp/assets/play.png)」をクリックします。
      * 広告の詳細を編集するには、![edit](/help/dsp/assets/edit.png)をクリックし、詳細を編集して、「**保存**」をクリックします。
      * 広告を削除するには、広告の行の&#x200B;**[!UICONTROL X]**&#x200B;をクリックします。

1. 「**[!UICONTROL Create *N *広告]**」をクリックします。

1. 次のいずれかの操作を行います。

   * クリック **[!UICONTROL Done]**.

   * （広告が拒否された場合）（オプション）広告レコードを編集し、広告をレビュー用に再送信するには：
      1. 広告名をクリックします。
      1. 広告設定を編集します。
      1. クリック **[!UICONTROL Save & submit for review]**.

>[!MORELIKETHIS]
>
>* [広告管理について](ad-about.md)
>* [広告の作成](ad-create.md)
>* [使用可能な広告タイプ](ad-types.md)
>* [広告の仕様](/help/dsp/assets/ad-specs.pdf)

