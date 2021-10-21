---
title: について [!UICONTROL Deal ID Inbox]
description: 詳しくは、 [!UICONTROL Deal ID inbox] 機能。 [!DNL FreeWheel], [!DNL Google Authorized Buyers] (formerly known as [!DNL AdX]), and [!DNL Magnite DV+] ( [!DNL Rubicon]) をクリックします。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 2539d9b8ec7de7202dd6c3400dda85aa133853e3
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# について [!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox] では、サプライサイドプラットフォーム (SSP) を使用してAdvertising Cloud DSPからパブリッシャーから読み込んだ取引をすばやく設定できるので、各取引を手動で設定する必要がありません。 で既にパブリッシャーとネゴシエートした保証付きおよび保証なしのプライベートインベントリ取引を受け入れることができます。 [!DNL FreeWheel], [!DNL Google Authorized Buyers] ( 旧称： [!DNL AdX]) および [!DNL Magnite DV+] ( [!DNL Rubicon]) を [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising Cloud DSPは、 [!DNL FreeWheel] API

の [!UICONTROL Deal ID inbox]を使用すると、パブリッシャーが表示した案件の詳細を確認し、案件の設定を迅速に行い、手動での入力エラーを回避できます。

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSPは、米国東部標準時間の午前 4 時 30 分に、すべての取引の詳細を自動的に更新します。 また、すべての [!DNL FreeWheel] 既存の取引の詳細 [!DNL Google] および [!DNL Magnite DV+] 1 時間ごと また、取引の詳細を手動で更新して、新規取引をいつでも入力できます。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>を通じてプログラム的に保証された取引の場合 [!DNL Google Authorized Buyers]を使用している場合、予算の 90%以上を配信する必要があります。配信しないと、アカウントから [!DNL Google] 取引 [!UICONTROL Deal ID inbox].

## の実装 [!UICONTROL Deal ID Inbox]

お客様の [!UICONTROL Deal ID inbox]の場合、SSP アカウントは組織のDSPアカウントを SSP アカウントにマッピングする必要があります。 DSPは、組織のアカウント名を関連する SSP と共有します。 お問い合わせ [!DNL Adobe] アカウントマネージャーを参照してください。

取引ネゴシエーション中に、パブリッシャーに対して、親DSPアカウントではなく、購入者に取引を送信するように指示します。 取引 ID は、SSP に応じて、名前または ID になります。

## お客様の取引に対して実行できるアクション

* **取引のレビュー** SSP が正しい発行者、フライト日、CPM、その他の案件の詳細を送信したことを確認する。 パブリッシャーが間違いを犯した場合は、DSPの外部で問い合わせて、取引を修正し、再送できるようにします。

* **取引の承認** レビュー後、 [!UICONTROL Deal ID inbox]. 受け入れられた取引は、 [!UICONTROL Inventory] > [!UICONTROL Deals] およびは、広告主のプレースメント内でターゲット設定する準備が整っています。

* **詳細を無視** 不要なものや、迷惑をかけているものを除き、 無視された取引は、 [!UICONTROL Ignored Deals] タブ内の [!UICONTROL Deal ID inbox]：アーカイブとして機能します。 オファーを無視した場合、DSPは SSP および発行者にアラートを出しません。

* **既に受け入れられた取引の詳細を変更** から [!UICONTROL Inventory] > [!UICONTROL Deals] ( [!UICONTROL Deal ID inbox]) をクリックします。 同様に、パブリッシャーが掘り出し物に変更を送信する場合、広告主は、 [!UICONTROL Inventory] > [!UICONTROL Deals] なぜなら [!UICONTROL Deal ID inbox] では、詳細の設定後に SSP からの変更は同期されません。

## 受け入れられない取引の種類

取引リストに ![確定](/help/dsp/assets/accept.png) アイコンまたは [!UICONTROL Accept] ボタンをクリックすると、 [!UICONTROL Deal ID inbox]. 代わりに、 [取引 ID の詳細を手動で作成する](/help/dsp/inventory/deal-id-create.md).

次の種類の取引は受け入れられません。

* [!DNL Google] 米ドルではない取引。

* [!DNL Magnite DV+] 米ドル以外の取引

* [!DNL FreeWheel] 取引先企業の口座通貨ではない取引先企業。

* 今日より前に終了日を持つ取引。

* 古い [!DNL Magnite DV+] 「複数のメディアタイプ」とラベル付けされた取引

取引の詳細には、取引を受け入れられない理由が含まれます。

>[!MORELIKETHIS]
>
>* [Deal ID インボックスでの Deal の承認](deal-id-inbox-accept.md)
>* [在庫機能の概要](inventory-overview.md)

