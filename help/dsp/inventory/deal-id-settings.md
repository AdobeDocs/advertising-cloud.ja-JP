---
title: 手動の Deal ID 設定
description: 手動で入力した Deal ID の設定の説明を参照してください。
feature: DSP Private Inventory, DSP Deal IDs
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 手動の Deal ID 設定

| セクション | パラメータ | 説明 | 必須 | 編集可能 |
|---------|-----------|-------------|----------|----------|
| [契約の詳細] | [!UICONTROL Deal name] | 識別する名前 [!UICONTROL Deal ID] (Advertising DSPの ) 名前を入力するか、 **[!UICONTROL Auto-name]** 契約の詳細に基づいてDSPが名前を生成できるようにします。<br><br>自動生成された名前の例： `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | はい | はい |
|  | [!UICONTROL External deal ID] | パブリッシャーおよび SSP がこの契約を識別するために使用する ID。 | はい | いいえ |
|  | [!UICONTROL Publisher] | この在庫を販売している発行者の名前。 | はい | いいえ |
|  | [!UICONTROL SSP] | この契約が実行されるサプライサイドプラットフォーム (SSP)。 | はい | いいえ |
|  | [!UICONTROL Media type] | この契約で購入されたメディアのタイプ： *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*&#x200B;または *[!UICONTROL Audio]*. オプションは SSP によって異なります。<br><br> 契約で複数のメディアタイプが許可されている場合は、契約の作成時にデフォルトの配置のメディアタイプを選択します。 後で、値を変更するか、 [追加のメディアタイプで新しい配置を添付する](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | はい | いいえ |
|  | [!UICONTROL Deal type] | 契約のコミットメントと価格設定の構造は、次のとおりです。<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*:自分と発行者は、一定数のインプレッション配信をコミットしていません。 CPM は市場の状況に応じて変動し増加する場合がありますが、この契約は在庫の最小価格を指定します。</li><li>*[!UICONTROL Non guaranteed (fixed)]*:自分と発行者は、一定数のインプレッション配信をコミットしていません。 価格は、ネゴシエートされた固定価格で設定されます。</li><li>*[!UICONTROL Guaranteed (fixed)]*:お客様と発行者は、事前に定義されたインプレッション数、ターゲティング、フライト日および固定価格に関して同意しました。<br><br><b>注意：</b> 保証された契約には、フライト日と、 [!UICONTROL Tracking] 」セクションに入力します。 また、契約に対してデフォルトのプログラム保証 (PG) 配置を作成する必要があります。また、オプションで、他の配置に対する契約を使用することもできます。</li></ul> | はい | いいえ |
|  | [!UICONTROL CPM] | 1,000 インプレッション (CPM) あたりのネゴシエートされたコスト。 | はい | はい |
|  | [通貨] | 契約の通貨。<br><br>すべての SSP は、米ドルでの契約を受け付けます。 SSP がDSPアカウントの通貨を受け入れると、その通貨も使用できます。 | はい | いいえ |
|  | [!UICONTROL Billing method] | すべての契約 ID は [!DNL Adobe]-financed および —invoiced DSPは、使用状況、ベンダーとの不一致の管理、および 1 つの連結請求書をアカウントに送信することに基づいて、利用可能なすべてのメディアベンダーに支払いを行います。 このオプションには、アカウントの料金カードで説明されているように、追加料金が発生します。 | はい | いいえ |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 契約にアクセスできるユーザーアカウントの電子メールアドレス。 | いいえ | はい |
|  | [!UICONTROL Advertisers that can access this deal] | この契約にアクセスできるアカウント内の特定の広告主。<br><br><b>注意：</b> この契約は、 [!UICONTROL Deals] 表示 契約行で、「 **[!UICONTROL #]**&#x200B;をクリックし、 **[!UICONTROL share]**&#x200B;をクリックし、メールアドレスと契約を共有します。 | はい | はい |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | この契約を使用するトラフィックの開始日と終了日。 これらの日付は、追跡のみを目的とし、広告配信には影響しません。<br><br><b>ヒント：</b> 内 [!UICONTROL Inventory] > [!UICONTROL Deals] ビュー、 [!UICONTROL Pacing & Budget] 列には、指定したフライト日とインプレッション目標に対する契約のペーシングが示されます。 配信のペーシングが不十分または過剰な場合は、パブリッシャーに連絡して、契約を通じて送信するボリュームを調整します。 | 保証された契約：はい<br>保証されていない契約：いいえ | はい |
|  | [!UICONTROL Impressions] | （保証されていない契約の場合はオプション）この契約を使用して実行すると予想されるインプレッション数。 この値は、追跡の目的でのみ使用されます。パブリッシャーが広告配信を制御します。 | 保証された契約：はい<br>保証されていない契約：いいえ | はい |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Deal ID の詳細の手動作成](deal-id-create.md)
>* [SSP パートナー](ssp-partners.md)
>* [プライベート在庫について](private-inventory-about.md)

