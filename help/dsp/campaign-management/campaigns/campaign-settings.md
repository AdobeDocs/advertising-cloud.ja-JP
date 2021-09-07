---
title: キャンペーン設定
description: 使用可能なキャンペーン設定の説明を参照してください。
feature: Campaigns
exl-id: ff2e22ff-8073-4532-884b-36e0c1f22641
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 0%

---

# キャンペーン設定

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** キャンペーン名。

**[!UICONTROL Advertiser]:** （既存のキャンペーンの読み取り専用）該当する広告主（ブランド）。既存の広告主を選択するか、新しい広告主を作成します。

**[!UICONTROL Advertiser URL]:** 広告主の公式ページ。このフィールドは、在庫パートナーとの広告承認プロセスをスピードアップします。

**[!UICONTROL Timezone]:** （既存のキャンペーンの場合は読み取り専用）レポートおよび入札のタイムゾーン。

**[!UICONTROL Customer PO]:** （オプション）挿入注文/発注書の顧客発注書。

**[キャンペーン日]:** キャンペーンの開始日と終了日です。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** キャンペーンの余白を管理するかどうかを指定します。 *[!UICONTROL Yes]* また *[!UICONTROL No]* は（デフォルト）。

*[!UICONTROL Yes],*&#x200B;を選択した場合は、余白の種類と金額を指定します。

* **[!UICONTROL Margin Type]:** 余白のタイプ。利益管理を有効にしてキャンペーンを保存すると、利益のタイプを変更できなくなります。

   * *[!UICONTROL Fixed]:* （デフォルト）Advertising Cloud DSPが、の固定利益率に基づいて支出を自動計算および上限計上できるようにしま [!UICONTROL Gross Budget]す。

   * *[!UICONTROL Dynamic]:* キャンペーン内のパッケージおよび配置ごとに個別のおよびを指定するこ [!UICONTROL Budget Reserve %] と [!UICONTROL Gross Budget] で、配置レベルまでマージンを管理できます。Advertising Cloud DSPは、特定の利益を保証することなく、各配置の財務効率に基づいて最適化されます。 このオプションは、固定レートで固定金額の単位または単位タイプを配信することに同意した複数の行項目で構成される挿入注文に使用します。

* **[!UICONTROL Fixed Margin %]:** （余白が固定されたキャンペーンのみ）各挿入注文のデフォルトのマークアッ <!-- impression? -->プ（割合）。この金額は[!UICONTROL Gross Budget]から差し引かれ、正味キャンペーン予算が定義されます。

