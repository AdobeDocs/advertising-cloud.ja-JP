---
title: のエラーコード [!DNL FreeWheel] 広告送信
description: に対する広告送信で返されるエラーコードを参照します。 [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 2eb93971-ba82-4de8-96c5-48524d628b70
source-git-commit: 39f491a39bdc9d8dd820eb4c69594dda71d8b3c2
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 2%

---

# のエラーコード [!DNL FreeWheel] 広告送信

失敗した広告送信のエラーメッセージは、Advertising Cloud DSPまたは [!DNL FreeWheel]. エラーメッセージは、 [!UICONTROL API Response] 列 [[!UICONTROL Freewheel Status] ダイアログ](freewheel-check-status.md).

## Advertising Cloud DSP内部エラー

| エラーメッセージ | 説明 | 次の手順 |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] は、送信が成功したか失敗したかをまだ返していません。 | 10 分後にもう一度ステータスを確認します。 |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] では、時計番号が割り当てられていない英国の広告を受け付けません。 | 広告に時計番号を割り当ててから、広告を再送信してください。 |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | 広告の送信時に、トランスコーダーが広告のトランスコードを完了していませんでした。 | 10 分待ってから、広告を再送信してください。 |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | 送信された契約は、プログラム的に保証された契約として設定されていません。 [!DNL FreeWheel] は保証された契約のみを受け入れます。 | プログラム的に保証された契約として、契約 ID を設定します。 広告はに自動的に送信されます [!DNL FreeWheel] 契約 ID ワークフローの最後に、プログラムで保証されたデフォルトの配置を保存する場合。 |
| [!DNL Invalid external_deal_id:] \&lt;deal_id> | 送信された契約 ID は、存在しないか、Adobe側でアクティブではありません。 | 契約がアクティブであることを確認し、広告を再送信します。 |
| [!DNL \[public_id=]\&lt;deal>] が存在しません | 送信された契約 ID がに存在しません [!DNL FreeWheel] 終了 | お問い合わせ [!DNL FreeWheel] 担当者を使用して、契約 ID を確認します。 |
| [!DNL Ad with identifier] \&lt;*広告名*\> [!DNL was not found.] | 送信された広告キーは、存在しないか、Adobe側でアクティブではありません。 | 正しい広告キーを見つけて、広告を再送信してください。 |
| [!DNL Pending Submission] | 送信はまだ保留中です。 | ページを更新します。 |

{style=&quot;table-layout:auto&quot;}

## [!DNL Freewheel] API エラー

| コード | 意味 | 説明 | 次の手順 |
|--- |--- |--- |--- |
| 401 | 未認証 | アクセス資格情報が正しくない、見つからない、または無効です。 | お問い合わせ [!DNL Adobe] アカウントチーム。 |
| 403 | Forbidden | サーバーはリクエストを認識しましたが、承認を拒否しました。 | お問い合わせ [!DNL Adobe] アカウントチーム。 |
| 404 | 見つかりません | 要求したリソースは使用できません。 クリエイティブ ID がPUT操作で見つからない場合は、404 が返されます。 | お問い合わせ [!DNL Adobe] アカウントチーム。 |
| 405 | 許可されていないメソッド | リクエストが、そのリソースでサポートされていないリクエストメソッドを使用してリソースでおこなわれました ( 例えば、POSTでGETを送信する必要があるメソッドのデータを使用したり、読み取り専用リソースのPUTを使用した )。 | お問い合わせ [!DNL Adobe] アカウントチーム。 |
| 408 | リクエストタイムアウト | このリクエストの処理中にタイムアウトが発生しました。 タイムアウトは、通常、特定のリソースへの排他的なアクセス要求が同時に実行されたことが原因で発生します。 | このステータスを受け取ったら、要求を再送信します。 問題が解決しない場合は、 [!DNL Adobe] アカウントチーム。 |
| 422 | 処理不可のエンティティ | 無効なリソースです。 このエラーは、リクエスト本文が無効な場合、または作成/更新されたリソースが無効な場合（例えば、Deal ID が見つからなかった場合）に発生します。 詳しくは、 [FreeWheel API 422 エラー](#freewheel-422-errors) を参照してください。 | お問い合わせ [!DNL Adobe] アカウントチーム。 |
| 500 | 内部サーバーエラー | API システムエラー。 | お問い合わせ [!DNL Adobe] アカウントチーム。 |

{style=&quot;table-layout:auto&quot;}

## [!DNL Freewheel] API 422 エラー {#freewheel-422-errors}

| コード | HTTP コード | 説明 |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | リクエストデータの JSON 形式が無効です。 詳しくは、エラーメッセージを確認してください。 |
| DATA_VALIDATION_FAILURE | 422 | リクエストデータに必須フィールドがないか、無効なデータタイプが含まれています。 詳しくは、エラーメッセージを確認してください。 |
| DATA_DEAL_INVALID | 422 | 契約の設定が正しくないか、存在しません。 詳しくは、エラーメッセージを確認してください。 |
| DATA_DEAL_DATA_FAILURE | 422 | 契約が見つからなかったか、設定に問題があります。 詳しくは、エラーメッセージを確認してください。 |
| DATA_CREATIVE_INGEST_FAILURE | 422 | クリエイティブ URL が無効です。 詳しくは、エラーメッセージを確認してください。 |
| DATA_CREATIVE_LINK_FAILURE | 422 | クリエイティブは、契約の広告ユニットノードにリンクされませんでした。 詳しくは、エラーメッセージを確認してください。 |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | クリエイティブは更新されませんでした。 詳しくは、エラーメッセージを確認してください。 |
| DATA_DSP_GET_FAILURE | 422 | システム内にDSPが存在しません。 |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | クリエイティブのリンクが広告ユニットから解除されませんでした。 |
| DATA_CREATIVE_FAILURE_DELETE | 422 | クリエイティブは削除されませんでした。 |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | URL が検出されませんでした。 |
| DATA_ENTITY_NOT_FOUND | 422 | クリエイティブが存在しません。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [プログラムで保証された取引の設定の概要 [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [Deal ID インボックスでの契約の承認](deal-id-inbox-accept.md)
>* [プログラム的に保証された契約の広告をに送信する [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [次の広告のステータスの確認 [!DNL FreeWheel] プログラム的に保証された取引](/help/dsp/inventory/freewheel-check-status.md)

