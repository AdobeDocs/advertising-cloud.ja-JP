---
title: Advertising Cloud DSPの Audience Management について
description: Audience Management 機能について説明します。
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 0%

---

# Advertising Cloud DSPの Audience Management について

Advertising Cloud DSPでは、オーディエンスセグメントとオーディエンスセットを作成および管理できます。これらは、配置のターゲットとして使用できます。

* セグメントを作成および実装することで、独自のファーストパーティオーディエンスデータを収集できます。 後で、広告を含むセグメント内のユーザーを再ターゲット化したり、セグメント内のユーザーが広告を受け取らないようにしたりできます。 次のタイプのセグメントを作成できます。

   * [カスタムセグメント](/help/dsp/audiences/custom-segment-create.md) (a) デスクトップ、モバイル、CTV デバイスから広告を受けるユーザー、および (b) 特定の web ページを訪問するユーザーを追跡するため。

   * [CCPA オプトアウトオブセールセグメント](/help/dsp/audiences/ccpa-opt-out-segment-create.md) を使用して、カリフォルニア州消費者プライバシー法 (CCPA) に従って、Web サイト上の消費者のオプトアウトオブセール要求からユーザー ID を追跡します。 販売オプトアウトリクエストからユーザー ID の月別レポートを取得できます。

      CCPA オプトアウトオブセールのリクエストに対するAdvertising Cloudのサポートについて詳しくは、 [Adobe Advertising Cloud州消費者プライバシー法のサポート：消費者のオプトアウトのサポート](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html).

* オーディエンスライブラリを作成するには、 [再利用可能なオーディエンス](/help/dsp/audiences/reusable-audience-create.md). 保存されたオーディエンスは、使用可能なオーディエンスセグメントと、その他の保存されたオーディエンスで構成されます。 保存したオーディエンスに加えた変更は、そのオーディエンスをターゲットにしたすべてのプレースメントに自動的に適用されたり、オーディエンスを除外したりします。また、保存したオーディエンスを含む他のすべてのオーディエンスにも適用されます。

   保存されたオーディエンスを使用すると、メディアプランナーは、複雑なブール論理を使用して複数のセグメントを含めたり除外したりすることで、必要に応じてオーディエンスをグループ化できます。 オーディエンスの作成時に、各セグメントのサイズと合計オーディエンスサイズが示されます。 その後、キャンペーン実行者は、各プレースメントに対してオーディエンスターゲットを手動で設定する代わりに、1 つ以上の保存済みオーディエンスをプレースメントターゲットとして選択するだけで済みます。

プレースメントのターゲティングには、追加のオーディエンスタイプも使用できます。

## ファーストパーティおよびサードパーティのデータセグメントの読み込み

Advertising Cloud DSPでは、必要に応じて、データ管理プラットフォーム (DMP) から独自のファーストパーティデータセグメントを読み込み、それらを任意の広告主セットに提供できます。

Advertising Cloud DSPでは、サードパーティセグメントの複雑な組み合わせを含む、カスタムサードパーティセグメントを読み込むこともできます。 必要に応じて、任意の広告主セットにセグメントを提供できます。

お問い合わせ [!DNL Adobe] アカウントチームを参照してください。

## プレースメントターゲットとして使用可能なオーディエンス

配置は、次のすべてのタイプのオーディエンスにターゲット設定できます。

* Advertising Cloud DSPに保存されたすべてのユーザー作成オーディエンスセット。

* Advertising Cloud DSPで作成されたすべてのユーザー作成オーディエンスセグメント：

   * 特定の Web ページを訪問したユーザーと、特定の広告のインプレッションにさらされたユーザーのカスタムセグメント。

   * カリフォルニア州消費者プライバシー法 (CCPA) に従って、Web サイトで販売のオプトアウトリクエストを送信したユーザーに対する CCPA の販売のオプトアウトオーディエンスセグメント。

* 読み込まれたすべてのファーストパーティデータセグメント。

* 読み込まれたすべてのカスタムサードパーティデータセグメント。

* （米国をターゲットとするプレースメントのみ） [30 を超えるプロバイダーからAdvertising Cloud DSPのお客様が利用できるすべてのサードパーティデータセグメント](/help/dsp/audiences/third-party-data-providers.md)を含む [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast]、その他多数

   特定のセグメントをターゲット設定し、オーディエンスデータ（特定の人口統計、興味、目的、行動プロファイルを持つユーザーなど）に基づいてユーザーをターゲット設定できます。 データプロバイダーとカテゴリで参照したり、名前またはセグメント ID でセグメントを検索したり、データプロバイダー、合計セグメントサイズ、Web ブラウザー数またはデバイス数で結果をフィルタリングしたりできます。

   サードパーティセグメントには、追加料金が発生します。各セグメント名の横に表示されます。

