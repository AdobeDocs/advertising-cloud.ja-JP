---
title: 実装の前提条件と主な情報 [!DNL Analytics for Advertising Cloud]
description: 実装の前提条件と主な情報 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: d4d743ade0e2dad2b967b8316ff2261d0a82d5b0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 実装の前提条件と主な情報 [!DNL Analytics for Advertising Cloud]

*Advertising Cloud DSPとAdvertising Cloud Searchの広告主*

Advertising CloudをAdobe Analyticsと統合する前に、次の情報を確認してください。

## でのAdvertising Cloudデータのレポートの要件 [!DNL Analytics]

* 次のいずれかを実行します。
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience CloudID サービス： `visitorAPI.js` バージョン 2.0 以降
* Adobe Analytics( [!DNL Prime], [!DNL Premium]または [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` バージョン 2.1 以降

>[!TIP]
>
>データの正確性を向上させるには、各ライブラリの最新バージョンを使用します。

## Analytics セグメントをAdvertising Cloudと共有するための要件

* Experience CloudID サービス： `visitorAPI.js` バージョン 2.1 以降
* Adobe Analytics: `!DNL appMeasurement.js` バージョン 1.8 以降

## 報告の要件 [!DNL Analytics] Advertising Cloudのデータ

Advertising Cloud実装チームに以下の情報を提供します。

* この [!DNL Analytics] 有料メディアアクティビティのレポートや、Advertising Cloudでの最適化とレポートのためのサイトアクティビティのフィードに使用されるレポートスイート ID です。
* 会社のExperience Cloud組織 ID （組織 ID）。

これらの ID はどちらも [Adobe Experience Cloud Debugger の概要画面](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html).

![Experience Cloud Debugger概要画面](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Advertising Cloudのデータ {#lookback-a4adc}

理由： [!DNL Analytics] レポートと最適化のためにデータがAdvertising Cloudに送信される場合、データは、Advertising Cloudの広告主に対して設定されたインプレッションウィンドウやクリックルックバックウィンドウを含むアトリビューションルールに従います。

![Advertising Cloudの広告主レベルのルックバックウィンドウ設定](/help/integrations/assets/a4adc-lookbacks.png)

* Advertising Cloudアトリビューションクリックルックバックウィンドウ：最初のクリックが発生してからの日数。クリックはコンバージョンに関連付けられます。 デフォルトでは、この値は 60 日です。最大 90 日
* Advertising Cloudアトリビューションインプレッションのルックバックウィンドウ：インプレッションがコンバージョンに関連付けられる広告インプレッションが発生してからの日数。 デフォルトでは、この値は 14 日です。最大 30 日

   >[!NOTE]
   >
   > インプレッションのルックバックウィンドウはAdvertising Cloudに固有で、 [!DNL Analytics for Advertising Cloud]、レポート。

この [!DNL Analytics for Advertising Cloud] JavaScript では、これらの設定を使用して、ビュースルーエントリまたはクリックスルーエントリをサイトへの有効と見なすまでの距離を判断します。 ビュースルー数とクリックスルー数の決定方法について詳しくは、[Analytics で使用されるAdvertising Cloud ID](ids.md).&quot;

## Advertising Cloudでのデータ [!DNL Analytics]

[!DNL Analytics] は、広告主のeVar永続化設定に従って、Analytics ヒット内にAdvertising Cloud ID(AMO ID) を設定します。この設定は、クリックスルーとビュースルーの両方に適用されます。 永続性設定は、Advertising Cloudのバックエンドで設定され、 [!DNL Adobe] アカウントマネージャーが変更できます。

* [!DNL Analytics for Advertising Cloud] eVarの有効期限：AMO ID のデフォルトで 60 日間

>[!NOTE]
>
>別の期間でデータをセグメント化するには、次の操作を実行します。 [カスタムセグメントの設定](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) Analysis Workspace内の様々なルックバックウィンドウを使用できます。

## サポートされる広告環境

* 検索
* 表示
* ビデオ
* オンラインビデオ
* ネイティブ

お問い合わせ [!DNL Adobe] 各チャネルでサポートされる最新の広告環境のアカウントマネージャー。

## 導入の前に知っておくべきこと

* Advertising Cloud実装チームが統合を設定します。

* この統合に対して追加のコストは請求されず、サーバー呼び出しによって追加の費用が発生することもありません [!DNL Analytics] Advertising Cloud料

* [!DNL Analytics for Advertising Cloud] は、広告サーバーに依存しません。ビュースルーまたはクリックスルーは、任意の広告サーバーから発生する場合があり、サイトへのエントリ時に適切な ID が生成されます。

* 統合が渡すのは [!DNL Analytics] 後続の有料メディアおよび広告活動の入札最適化のための標準およびカスタムイベントをAdvertising Cloudに送信。 合わない [!DNL Analytics] セグメント、計算指標、eVar(Advertising Cloudへの eVar) を使用して、入札を最適化できます。

* Advertising Cloudが内で永続的な ID を作成する [!DNL Analytics] ユーザーがサイトに入る前にクリックまたは表示された最後の広告に基づき、 [クリックおよびビュースルーのルックバックウィンドウ](#lookback-a4adc) Advertising Cloudで設定されます。 サイト訪問者がプロファイル内で両方のタイプのサイトエントリインタラクションをおこなう場合で、クリックがルックバック期間内の場合、訪問者のクリックスルー ID は、サイトレポートのビュースルー ID よりも優先されます。

* [!DNL Analytics for Advertising Cloud] Adobe Analyticsのコンバージョントラッキングでは、設定可能なトラッキングルックバックウィンドウが使用されます（デフォルトで 60 日間）。 Advertising Cloudレポートは、このトラッキングルックバックウィンドウの終わりに、サイトのコンバージョンとエンゲージメントを反映しています。

* すべての広告タイプがサポートされています。 ただし、一部の広告環境がサポートされているわけではありません。

   例えば、接続された TV(CTV) 広告は、CTV でクリックが発生せず、同じデバイスでコンバージョンが発生しないので、追跡されません。 ただし、広告がデスクトップ環境内で表示される場合、一部のビュースルーサイトエントリデータが追跡される可能性があります。

* [!DNL Analytics] コンバージョンは現在追跡されており、同じデバイス上の訪問者にのみ関連付けられます。

* [!DNL Analytics for Advertising Cloud] では、アプリ内ビュースルーコンバージョンをサポートしていません。

* ビュースルートラッキングは、 [!DNL Analytics].

### 追加の ID

サイトにExperience CloudID サービスを実装すると、 [!DNL Analytics] またはAdvertising Cloudには追加の ID が含まれています。

例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

正確なデータ統合のために、 [!DNL Analytics for Advertising Cloud] コンテンツを配信または目標指標を記録するアクティビティには、対応する [!DNL Analytics] 同じ追加の ID を共有するヒット。

を使用して [!DNL Analytics]に設定する場合は、 [!DNL Analytics] ヒット数。 内 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html)の場合、この ID は「 Advertising Cloud 」タブで `sdid` パラメーター。

>[!NOTE]
>
> この実装は、 [!DNL Analytics for Target] 統合とも呼ばれます。

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud向け Analytics 用 JavaScript コード](/help/integrations/analytics/javascript.md)

