---
title: '[!UICONTROL Deal ID Inbox]について'
description: '[!UICONTROL Deal ID inbox]機能について説明します。この機能を使用すると、 [!DNL Google Authorized Buyers], [!DNL FreeWheel], and [!DNL Rubicon]上で既にネゴシエート済みの非公開取引を受け入れることができます。'
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!UICONTROL Deal ID Inbox]について

DSP [!UICONTROL Deal ID inbox]を使用すると、Advertising Cloud DSPがサプライサイドプラットフォーム(SSP)を通じてパブリッシャーからインポートした取引をすばやく設定できるので、各取引を手動で設定する必要がなくなります。 [!UICONTROL Deal ID inbox]から、[!DNL Google Authorized Buyers]（旧称[!DNL AdX]）、[!DNL FreeWheel]および[!DNL Rubicon]に関して、既にパブリッシャーとネゴシエートした保証済みの、保証されていないプライベート在庫契約を受け入れることができます。

>[!NOTE]
>
>Advertising Cloud DSPは、[!DNL FreeWheel] APIと統合する最初のDSPです。

[!UICONTROL Deal ID inbox]では、パブリッシャーが案件を確認した際の案件の詳細を確認し、案件の設定を迅速に行い、手動での入力エラーを回避できます。

DSPは、米国東部標準時(EST)の午前4時30分に、すべての取引詳細を毎日自動的に更新します。 また、[!DNL FreeWheel]の取引情報をすべて更新し、[!DNL Google]と[!DNL Rubicon]の時間別の既存の取引情報を更新します。 また、取引の詳細を手動で更新して、いつでも新しい取引を入力できます。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>[!DNL Google Authorized Buyers]を通じてプログラム的に保証された取引の場合、予算の少なくとも90%を支払う必要があります。支払わないと、[!UICONTROL Deal ID inbox]での[!DNL Google]取引に対するアクセス権が失われます。

## [!UICONTROL Deal ID Inbox]の実装

[!UICONTROL Deal ID inbox]での取引を受けるには、SSPアカウントを組織のDSPアカウントとSSPアカウントをマッピングする必要があります。 DSPは、組織のアカウント名を関連するSSPと共有します。 手順については、Adobeのアカウントマネージャーにお問い合わせください。

取引のネゴシエーション中に、パブリッシャーに対し、親のDSPアカウントではなく、購入者に取引を送信するように伝えます。 取引識別子は、SSPに応じて、名前またはIDにすることができます。

## 取引に対して実行できるアクション

* **ディー** ルをレビューして、SSPが正しい発行者、フライト日、CPM、その他の取引詳細を送信したことを確認します。パブリッシャーが間違いを犯した場合は、DSPの外部で問い合わせて、取引を修正し、再送信できます。

* **確認後** の取引を受け入れると、に表示されなくなりま [!UICONTROL Deal ID inbox]す。受け入れられた契約は[!UICONTROL Inventory] > [!UICONTROL Deals]に記載され、広告主のプレースメント内でターゲットを設定する準備が整っています。

* **不要な** 取引や迷惑行為を無視する。無視された取引は、アーカイブとして機能する[!UICONTROL Deal ID inbox]内の[!UICONTROL Ignored Deals]タブに移動されます。 オファーを無視した場合、DSPはSSPおよび発行者にアラートを出しません。

* **/から承認済みの取引の詳細を** 変更しま [!UICONTROL Inventory] す( [!UICONTROL Deals] 内ではありま [!UICONTROL Deal ID inbox]せん)。同様に、パブリッシャーがオファーに変更を送信する場合、[!UICONTROL Deal ID inbox]はオファーの設定後にSSPの変更を同期しないので、広告主は[!UICONTROL Inventory] > [!UICONTROL Deals]で変更を実装する責任を負います。

## 受け入れられない取引の種類

取引リストに![Accept](/help/dsp/assets/accept.png)アイコンや[!UICONTROL Accept]ボタンが含まれていない場合、[!UICONTROL Deal ID inbox]からは承諾できません。 代わりに、[手動でDeal IDの詳細を作成](/help/dsp/inventory/deal-id-create.md)できます。

次の種類の取引は受け入れられません。

* [!DNL Google] の値は米ドルではありません。

* [!DNL Rubicon] 米ドル以外の取引

* [!DNL FreeWheel] 取引先企業の取引先企業の通貨ではありません。

* 今日より前に終了日が設定されている取引。

* 「複数のメディアタイプ」というラベルが付けられた古い[!DNL Rubicon]取引。

取引の詳細には、取引を承認できない理由が含まれます。

>[!MORELIKETHIS]
>
>* [Deal IDインボックスでのDealの承認](deal-id-inbox-accept.md)
>* [在庫機能の概要](inventory-overview.md)

