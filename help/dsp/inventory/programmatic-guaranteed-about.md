---
title: プログラムで保証された契約について
description: プログラムで保証された (PG) 取引と、提供の認定を受けている SSP について説明します。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 8cf85ae3-027d-4d9d-95a0-ac39d651627a
source-git-commit: 96f756b0f5239e2378d0a4da18335d909f96ab94
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# プログラムで保証された契約について

プログラム的に保証された (PG) 取引は、広告サーバータグを介するのではなく、取引 ID を介して発行者と直接購入する保証があります。 PG は、お客様および発行者が管理する柔軟性が高く、通常のタグの購入よりも透明性が高くなります。 請求とレポートは、Advertising Cloud DSPを通じて統合され、時間を節約できます。

## PG 契約の機能

* 契約は常にDSPを通じて請求されます。
* 契約は定価と数量を持っている。
* パブリッシャーまたはサプライサイドプラットフォーム (SSP) は、予算のペーシング、予算の上限、および任意のターゲティングをすべて処理します。
* 通常、パブリッシャーの広告サーバーでは、この契約の優先順位が高くなります。
* 入札リクエストは、1 つの契約または購入者に限定されません。
* 1 つの契約 ID で複数のタイプのビデオがサポートされます。
* SSP とパブリッシャーは配信 SLA を持っています。

PG 契約には、DSPが各入札リクエストにリクエストを返し、SSP を使用した配信 SLA を満たすために、PG のデフォルトの配置と広告が必要です。 必須の PG デフォルトの配置を設定したら、他の配置でも PG 契約のターゲットを設定できます。

## DSPの PG 契約で認定された SSP

* [!DNL Ambient Digital]
* [!DNL FreeWheel]
* [!DNL Google Authorized Buyers]
* [!DNL Magnite CTV] ( 以前の [!DNL Telaria])
* [!DNL Magnite DV+] ( 以前の [!DNL Rubicon])
* [!DNL OpenX]
* [!DNL SpotX]

>[!MORELIKETHIS]
>
>* [プログラム的に保証された契約の交渉に関するヒント](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [プログラム的に保証された契約の設定](programmatic-guaranteed-set-up.md)
>* [SSP パートナー](ssp-partners.md)
>* [在庫機能の概要](inventory-overview.md)

