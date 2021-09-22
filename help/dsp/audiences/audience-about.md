---
title: Advertising Cloud DSPのAudience Managementについて
description: Audience Management機能について説明します。
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---

# Advertising Cloud DSPのAudience Managementについて

Advertising Cloud DSPでは、オーディエンスセグメントとオーディエンスセットを作成および管理でき、これらを配置のターゲットとして使用できます。

* セグメントを作成および実装することで、独自のファーストパーティオーディエンスデータを収集できます。 後で、セグメント内のユーザーを広告付きで再ターゲット化したり、セグメント内のユーザーが広告を受け取らないようにしたりできます。 次のタイプのセグメントを作成できます。

   * [追跡す](/help/dsp/audiences/custom-segment-create.md) るカスタムセグメント(a)デスクトップ、モバイル、CTVデバイス、およびb)特定のWebページを訪問するユーザーから広告を受けたユーザー。

   * [CCPAの販売オプトアウトセグメントを使用し](/help/dsp/audiences/ccpa-opt-out-segment-create.md) て、カリフォルニア州消費者プライバシー法(CCPA)に従って、Webサイト上の消費者の販売オプトアウトリクエストからユーザーIDを追跡します。販売オプトアウトリクエストからユーザーIDの月別レポートを取得できます。

      CCPAオプトアウトオブセールリクエストのAdvertising Cloudサポートについて詳しくは、カリフォルニア州消費者プライバシー法(CCPA)のAdobe Advertising Cloudサポートを参照してください。[消費者のオプトアウトのサポート](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)。

* [再利用可能なオーディエンス](/help/dsp/audiences/reusable-audience-create.md)のオーディエンスライブラリを作成できます。 保存されたオーディエンスは、使用可能なオーディエンスセグメントと、その他の保存されたオーディエンスで構成されます。 保存したオーディエンスに対して行った変更は、そのオーディエンスをターゲットにする、または除外するすべての配置と、保存したオーディエンスを含む他のすべてのオーディエンスに自動的に適用されます。

   保存されたオーディエンスを使用すると、メディアプランナーは、複雑なブール論理を使用して複数のセグメントを含めたり除外したりすることで、必要に応じてオーディエンスをグループ化できます。 オーディエンスの作成時に、各セグメントのサイズと合計オーディエンスサイズが示されます。 その後、キャンペーンの実行者は、各プレースメントに対してオーディエンスターゲットを手動で設定する代わりに、1つ以上の保存済みオーディエンスをプレースメントターゲットとして選択するだけで済みます。

追加のオーディエンスタイプは、プレースメントのターゲティングにも使用できます。

## ファーストパーティおよびサードパーティのデータセグメントの読み込み

Advertising Cloud DSPでは、データ管理プラットフォーム(DMP)から独自のファーストパーティデータセグメントを読み込み、必要に応じて任意の広告主に提供できます。

Advertising Cloud DSPでは、サードパーティセグメントの複雑な組み合わせを含む、カスタムのサードパーティセグメントを読み込むこともできます。 必要に応じて、任意のセットの広告主にセグメントを提供できます。

詳しくは、アカウントマネージャーにお問い合わせください。

## プレースメントターゲットとして使用可能なオーディエンス

配置は、次のすべてのタイプのオーディエンスにターゲット設定できます。

* Advertising Cloud DSPに保存されたすべてのユーザーが作成したオーディエンスセット。

* Advertising Cloud DSPで作成されたすべてのユーザー作成オーディエンスセグメント：

   * 特定のWebページを訪問したユーザーと特定の広告のインプレッションにさらされたユーザーのカスタムセグメント。

   * カリフォルニア州消費者プライバシー法(CCPA)に従い、Webサイトで販売のオプトアウトリクエストを送信したユーザーに対するCCPA販売のオプトアウトオーディエンスセグメント。

* 読み込まれたすべてのファーストパーティデータセグメント。

* インポートされたすべてのカスタムサードパーティデータセグメント。

* （米国のみをターゲットとする配置） [Advertising Cloud DSPのお客様が、[!DNL Acxiom]、[!DNL Datalogix]、[!DNL eXelate]([!DNL Nielsen])、[!DNL Lotame]、[!DNL Oracle]、[!DNL Quantcast]など、30を超えるプロバイダーから利用できるすべてのサードパーティデータセグメント。](/help/dsp/audiences/third-party-data-providers.md)

   特定のセグメントをターゲット設定し、オーディエンスデータ（特定の人口統計、興味、目的、行動プロファイルを持つユーザーなど）に基づいてユーザーをターゲット設定できます。 データプロバイダーとカテゴリ別、名前またはセグメントID別にセグメントを検索したり、結果をデータプロバイダー別、合計セグメントサイズ別、Webブラウザー数別、デバイス数別にフィルタリングしたりできます。

   サードパーティセグメントには追加料金が発生し、各セグメント名の横に表示されます。

