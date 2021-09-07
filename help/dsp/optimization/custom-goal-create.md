---
title: カスタム目標の作成
description: カスタム目標の作成
feature: Optimization
exl-id: 440ded21-92d3-41ad-839f-ebc8376aa932
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# カスタム目標の作成

>[!TIP]
>
>カスタム目標の設定方法に関するヒントについては、[カスタム目標の作成のベストプラクティス](custom-goal-best-practices.md)を参照してください。

1. （米国の会社） [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com)または（他のすべての国の会社） [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com)でAdvertising Cloud Searchにログインします。
1. 目標に含める指標が追跡され、製品で使用可能であること、および表示名が含まれていることを確認します。
   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**&#x200B;をクリックします。
   1. 指標を探し、その指標に対して&#x200B;**[!UICONTROL Show in UI and Reports]**&#x200B;が有効になっていることを確認します。
   1. 指標の&#x200B;**[!UICONTROL Display Name]**&#x200B;列に値がない場合は、セル内をクリックし、表示名を入力して、「**[!UICONTROL Apply].**」をクリックします
1. *目標*&#x200B;としてカスタム目標を作成します。
   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**&#x200B;をクリックします。
   1. ツールバーで、「**[!UICONTROL Create objective].**」をクリックします。
   1. 目標設定を入力します。
      1. **[!UICONTROL Change Objective Name]**&#x200B;フィールドに、目的の名前を入力します。

         目的名は、Advertising Cloud DSPパッケージ設定の[!UICONTROL Custom Goals]リストに表示されます。

      1. 目的とのプロパティの関連付け：

         >[!NOTE]
         >
         > デフォルトでは、広告主に対して追跡されるトランザクションプロパティはすべて[!UICONTROL Available Properties]リストに表示されます。

         * プロパティと重み付けを含むCSVファイルを読み込むには、**[!UICONTROL Import]**&#x200B;をクリックし、読み込むファイルを見つけます。

            読み込まれたプロパティは、既に広告主用に存在している必要があります。名前では大文字と小文字が区別されません。

            読み込まれたプロパティは、指定された既存のプロパティを置き換えます。

         * デフォルトの重み付け(1)を使用して最初のプロパティを手動で指定するには、広告主に対して追跡されるすべてのトランザクションプロパティのリストから選択します。

         * デフォルトの重み付け(1)を指定して別のプロパティを手動で追加するには、 **[!UICONTROL +]**&#x200B;をクリックします。

            >[!TIP]
            >
            > リスト内のプロパティを検索するには、プロパティ名の任意の場所から文字列を入力します。

         * 複数のプロパティを手動で追加するには、「**[!UICONTROL Add Multiple Properties]」をクリックします。** 追加する各プロパティについて、列のプロパティ名をク [!UICONTROL Available Properties] リックし、列にドラッグし [!UICONTROL Added Properties] ます。プロパティの追加が完了したら、「**[!UICONTROL Add]**」をクリックします。

            >[!TIP]
            >
            >* リスト内のプロパティを検索するには、入力フィールドにプロパティ名内の任意の場所から文字列を入力します。
            >* リストにフィルターを適用して、レポートから除外されるプロパティを除外するには、**[!UICONTROL Hide properties excluded from reports].**&#x200B;オプションを選択します。


         * （目標に複数のプロパティが含まれる場合）目的の他のプロパティと比較してプロパティの重みを変更するには、**[!UICONTROL Weight]**&#x200B;フィールドに値を入力します。
      1. 設定の下部で、「**[!UICONTROL Save]**」をクリックします。


目標を作成したら、最適化目標が「[!UICONTROL Highest ROAS - Custom Goal]」または「[!UICONTROL Lowest CPA - Custom Goal]」の場合に、カスタム目標としてAdvertising Cloud DSPパッケージに割り当てることができます。

>[!TIP]
>
><!-- optimum? Or optimization won't happen at all w/out it? -->パフォーマンスを最適化するには、カスタム目標（目標）の組み合わせ指標の合計が1日に10回以上必要です。 表示されない場合、ベストプラクティスは、製品ページやアプリケーションの開始など、サポートするイベント（トランザクションプロパティ）を目的に追加することです。 ガイドラインについては、[カスタム目標の構築のベストプラクティス](custom-goal-best-practices.md)を参照してください。

>[!MORELIKETHIS]
>
>* [カスタム目標について](custom-goal-about.md)
>* [カスタム目標を作成するためのベストプラクティス](custom-goal-best-practices.md)
>* [最適化目標とその使用方法](optimization-goals.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [キャンペーンの最適化方法](optimization-how-dsp-optimizes-campaigns.md)

