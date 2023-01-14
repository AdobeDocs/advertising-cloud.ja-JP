---
title: について [!UICONTROL Deal ID Inbox]
description: 詳しくは、 [!UICONTROL Deal ID inbox] 機能を使用すると、 [!DNL FreeWheel], [!DNL Google Authorized Buyers] ( 旧称： [!DNL AdX]), and [!DNL Magnite DV+] ( 以前の [!DNL Rubicon]) をクリックします。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# について [!UICONTROL Deal ID Inbox]

Advertising DSP [!UICONTROL Deal ID inbox] では、DSPがサプライサイドプラットフォーム (SSP) を通じてパブリッシャーからインポートした契約をすばやく設定できるので、各契約を手動で設定する必要がありません。 既にパブリッシャーと交渉した保証付きの、保証されていない非保証のプライベートインベントリ取引を受け入れることができます。 [!DNL FreeWheel], [!DNL Google Authorized Buyers] ( 旧称： [!DNL AdX]) および [!DNL Magnite DV+] ( 以前の [!DNL Rubicon]) を [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising DSPは、 [!DNL FreeWheel] API

内 [!UICONTROL Deal ID inbox]を使用すると、パブリッシャーが契約を確認したときに契約の詳細を表示し、契約の設定を迅速化し、手動入力エラーを回避できます。

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSPは、米国東部標準時の午前 4 時 30 分に、すべての契約の詳細を自動的に更新します。 また、すべての [!DNL FreeWheel] 既存の契約の契約と更新 [!DNL Google] および [!DNL Magnite DV+] 1 時間ごと。 また、契約の詳細を手動で更新して、新しい契約をいつでも作成できます。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>を通じてプログラムで保証された取引の場合 [!DNL Google Authorized Buyers]を使用する場合、予算の 90%以上を配信する必要があります。配信しないと、アカウントが [!DNL Google] 契約 [!UICONTROL Deal ID inbox].

## の実装 [!UICONTROL Deal ID Inbox]

お客様の契約を [!UICONTROL Deal ID inbox]の場合、SSP アカウントは組織のDSPアカウントを SSP アカウントにマッピングする必要があります。 DSPは、組織のアカウント名を関連する SSP と共有します。 お問い合わせ [!DNL Adobe] アカウントチームを参照してください。

契約ネゴシエーション中に、親DSPアカウントではなく購入者に契約を送信するようにパブリッシャーに伝えます。 契約識別子は、SSP に応じて、名前または ID にすることができます。

## 契約に対して実行できるアクション

* **契約のレビュー** SSP が正しい発行者、フライト日、CPM、その他の契約の詳細を送信したことを確認する。 パブリッシャーが間違いを犯した場合は、DSPの外部で問い合わせて、契約を修正し、再送信できるようにします。

* **契約の承認** 確認後、これらは [!UICONTROL Deal ID inbox]. 受け入れられた契約は、 [!UICONTROL Inventory] > [!UICONTROL Deals] 広告主の配置内でターゲティングする準備が整っている。

* **契約を無視** 不要なものや迷惑をかけているものを除き、 無視された契約は、 [!UICONTROL Ignored Deals] タブ内の [!UICONTROL Deal ID inbox]：アーカイブとして機能します。 契約を無視した場合、DSPは SSP および発行者に警告を出しません。

* **既に承諾済みの契約の詳細を変更** から [!UICONTROL Inventory] > [!UICONTROL Deals] ( [!UICONTROL Deal ID inbox]) をクリックします。 同様に、パブリッシャーが契約に変更を送信する場合、広告主は、 [!UICONTROL Inventory] > [!UICONTROL Deals] なぜなら [!UICONTROL Deal ID inbox] は、契約の設定後に SSP からの変更を同期しません。

## 受け入れられない契約のタイプは何ですか？

契約リストに ![確定](/help/dsp/assets/accept.png) アイコンまたは [!UICONTROL Accept] ボタンをクリックした場合、 [!UICONTROL Deal ID inbox]. 代わりに、 [契約 ID の詳細を手動で作成する](/help/dsp/inventory/deal-id-create.md).

次の種類の契約は受け入れられません。

* [!DNL Google] の契約です。

* [!DNL Magnite DV+] 米ドル以外の取引

* [!DNL FreeWheel] 取引先責任者の口座通貨に含まれていない取引先責任者。

* 今日より前の終了日を持つ契約。

* 古い [!DNL Magnite DV+] 「複数のメディアタイプ」というラベルの付いた契約。

契約の詳細には、契約を承認できない理由が含まれます。

>[!MORELIKETHIS]
>
>* [Deal ID インボックスでの契約の承認](deal-id-inbox-accept.md)
>* [在庫機能の概要](inventory-overview.md)

