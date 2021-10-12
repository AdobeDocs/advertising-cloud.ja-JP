---
title: プログラム的に保証された取引の設定
description: パブリッシャーとネゴシエートしたプログラム保証 (PG) 取引を設定する方法を説明します。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 9e371606-5428-4635-9653-7dc43449e489
source-git-commit: 8046ec79ec24f47fe33e49c6097e44dbba450f1f
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# プログラム的に保証された取引の設定

*[サポートされる供給側プラットフォームのみ](programmatic-guaranteed-about.md)*

プログラム保証 (PG) 取引をサポート対象のパブリッシャーと交渉した後、[!DNL Deal ID inbox] を使用するか、取引の詳細を手動で入力して、DSP内で取引を設定できます。

>[!NOTE]
>
> PG 取引の場合、パブリッシャーはすべての予算ペーシング、予算上限、ターゲティングを処理します。 DSPを介して PG を許可するすべての SSP で、パブリッシャーが予算制限を設定できることを確認します。
>
> [!DNL FreeWheel] でプログラム的に保証された発行者との取引を設定するには、追加の権限と手順が必要です。 詳細は、「[ [!DNL FreeWheel]](freewheel-overview.md) でのプログラム保証取引の設定の概要」を参照してください。

## [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

[!DNL FreeWheel]、[!DNL Google Authorized Buyers]、[!DNL Magnite DV+] には、この方法が推奨されます。

1. [取引を受け入れる](deal-id-inbox-accept.md)。

1. 取引を保存した後、その取引に使用する広告を選択し、指示に従って、プログラム的に保証された (PG) デフォルトの配置を作成します。

   購入の 100%を提供するには、デフォルトの PG プレースメントを作成する必要があります。 このタイプの配置にはターゲティングがないので、DSPはパブリッシャーからのすべての入札リクエストに入札を返すことができます。

   * 1 件の取引を承認すると、PG のデフォルト配置作成ワークフローに自動的にリダイレクトされます。

      [!DNL FreeWheel] の取引はすべて 1 つの取引として提案されます。

   * 複数の PG 取引 ID を持つ提案を受け入れる場合は、作成する必要がある各 PG のデフォルトの配置を特定します。 必要な配置をすべて作成すると、「続行」ボタンが有効になります。

1. （オプション）PG 案件を追加の非 PG 配置でターゲット設定します。

## プログラム的に保証された取引の手動設定

他のすべての SSP にこの方法を使用します。

1. [取引 ID の詳細を手動で設定します](deal-id-create.md)。

1. 取引を保存した後、その取引に使用する広告を選択し、指示に従って PG のデフォルトの配置を作成します。

   購入の 100%を提供するには、ディールの PG デフォルトの配置を作成する必要があります。 このタイプの配置にはターゲティングがないので、DSPはパブリッシャーからのすべての入札リクエストに入札を返すことができます。

1. （オプション）PG 案件を追加の、PG 以外の配置でターゲティングします。

>[!MORELIKETHIS]
>
>* [プログラム保証取引について](programmatic-guaranteed-about.md)
>* [プログラム的に保証された取引の交渉に関するヒント](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [プログラムで保証された取り引きの広告を送信 [!DNL FreeWheel]](freewheel-submit.md)
>* [Deal ID インボックスでの Deal の承認](deal-id-inbox-accept.md)
>* [Deal ID の詳細の手動作成](deal-id-create.md)
>* [SSP パートナー](ssp-partners.md)
>* [在庫機能の概要](inventory-overview.md)

