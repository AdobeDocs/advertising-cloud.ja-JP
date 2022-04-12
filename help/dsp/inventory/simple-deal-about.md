---
title: について [!UICONTROL Simple Ad Serving]
description: 詳細 [!UICONTROL Simple Ad Serving] は、イベント追跡ピクセルを使用します。
feature: DSP Simple Ad Serving
exl-id: d65d1d8e-4d10-4d1d-86d3-f4457c29ae8d
source-git-commit: 5a8aaa3fba6cca33915fc9720c78493f98244b61
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# について [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] は、1 つの専用の配置を使用して、指定したパブリッシャーと単一の広告タイプに対して、決定されない保証された広告配信およびレポートを提供します。 用途 [!DNL Simple Ad Serving] パブリッシャーが deal ID を使用して契約を実行できない場合に発生します。 すべてのターゲティング、予算のペーシングと上限、頻度キャップは、投稿者が処理します。 イベント追跡ピクセルを使用して、これらの取引を実行します。

を使用 [!UICONTROL Simple Ad Serving]各広告はパブリッシャー（サイト提供）によって直接提供され、DSPは、ピクセルを実装しDSP広告をトラフィックする必要があるパブリッシャーに送信するイベントトラッキングピクセルを提供します。 インベントリタイプに応じて、イベントピクセルはインプレッション、クリックスルー、ビデオ再生の各イベントを測定します。

次の広告タイプを使用できます。

* desktop standard プリロール
* タブレットおよびモバイル標準プリロール
* 接続された TV 標準プリロール
* 表示
* オーディオ

次の項目を作成できます。 [!UICONTROL Simple Ad Serving] 取り扱う [!UICONTROL Inventory] > [!UICONTROL Deals] 表示 DSPは、サブタイプ「[!DNL Simple ad serving]」を追加しました。 プレースメントは、契約をターゲットにしますが、追加のターゲティング、予算、頻度制限は許可されません。 契約名、CPM、インプレッション、フライト日など、一部の契約設定のみを編集できます。<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] 配置は、アカウントの使用可能な資金、またはキャンペーンとパッケージの予算に従っていません。 ただし、支出は追跡され、その予算に対してカウントされます。 CPM が$0 の場合でも、イベントデータは常に追跡されます。

>[!MORELIKETHIS]
>
>* [の作成 [!UICONTROL Simple Ad Serving] 契約](simple-deal-create.md)
>* [[!UICONTROL Simple Ad Serving] 設定](simple-deal-settings.md)
>* [イベント追跡ピクセルの表示 [!UICONTROL Simple Ad Serving] 契約](simple-deal-show-pixels.md)

