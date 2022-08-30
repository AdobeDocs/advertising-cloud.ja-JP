---
title: キャンペーン設定
description: 使用可能なキャンペーン設定の説明を参照してください。
feature: DSP Campaigns
exl-id: ff2e22ff-8073-4532-884b-36e0c1f22641
source-git-commit: d7afcc2200adc41e583d21712226cb25f35aab66
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# キャンペーン設定

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** キャンペーン名。

**[!UICONTROL Advertiser]:** （既存のキャンペーンの読み取り専用）該当する広告主（ブランド）。 既存の広告主を選択するか、新しく作成します。

**[!UICONTROL Advertiser URL]:** 広告主の公式ページ。 このフィールドは、在庫パートナーとの広告承認プロセスをスピードアップします。

**[!UICONTROL Timezone]:** （既存のキャンペーンの場合は読み取り専用）レポートおよび入札のタイムゾーン。

**[!UICONTROL Customer PO]:** （オプション）発注/発注の顧客発注。

**[キャンペーン日]:** キャンペーンの開始日と終了日です。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** キャンペーンの余白を管理するかどうか： *[!UICONTROL Yes]* または *[!UICONTROL No]* （デフォルト）。

選択時 *[!UICONTROL Yes],* 利益のタイプと金額を指定します。

* **[!UICONTROL Margin Type]:** 利益のタイプ。 マージン管理を有効にしてキャンペーンを保存すると、マージンのタイプを変更できなくなります。

   * *[!UICONTROL Fixed]:* （デフォルト）Advertising Cloud DSPが、 [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* 別の [!UICONTROL Budget Reserve %] および [!UICONTROL Gross Budget] キャンペーン内の各パッケージおよび配置に対して Advertising Cloud DSPは、特定の利益を保証することなく、各配置の財務効率に基づいて最適化されます。 これは、一定金額の単位または単位タイプを一定のレートで配信することに同意した複数の明細品目で構成される挿入注文に使用します。

* **[!UICONTROL Fixed Margin %]:** （余白が固定されたキャンペーンのみ）各広告掲載順のデフォルトのマークアップです。 <!-- impression? -->（割合） この金額はから引かれている [!UICONTROL Gross Budget] ：ネットキャンペーン予算を定義します。

* **[!UICONTROL Budget Reserve %]:** ( マージンが一定のキャンペーンのみ。（任意） [!UICONTROL Gross Budget] 安全策として この金額はから引かれている [!UICONTROL Gross Budget] ：ネットキャンペーン予算を定義します。

**[!UICONTROL Gross Budget]:** （利益管理のあるキャンペーンのみ）指定したわずかな調整が適用される前の総キャンペーン予算。

必要に応じて、日次、週次または月次の予算総予算を追加できます。

1. クリック **[!UICONTROL Add an additional Gross Budget]**.

1. 次を入力します。 **[!UICONTROL Gross Budget]** 予算間隔を選択します。 *[!UICONTROL Daily],* *[!UICONTROL Weekly],* または *[!UICONTROL Monthly]*.

合計純予算（キャンペーンの支出上限）は、利益幅の設定に基づいて自動的に計算され、この値の下に表示されます。

**[!UICONTROL Budget]:** （利益管理のないキャンペーン）キャンペーンの予算全体。

**[!UICONTROL Estimated Tax Withholding]:** 国または地方税のアカウントレベルで、広告料、広告提供料、および/またはデータ料金全体の合計支出額の割合を保留します。 レートは予算およびペーシングの目的で見積もられるので、請求済み税率は変動する場合があります。

控除する税金を見積る手順は、次のとおりです。

1. クリック **[!UICONTROL Update rates here]**.

1. 次を指定： **[!UICONTROL Estimated tax rate]**（割合）

1. 税金を控除する各手数料タイプの横にあるチェック・ボックスを選択します。 料金のタイプは次のとおりです。

   * *[!UICONTROL Include estimated tax - ads fee]:* キャンペーン管理料に対する税金を含む、すべてのAdvertising Cloud DSPメディア支出に適用されます。

   * *[!UICONTROL Include estimated tax - ad serving fee]:* メディアとデータを除く、Advertising Cloud DSPのすべての支出に適用されます。 キャンペーン管理手数料に対する税金は除外されます

   * *[!UICONTROL Include estimated tax - data fee]:* Advertising Cloud DSPでのすべてのデータ支出に適用されます。

1. クリック **[!UICONTROL Submit]**.

>[!NOTE]
>
>* 米国では、広告、広告配信、データ全体に税金が含まれる状況は異なる場合があります。 他の国の組織では、VAT に対応する税金の 3 つのカテゴリすべてを含めます。
>
>* これらの値は、アカウントの料金設定でも設定できます。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (2020 年 6 月 23 日以降に作成された既存のキャンペーンの場合は読み取り専用。（2020 年 6 月 23 日より前に作成されたキャンペーンでは使用できない） Advertising Cloudが広告をターゲットにし、頻度キャップを適用するレベル。 *同じデバイス* デバイスまたは *人* を使用して、既知のすべてのデバイスにわたってユーザーをターゲットに設定することができます。

**[!UICONTROL Device Graph]:** ( 既存のキャンペーンの場合は読み取り専用、ユーザーベースのクロスデバイスターゲティングのみを使用するキャンペーン ) クロスデバイスターゲティングと頻度管理に使用するデバイスグラフ。

* *[!UICONTROL LiveRamp - U.S. only]:* 0.35 CPM でのクロスデバイスターゲティングで、 [!DNL LiveRamp] デバイスグラフ（ターゲットとなるオーディエンスセグメント内に見つからないデバイスの場合）。 配置レベルで、クロスデバイスターゲティングを設定できます。

   また、このオプションは、頻度の管理とアトリビューションの測定のために、すべての広告主が無料で利用できます。

**[!UICONTROL Frequency Cap]:** （オプション）個別のデバイスまたは人物が ( 指定した [!UICONTROL Cross Device Level]) は、キャンペーンから広告を提供します。 次のオプションがあります *[!UICONTROL Unlimited]* または 1 日、1 週間、1 ヶ月あたりの特定の金額。

>[!NOTE]
>
> 頻度キャップは、キャンペーン、パッケージ、配置の各レベルで設定できます。 DSPは、キャンペーン階層で最も厳格な頻度キャップに従います。

**[!UICONTROL Packages]:** この [パッケージ](/help/dsp/campaign-management/packages/package-about.md) キャンペーンに含める。 既存のパッケージを選択するか、含めるパッケージを作成します。 パッケージを作成する場合は、 [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md) を参照してください。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>次の設定では、測定およびレポート機能のみを有効にします。 パフォーマンスの最適化は、パッケージおよび配置レベルでのみ実行されます。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** （オプション）有効 [!DNL IAS] 指定した設定を使用して、視認性、詐欺、ブランドの安全性、オーディエンスの検証を測定およびレポートします。 追加料金が適用されます。

* **[!UICONTROL Measure On]:** 測定対象の在庫： *[!UICONTROL Display and VPAID video inventory]* （デフォルト）または *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >ビデオの視認性は、VPAID インベントリでのみ測定できます。

* **[!UICONTROL IAS Account ID (AnID)]:** ( 自身の広告主 [!DNL IAS] アカウント（オプション）組織の [!DNL IAS] アカウント ID( [!DNL IAS] は直接使用料を請求します。

* **[!UICONTROL IAS Team ID]:** ( 自身の広告主 [!DNL IAS] アカウント（オプション）組織のチーム ID [!DNL IAS] アカウント [!DNL IAS] は直接使用料を請求します。 <!-- verify -->

**[!UICONTROL MOAT]:** （オプション）有効 [!DNL MOAT] 視認性、詐欺、ブランドの安全性、オーディエンスの検証に関する測定とレポート。 追加料金が適用されます。

#### オーディエンスの検証

**[!UICONTROL Nielsen]:** （オプション）有効 [!DNL Nielsen] 指定した設定を使用した、オーディエンスの検証の測定とレポート。 追加料金が適用されます。

* **[!UICONTROL Target Gender]:** ターゲットとする性別： *[!UICONTROL Both]* （デフォルト） *[!UICONTROL Male]*&#x200B;または *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** ターゲットとする年齢の範囲。 必要に応じて、左右のスライダを使用して範囲を狭めます。

* **[!UICONTROL Target Country]:** （オプション）ターゲットとする国。 [!DNL Nielsen] は、サポート対象国でのみ提供されるインプレッション数を測定します。

**[!UICONTROL comScore vCE]:** （オプション）有効 [!DNL Comscore validated Campaign Essentials (vCE)] 指定した設定を使用した、オーディエンスの検証の測定とレポート。 追加料金が適用されます。

* **[!UICONTROL Target Gender]:** ターゲットとする性別： *[!UICONTROL Both]* （デフォルト） *[!UICONTROL Male]*&#x200B;または *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** ターゲットとする年齢の範囲。 必要に応じて、左右のスライダを使用して範囲を狭めます。

* **[!UICONTROL Target Country]:** （オプション）ターゲットとする国。 [!DNL Comscore] は、サポート対象国でのみ提供されるインプレッション数を測定します。

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** を使用して、視認性のファーストパーティの測定とレポートを有効にします。 [!DNL IAB Open Video Viewability (OpenVV)] 指定した感度レベルに基づく技術。

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Campaign Managementについて](campaign-about.md)
>* [キャンペーンの作成](campaign-create.md)
>* [キャンペーンの編集](campaign-edit.md)