* (Adobe Experience Cloud、Adobe Audience ManagerまたはAdobe Analyticsで、Advertising Cloud JavaScriptコンバージョンタグのみを使用する広告主) Adobe Experience Cloudで作成された、Audience Managerで作成された、またはAudience Managerや[!DNL Analytics]からAdobe Experience Cloudに公開された、使用可能なすべてのファーストパーティ、セカンドまたはサードパーティのオーディエンスセグメント。

   セグメント使用の価格は事前にネゴシエートされ、Advertising Cloudには表示されません。 <!-- Verify -->

   Adobe Experience Cloudでセグメントを作成または公開してから約1時間後にAdobe Experience Cloudからセグメントを使用できるようになります。 セグメントをAudience Managerから直接取得してから約24時間後に使用可能になります。<!-- Verify all -->

   >[!NOTE]
   >
   >これらのソリューションでのセグメントのデータの設定と収集について詳しくは、 [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html)、[Analytics](https://experienceleague.adobe.com/docs/analytics/landing/home.html)および[Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html)のドキュメントを参照してください。

## オーディエンスサイズデータ

保存されたオーディエンス設定および配置設定内で、詳細なオーディエンスサイズデータを確認できます。

* 選択したすべてのセグメントおよび保存されたオーディエンスの合計およびアクティブな重複排除オーディエンスサイズが表示され、デバイスタイプ（ブラウザー、モバイル、接続されたTV）別に詳細を表示できます。

   ![結合オーディエンスのサイズ](/help/dsp/assets/audience-size.png)

* 個々のセグメントおよび保存されたオーディエンスの場合、合計オーディエンスサイズとCPM（該当する場合）がセグメント名の横に表示されます。 デバイスタイプ別のサイズ（ブラウザー、モバイル、または接続されたテレビ）を含む、セグメントに関する詳細を表示できます。 保存されたオーディエンスの合計サイズは、重複を除外した合計です。

   ![個々のセグメントのサイズ](/help/dsp/assets/audience-size-segment.png)

## オーディエンスビュー

### すべてのオーディエンス表示

[!UICONTROL All Audiences]ビューまたはオーディエンスライブラリでは、オーディエンスセグメントのグループや他の保存済みオーディエンスを含む、再利用可能なオーディエンスを保存および管理できます。 オーディエンスを複数の配置のターゲットとして使用できます。 各オーディエンスが使用される配置の数は、配置名の横に示されます。

任意のオーディエンスを編集、複製、削除、書き出し、または共有できます。

### セグメントビュー

[!UICONTROL Segments]ビューでは、すべてのユーザーが追加のカスタムセグメントを作成できます。

[!UICONTROL Segments]ビューには、次のセグメントタイプも表示されます。

* ユーザーが作成したすべてのカスタムセグメントが、そのユーザーに対して使用可能です。

   作成した任意のカスタムセグメントのトラッキングタグを表示して、他のユーザーと共有できます。 また、作成したカスタムセグメントを編集または削除することもできます。

   他のユーザーと共有しているカスタムセグメントを編集または共有することはできません。

* 読み込まれたすべてのファーストパーティセグメントが、ユーザーに対して使用可能です。

   自分と共有されているファーストパーティセグメントを編集または共有することはできません。 ファーストパーティセグメントを追加のユーザーと共有する必要がある場合は、アカウントマネージャーにお問い合わせください。

* ユーザーが使用できるすべてのカスタムサードパーティセグメント。

   自分と共有されているサードパーティセグメントを編集または共有することはできません。 サードパーティセグメントを追加のユーザーと共有する必要がある場合は、アカウントマネージャーにお問い合わせください。

>[!MORELIKETHIS]
>
>* [再利用可能なオーディエンスの作成](reusable-audience-create.md)
>* [オーディエンス設定](audience-settings.md)
>* [オーディエンスセグメントロジックの構文](audience-segment-logic-syntax.md)
>* [カスタムセグメントの作成と実装](custom-segment-create.md)
>* [セグメントの作成と [!UICONTROL CCPA Opt-Out-of-Sale] 実装](ccpa-opt-out-segment-create.md)
>* [使用可能なサードパーティデータプロバイダー](third-party-data-providers.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

