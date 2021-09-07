---
title: 手動のDeal ID設定
description: 手動で入力したDeal IDの設定の説明を参照してください。
feature: Private Inventory, Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: 3dbba61766411eadbad9a8257e2930b683d0d55b
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# 手動のDeal ID設定

| セクション | パラメーター | 説明 | 必須 | 編集可能 |
|---------|-----------|-------------|----------|----------|
| [取引の詳細] | [!UICONTROL Deal name] | Advertising Cloud DSPで[!UICONTROL Deal ID]を識別する名前。 名前を入力するか、「[!UICONTROL Auto-name]」を選択して、取引の詳細に基づいてAdvertising Cloudが名前を生成するようにします。<br><br>自動生成された名前の例： [!DNL *DEAL_ID*  — 取引ID — 保証済み固定 — USD - 5 - 24キッチン — プライベート] | はい | はい |
|  | [!UICONTROL External deal ID] | パブリッシャーおよびSSPがこの取引を識別するために使用するID。 | はい | いいえ |
|  | [!UICONTROL Publisher] | この在庫を販売する発行者の名前。 | はい | いいえ |
|  | [!UICONTROL SSP] | この取引が実行されるサプライサイドプラットフォーム(SSP)。 | はい | いいえ |
|  | [!UICONTROL Media type] | この取引で購入されるメディアのタイプ：[!UICONTROL Desktop video]、[!UICONTROL Mobile video]、[!UICONTROL Connected TV]、[!UICONTROL Display]、または[!UICONTROL Audio]。 オプションはSSPによって異なります。 | はい | いいえ |
|  | [!UICONTROL Deal type] | 取引コミットメントと価格設定の構造：<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*:自分と発行者は、一定数のインプレッション配信をコミットしていません。CPMは市場の状況に応じて変動し増加する場合がありますが、この取引では、在庫の最小価格を指定します。</li><li>*[!UICONTROL Non guaranteed (fixed)]*:自分と発行者は、一定数のインプレッション配信をコミットしていません。価格は、ネゴシエートされた固定レートで設定されます。</li><li>*[!UICONTROL Guaranteed (fixed)]*:お客様と発行者は、事前に定義されたインプレッション数、ターゲティング、フライト日、固定価格に同意しています。<br><br><b>注意：</b> 保証されたお得な情報には、セクションでフライト日と指定数のインプレッションが必 [!UICONTROL Tracking] 要です。また、デフォルトのプログラム保証(PG)プレースメントを作成し、オプションで他のプレースメントにそのデールを使用することもできます。</li></ul> | はい | いいえ |
|  | [!UICONTROL CPM] | 1,000インプレッションあたりのネゴシエートされたコスト(CPM)。 | はい | はい |
|  | [通貨] | 取引の通貨。<br><br>すべてのSSPは米ドルで取引を受け付けます。SSPがDSPアカウントの通貨を受け入れると、その通貨も使用できます。 | はい | いいえ |
|  | [!UICONTROL Billing method] | すべての取引IDは[!DNL Adobe]資金提供済みで請求済みです。 Advertising Cloudは、使用状況に基づいて利用可能なすべてのメディアベンダーに支払い、ベンダーとの不一致を管理し、1件の連結請求書をアカウントに送信します。 このオプションには、アカウントのレートカードで説明されている追加料金が必要です。 | はい | いいえ |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 取引にアクセスできるユーザーアカウントの電子メールアドレス。 | いいえ | はい |
|  | [!UICONTROL Advertisers that can access this deal] | この取引にアクセスできるアカウント内の特定の広告主。<br><br><b>注意：</b> ビューから、追加のアカウントで広告主と取引を共有で [!UICONTROL Deals] きます。Deal行で&#x200B;**[!UICONTROL #]**&#x200B;をクリックし、「**[!UICONTROL share]**」をクリックして、EメールアドレスとDealを共有します。 | はい | はい |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | このディールを使用するトラフィックの開始日と終了日。 これらの日付は、追跡の目的でのみ使用され、広告配信には影響しません。<br><br><b>ヒント：</b>  /表示では、 [!UICONTROL Inventory] 列に、指定 [!UICONTROL Deals] したフライト日 [!UICONTROL Pacing & Budget] 付とインプレッションの目標に対するデータのペーシングが表示されます。配信のペーシング率が低い場合や超過している場合は、パブリッシャーに問い合わせて、配信がデールを通じて送信するボリュームを調整します。 | 保証された取引：はい<br>保証されていない取引：いいえ | はい |
|  | [!UICONTROL Impressions] | （保証されていない取引の場合はオプション）この取引を使用して実行すると予想されるインプレッション数。 この値は、追跡の目的のみです。パブリッシャーが広告配信を制御します。 | 保証された取引：はい<br>保証されていない取引：いいえ | はい |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Deal IDの詳細の手動作成](deal-id-create.md)
>* [SSPパートナー](ssp-partners.md)

<!-- >* [About Private Inventory](private-inventory-about.md) -->
