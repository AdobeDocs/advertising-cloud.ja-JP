---
title: カスタム目標の作成
description: カスタム目標の作成
feature: DSP Optimization
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# カスタム目標の作成

カスタム目標は、 *目標* 範囲 [!DNL Adobe Advertising Search].

カスタム目標を作成するには、DSPアカウントを [!DNL Search] 内から同じAdobe Experience Cloud組織 ID を持つアカウント [!DNL Search] クライアント設定。 DSPアカウントが [!DNL Search] アカウント、 [!DNL Adobe] アカウントチーム。

>[!TIP]
>
>詳しくは、 [カスタム目標の作成に関するベストプラクティス](custom-goal-best-practices.md) カスタム目標の設定方法に関するヒントを参照してください。

1. ログイン [!DNL Adobe Advertising Search] （米国の会社）で [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) または（他のすべての国の会社） [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. 目標に含める指標が追跡され、製品で利用できること、および表示名が含まれていることを確認します。
   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.
   1. 指標を見つけ、 **[!UICONTROL Show in UI and Reports]** は指標に対して有効になっています。
   1. 指標の値が **[!UICONTROL Display Name]** 列をクリックし、セル内をクリックして表示名を入力し、 **[!UICONTROL Apply].**
1. カスタム目標を *目的*:
   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**.
   1. ツールバーで、 **[!UICONTROL Create objective].**
   1. 目標設定を入力します。
      1. 内 **[!UICONTROL Change Objective Name]** 「 」フィールドに、目標名を入力します。

         目標名は、 [!UICONTROL Custom Goals] リストをDSPパッケージ設定に表示します。

      1. プロパティを目的に関連付けます。

         >[!NOTE]
         >
         > 広告主に対してトラッキングされるすべてのトランザクションプロパティは、デフォルトで [!UICONTROL Available Properties] リスト。

         * プロパティとその重みを含む CSV ファイルを読み込むには、 **[!UICONTROL Import]** をクリックし、インポートするファイルを探します。

            読み込まれたプロパティは、広告主用に既に存在している必要があります。名前では大文字と小文字が区別されません。

            読み込まれたプロパティは、指定された既存のプロパティを置き換えます。

         * デフォルトの重み付け (1) を使用して最初のプロパティを手動で指定するには、広告主に対してトラッキングされるすべてのトランザクションプロパティのリストから選択します。

         * デフォルトの重み付け (1) を指定して別のプロパティを手動で追加するには、 **[!UICONTROL +]** .

            >[!TIP]
            >
            > リスト内のプロパティを検索するには、プロパティ名の任意の場所から文字列を入力します。

         * 複数のプロパティを手動で追加するには、 **[!UICONTROL Add Multiple Properties].** 追加する各プロパティに対して、 [!UICONTROL Available Properties] 列をクリックし、 [!UICONTROL Added Properties] 列。 プロパティの追加が完了したら、 **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* リスト内のプロパティを検索するには、入力フィールドにプロパティ名内の任意の場所から文字列を入力します。
            >* リストをフィルタリングして、レポートから除外されるプロパティを除外するには、「 」オプションを選択します **[!UICONTROL Hide properties excluded from reports].**


         * （目的に複数のプロパティが含まれる場合）目的の他のプロパティに対するプロパティの重みを変更するには、 **[!UICONTROL Weight]** フィールドに値を入力します。
      1. 設定の下部で、 **[!UICONTROL Save]**.


目標を作成したら、最適化目標が「 」の場合に、カスタム目標としてDSPパッケージに割り当てることができます。[!UICONTROL Highest ROAS - Custom Goal]&quot;または&quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>パフォーマンスを最適化するために、カスタム目標（目標）の組み合わせ指標では、1 日に少なくとも 10 のコンバージョンを合計する必要があります。 表示されない場合は、ベストプラクティスとして、製品ページやアプリケーションの開始などのサポートイベント（トランザクションプロパティ）を目的に追加します。 詳しくは、 [カスタム目標を構築するためのベストプラクティス](custom-goal-best-practices.md) 」を参照してください。

>[!MORELIKETHIS]
>
>* [カスタム目標について](custom-goal-about.md)
>* [カスタム目標を構築するためのベストプラクティス](custom-goal-best-practices.md)
>* [最適化目標とその使用方法](optimization-goals.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [キャンペーンの最適化方法](optimization-how-dsp-optimizes-campaigns.md)

