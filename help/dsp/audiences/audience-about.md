---
title: Advertising Cloud DSPの Audience Management について
description: Audience Management 機能について説明します。
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: 578651a458ffd505573df0e9a61e26bd2176ad17
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 0%

---

# Advertising Cloud DSPの Audience Management について

Advertising Cloud DSPでは、オーディエンスセグメントとオーディエンスセットを作成および管理でき、これらを配置のターゲットとして使用できます。

* セグメントを作成および実装することで、独自のファーストパーティオーディエンスデータを収集できます。 後で、セグメント内のユーザーを広告付きで再ターゲット化したり、セグメント内のユーザーが広告を受け取らないようにすることができます。 次のタイプのセグメントを作成できます。

   * [追跡す](/help/dsp/audiences/custom-segment-create.md) るカスタムセグメント a) デスクトップ、モバイル、CTV デバイスから広告を受けたユーザー、および b) 特定の Web ページを訪問したユーザー。

   * [CCPA の販売オプトアウトセグメントを使用し](/help/dsp/audiences/ccpa-opt-out-segment-create.md) て、カリフォルニア州消費者プライバシー法 (CCPA) に従って、Web サイト上の消費者の販売オプトアウトリクエストからユーザー ID を追跡します。販売オプトアウトリクエストからユーザー ID の月別レポートを取得できます。

      CCPA オプトアウトオブセールのリクエストに対するAdvertising Cloudのサポートについて詳しくは、 [ カリフォルニア州消費者プライバシー法に対するAdobe Advertising Cloudのサポートを参照してください。消費者のオプトアウトのサポート ](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)。

* [ 再利用可能なオーディエンス ](/help/dsp/audiences/reusable-audience-create.md) のオーディエンスライブラリを作成できます。 保存されたオーディエンスは、使用可能なオーディエンスセグメントと、その他の保存されたオーディエンスで構成されます。 保存したオーディエンスに加えた変更は、そのオーディエンスをターゲットにする、または除外するすべての配置と、保存したオーディエンスを含む他のすべてのオーディエンスに自動的に適用されます。

   保存されたオーディエンスを使用すると、メディアプランナーは、複雑な Boolean ロジックを使用して複数のセグメントを含めたり除外したりすることで、必要に応じてオーディエンスをグループ化できます。 オーディエンスの作成時に、各セグメントのサイズと合計オーディエンスサイズが示されます。 その後、キャンペーンの実行者は、保存済みのオーディエンスを配置ターゲットとして選択するだけで、各配置のオーディエンスターゲットを手動で設定する必要はありません。

プレースメントのターゲティングには、追加のオーディエンスタイプも使用できます。

## ファーストパーティおよびサードパーティのデータセグメントの読み込み

Advertising Cloud DSPでは、データ管理プラットフォーム (DMP) から独自のファーストパーティデータセグメントを読み込み、必要に応じて任意の広告主に提供できます。

Advertising Cloud DSPでは、サードパーティセグメントの複雑な組み合わせを含む、カスタムのサードパーティセグメントを読み込むこともできます。 必要に応じて、任意の広告主セットにセグメントを提供できます。

詳しくは、担当のアカウントマネージャーにお問い合わせください。

## プレースメントターゲットとして使用可能なオーディエンス

配置を、次のすべてのタイプのオーディエンスにターゲット設定できます。

* Advertising Cloud DSPに保存されたすべてのユーザー作成オーディエンスセット。

* Advertising Cloud DSPで作成されたすべてのユーザー作成オーディエンスセグメント：

   * 特定の Web ページを訪問したユーザーと特定の広告のインプレッションにさらされたユーザーのカスタムセグメント。

   * カリフォルニア州消費者プライバシー法 (CCPA) に従い、Web サイトで販売のオプトアウトリクエストを送信したユーザーに対する CCPA の販売のオプトアウトオーディエンスセグメント。

* 読み込まれたすべてのファーストパーティデータセグメント。

* インポートされたすべてのカスタムサードパーティデータセグメント。

* （米国のみを対象とする配置） [Advertising Cloud DSPのお客様が、[!DNL Acxiom]、[!DNL Datalogix]、[!DNL eXelate]([!DNL Nielsen])、[!DNL Lotame]、[!DNL Oracle]、[!DNL Quantcast] など、30 を超えるプロバイダーから利用できるすべてのサードパーティデータセグメント。](/help/dsp/audiences/third-party-data-providers.md)

   特定のセグメントをターゲット設定して、オーディエンスデータ（特定の人口統計、興味、目的、行動プロファイルを持つユーザーなど）に基づいてユーザーをターゲット設定できます。 データプロバイダーとカテゴリ別に参照したり、名前やセグメント ID 別にセグメントを検索したり、データプロバイダー別、合計セグメントサイズ別、Web ブラウザー数別、デバイス数別に結果をフィルタリングしたりできます。

   サードパーティセグメントには追加料金が発生し、各セグメント名の横に表示されます。

