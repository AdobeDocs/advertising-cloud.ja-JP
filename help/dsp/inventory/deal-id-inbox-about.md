---
title: '[!UICONTROL Deal ID Inbox] について'
description: ' [!DNL FreeWheel], [!DNL Google Authorized Buyers] (formerly known as [!DNL AdX]), and [!DNL Magnite DV+] （以前の  [!DNL Rubicon]）で既にネゴシエート済みの非公開取引を受け入れる [!UICONTROL Deal ID inbox] 機能について説明します。'
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 8046ec79ec24f47fe33e49c6097e44dbba450f1f
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!UICONTROL Deal ID Inbox] について

DSP [!UICONTROL Deal ID inbox] では、Advertising Cloud DSPがサプライサイドプラットフォーム (SSP) を通じてパブリッシャーからインポートした取引をすばやく設定できるので、各取引を手動で設定する必要がありません。 [!DNL FreeWheel]、[!DNL Google Authorized Buyers]（旧称 [!DNL AdX]）および [!DNL Magnite DV+]（旧称 [!DNL Rubicon]）で、[!UICONTROL Deal ID inbox] から既にネゴシエート済みの保証済みおよび保証なしのプライベート在庫契約を受け入れることができます。

>[!NOTE]
>
>Advertising Cloud DSPは、[!DNL FreeWheel] API と統合する最初のDSPです。

[!UICONTROL Deal ID inbox] では、パブリッシャーが見たときの取引の詳細を確認し、取引の設定を迅速に行い、手動入力エラーを回避できます。

DSPは、米国東部標準時間の午前 4 時 30 分に、すべての取引の詳細を自動的に更新します。 また、[!DNL FreeWheel] 取引をすべて更新し、[!DNL Google] と [!DNL Magnite DV+] からの既存の取引を 1 時間ごとに更新します。 また、取引の詳細を手動で更新して、新規取引をいつでも入力できます。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>[!DNL Google Authorized Buyers] を通じてプログラム的に保証された取引の場合、予算の少なくとも 90%を支払う必要があります。そうしないと、お客様のアカウントから [!UICONTROL Deal ID inbox] での [!DNL Google] 取引へのアクセス権が失われます。

## [!UICONTROL Deal ID Inbox] の実装

[!UICONTROL Deal ID inbox] での取引を受け取るには、SSP アカウントを組織のDSPアカウントと SSP アカウントをマッピングする必要があります。 DSPは、組織のアカウント名を関連する SSP と共有します。 手順については、Adobeのアカウントマネージャーにお問い合わせください。

取引ネゴシエーション中に、パブリッシャーに対して、親DSPアカウントではなく、購入者に取引を送信するように指示します。 取引 ID は、SSP に応じて、名前または ID になります。

## お客様の取引に対して実行できるアクション

* **SSP が** 正しい発行者、フライト日、CPM、およびその他の取引の詳細を送信したことを確認するために、取引を確認します。パブリッシャーが間違いを犯した場合は、DSPの外部で問い合わせて、取引を修正し、再送できるようにします。

* **確認** 後に取り消しを受け入れると、に表示されなくなりま [!UICONTROL Deal ID inbox]す。受け入れられた契約は [!UICONTROL Inventory] > [!UICONTROL Deals] に記載され、広告主の配置内でターゲティングする準備が整っています。

* **不要な** 取引や迷惑行為を無視します。無視された取引は [!UICONTROL Deal ID inbox] 内の [!UICONTROL Ignored Deals] タブに移動され、アーカイブとして機能します。 オファーを無視した場合、DSPは SSP および発行者にアラートを出しません。

* **/から既に受け入れられた取引の詳** 細を変 [!UICONTROL Inventory] 更しま [!UICONTROL Deals] す ( ではありま [!UICONTROL Deal ID inbox]せん )。同様に、パブリッシャーが掘り出し物に変更を送信する場合、[!UICONTROL Deal ID inbox] は掘り出し物の設定後に SSP の変更を同期しないので、広告主は [!UICONTROL Inventory] > [!UICONTROL Deals] に変更を実装する責任を負います。

## 受け入れられない取引の種類

案件リストに ![Accept](/help/dsp/assets/accept.png) アイコンや [!UICONTROL Accept] ボタンが含まれていない場合、[!UICONTROL Deal ID inbox] からは案件リストを受け入れることはできません。 代わりに、[ 手動で Deal ID の詳細を作成できます ](/help/dsp/inventory/deal-id-create.md)。

次の種類の取引は受け入れられません。

* [!DNL Google] 米ドルではない取引。

* [!DNL Magnite DV+] 米ドル以外の取引

* [!DNL FreeWheel] 取引先企業の口座通貨ではない取引先企業。

* 今日より前に終了日を持つ取引。

* 古い [!DNL Magnite DV+] 取引で「複数のメディアタイプ」というラベルが付けられていました。

取引の詳細には、取引を受け入れられない理由が含まれます。

>[!MORELIKETHIS]
>
>* [Deal ID インボックスでの Deal の承認](deal-id-inbox-accept.md)
>* [在庫機能の概要](inventory-overview.md)

