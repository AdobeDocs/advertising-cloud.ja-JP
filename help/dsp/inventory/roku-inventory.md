---
title: 使用 [!DNL Roku] 在庫
description: とのDSPパートナーシップについて学ぶ [!DNL Roku]（在庫オプション、承認されたサードパーティトラッキングベンダー、および以下のベストプラクティスを含む） [!DNL Roku] — 特定の配置。
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# 使用 [!DNL Roku] 在庫

Advertising DSPは、 [!DNL Roku].

## DSPと [!DNL Roku] パートナーシップ

Roku とDSPは、お客様の [!DNL DSP] オーディエンス [!DNL Roku] での 1:1 決定論的オーディエンスのターゲティングのための ID [!DNL Roku] 在庫。

Roku 独自のDSP(OneView) 以外では、Advertising DSPはこれらのターゲティング機能にのみアクセスできます。 また、測定権限を持つDSPは Advertising DSPのみです [!DNL Roku] 他のすべての接続済みテレビ (CTV) 在庫の横にある供給。 理由： [!DNL Roku] では、すべての標準的な RTB とインプレッションピクセル信号を共有するわけではなく、Roku が販売する CTV サプライ全体を対象にしたり測定したりできるDSPは他にありません。

## [!DNL Roku] 在庫オプション

(a) を使用して直接個人契約 ID を設定するか、 [!DNL Roku] 次に、契約 ID データをDSPに入力するか、b) [!DNL On Demand] 購読するギャラリー [!DNL Roku] プロファイル：

>[!NOTE]
>
>[!DNL Roku] オープンなマーケットプレイスやエクスチェンジでは、在庫を利用できません。

* 個人的な取引の場合 [DSPでの契約 ID に関する情報の設定](/help/dsp/inventory/deal-id-create.md) その後、[!UICONTROL Roku Network – Audience]&quot;および&quot;[!UICONTROL The Roku Channel – Audience]」内 [!DNL Roku] 配置。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* 以下が可能です。 [以下を購読する [!DNL Roku] 内の在庫 [!DNL On Demand] ギャラリー](/help/dsp/inventory/on-demand-inventory-subscribe.md)をクリックし、内で承認済みの契約のターゲットを設定します。 [!DNL Roku] 配置：

   * &quot;[!UICONTROL Roku Network – Audience]&#39;&#39;全体のインベントリに対して [!DNL Roku] プレミアムコンテンツパートナーを持つエコシステム： [!DNL The CW], [!DNL ABC]、および [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]」 [!DNL Roku] 所有および運用 (O&amp;O) アプリコンテンツ。

### を使用したプライベートマーケットプレースのカスタマイズの利点 [!DNL Roku]

プライベート契約では、ニーズに応じて契約パラメーターをカスタマイズできます。

* **ネゴシエートされた価格：** の操作 [!DNL Roku] セールスチームが交渉し、キャンペーンのニーズを満たす契約を構築する。

* **スケールの優先度：** プライベートマーケットプレイス (PMP) は、常時取引 ( [!DNL On Demand] 契約 )。

* **頻度管理：** この [!DNL Roku] デフォルトの頻度キャップは、1 人のユーザーにつき 1(1)、30 分ごとに 1 ですが、この上限は時間、日、週、月、または全期間ごとにカスタマイズできます。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]データのターゲティング：** [!DNL Roku] オーディエンスは [!DNL Roku] デバイスとテレビ信号、 [!DNL The Roku Channel] （TV ジャンルの親和性、ストリーミング TV の行動、ケーブル購読のステータスなど）および [!DNL Roku] 顧客関係管理 (CRM) システム。

* **[!DNL Roku]コンテンツのターゲット設定：** プライベート契約では、ジャンル別、アプリのの適用ブロックリスト別、季節別、テンポレイアントイベント別、および [!DNL The Roku Channel] のみ。

## [!DNL Roku] 配置

DSPキャンペーンで、 [作成 [!DNL Roku] — 特定の配置](/help/dsp/campaign-management/placements/placement-create.md) 配置タイプ&quot;[!UICONTROL Connected TV (Roku)].&quot; 次を含む [!DNL Roku] 配置 [!DNL Roku] — 定義された目標を含む特定のパッケージ。

各 [!DNL Roku] 配置は少なくとも 1 つをターゲットにする必要があります [!DNL Roku] 契約またはソース。 次と一致するDSPの一意のオーディエンスを使用するには： [!DNL Roku]の場合、 [!DNL Roku] （オプトイン）決定論的データセット。

### [!DNL Roku] — 承認済みのサードパーティ追跡ベンダー

[!DNL Roku] 配置には、次のベンダーのサードパーティイベントピクセルとコンバージョンピクセルを含めることができます。  [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]、および [!DNL Research Now].

### 配置戦略別のベストプラクティス

次に、 [!DNL Roku] — 特定の配置。

増分リーチを最大化するには：

* 次の公開されたオーディエンスを抑制： [!DNL Roku O&O] 既に次を使用して到達済みのオーディエンスを除外する [!DNL The Roku Channel].

* 次の公開されたオーディエンスを抑制： [!DNL All Roku] を除外するために、 [!DNL Roku] プラットフォーム。

最も速いセットアップのために：

* の既存の、常時オンの契約のターゲット設定 [!DNL The Roku Channel] in [[!DNL On Demand] 在庫](/help/dsp/inventory/on-demand-inventory-subscribe.md) 素早くアクセスする [!DNL Roku] 所有および運用される在庫
* の既存の、常時オンの契約のターゲット設定 [!DNL Roku Network] in [[!DNL On Demand] 在庫](/help/dsp/inventory/on-demand-inventory-subscribe.md) 大きさを早く達成する [!DNL Roku] プラットフォーム。

最大スケールに対して：

* のカスタマイズ [!DNL Roku] ～へのアクセスを優先する民間市場 [!DNL Roku] 交渉価格での供給。

>[!MORELIKETHIS]
>
>* [Deal ID の詳細の手動作成](/help/dsp/inventory/deal-id-create.md)
> * [購読してへのアクセスをリクエスト [!DNL On Demand] プレミアム在庫取引](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [配置の作成](/help/dsp/campaign-management/placements/placement-create.md)

