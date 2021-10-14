---
title: 手動の Deal ID 設定
description: 手動で入力した Deal ID の設定の説明を参照してください。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: 5f39608155f9237fb6d69a7b31c007d1b8d0306f
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# 手動の Deal ID 設定

| セクション | パラメーター | 説明 | 必須 | 編集可能 |
|---------|-----------|-------------|----------|----------|
| [案件の詳細] | [!UICONTROL Deal name] | Advertising Cloud DSPで [!UICONTROL Deal ID] を識別する名前。 名前を入力するか、「[!UICONTROL Auto-name]」を選択して、取引の詳細に基づいてAdvertising Cloudが名前を生成できるようにします。<br><br>自動生成された名前の例： [!DNL *DEAL_ID*  — 取引 ID — 保証済み — USD - 5 - 24 キッチン — プライベート] | はい | はい |
|  | [!UICONTROL External deal ID] | この取引を識別するためにパブリッシャーおよび SSP で使用される ID。 | はい | いいえ |
|  | [!UICONTROL Publisher] | この在庫を販売する発行者の名前。 | はい | いいえ |
|  | [!UICONTROL SSP] | この取引が実行されるサプライサイドプラットフォーム (SSP)。 | はい | いいえ |
|  | [!UICONTROL Media type] | この取引で購入されるメディアのタイプ：[!UICONTROL Desktop video]、[!UICONTROL Mobile video]、[!UICONTROL Connected TV]、[!UICONTROL Display]、または [!UICONTROL Audio]。 オプションは SSP によって異なります。<br><br> 取引で複数のメディア・タイプを許可する場合は、取引の作成時にデフォルトの配置のメディア・タイプを選択します。後で、別のメディアタイプを選択して、追加のメディアタイプを持つ新しい場所を作成できます。<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | はい | いいえ |
|  | [!UICONTROL Deal type] | 取引のコミットメントと価格設定の構造：<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*:自分と発行者は、一定数のインプレッション配信にコミットしていません。CPM は市場の状況に応じて変動し、増加する可能性がありますが、この取引は在庫の最小価格を指定します。</li><li>*[!UICONTROL Non guaranteed (fixed)]*:自分と発行者は、一定数のインプレッション配信にコミットしていません。価格は、ネゴシエートされた固定レートで設定されます。</li><li>*[!UICONTROL Guaranteed (fixed)]*:インプレッション数、ターゲティング、フライト日、固定価格が事前に定義されていることに同意したとします。<br><br><b>注意：</b> 保証されたお得な情報には、セクションでフライト日と指定数のインプレッションが必 [!UICONTROL Tracking] 要です。また、デフォルトのプログラム保証 (PG) プレースメントを作成する必要があり、オプションでその他のプレースメントにそのデールを使用できます。</li></ul> | はい | いいえ |
|  | [!UICONTROL CPM] | 1,000 インプレッションあたりのネゴシエートされたコスト (CPM)。 | はい | はい |
|  | [通貨] | 取引の通貨。<br><br>すべての SSP は米ドルで取引を受け入れます。SSP がDSPアカウントの通貨を受け入れると、その通貨も使用できます。 | はい | いいえ |
|  | [!UICONTROL Billing method] | すべての取引 ID は [!DNL Adobe] 資金提供済みで請求済みです。 Advertising Cloudは、使用状況に基づいて利用可能なすべてのメディアベンダーに支払い、ベンダーとの不一致を管理し、1 件の請求書をアカウントに送信します。 このオプションを使用する場合は、アカウントのレートカードで説明されているように追加料金が発生します。 | はい | いいえ |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 取引にアクセスできるユーザーアカウントの電子メールアドレス。 | いいえ | はい |
|  | [!UICONTROL Advertisers that can access this deal] | この取引にアクセスできるアカウント内の特定の広告主。<br><br><b>注意：</b> この取引は、ビューから追加のアカウントで広告主と共有で [!UICONTROL Deals] きます。Deal 行で **[!UICONTROL #]** をクリックし、**[!UICONTROL share]** をクリックして、E メールアドレスと Deal を共有します。 | はい | はい |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | この取引を使用するトラフィックの開始日と終了日。 この日付は、追跡の目的でのみ使用され、広告配信には影響しません。<br><br><b>ヒント：</b> > 表示では、 [!UICONTROL Inventory] この列に [!UICONTROL Deals] は、指定したフライト日 [!UICONTROL Pacing & Budget] 付とインプレッションの目標に対して、取引がどのようにペーシングしているかが示されます。配信のペーシング率が低い場合や超過している場合は、パブリッシャーに連絡して、配信がデールを通じて送信するボリュームを調整してください。 | 保証された取引：はい <br> 保証されていない取引：いいえ | はい |
|  | [!UICONTROL Impressions] | （保証されていない取引の場合はオプション）この取引を使用して実行すると予想されるインプレッションの数。 この値は追跡の目的でのみ使用します。パブリッシャーが広告配信を制御します。 | 保証された取引：はい <br> 保証されていない取引：いいえ | はい |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Deal ID の詳細の手動作成](deal-id-create.md)
>* [SSP パートナー](ssp-partners.md)

<!-- >* [About Private Inventory](private-inventory-about.md) -->