* (Adobe Experience Cloud、Adobe Audience ManagerまたはAdobe Analyticsで、Advertising Cloud JavaScript コンバージョンタグのみを使用する広告主 )Adobe Experience Cloudで作成された、Audience Managerで作成された、またはAudience Managerや [!DNL Analytics].

   セグメントを使用するための価格は事前にネゴシエートされており、Advertising Cloudには表示されません。  <!-- Verify -->

   Adobe Experience Cloudでセグメントを作成または公開してから、約 1 時間後にAdobe Experience Cloudでセグメントを使用できるようになります。 Audience Managerから直接取得されたセグメントは、作成後約 24 時間で利用できます。 <!-- Verify all -->

   >[!NOTE]
   >
   >詳しくは、 [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html)、および [Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) を参照してください。

## オーディエンスサイズデータ

保存したオーディエンス設定および配置設定内で、詳細なオーディエンスサイズデータを確認できます。

* 選択したすべてのセグメントおよび保存済みのオーディエンスに関する重複を除外した合計オーディエンスサイズとアクティブなオーディエンスサイズが表示され、デバイスタイプ（ブラウザー、モバイル、または接続された TV）別に詳細を表示できます。

   ![結合オーディエンスのサイズ](/help/dsp/assets/audience-size.png)

* 個々のセグメントおよび保存したオーディエンスの場合、合計オーディエンスサイズと CPM（該当する場合）がセグメント名の横に表示されます。 デバイスタイプ別のサイズ（ブラウザー、モバイル、または接続された TV）を含む、セグメントに関する詳細を表示できます。 保存されたオーディエンスの合計サイズは、重複を除外した合計です。

   ![個々のセグメントのサイズ](/help/dsp/assets/audience-size-segment.png)

## オーディエンスビュー

### すべてのオーディエンス表示

内 [!UICONTROL All Audiences] オーディエンスライブラリを表示する場合は、再利用可能なオーディエンスを保存および管理できます。このオーディエンスには、オーディエンスセグメントのグループや、他の保存済みのオーディエンスも含まれます。 オーディエンスを複数の配置のターゲットとして使用できます。 各オーディエンスが使用される配置の数は、配置名の横に表示されます。

任意のオーディエンスを編集、複製、削除、書き出し、共有できます。

### セグメントビュー

内 [!UICONTROL Segments] すべてのユーザーが追加のカスタムセグメントを作成できます。

この [!UICONTROL Segments] また、表示には次のセグメントタイプも表示されます。

* ユーザーが使用できるすべてのユーザー作成カスタムセグメント。

   作成した任意のカスタムセグメントのトラッキングタグを表示して、それらのセグメントを他のユーザーと共有できます。 また、作成したカスタムセグメントを編集または削除することもできます。

   他のユーザーが自分と共有しているカスタムセグメントを編集または共有することはできません。

* 読み込まれたすべてのファーストパーティセグメントが、ユーザーが使用できます。

   自分と共有されていたファーストパーティセグメントを編集または共有することはできません。 お問い合わせ [!DNL Adobe] ファーストパーティセグメントを他のユーザーと共有する必要がある場合は、アカウントチームに問い合わせてください。

* ユーザーが使用できるすべてのカスタムサードパーティセグメント。

   自分と共有されていたサードパーティのセグメントを編集または共有することはできません。 お問い合わせ [!DNL Adobe] サードパーティセグメントを他のユーザーと共有する必要がある場合は、アカウントチームに問い合わせてください。

>[!MORELIKETHIS]
>
>* [再利用可能なオーディエンスを作成](reusable-audience-create.md)
>* [オーディエンス設定](audience-settings.md)
>* [オーディエンスセグメントロジックの構文](audience-segment-logic-syntax.md)
>* [カスタムセグメントの作成と実装](custom-segment-create.md)
>* [の作成と実装 [!UICONTROL CCPA Opt-Out-of-Sale] セグメント](ccpa-opt-out-segment-create.md)
>* [利用可能なサードパーティデータプロバイダー](third-party-data-providers.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

