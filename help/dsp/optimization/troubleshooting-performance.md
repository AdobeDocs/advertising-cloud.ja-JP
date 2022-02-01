---
title: パフォーマンスのトラブルシューティング
description: 一般的なパフォーマンスの問題を参照し、それらのトラブルシューティング方法を確認します。
feature: DSP Optimization
exl-id: adb32257-dede-4623-9840-33221c218443
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# パフォーマンスのトラブルシューティング

| 問題 | 考えられる原因 | 実行すべきアクション |
| --- | --- | --- |
| 配置に費やしない | プレースメントに広告が含まれていないか、広告がアクティブではありません。 | 予想されるすべての広告が配置に添付され、承認済みでアクティブであることを確認します。<br><br>また、配置にカスタム広告スケジュールが含まれているかどうかを確認します。これは、各広告の期間を制限する可能性があります。 配置ビューから配置の広告スケジュールを表示するには、  **[!UICONTROL ...]>[!UICONTROL Ad schedule]** 配置名の横に表示されます。 |
|  | 影響を受ける日付は、設定されたフライト日付内ではありません。 | フライト日がキャンペーン、パッケージ、配置レベルで有効であることを確認しま&#x200B;す。 |
|  | 予算の目標を満たした、または/または十分に高くない。 | キャンペーン、パッケージ、配置レベルで予算設定を確認します。 |
|  | このアカウントには十分な資金がありません。 | お客様のアカウントが十分な資金を提供しているかどうかを確認するには、 **[!UICONTROL Settings]>[!UICONTROL Account]** そして、 [!UICONTROL Usable Funds]. 追加の資金が必要な場合は、 [!DNL Adobe] アカウントチーム。 |
|  | 在庫がありません。 | 指定した在庫ソース ([!UICONTROL Public], [!UICONTROL Private]または [!UICONTROL On Demand]) は次のとおりです。<ul><li>を正しく設定します。</li><li>オークションを通じてアクティブで送信。</li><li>該当する広告およびプレースメントタイプとの互換性。</li></ul><br>在庫ソースがすべて有効で有効な場合は、可能な場合は追加またはすべての在庫ソースをターゲットにします。 |
|  | 利用できるユーザーがありません。 | 指定したオーディエンスのターゲットに十分なアクティブユーザーが含まれていることを確認します。 表示されない場合は、オーディエンスを追加してターゲットを拡張します。 |
| 配置に費やす費用が少ない | この [!UICONTROL Non Bids] 「配置の診断」レポートの「 」セクションに、配置が入札しなかった理由が表示されます。 | [以下を確認します。 [!UICONTROL Non Bids] レポート](/help/dsp/campaign-management/reports/placement-diagnostics.md) 配置が入札しなかった理由を理解するために  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | この配置は、 [入札前フィルター](/help/dsp/campaign-management/placements/placement-settings.md) 入札を制限する | 入札前フィルターのしきい値を 5%下げて、支出とパフォーマンスのバランスを評価します。 <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>入札前フィルター、地域、在庫、オーディエンスなど、複数の配置ターゲットを使用すると、累積的に入札と支出が制限される場合があることに注意してください。 |
|  | 配置の勝率が低い。 | を [!UICONTROL Max Bid] 勝率を向上させる。<br><br><b>注意：</b> 在庫価格は、配置のターゲティングに基づいて異なる場合があります。<br><br>10%の勝率は健全と見なされます。 |
|  | 在庫数が少ない。 | 可能な場合は、追加またはすべての在庫ソースをターゲットにします。<br><br>入札前フィルター、地域、在庫、オーディエンスなど、複数の配置ターゲットを使用すると、累積的に入札と支出が制限される場合があることに注意してください。 |
|  | 利用できるユーザーの数が少ない。 | 指定したオーディエンスのターゲットに十分なアクティブユーザーが含まれていることを確認します。 表示されない場合は、オーディエンスを追加してターゲットを拡張します。<br><br>入札前フィルター、地域、在庫、オーディエンスなど、複数の配置ターゲットを使用すると、累積的に入札と支出が制限される場合があることに注意してください。 |
|  | このパッケージには、多数のアクティブな配置が含まれています。 | パッケージ内のアクティブな配置の数を減らすか、パッケージの予算全体を増やします。<br><br>パッケージに多数の配置があるが、十分な予算がない場合、DSPは各配置に十分な予算を割り当てられない可能性があります。 各プレースメントには、少なくとも 2 米ドル/日を費やす機会が必要です。 例えば、パッケージの予算が 10 米ドル/日の場合、5 つ以下のプレースメントを含めることをお勧めします。&#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [キャンペーン設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)

