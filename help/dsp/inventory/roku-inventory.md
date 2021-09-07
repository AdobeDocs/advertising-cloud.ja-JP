---
title: ' [!DNL Roku] インベントリの使用'
description: 'DSPと [!DNL Roku], including inventory options, approved third-party tracking vendors, and best practices for [!DNL Roku]固有の配置について説明します。 '
feature: On Demand Inventory, Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# [!DNL Roku]インベントリの使用

Advertising Cloud DSPは、[!DNL Roku]上で広告を行うための独自の機能を提供します。

## Advertising Cloud DSPと[!DNL Roku]パートナーシップ

RokuとAdvertising Cloud DSPは、[!DNL Roku]インベントリ上で1:1決定論的オーディエンスのターゲティングをおこなうために、[!DNL DSP]オーディエンスと[!DNL Roku] IDを一致させる一意のパートナーシップを持っています。

Advertising Cloud DSPは、Roku独自のDSP(OneView)を除き、これらのターゲティング機能にのみアクセスできます。 また、Advertising Cloud DSPは、他のすべての接続テレビ(CTV)インベントリの横にある[!DNL Roku]供給を測定する権限を持つ唯一のDSPです。 [!DNL Roku]は、標準のRTBとインプレッションピクセル信号のすべてを共有するわけではないので、他のDSPはRokuで販売されているCTVサプライ全体をターゲットにしたり測定したりすることはできません。

## [!DNL Roku] 在庫オプション

a)[!DNL Roku]で直接非公開取引IDを設定し、Deal IDデータをDSPに入力するか、b)[!DNL On Demand]ギャラリーにアクセスして、[!DNL Roku]プロファイルを購読します。

>[!NOTE]
>
>[!DNL Roku] 在庫は、オープンな市場や取引所では利用できません。

* プライベート契約の場合は、[DSP](/help/dsp/inventory/deal-id-create.md)で取引IDに関する情報を設定し、[!DNL Roku]プレースメント内で「[!UICONTROL Roku Network – Audience]」と「[!UICONTROL The Roku Channel – Audience]」をターゲットにします。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* [以下の [!DNL Roku] inventory within the [!DNL On Demand] Gallery](/help/dsp/inventory/on-demand-inventory-subscribe.md)を購読し、[!DNL Roku]プレースメント内で承認された取引のターゲットを設定できます。

   * 「[!UICONTROL Roku Network – Audience]」は、[!DNL The CW]、[!DNL ABC]、[!DNL ESPN]などのプレミアムコンテンツパートナーを持つ[!DNL Roku]エコシステム全体のインベントリです。
   * [!DNL Roku]所有および操作(O&amp;O)アプリコンテンツの場合は「[!UICONTROL The Roku Channel – Audience]」。

### [!DNL Roku]を使用してプライベートマーケットプレイスをカスタマイズする利点

非公開取引では、ニーズに応じて取引パラメーターをカスタマイズできます。

* **ネゴシエートされた価格：** セールスチ [!DNL Roku] ームと協力して、キャンペーンのニーズに合った取引の交渉と構築を行います。

* **スケールの優先度：** プライベートマーケットプレイス(PMP)は、常時オンの取引（取引など）よりも高い優先度を [!DNL On Demand] 受け取ります。

* **頻度管理：** デフォルトの頻度上限 [!DNL Roku] は、1人のユーザーにつき1(1)分、30分につき1つですが、上限は時間、日、週、月、またはフライト期間全体でカスタマイズできます。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]データのターゲット設定：** [!DNL Roku] オーディエンスは、デバイスとテレビの信号、で追跡されるデータ（TVジャンルの親和性、ストリーミングTVの行動、ケーブル購読のステータスなど）、顧客関係管理(CRM)システムの追加データから構築されま [!DNL Roku]  [!DNL The Roku Channel]  [!DNL Roku] す。

* **[!DNL Roku]コンテンツのターゲット設定：** 個人のお得な情報は、ジャンル別、アプリの適用別、季節ブロックリスト別、およびテンポレートイベント別にアプリのターゲットを設定でき、番組内のみを対象に [!DNL The Roku Channel] できます。

## [!DNL Roku] 配置

DSPキャンペーンでは、配置タイプ「[!UICONTROL Connected TV (Roku)]」を使用して[ [!DNL Roku]固有の配置](/help/dsp/campaign-management/placements/placement-create.md)を作成します。 [!DNL Roku]配置を、定義された目標と共に[!DNL Roku]固有のパッケージに含めます。

各[!DNL Roku]プレースメントは、少なくとも1つの[!DNL Roku]取引またはソースをターゲットにする必要があります。 [!DNL Roku]とのDSPの一意のオーディエンスの一致を活用するには、 [!DNL Roku]（オプトイン）決定論的データセットと照合できる1つ以上のオーディエンスセグメントを含めます。

### [!DNL Roku] — 承認済みのサードパーティ追跡ベンダー

[!DNL Roku] 配置には、次のベンダーのサードパーティイベントピクセルとコンバージョンピクセルを含めることができます。  [!DNL Acxiom]、  [!DNL comScore]、  [!DNL Data Plus Math]、  [!DNL Experian]、  [!DNL Factual]、  [!DNL Kantar]、  [!DNL Marketing Evolution]、  [!DNL Neustar]、  [!DNL Nielsen]、  [!DNL Nielsen Catalina Solutions]、  [!DNL NinthDecimal]、  [!DNL Oracle]、  [!DNL Placed]、  [!DNL Polk]、  [!DNL Research Now]、 、を選択します。

### 配置方法別のベストプラクティス

[!DNL Roku]固有の配置に関する推奨プラクティスは次のとおりです。

リーチの増分を最大化するには：

* [!DNL The Roku Channel]を使用して既に到達したオーディエンスを除外することで、[!DNL Roku O&O]上の公開されたオーディエンスを抑制します。

* [!DNL Roku]プラットフォームをまたいで既に到達したオーディエンスを除外することで、[!DNL All Roku]上の公開されたオーディエンスを抑制します。

最も速いセットアップのために：

* [[!DNL On Demand] 在庫](/help/dsp/inventory/on-demand-inventory-subscribe.md)の[!DNL The Roku Channel]に対して、常にオンになっている既存の取引をターゲットにして、[!DNL Roku]の所有および運用済みの在庫にすばやくアクセスします。
* [[!DNL On Demand] インベントリ](/help/dsp/inventory/on-demand-inventory-subscribe.md)の[!DNL Roku Network]に対して常にオンにする取引をターゲットにして、[!DNL Roku]プラットフォーム全体で迅速に規模を拡大します。

最大スケールに設定するには：

* [!DNL Roku]個人市場をカスタマイズし、ネゴシエートされた価格で[!DNL Roku]の供給に優先的にアクセスする。

>[!MORELIKETHIS]
>
>* [Deal IDの詳細の手動作成](/help/dsp/inventory/deal-id-create.md)
> * [Premiumの在庫取引の購読と [!DNL On Demand] リクエスト](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [プレースメントの作成](/help/dsp/campaign-management/placements/placement-create.md)

