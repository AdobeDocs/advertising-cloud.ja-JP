---
title: ' [!DNL FreeWheel] 広告送信のエラーコード'
description: ' [!DNL FreeWheel]への広告送信に対して返されるエラーコードを参照します。'
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 2%

---

# [!DNL FreeWheel]広告送信のエラーコード

失敗した広告送信のエラーメッセージは、Advertising Cloud DSPまたは[!DNL FreeWheel]のどちらかから送信された可能性があります。 エラーメッセージは、[[!UICONTROL Freewheel Status]ダイアログ](freewheel-check-status.md)の[!UICONTROL API Response]列に表示されます。

## Advertising Cloud DSP内部エラー

| エラーメッセージ | 説明 | 次の手順 |
|--- |--- |--- |
| [!DNL [!DNL FreeWheel]からのステータス応答待ち] | [!DNL FreeWheel] は、送信が成功したか失敗したという応答をまだ返していません。 | 10分後にもう一度ステータスを確認します。 |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] では、時計番号が割り当てられていない英国の広告を受け付けません。 | 広告に時計番号を割り当て、広告を再送信します。 |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | 広告の送信を試みた際に、トランスコーダーが広告のトランスコードを完了していませんでした。 | 10分待ってから、広告を再送信してください。 |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | 提出された取引は、プログラム的に保証された取引として設定されていません。 [!DNL FreeWheel] は、保証された契約のみを受け入れます。 | プログラムで保証された取引として、取引IDを設定します。 Deal IDワークフローの終了時に、プログラムで保証されたデフォルトの配置を保存すると、広告は自動的に[!DNL FreeWheel]に送信されます。 |
| [!DNL Invalid external_deal_id:] \&lt;deal_id> | 送信された取引IDは、存在しないか、Adobe終了時にアクティブではありません。 | 取引がアクティブであることを確認し、広告を再送信します。 |
| [!DNL \[public_id=]\&lt;deal>]が存在しません | 送信されたディールIDが[!DNL FreeWheel]の最後に存在しません。 | [!DNL FreeWheel]担当者に問い合わせて、取引IDを確認してください。 |
| [!DNL Ad with identifier] \&lt;>ad name *\>  [!DNL was not found.]* | 送信された広告キーは、存在しないか、Adobe終了時にアクティブではありません。 | 正しい広告キーを見つけて、広告を再送信してください。 |
| [!DNL Pending Submission] | 送信は保留中です。 | ページを更新します。 |

{style=&quot;table-layout:auto&quot;}

## FreeWheel APIエラー

| コード | 意味 | 説明 | 次の手順 |
|--- |--- |--- |--- |
| 401 | 未認証 | アクセス資格情報が正しくない、見つからない、または無効です。 | 担当のAdobeアカウントマネージャーにお問い合わせください。 |
| 403 | 禁止 | サーバーは要求を理解しましたが、承認を拒否しました。 | 担当のAdobeアカウントマネージャーにお問い合わせください。 |
| 404 | 見つかりません | 要求したリソースは使用できません。 クリエイティブIDがPUT操作で見つからない場合は、404が返されます。 | 担当のAdobeアカウントマネージャーにお問い合わせください。 |
| 405 | メソッドが許可されていません | リクエストが、そのリソースでサポートされていないリクエストメソッドを使用してリソースから作成されました(例えば、POSTからGETを送信する必要があるメソッドのデータを使用する、読み取り専用リソースのPUTを使用する)。 | 担当のAdobeアカウントマネージャーにお問い合わせください。 |
| 408 | 要求タイムアウト | この要求の処理中にタイムアウトが発生しました。 タイムアウトは、通常、特定のリソースに対する排他的アクセスの同時要求によって発生します。 | このステータスを受け取ったら、要求を再送信します。 問題が解決しない場合は、担当のAdobeアカウントマネージャーにお問い合わせください。 |
| 422 | 処理不可なエンティティ | リソースが無効です。 このエラーは、リクエスト本文が無効な場合、または作成/更新されたリソースが無効な場合（例えば、Deal IDが見つからなかった場合）に発生します。 詳しくは、[FreeWheel API 422 Errors](#freewheel-422-errors)を参照してください。 | 担当のAdobeアカウントマネージャーにお問い合わせください。 |
| 500 | 内部サーバーエラー | APIシステムエラー。 | 担当のAdobeアカウントマネージャーにお問い合わせください。 |

{style=&quot;table-layout:auto&quot;}

## FreeWheel API 422エラー {#freewheel-422-errors}

| コード | HTTPコード | 説明 |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | 要求データは無効なJSON形式です。 詳しくは、エラーメッセージを確認してください。 |
| DATA_VALIDATION_FAILURE | 422 | 要求データに必須フィールドがないか、無効なデータ型が含まれています。 詳しくは、エラーメッセージを確認してください。 |
| DATA_DEAL_INVALID | 422 | 取引の設定が正しくないか、存在しません。 詳しくは、エラーメッセージを確認してください。 |
| DATA_DEAL_GET_FAILURE | 422 | 取引が見つからなかったか、その設定に問題がある。 詳しくは、エラーメッセージを確認してください。 |
| DATA_CREATIVE_INGEST_FAILURE | 422 | クリエイティブURLが無効です。 詳しくは、エラーメッセージを確認してください。 |
| DATA_CREATIVE_LINK_FAILURE | 422 | クリエイティブは、ディールの広告ユニットノードにリンクされませんでした。 詳しくは、エラーメッセージを確認してください。 |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | クリエイティブは更新されませんでした。 詳しくは、エラーメッセージを確認してください。 |
| DATA_DSP_GET_FAILURE | 422 | システム内にDSPが存在しません。 |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | クリエイティブは広告ユニットとのリンクを解除されませんでした。 |
| DATA_CREATIVE_FAILURE_DELETE_失敗 | 422 | クリエイティブは削除されませんでした。 |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | URLが検出されませんでした。 |
| DATA_ENTITY_NOT_FOUND | 422 | クリエイティブが存在しません。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [FreeWheelでのプログラム保証取引の設定の概要](/help/dsp/inventory/freewheel-overview.md)
>* [Deal IDインボックスでのDealの承認](deal-id-inbox-accept.md)
>* [プログラムで保証された契約の広告をFreeWheelに送信](/help/dsp/inventory/freewheel-submit.md)
>* [プログラムで保証された取引の広 [!DNL FreeWheel] 告のステータスの確認](/help/dsp/inventory/freewheel-check-status.md)

