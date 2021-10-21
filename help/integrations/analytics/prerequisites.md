---
title: 実装の前提条件と主な情報 [!DNL Analytics for Advertising Cloud]
description: 実装の前提条件と主な情報 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: bfbfc293ad04b294c813ce7c8a11200e70fc812f
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---

# 実装の前提条件と主な情報 [!DNL Analytics for Advertising Cloud]

*Advertising Cloud DSPとAdvertising Cloud Searchの広告主*

Advertising CloudをAdobe Analyticsと統合する前に、次の情報を確認してください。

## でのAdvertising Cloudデータのレポートの要件 [!DNL Analytics]

* Experience CloudID サービス： `visitorAPI.js` バージョン 2.0 以降
* Adobe Analyticsの任意のバージョン ( [!DNL Prime], [!DNL Premium]または [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` バージョン 2.1 以降

>[!TIP]
>
>データの正確性を向上させるには、CNAME をサポートする最新バージョンのExperience CloudID サービスと、JavaScript 版 Analytics AppMeasurement の最新バージョンを使用します。

## Analytics セグメントをAdvertising Cloudと共有するための要件

* Experience CloudID サービス： `visitorAPI.js` バージョン 2.1 以降
* Adobe Analytics: `!DNL appMeasurement.js` バージョン 1.8 以降

## 報告の要件 [!DNL Analytics] Advertising Cloudのデータ

Advertising Cloud実装チームに次の情報を提供します。

* 10. [!DNL Analytics] 有料メディアアクティビティのレポートや、Advertising Cloudの最適化とレポートのためのサイトアクティビティのフィードに使用されるレポートスイート ID。
* 会社のExperience Cloud組織 ID（組織 ID）。

これらの ID は、 [Adobe Experience Cloud Debugger の概要画面](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html).

![Experience Cloud Debugger概要画面](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Advertising Cloudのデータ {#lookback-a4adc}

理由 [!DNL Analytics] データはレポートと最適化のためにAdvertising Cloudに送信され、Advertising Cloudの広告主に対して設定されたインプレッションウィンドウやクリックルックバックウィンドウなどのアトリビューションルールが適用されます。

![Advertising Cloudの広告主レベルのルックバックウィンドウ設定](/help/integrations/assets/a4adc-lookbacks.png)

* Advertising Cloudアトリビューションクリックルックバックウィンドウ：最初のクリックが発生してからの日数。クリックはコンバージョンに関連付けられます。 デフォルトでは、この値は 60 日です。最大 90 日
* Advertising Cloudアトリビューションインプレッションのルックバックウィンドウ：インプレッションがコンバージョンに関連付けられる広告インプレッションが発生してからの日数。 デフォルトでは、この値は 14 日です。最大 30 日

   >[!NOTE]
   >
   > インプレッションのルックバックウィンドウは、Advertising Cloudに固有で、 [!DNL Analytics for Advertising Cloud]、レポート。

10. [!DNL Analytics for Advertising Cloud] JavaScript では、これらの設定を使用して、ビュースルーエントリまたはクリックスルーエントリをサイトに有効と見なす距離を決定します。 ビュースルーとクリックスルーの決定方法について詳しくは、「[Analytics で使用されるAdvertising Cloud ID](ids.md).」

## Advertising Cloudでのデータ [!DNL Analytics]

[!DNL Analytics] は、Advertising Cloud ID(AMO ID) を Analytics ヒット内に設定します。広告主のeVar永続化設定は、クリックスルーとビュースルーの両方に適用されます。 永続性設定は、Advertising Cloudのバックエンドで設定され、 [!DNL Adobe] アカウントマネージャーが変更できます。

* [!DNL Analytics for Advertising Cloud] eVarの有効期限：AMO ID のデフォルトで 60 日

>[!NOTE]
>
>別の期間でデータをセグメント化するには、次の操作をおこないます。 [カスタムセグメントの設定](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) Analysis Workspace内の様々なルックバックウィンドウを使用

## サポートされる広告環境

* 検索
* 表示
* ビデオ
* オンラインビデオ
* ネイティブ

お問い合わせ [!DNL Adobe] 各チャネルでサポートされる最新の広告環境のアカウントマネージャー。

## 導入の前に知っておくべきこと

* この統合に関して追加費用は請求されず、サーバー呼び出しによって追加の費用が発生することはありません [!DNL Analytics] Advertising Cloud料

* [!DNL Analytics for Advertising Cloud] は、サーバーに依存しません。ビュースルーまたはクリックスルーは任意の広告サーバーから発生する場合があり、サイトのエントリ時に適切な ID が生成されます。

* 統合が渡すのは [!DNL Analytics] 標準およびカスタムイベントをAdvertising Cloudに送信し、後続の有料メディアおよび広告活動の入札の最適化をおこなう。 通り過ぎない [!DNL Analytics] セグメント、計算指標および eVar(Advertising Cloudへの入札の最適化用 )

* Advertising Cloudは、 [!DNL Analytics] ユーザーがサイトに入る前にクリックまたは閲覧した最後の広告に基づき、 [クリックおよびビュースルールックバックウィンドウ](#lookback-a4adc) Advertising Cloudで設定されます。 サイト訪問者がプロファイル内で両方のタイプのサイトエントリインタラクションをおこない、そのクリックがルックバック期間内の場合、訪問者のクリックスルー ID は、サイトレポートのビュースルー ID よりも優先されます。

* [!DNL Analytics for Advertising Cloud] Adobe Analyticsでのコンバージョントラッキングでは、設定可能なトラッキングルックバックウィンドウを使用します（デフォルトで 60 日間）。 Advertising Cloudレポートは、このトラッキングルックバックウィンドウの終わりを通じたサイトのコンバージョンとエンゲージメントを反映しています。

* すべての広告タイプがサポートされています。 ただし、一部の広告環境がサポートされているわけではありません。

   例えば、接続された TV(CTV) 広告は、CTV でクリックが発生せず、同じデバイスでコンバージョンが発生しないので、追跡されません。 ただし、広告がデスクトップ環境で表示される場合は、一部のビュースルーサイトエントリデータが追跡される可能性があります。

* [!DNL Analytics] コンバージョンは現在追跡され、同じデバイス上の訪問者のみに関連付けられます。

* [!DNL Analytics for Advertising Cloud] では、アプリ内ビュースルーコンバージョンをサポートしていません。

* ビュースルートラッキングは、 [!DNL Analytics].

### 追加の ID

Experience CloudID サービスをサイトに実装すると、 [!DNL Analytics] またはAdvertising Cloudには追加の ID が含まれています。

例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

正確なデータ統合のために、 [!DNL Analytics for Advertising Cloud] コンテンツの配信や目標指標の記録をおこなうアクティビティには、対応する [!DNL Analytics] 同じ追加 ID を共有するヒット。

を使用して [!DNL Analytics]を使用する場合は、 [!DNL Analytics] ヒット数。 の [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html)の場合、この ID は「 Advertising Cloud 」タブで、 `sdid` パラメーター。

>[!NOTE]
>
> この実装は、 [!DNL Analytics for Target] 統合とも呼ばれます。

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud用 Analytics の JavaScript コード](/help/integrations/analytics/javascript.md)

