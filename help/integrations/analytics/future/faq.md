---
title: よくある質問
description: xxx
source-git-commit: 5dfc4e8f2e6d2532e40eb4da8748fec0ed096e71
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# FAQs xxx

## タイトル

https://adobeadcloud.zendesk.com/agent/tickets/14214デフォルトでは、Adobe Analyticsは、すべてのレポートでキャプチャされたイベントをすべてレポートします。 &quot;[!UICONTROL Unspecified]「 」イベントは、Advertising Cloudに接続されなかったフォーム完了イベントを表します。 例えば、広告プラットフォームレポートでは、電子メールキャンペーンによって駆動されるオーガニックコンバージョンやコンバージョンは、「未指定」に分類されます。

このフィルターを使用して、「未指定（なし）を含む」オプションのチェックマークを外すことで、未指定のイベントをレポートから削除できます。 <!-- Not sure if this is in DSP or in Analytics Workspace -->

## タイトル

https://adobeadcloud.zendesk.com/agent/tickets/24323 Analytics のイベントタグは、Ad Cloudのピクセルと同じ場所に配置し、XXX が一致するようにします。

## タイトル

https://adobeadcloud.zendesk.com/agent/tickets/24323

Q:内部セキュリティ監査では、Ad Cloudを既存のAdobe Analyticsインストールに統合した際に有効にしたセキュリティ上の問題として、一部の機能がフラグ付けされました。

問題となる統合は、AdCloud とAdobe Audience Managerの間のものです。 この機能は、AdCloud とAdobe Audience Managerの間の訪問者 ID の一致率を高めます。 これをおこなうには、ネットワークリクエストを pagead.l.doubleclick.net、star-mini.c10r.facebook.com およびpug88000nf.pubmatic.com に送信して、利用可能な訪問者の既存の ID がこれらのサービスに含まれているかどうかを判断します。 セキュリティリスクとしてフラグ付けされ、すべてのサイト訪問者に対して発生しているネットワーク要求です。

Auditor から、この機能を無効にするよう求められています。 これらのネットワーク要求をブロックするとどうなりますか？

回答：当社の製品で確認し、問題のピクセルはAd Cloud、(DSPに関して ) 特定の在庫/SSP パートナー、およびAAM間の cookie の一致率を高める目的であると述べました。  削除された場合、AAC/AAMと各ピクセルが対象とする在庫パートナーとの間のマッチ率がある程度低下することがありますが、相当なものではないと考えられます。

Ad Cloud Search の場合、IMS Org が Mathworks 用に設定されていますが、Ad Cloudでオーディエンスをアクティブ化するための Mathworks 設定が製品チームに表示されません。 Ad Cloud検索にオーディエンスをAdobeAudience Manager を使用して送信している場合。 そうでない場合、これらを削除しても、現在のワークフローには影響しません。 これらのピクセルを起動したくない場合、AAMカスタマーケアは、これらのピクセルの削除に役立ちます。

