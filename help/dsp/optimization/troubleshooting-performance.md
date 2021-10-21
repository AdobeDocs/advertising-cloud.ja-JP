---
title: パフォーマンスのトラブルシューティング
description: 一般的なパフォーマンスの問題を参照し、そのトラブルシューティング方法を確認します。
feature: DSP Optimization
exl-id: adb32257-dede-4623-9840-33221c218443
source-git-commit: d2ad7d47d9cf13411fc831526a6fa4ff698b0a15
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# パフォーマンスのトラブルシューティング

| 問題 | 考えられる原因 | 措置 |
| --- | --- | --- |
| 配置に費用はかかりません | 配置に広告が含まれていないか、広告がアクティブではありません。 | 予想されるすべての広告が配置に添付され、承認され、アクティブであることを確認します。<br><br>また、配置にカスタム広告スケジュールが含まれているかどうかを確認します。これは各広告のフライト期間を制限する可能性があります。 配置ビューで配置の広告スケジュールを表示するには、  **[!UICONTROL ...]>[!UICONTROL Ad schedule]** をクリックします。 |
|  | 影響を受ける日付は、設定されたフライト日付の範囲内ではありません。 | フライト日がキャンペーン、パッケージ、配置レベルで有効であることを確認し&#x200B;ます。 |
|  | 予算の目標が満たされたか、または十分に高くない。 | キャンペーン、パッケージ、配置レベルで予算設定を確認します。 |
|  | その口座には十分な資金がない。 | アカウントが十分な資金を提供しているかどうかを確認するには、 **[!UICONTROL Settings]>[!UICONTROL Account]** そして、 [!UICONTROL Usable Funds]. 追加する資金が必要な場合は、 [!DNL Adobe] アカウントマネージャー |
|  | 在庫がありません。 | 指定した在庫ソース ([!UICONTROL Public], [!UICONTROL Private]または [!UICONTROL On Demand]) は次のとおりです。<ul><li>を正しくセットアップする。</li><li>アクティブで、オークションを通じて送信。</li><li>適用可能な広告および配置タイプと互換性があります。</li></ul><br>在庫ソースがすべて有効で有効な場合は、可能な場合は、追加またはすべての在庫ソースをターゲットにします。 |
|  | 利用できるユーザーはいません。 | 指定したオーディエンスターゲットに十分なアクティブユーザーが含まれていることを確認します。 表示されない場合は、オーディエンスを追加してターゲットを拡張します。 |
| 配置費用が少ない | 10. [!UICONTROL Non Bids] 「配置の診断」レポートの「 」セクションに、配置が入札しなかった理由の考えられる理由が表示されます。 | [の [!UICONTROL Non Bids] レポート](/help/dsp/campaign-management/reports/placement-diagnostics.md) 配置が入札しなかった理由を理解するために  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | この配置は、 [入札前フィルター](/help/dsp/campaign-management/placements/placement-settings.md) 入札を制限する | 入札前のフィルターのしきい値を 5%下げて、支出とパフォーマンスのバランスを評価します。 <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>入札前フィルター、地域、在庫、オーディエンスなど、複数の配置ターゲットを使用すると、累積的に入札と支出が制限される場合があることに注意してください。 |
|  | その配置は勝率が低い。 | の [!UICONTROL Max Bid] 勝利率を向上させる。<br><br><b>注意：</b> 在庫価格は、プレースメントのターゲティングに基づいて異なる場合があります。<br><br>10%の勝率は健全と見なされる。 |
|  | 在庫数が少ない。 | 可能な場合は、追加の在庫ソースまたはすべての在庫ソースをターゲットに設定します。<br><br>入札前フィルター、地域、在庫、オーディエンスなど、複数の配置ターゲットを使用すると、累積的に入札と支出が制限される場合があることに注意してください。 |
|  | 利用できるユーザーの数が少ない。 | 指定したオーディエンスターゲットに十分なアクティブユーザーが含まれていることを確認します。 表示されない場合は、オーディエンスを追加してターゲットを拡張します。<br><br>入札前フィルター、地域、在庫、オーディエンスなど、複数の配置ターゲットを使用すると、累積的に入札と支出が制限される場合があることに注意してください。 |
|  | パッケージには、多数のアクティブな配置が含まれています。 | パッケージ内のアクティブな配置の数を減らすか、パッケージの予算全体を増やします。<br><br>パッケージに多数の配置があるが十分な予算がない場合、DSPは各配置に十分な予算を割り当てることができない可能性があります。 各配置には、少なくとも 2 米ドル/日を費やす機会が必要です。 例えば、パッケージの予算が 10 米ドル/日の場合は、5 つ以下の配置を含めることをお勧めします。&#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [キャンペーンの設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)

