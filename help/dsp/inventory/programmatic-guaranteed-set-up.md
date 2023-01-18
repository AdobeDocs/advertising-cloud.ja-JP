---
title: プログラム的に保証された契約の設定
description: パブリッシャーとネゴシエートした、プログラム的に保証された (PG) 取引を設定する方法を説明します。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# プログラム的に保証された契約の設定

*[サポートされる供給側プラットフォームのみ](programmatic-guaranteed-about.md)*

サポート対象のパブリッシャーとプログラム的に保証された (PG) 契約を交渉した後、DSP内で [!DNL Deal ID inbox] または、契約の詳細を手動で入力します。

>[!NOTE]
>
> PG 契約の場合、パブリッシャーはすべての予算のペーシング、予算の上限、ターゲティングを処理します。 DSPを介して PG を許可するすべての SSP で、パブリッシャーが予算制限を設定できることが確認されます。
>
> の発行者とのプログラム的な保証契約の設定 [!DNL FreeWheel] には、追加の権限と手順が必要です。 参照：[プログラムで保証された取引の設定の概要 [!DNL FreeWheel]](freewheel-overview.md)」を参照してください。

## を使用してプログラム的に保証された契約を設定する [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

次の方法が、 [!DNL FreeWheel], [!DNL Google Authorized Buyers]、および [!DNL Magnite DV+].

1. [契約を承認](deal-id-inbox-accept.md).

1. 契約を保存したら、その契約に使用する広告を選択し、指示に従って、プログラム的に保証された (PG) デフォルトの配置を作成します。

   購入の 100%を配信するには、契約のデフォルトの PG 配置を作成する必要があります。 このタイプの配置にはターゲティングがないので、DSPはパブリッシャーからのすべての入札リクエストに入札を返すことができます。

   * 単一の契約を承認する場合、PG のデフォルトの配置作成ワークフローに自動的にリダイレクトされます。

      すべて [!DNL FreeWheel] 契約は、単一の契約として提案されます。

   * 複数の PG 契約 ID を持つ提案を受け入れる場合は、作成する必要のある各 PG のデフォルトの配置を特定します。 必要な配置をすべて作成すると、「続行」ボタンが有効になります。

1. （オプション）クリックして、追加の PG または PG 以外の配置で PG 契約をターゲット化します ![オプションメニュー](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   1 つの契約では、任意の種類のメディア（接続された TV、デスクトップ、オーディオなど）の組み合わせをサポートする複数の配置をターゲットに設定できます。

## プログラム的に保証された契約の手動設定

他のすべての SSP に対してこのメソッドを使用します。

1. [契約 ID の詳細の手動設定](deal-id-create.md).

1. 契約を保存したら、その契約に使用する広告を選択し、指示に従って PG のデフォルトの配置を作成します。

   購入の 100%を提供するには、契約の PG デフォルトの配置を作成する必要があります。 このタイプの配置にはターゲティングがないので、DSPはパブリッシャーからのすべての入札リクエストに入札を返すことができます。

1. （オプション）クリックして、追加の PG または PG 以外の配置で PG 契約をターゲット化します ![オプションメニュー](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   1 つの契約では、任意の種類のメディア（接続された TV、デスクトップ、オーディオなど）の組み合わせをサポートする複数の配置をターゲットに設定できます。

>[!MORELIKETHIS]
>
>* [プログラムで保証された契約について](programmatic-guaranteed-about.md)
>* [プログラム的に保証された契約の交渉に関するヒント](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [プログラム的に保証された取引に対する広告の送信 [!DNL FreeWheel]](freewheel-submit.md)
>* [Deal ID インボックスでの契約の承認](deal-id-inbox-accept.md)
>* [Deal ID の詳細の手動作成](deal-id-create.md)
>* [SSP パートナー](ssp-partners.md)
>* [在庫機能の概要](inventory-overview.md)

