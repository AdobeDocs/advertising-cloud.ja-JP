---
title: Advertising DSP Campaigns からクリックおよびインプレッションデータを収集
description: Audience Managerピクセルを使用して Advertising DSP広告から cookie ベースのインプレッションとクリックイベントをキャプチャする方法を説明します
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Advertising DSP Campaigns からメディア露出データを収集

*Advertising DSPのみの広告主*

*Advertising とAdobe Audience ManagerのAdobeの統合のみの広告主*

このドキュメントでは、Advertising DSP広告にタグを付け、Audience Managerピクセルを使用した cookie ベースのインプレッションおよびクリックイベントを取り込む方法と、データの使用に必要な追加タスクについて説明します。

イベントピクセルは、モバイルアプリや接続済み TV(CTV) など、Cookie がない環境で発生するイベントをキャプチャしません。

## 手順 1:データソースをAudience Manager {#set-up-data-source}

Audience Managerで、 [データソース](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) DSPインプレッションとクリックデータ用に作成されます。 データソース ID を含める [各イベントタグ](#implement-dsp-pixels) したがって、追跡されるすべてのイベントがデータソースに関連付けられます。

>[!NOTE]
> 1 つのデータソース内で複数のDSP上で実行される広告キャンペーンのすべてのインプレッションとクリックデータを収集できます。

## 手順 2:Web ページにインプレッションとクリックイベントのピクセルを実装する {#implement-dsp-pixels}

広告主は、自社のブランドのイベントタグを作成して実装できます。 必要に応じて、担当のAdobe Audience Managerコンサルタントまたは [!DNL Adobe] サポートのアカウントマネージャー。

>[!NOTE]
>
>組織が [!DNL Analytics] をトラッキングする場合、Audience Managerクリックの追跡が不要な場合があります。 Adobe Analyticsはクリックシグナルをキャプチャし、を通じてAudience Managerに送信できます。 [サーバー側転送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### ピクセル構文

イベントピクセルには、次のパラメーターを含める必要があります。

**インプレッション追跡ピクセル：**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

と [オプションの追加パラメーター](#parameters) 先頭に `&`

**クリック追跡ピクセル：**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

と [オプションの追加パラメーター](#parameters) 先頭に `&`

ここで、

* `[Audience Manager customer domain]` は、インプレッションまたはクリックイベントを送信する先のドメイン名です。 [!DNL Adobe].

* `[source id]` は、 [データソース](#set-up-data-source) DSPのインプレッションとクリックデータを追跡する場所です。

* `[redirect URL]` は、二重エンコードされたリダイレクト URL です。 www.urlencoder.orgなどのオンラインエンコーディングツールを使用している場合は、エンコーダーを通じて文字列を実行し、結果を再エンコードします。

* `${TM_CAMPAIGN_ID_NUM}` は、DSPのキャンペーン ID（数値）です。 DSPマクロを使用する代わりに個々のキャンペーン ID をハードコードする場合は、キャンペーン設定で ID を探します。

* 各 [パラメータ](#key-value-pairs) は、 `&` とはの形式です。 `d_parameter=parameter_id`で、 `parameter` は、新しいフィールドのキーと値のペアに置き換えられます。 例： `&d_placement=${TM_PLACEMENT_ID_NUM}`

### キーと値のペアとしてのパラメーター {#parameters}

**形式：**  `d_parameter=parameter_id`

    場所：
    
    *パラメーターには「&amp;」のプレフィックスが付きます。
    
    * &#39;parameter&#39;は、新しいフィールドのキーと値のペアに置き換えられます
    
    例：&#39;&amp;d_placement=${TM_PLACEMENT_ID_NUM}&#39;

どちらのタイプのピクセルにも、追加のパラメーターを *キー値ペア* 特性を収集したり、他のレポートにキャンペーンメタデータ（配置名やキャンペーン名など）を提供したりする場合。 キーと値のペアは、次の 2 つの関連要素で構成されます。a *key*：データセットを定義する定数で、 *値*：セットに属する変数。

キーと値のペアでは、値変数は、ハードコードされた ID または *マクロ*：自己完結型のコードの小さな単位です。広告タグがキャンペーンおよびユーザートラッキング用に読み込まれる際に、対応する値に動的に置き換えられます。 キャンペーン関連のパラメーターの場合は、 [DSPマクロ](/help/dsp/campaign-management/macros.md) Audience Managerマクロの代わりに、キャンペーン属性を対応するインプレッションまたはクリックデータと共にAudience Managerに送信し、すべての広告で 1 つのピクセルを使用します。 イベントピクセルに挿入するDSPマクロは、ピクセル内に含めるキーと値のペアに適した値である必要があります。 例えば、 `d_placement` キー、DSPマクロを使用します。 `${TM_PLACEMENT_ID_NUM}` を値として使用して、Adobe広告マクロで生成される配置 ID を取り込みます。

インプレッションイベントピクセルでAudience Managerがサポートするマクロの一覧については、[ピクセル呼び出しを使用したキャンペーンのインプレッションデータのキャプチャ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

クリックイベントのピクセルに対してAudience Managerがサポートするマクロの一覧については、[ピクセル呼び出しを使用したキャンペーンのクリックデータのキャプチャ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* ベストプラクティスは、キャンペーン、プレースメント、クリエイティブ（広告）およびサイト ID を含め、キャンペーン属性を使用してAudience Manager特性を作成できるようにすることです。
>* Audience Optimizationレポートを作成するには、追加のパラメーターが必要です。
>* キーと値のペアで、値を [DSPマクロ](/help/dsp/campaign-management/macros.md) したがって、すべてのキャンペーンのすべての広告で 1 つのピクセルを使用できます。 例えば、 `d_campaign=[%campaignID%]`から `d_campaign=${TM_CAMPAIGN_ID_NUM}` を使用して、キャンペーン広告マクロで生成されたAdobeID を取り込みます。
>* 必要に応じて、ハードコードされた値を持つ独自のパラメーターを作成できます。 例： `d_DSP=AdCloud`


インプレッションイベントピクセルの例：

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### ピクセルを追加する場所

#### Impression-Tracking ピクセル

内のすべての広告にインプレッションイベントトラッキングピクセルをアタッチする [!DNL DSP] キャンペーン。 これは、次のいずれかの場所で実行できます。

* 配置レベル。配置内のすべての広告にデフォルトでピクセルを適用します。 配置設定の「トラッキング」セクションで、 [[!UICONTROL Event pixels] フィールド](/help/dsp/campaign-management/placements/placement-settings.md).

* 広告レベル。配置レベルのイベントピクセルを上書きします。 広告設定で、 [上にイベントピクセルを作成する [!UICONTROL Pixel] タブ](/help/dsp/campaign-management/ads/ad-edit.md).

* （サードパーティの広告サーバー上の広告の場合）広告サーバー内の広告レベル。

#### クリック追跡ピクセル

広告サーバー内で、広告のクリックスルー URL を通常挿入する場所に、クリックイベントピクセル（エンコードされた URL が付く）を挿入します。

## 手順 3:導入後のタスク

イベントタグが実装されると、データはイベントデータ収集サーバーにAudience Managerされます。 レポートでデータを使用する前に、次の作業を実行します。

### の作成 [!DNL Amazon S3] バケットとデータソース

データがAudience Managerサーバー上に配置されたら、 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) バケットに送信され、そのデータソースに対して、すべてのピクセルデータが送信されます。 担当のAudience Managerコンサルタントまたは [カスタマーケア](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) サポートが必要な場合は、をクリックします。

### Audience Manager特性とセグメントの作成

イベントデータは、次のようにAudience Managerに送られます。 [未使用シグナル](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). 手動で作成 [ルールベースの特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 取り込んだデータから、 [セグメント](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) これらの特性を使用して、データをレポートで使用できるようにします。

DSPで特定のクリエイティブに公開されたユーザーのユーザーレベルのデータを入力する特性の例：

1. イベントの特定： `d_event = imp`.
1. DSPキャンペーン内のクリエイティブ ID を特定し、 `d_creative=[Creative ID]`.

![特性作成画面](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSPマクロ](/help/dsp/campaign-management/macros.md)
>* [DSP Media Exposure データのAdobe Audience Managerへの送信の概要](overview.md)
>* [使用例](use-cases.md)

