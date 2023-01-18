---
title: 実装の前提条件と主な情報 [!DNL Analytics for Advertising]
description: 実装の前提条件と主な情報 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# 実装の前提条件と主な情報 [!DNL Analytics for Advertising]

*Advertising DSPおよび[!DNL Advertising Search]*

Adobe AnalyticsとAdobe広告を統合する前に、次の情報を確認してください。

## でのAdobe広告データのレポート要件 [!DNL Analytics]

* 次のいずれかを実行します。
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience CloudID サービス： `visitorAPI.js` バージョン 2.0 以降
* Adobe Analytics( [!DNL Prime], [!DNL Premium]または [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` バージョン 2.1 以降

>[!TIP]
>
>データの正確性を向上させるには、各ライブラリの最新バージョンを使用します。

## Analytics セグメントをAdobe広告と共有する際の要件

* Experience CloudID サービス： `visitorAPI.js` バージョン 2.1 以降
* Adobe Analytics: `!DNL appMeasurement.js` バージョン 1.8 以降

## 報告の要件 [!DNL Analytics] Adobe広告のデータ

以下をAdobe広告実装チームに提供します。

* この [!DNL Analytics] 有料メディアアクティビティのレポートや、Adobe広告での最適化とレポートのためのサイトアクティビティのフィードに使用されるレポートスイート ID です。
* 会社のExperience Cloud組織 ID （組織 ID）。

これらの ID はどちらも [Adobe Experience Cloud Debugger の「概要」タブ](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Experience Cloud Debugger概要画面](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Adobe広告のデータ {#lookback-a4adc}

理由： [!DNL Analytics] レポートと最適化のためにデータがAdobe広告に送信され、データは、Adobe広告の広告主に対して設定されたインプレッションおよびクリックのルックバックウィンドウを含むアトリビューションルールに従います。

![Adobe広告における広告主レベルのルックバックウィンドウ設定](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe広告アトリビューションのルックバックウィンドウをクリック：最初のクリックが発生してからの日数。クリックはコンバージョンに関連付けられます。 デフォルトでは、この値は 60 日です。最大 90 日
* Adobe広告アトリビューションインプレッションのルックバックウィンドウ：インプレッションがコンバージョンに関連付けられる広告インプレッションが発生してからの日数。 デフォルトでは、この値は 14 日です。最大 30 日

   >[!NOTE]
   >
   > インプレッションのルックバックウィンドウはAdobe広告に固有で、 [!DNL Analytics for Advertising]、レポート。

この [!DNL Analytics for Advertising] JavaScript では、これらの設定を使用して、ビュースルーエントリまたはクリックスルーエントリをサイトへの有効と見なすまでの距離を判断します。 ビュースルー数とクリックスルー数の決定方法について詳しくは、[Analytics で使用されるAdobe広告 ID](ids.md).&quot;

## でのAdobe広告データ [!DNL Analytics]

[!DNL Analytics] は、広告主のeVar永続性設定（クリックスルー数とビュースルー数の両方に適用）に従って、Analytics ヒット内に広告 ID(AMO ID) を設定します。 永続性設定は、Adobe広告のバックエンドで設定され、 [!DNL Adobe] アカウントチームが変更できます。

* [!DNL Analytics for Advertising] eVarの有効期限：AMO ID のデフォルトで 60 日間

>[!NOTE]
>
>別の期間でデータをセグメント化するには、次の操作を実行します。 [カスタムセグメントの設定](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) Analysis Workspace内の様々なルックバックウィンドウを使用できます。

## サポートされる広告環境

* 検索
* 表示
* ビデオ
* オンラインビデオ
* ネイティブ

お問い合わせ [!DNL Adobe] 各チャネルでサポートされる最新の広告環境については、アカウントチームにお問い合わせください。

## 導入の前に知っておくべきこと

* Adobe広告の実装チームが統合を設定します。

* この統合に対して追加のコストは請求されず、サーバー呼び出しによって追加の費用が発生することもありません [!DNL Analytics] またはAdobe広告料。

* [!DNL Analytics for Advertising] は、広告サーバーに依存しません。ビュースルーまたはクリックスルーは、任意の広告サーバーから発生する場合があり、サイトへのエントリ時に適切な ID が生成されます。

* 統合が渡すのは [!DNL Analytics] 後続の有料メディアおよび広告活動の入札最適化のための標準およびカスタムイベントをAdobe広告に対して。 合わない [!DNL Analytics] セグメント、計算指標、eVar をAdobe広告に追加し、入札を最適化しました。

* Adobe広告が内に永続的な ID を作成する [!DNL Analytics] ユーザーがサイトに入る前にクリックまたは表示された最後の広告に基づき、 [クリックおよびビュースルーのルックバックウィンドウ](#lookback-a4adc) Adobe広告で設定 サイト訪問者がプロファイル内で両方のタイプのサイトエントリインタラクションをおこなう場合で、クリックがルックバック期間内の場合、訪問者のクリックスルー ID は、サイトレポートのビュースルー ID よりも優先されます。

* [!DNL Analytics for Advertising] Adobe Analyticsのコンバージョントラッキングでは、設定可能なトラッキングルックバックウィンドウが使用されます（デフォルトで 60 日間）。 Adobe広告レポートは、このトラッキングルックバックウィンドウの終わりに、サイトのコンバージョンとエンゲージメントを反映しています。

* すべての広告タイプがサポートされています。 ただし、一部の広告環境がサポートされているわけではありません。

   例えば、接続された TV(CTV) 広告は、CTV でクリックが発生せず、同じデバイスでコンバージョンが発生しないので、追跡されません。 ただし、広告がデスクトップ環境内で表示される場合、一部のビュースルーサイトエントリデータが追跡される可能性があります。

* [!DNL Analytics] コンバージョンは現在追跡されており、同じデバイス上の訪問者にのみ関連付けられます。

* [!DNL Analytics for Advertising] では、アプリ内ビュースルーコンバージョンをサポートしていません。

* ビュースルートラッキングは、 [!DNL Analytics].

### 追加の ID

サイトにExperience CloudID サービスを実装すると、 [!DNL Analytics] またはAdobe広告には、追加の ID が含まれています。

例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

正確なデータ統合のために、 [!DNL Analytics for Advertising] コンテンツを配信または目標指標を記録するアクティビティには、対応する [!DNL Analytics] 同じ追加の ID を共有するヒット。

を使用して [!DNL Analytics]に設定する場合は、 [!DNL Analytics] ヒット数。 内 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)の場合、この ID は、「Adobe広告」タブで `sdid` パラメーター。

>[!NOTE]
>
> この実装は、 [!DNL Analytics for Target] 統合とも呼ばれます。

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [広告用 Analytics の JavaScript コード](/help/integrations/analytics/javascript.md)

