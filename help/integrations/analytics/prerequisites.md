---
title: ' [!DNL Analytics for Advertising Cloud]の実装の前提条件と主な情報'
description: ' [!DNL Analytics for Advertising Cloud]の実装の前提条件と主な情報'
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# [!DNL Analytics for Advertising Cloud]の実装の前提条件と主な情報

*Advertising Cloud DSPとAdvertising Cloud Searchの広告主*

Advertising CloudをAdobe Analyticsと統合する前に、次の情報を確認してください。

## [!DNL Analytics]でのAdvertising Cloudデータのレポートの要件

* Experience CloudIDサービス：`visitorAPI.js`バージョン2.0以降
* Adobe Analyticsの任意のバージョン（[!DNL Prime]、[!DNL Premium]、[!DNL Ultimate]を含む）
* Adobe Analytics:`appMeasurement.js`バージョン2.1以降

>[!TIP]
>
>データの正確性を向上させるには、CNAMEをサポートするExperience CloudIDサービスの最新バージョンと、JavaScript版Analytics AppMeasurementの最新バージョンを使用します。

## AnalyticsセグメントをAdvertising Cloudと共有するための要件

* Experience CloudIDサービス：`visitorAPI.js`バージョン2.1以降
* Adobe Analytics:`!DNL appMeasurement.js`バージョン1.8以降

## Advertising Cloudでの[!DNL Analytics]データのレポートの要件

Advertising Cloud実装チームに次の情報を提供します。

* Advertising Cloudでの最適化とレポートのための有料メディアアクティビティのレポートやサイトアクティビティのフィードに使用される[!DNL Analytics]レポートスイートID。
* 会社のExperience Cloud組織ID（組織ID）。

これらのIDは両方とも、Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html)の[概要画面に表示されます。

![Experience Cloud Debugger概要画面](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Advertising Cloudのデータ {#lookback-a4adc}

[!DNL Analytics]データはレポートと最適化のためにAdvertising Cloudに送信されるので、Advertising Cloudの広告主に対して設定されたインプレッションウィンドウやクリックルックバックウィンドウなどのアトリビューションルールが適用されます。

![Advertising Cloudの広告主レベルのルックバックウィンドウ設定](/help/integrations/assets/a4adc-lookbacks.png)

* Advertising Cloudアトリビューションは、ルックバックウィンドウをクリックします。最初のクリックが発生してからの日数で、クリックがコンバージョンに関連付けられる。 デフォルトでは、この値は60日です。最大90日
* Advertising Cloudアトリビューションインプレッションのルックバックウィンドウ：インプレッションがコンバージョンに関連付けられる広告インプレッションが発生してからの日数。 デフォルトでは、この値は14日です。最大30日

   >[!NOTE]
   >
   > インプレッションのルックバックウィンドウは、Advertising Cloudに固有で、[!DNL Analytics for Advertising Cloud]レポートには固有ではありません。

[!DNL Analytics for Advertising Cloud] JavaScriptは、これらの設定を使用して、サイトへのビュースルーエントリまたはクリックスルーエントリを有効と見なす範囲を決定します。 ビュースルーとクリックスルーの決定方法について詳しくは、「[Analyticsで使用されるAdvertising Cloud ID](ids.md)」を参照してください。

## [!DNL Analytics]のAdvertising Cloudデータ

[!DNL Analytics] は、Advertising Cloud ID(AMO ID)をAnalyticsヒット内に設定します。広告主のeVar永続化設定は、クリックスルーとビュースルーの両方に適用されます。永続性設定はAdvertising Cloudバックエンドで設定され、Adobeアカウントマネージャーが変更できます。

* [!DNL Analytics for Advertising Cloud] eVarの有効期限：AMO IDのデフォルトは60日

>[!NOTE]
>
>異なる期間でデータをセグメント化するには、Analysis Workspace内で異なるルックバックウィンドウで[カスタムセグメント](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html)を設定します。

## サポートされる広告環境

* 検索
* 表示
* ビデオ
* オンラインビデオ
* ネイティブ

各チャネルでサポートされる最新のAdobe環境については、チャネルのアカウントマネージャーにお問い合わせください。

## 導入の前に知っておくべきこと

* この統合に関して追加費用は請求されません。また、サーバー呼び出しによって追加の[!DNL Analytics]やAdvertising Cloud料が発生することもありません。

* [!DNL Analytics for Advertising Cloud] は、広告サーバーに依存しません。ビュースルーまたはクリックスルーは任意の広告サーバーから発生する場合があり、適切なIDはサイトのエントリ時に生成されます。

* この統合では、標準およびカスタムのイベントのみをAdvertising Cloudに渡し、後続の有料メディアおよび広告活動の入札最適化をおこないます。 [!DNL Analytics]入札の最適化のために、[!DNL Analytics]セグメント、計算指標およびeVarをAdvertising Cloudに渡すことはありません。

* Advertising Cloudは、Advertising Cloudで設定された[クリックおよびビュースルールックバックウィンドウ](#lookback-a4adc)に基づいて、ユーザーがサイトに入る前にクリックまたは表示した最後の広告に基づいて、[!DNL Analytics]内に永続的なIDを作成します。 サイト訪問者がプロファイル内で両方のタイプのサイトエントリインタラクションをおこなう場合で、クリックがルックバック期間内の場合、訪問者のクリックスルーIDは、サイトレポートのビュースルーIDよりも優先されます。

* [!DNL Analytics for Advertising Cloud] Adobe Analyticsでのコンバージョントラッキングでは、設定可能なトラッキングルックバックウィンドウを使用します（デフォルトで60日間）。Advertising Cloudレポートは、このトラッキングルックバックウィンドウの終わりを通じてサイトのコンバージョンとエンゲージメントを反映しています。

* すべての広告タイプがサポートされています。 ただし、一部の広告環境がサポートされているわけではありません。

   例えば、CTVでクリックが発生せず、同じデバイスでコンバージョンが発生しないので、接続されたテレビ(CTV)広告は追跡されません。 ただし、広告がデスクトップ環境で表示される場合は、一部のビュースルーサイトエントリデータが追跡される可能性があります。

* [!DNL Analytics] コンバージョンは現在追跡され、同じデバイス上の訪問者にのみ関連付けられます。

* [!DNL Analytics for Advertising Cloud] では、アプリ内ビュースルーコンバージョンをサポートしていません。

* [!DNL Analytics]のサーバー側転送実装を使用する広告主では、ビュースルートラッキングはサポートされていません。

### 追加のID

Experience CloudIDサービスをサイトに実装すると、[!DNL Analytics]またはAdvertising Cloudのデータを含むヒットに追加のIDが含まれます。

例：`sdid=2F3C18E511F618CC-45F83E994AEE93A0`

正確なデータ統合を実現するために、コンテンツを配信したり目標指標を記録したりするために[!DNL Analytics for Advertising Cloud]アクティビティで使用されるすべてのAdvertising Cloud呼び出しに、同じ追加のIDを共有する対応する[!DNL Analytics]ヒットが必要です。

[!DNL Analytics]でトラブルシューティングを行う場合は、[!DNL Analytics]ヒットに追加のIDが存在することを確認してください。 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html)では、このIDが「Advertising Cloud」タブで`sdid`パラメーターとして表示されます。

>[!NOTE]
>
> この実装は、[!DNL Analytics for Target]統合と同様に機能します。

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud用AnalyticsのJavaScriptコード](/help/integrations/analytics/javascript.md)

