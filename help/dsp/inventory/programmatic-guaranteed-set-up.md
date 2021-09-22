---
title: プログラム保証契約の設定
description: パブリッシャーとネゴシエートしたプログラム保証(PG)取引を設定する方法を説明します。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 9e371606-5428-4635-9653-7dc43449e489
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# プログラム保証契約の設定

*[サポートされる供給側プラットフォームのみ](programmatic-guaranteed-about.md)*

サポート対象のパブリッシャーとプログラム保証(PG)取引を交渉した後、[!DNL Deal ID inbox]を使用するか、取引の詳細を手動で入力して、DSP内で取引を設定できます。

>[!NOTE]
>
> PGディールの場合、パブリッシャーはすべての予算ペーシング、予算上限、ターゲティングを処理します。 DSP経由のPGを許可するすべてのSSPは、パブリッシャーが予算上限を設定できることを確認します。
>
> [!DNL FreeWheel]上でパブリッシャーとのプログラム的な取引を保証するには、追加の権限と手順が必要です。 詳細は、「[ [!DNL FreeWheel]](freewheel-overview.md)でのプログラム保証取引の設定の概要」を参照してください。

## [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

[!DNL FreeWheel]、[!DNL Google Authorized Buyers]、[!DNL Rubicon]には、この方法が推奨されます。

1. [取引を受け入れる](deal-id-inbox-accept.md)。

1. 取引を保存した後、その取引に使用する広告を選択し、指示に従って、プログラム的に保証された(PG)デフォルトの配置を作成します。

   購入の100%を配信するには、デフォルトのPG配置を作成する必要があります。 このタイプの配置にはターゲティングがないので、DSPはパブリッシャーからのすべての入札リクエストに入札を返すことができます。

   * 1件の取引を承認する場合、PGのデフォルトの配置作成ワークフローに自動的にリダイレクトされます。

      すべての[!DNL FreeWheel]取引は、1つの取引として提案されます。

   * 複数のPG取引IDを持つ提案を受け入れる場合は、作成する必要がある各PGのデフォルトの配置を特定します。 必要な配置をすべて作成したら、「続行」ボタンが有効になります。

1. （オプション）追加の、PG以外の配置でPG取引をターゲットにします。

## プログラム的に保証された取引の手動設定

他のすべてのSSPにこのメソッドを使用します。

1. [取引IDの詳細を手動で設定します](deal-id-create.md)。

1. 取引を保存した後、その取引に使用する広告を選択し、指示に従ってPGのデフォルトの配置を作成します。

   購入の100%を提供するには、ディールのPGデフォルトの配置を作成する必要があります。 このタイプの配置にはターゲティングがないので、DSPはパブリッシャーからのすべての入札リクエストに入札を返すことができます。

1. （オプション）追加の、PG以外の配置でPG取引をターゲットにします。

>[!MORELIKETHIS]
>
>* [プログラム保証取引について](programmatic-guaranteed-about.md)
>* [プログラム的に保証された契約の交渉に関するヒント](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [プログラムで保証された取引の広告を送信する [!DNL FreeWheel]](freewheel-submit.md)
>* [Deal IDインボックスでのDealの承認](deal-id-inbox-accept.md)
>* [Deal IDの詳細の手動作成](deal-id-create.md)
>* [SSPパートナー](ssp-partners.md)
>* [在庫機能の概要](inventory-overview.md)