* **[!UICONTROL Budget Reserve %]:** (マージンが固定されたキャンペーンのみ。（オプション）の指定した割合をセーフガードと [!UICONTROL Gross Budget] して予約します。この金額は[!UICONTROL Gross Budget]から差し引かれ、正味キャンペーン予算が定義されます。

**[!UICONTROL Gross Budget]:** （マージン管理を含むキャンペーンのみ）指定したわずかな調整が適用される前の総キャンペーン予算。

オプションで、日次、週次または月次の総予算を追加できます。

1. クリック **[!UICONTROL Add an additional Gross Budget]**.

1. **[!UICONTROL Gross Budget]**&#x200B;を入力し、予算間隔を選択します。*[!UICONTROL Daily]、* *[!UICONTROL Weekly]、*&#x200B;または&#x200B;*[!UICONTROL Monthly]*。

合計純予算（キャンペーンの支出上限）は、マージンの設定に基づいて自動的に計算され、この値の下に表示されます。

**[!UICONTROL Budget]:** （利益管理がないキャンペーン）キャンペーンの予算全体。

**[!UICONTROL Estimated Tax Withholding]:** 国や地方税のアカウントレベルで、広告料、広告配送料、データ料の合計支出額の割合を源泉徴収します。レートは予算作成とペーシングの目的で見積もられるので、請求税率は異なる場合があります。

源泉徴収税を見積る手順は、次のとおりです。

1. クリック **[!UICONTROL Update rates here]**.

1. **[!UICONTROL Estimated tax rate]**&#x200B;をパーセンテージで指定します。

1. 税金を控除する各手数料タイプの横にあるチェック・ボックスを選択します。 料金のタイプは次のとおりです。

   * *[!UICONTROL Include estimated tax - ads fee]:* キャンペーン管理料に対する税を含め、すべてのAdvertising Cloud DSPメディア支出に適用されます。

   * *[!UICONTROL Include estimated tax - ad serving fee]:* メディアとデータを除く、Advertising Cloud DSPでのすべての支出に適用されます。キャンペーン管理料の税は除外されます

   * *[!UICONTROL Include estimated tax - data fee]:* すべてのデータがAdvertising Cloud DSPに費やされる場合に適用されます。

1. クリック **[!UICONTROL Submit]**.

>[!NOTE]
>
>* 米国では、広告、広告配信、データに税金を含める場合、州によって異なる場合があります。 他の国の組織では、VATを考慮する3つのカテゴリすべての税金を含めます。
>
>* これらの値は、アカウントの料金設定でも設定できます。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (2020年6月23日以降に作成された既存のキャンペーンの場合は読み取り専用。（2020年6月23日より前に作成されたキャンペーンでは使用不可） Advertising Cloudが広告をターゲットにし、頻度キャップを適用するレベル。 *同じデバ* イスを使用して、デバイスやユーザー ** が既知のすべてのデバイスをまたいでユーザーをターゲットに設定します。

**[!UICONTROL Device Graph]:** (既存のキャンペーンの場合は読み取り専用。ユーザーベースのクロスデバイスターゲティングのみを使用するキャンペーン)クロスデバイスターゲティングと頻度管理に使用するデバイスグラフ。

* *[!UICONTROL LiveRamp - U.S. only]:* デバイスグラフを使用して配信されるインプレッション（つまり、ターゲットオーディエンスセグメント内に見つからないデバイス）について、0.35 CPMでのクロスデバイスターゲティングの広告主全員が利用できま [!DNL LiveRamp] す。配置レベルでクロスデバイスターゲティングを設定できます。

   また、このオプションは、頻度管理とアトリビューション測定のために、無料ですべての広告主に提供されます。

* *[!UICONTROL Adobe Co-op U.S. and Canada only]:* Adobe Experience Cloudの参加者のみ [!DNL Device Co-op] が追加料金なしで利用できます。

>[!TIP]
>
>広告主がクロスデバイスアトリビューションも使用する場合、ベストプラクティスは、ターゲティングと頻度管理に、広告主のクロスデバイスアトリビューション設定で指定されたものと同じデバイスグラフ設定を使用することです。 このキャンペーンで別のデバイスグラフを選択すると、レポートの相違が発生する場合があります。

**[!UICONTROL Frequency Cap]:** （オプション）（指定したに応じて）一意のデバイスまたはユーザーがキャンペーンから広告を [!UICONTROL Cross Device Level]提供される回数。*[!UICONTROL Unlimited]*&#x200B;や、日、週、月ごとの特定の金額を選択できます。

>[!NOTE]
>
> 頻度キャップは、キャンペーン、パッケージおよび配置レベルで設定できます。 DSPは、キャンペーン階層で最も厳格な頻度キャップを尊重します。

**[!UICONTROL Packages]:** キャンペーン [](/help/dsp/campaign-management/packages/package-about.md) に含めるパッケージ。既存のパッケージを選択するか、含めるパッケージを作成します。 パッケージを作成する場合、詳しくは[パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)の説明を参照してください。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>次の設定は、測定およびレポート機能のみを有効にします。 パフォーマンスの最適化は、パッケージおよび配置レベルでのみ実行されます。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** （オプション）指定した設 [!DNL IAS] 定を使用して、視認性、不正、ブランドの安全性、オーディエンスの検証の測定とレポートを有効にします。追加料金が適用されます。

* **[!UICONTROL Measure On]:** 測定対象の在庫。 *[!UICONTROL Display and VPAID video inventory]* （デフォルト）または *[!UICONTROL Display, VPAID & VAST video inventory]*。

   >[!NOTE]
   >
   >ビデオの視認性は、VPAIDインベントリでのみ測定可能です。

* **[!UICONTROL IAS Account ID (AnID)]:** (独自のアカウントを持つ広 [!DNL IAS] 告主。（オプション）組織のアカウ [!DNL IAS] ントID(直接使 [!DNL IAS] 用を請求します)。

* **[!UICONTROL IAS Team ID]:** (独自のアカウントを持つ広 [!DNL IAS] 告主。（オプション）組織のアカウントのチームID( [!DNL IAS] 直接使用 [!DNL IAS] のために請求されます)。  <!-- verify -->

**[!UICONTROL MOAT]:** （オプション）視認性、不正 [!DNL MOAT] 行為、ブランドの安全性、オーディエンスの検証の測定とレポートを有効にします。追加料金が適用されます。

#### オーディエンスの検証

**[!UICONTROL Nielsen]:** （オプション）指定した設 [!DNL Nielsen] 定を使用して、オーディエンスの検証の測定とレポートを有効にします。追加料金が適用されます。

* **[!UICONTROL Target Gender]:** ターゲットとする性別： *[!UICONTROL Both]* （デフォルト）、ま *[!UICONTROL Male]*&#x200B;たは  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** ターゲットとする年齢範囲。必要に応じて、左右のスライダを使用して範囲を狭めます。

* **[!UICONTROL Target Country]:** （オプション）ターゲットとする国。[!DNL Nielsen] は、サポート対象国でのみ提供されたインプレッション数を測定します。

**[!UICONTROL comScore vCE]:** （オプション）指定した設 [!DNL Comscore validated Campaign Essentials (vCE)] 定を使用して、オーディエンスの検証の測定とレポートを有効にします。追加料金が適用されます。

* **[!UICONTROL Target Gender]:** ターゲットとする性別： *[!UICONTROL Both]* （デフォルト）、ま *[!UICONTROL Male]*&#x200B;たは  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** ターゲットとする年齢範囲。必要に応じて、左右のスライダを使用して範囲を狭めます。

* **[!UICONTROL Target Country]:** （オプション）ターゲットとする国。[!DNL Comscore] は、サポート対象国でのみ提供されたインプレッション数を測定します。

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** 指定した感度レベルに基づいて、テクノロジーを使用した視認性のファ [!DNL IAB Open Video Viewability (OpenVV)] ーストパーティ測定およびレポートを有効にします。

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [キャンペーン管理について](campaign-about.md)
>* [キャンペーンの作成](campaign-create.md)
>* [キャンペーンの編集](campaign-edit.md)