* (Advertising Cloud JavaScript 変換タグのみを使用しているAdobe Experience Cloud、Adobe Audience Manager、Adobe Analyticsの広告主 ) Adobe Experience Cloudで作成された、Audience Managerで作成された、またはAudience Managerや [!DNL Analytics] からAdobe Experience Cloudに公開された、使用可能なファーストパーティ、セカンドパーティ、サードパーティのオーディエンスセグメント。

   セグメントを使用するための価格は事前にネゴシエートされ、Advertising Cloudには表示されません。 <!-- Verify -->

   Adobe Experience Cloudでセグメントを作成または公開してから、約 1 時間後にAdobe Experience Cloudからセグメントを使用できます。 Audience Managerから直接取得したセグメントは、作成してから約 24 時間後に使用できます。<!-- Verify all -->

   >[!NOTE]
   >
   >これらのソリューションでのセグメントのデータの設定と収集について詳しくは、[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html)、[Analytics](https://experienceleague.adobe.com/docs/analytics.html) および [Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) のドキュメントを参照してください。

## オーディエンスサイズデータ

保存されたオーディエンス設定および配置設定内で、詳細なオーディエンスサイズデータを確認できます。

* 選択したすべてのセグメントおよび保存済みのオーディエンスの合計およびアクティブな重複排除オーディエンスサイズが表示され、デバイスタイプ（ブラウザー、モバイル、接続済み TV）別に詳細を表示できます。

   ![結合オーディエンスのサイズ](/help/dsp/assets/audience-size.png)

* 個々のセグメントおよび保存したオーディエンスの場合、合計オーディエンスサイズと CPM（該当する場合）がセグメント名の横に表示されます。 デバイスタイプ別のサイズ（ブラウザー、モバイル、接続された TV）を含む、セグメントに関する詳細を表示できます。 保存したオーディエンスの合計サイズは、重複を除外した合計です。

   ![個々のセグメントのサイズ](/help/dsp/assets/audience-size-segment.png)

## オーディエンスビュー

### 「All Audiences」表示

[!UICONTROL All Audiences] ビューまたはオーディエンスライブラリでは、オーディエンスセグメントのグループや他の保存済みのオーディエンスを含む、再利用可能なオーディエンスを保存および管理できます。 オーディエンスを複数の配置のターゲットとして使用できます。 各オーディエンスが使用される配置の数は、配置名の横に示されます。

任意のオーディエンスを編集、複製、削除、書き出し、共有できます。

### セグメントビュー

[!UICONTROL Segments] ビューでは、すべてのユーザーが追加のカスタムセグメントを作成できます。

[!UICONTROL Segments] ビューには、次のセグメントタイプも表示されます。

* ユーザーが使用できるすべてのユーザー作成カスタムセグメント。

   作成した任意のカスタムセグメントのトラッキングタグを表示して、他のユーザーとセグメントを共有できます。 また、作成したカスタムセグメントを編集または削除することもできます。

   他のユーザーが自分と共有しているカスタムセグメントを編集または共有することはできません。

* 読み込まれたすべてのファーストパーティセグメントが、ユーザーに対して使用可能です。

   自分と共有されていたファーストパーティセグメントを編集または共有することはできません。 ファーストパーティセグメントを追加のユーザーと共有する必要がある場合は、アカウントマネージャーにお問い合わせください。

* ユーザーが使用できるすべてのカスタムサードパーティセグメント。

   自分と共有されているサードパーティのセグメントを編集または共有することはできません。 サードパーティのセグメントを追加のユーザーと共有する必要がある場合は、アカウントマネージャーにお問い合わせください。

>[!MORELIKETHIS]
>
>* [再利用可能なオーディエンスの作成](reusable-audience-create.md)
>* [オーディエンスの設定](audience-settings.md)
>* [オーディエンスセグメントロジックの構文](audience-segment-logic-syntax.md)
>* [カスタムセグメントの作成と実装](custom-segment-create.md)
>* [セグメントの作成と [!UICONTROL CCPA Opt-Out-of-Sale] 実装](ccpa-opt-out-segment-create.md)
>* [使用可能なサードパーティデータプロバイダー](third-party-data-providers.md)
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)

