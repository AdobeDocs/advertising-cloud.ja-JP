---
title: DSP Media Exposure データのAdobe Audience Managerへの送信の概要
description: Advertising DSPキャンペーンからAudience Managerイベントピクセルを使用してインプレッションレベルおよびクリックレベルのデータをキャプチャする方法を説明します
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# DSP Media Exposure データのAdobe Audience Managerへの送信の概要

*Advertising DSPのみの広告主*

*Advertising とAdobe Audience ManagerのAdobeの統合のみの広告主*

Adobe Audience Managerを使用した Advertising DSPのお客様は、Audience Managerイベントピクセルを使用して、DSPキャンペーンからインプレッションレベルのデータとクリックレベルのデータをキャプチャできます。 イベントピクセルは、データをアクションにつながるシグナルとしてAudience Managerに送信します。 これらのシグナルにより、より高度なセグメント化、頻度管理、マーケティング分析、レポートインサイトなど、様々なDSPのユースケースが可能になります。

DSPでは、これらのシグナルのAudience Managerへの送信に料金はかかりません。 ただし、サーバーコールに基づいて、Audience Manager契約ごとに標準的なAudience Manager取り込みコストを支払います。 Audience Managerは、2 つの異なる方法で追跡される重複イベントを削除し、各イベントが 1 回のみ課金されるようにします。

>[!NOTE]
>
> Audience Managerは、広告サーバーログファイルからのデータのキャプチャもサポートしているので、柔軟性が低くなります。 このプロセスは、このドキュメントでは扱っていません。

## プライマリの利点

* DSP campaign のデータは、リアルタイムにAudience Managerに送られ、それを使用して、セグメントの定義に使用するルールベースの特性を作成できます。

* セグメントは、ユーザーの特性およびセグメントの認定の直後にターゲティングに使用でき、リアルタイムのターゲティング作業を強化します。

* クリエイティブ全体での頻度キャップ、以前のキャンペーンに触れたリターゲティングユーザー、ダウンストリームサイトの行動やエントリポイントの分析など、キャンペーンデータを活用できます。

* 集計データを使用すると、キャンペーンのパフォーマンスを一元的に把握し、カスタムコンバージョンパスを特定し、Audience Managerを通じてコンバージョンにつながるイベントのシーケンスを改善できます [!DNL Audience Optimization Reports] または、 [[!DNL Audience Analytics] Adobe Analyticsとの統合](/help/integrations/audience-manager/audience-analytics.md).

## データの追跡方法

Audience Managerインプレッションとクリックイベントのピクセルは cookie ベースです。 ピクセルは、モバイルアプリや接続された TV(CTV) など、cookie がない環境で発生するイベントをキャプチャしません。

### Impression-Tracking ピクセル

Audience Managerは、広告に 1xl ピクセルの透過イベントトラッキングピクセルをアタッチした場合に、広告のインプレッションデータを追跡します。 イベントピクセルは、広告がユーザーに提供され、Web ブラウザーによって読み込まれるたびに読み込まれます。 ピクセルは、 [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html):Audience Managerの従来のドメインで、パラメーターをキー値ペアとして含みます。 イベント呼び出しはインプレッションとコンバージョンのデータを収集し、Audience Managerのデータ収集サーバーに送信します。

### クリック追跡ピクセル

Audience Managerは、インプレッションと同様にクリックを追跡しますが、広告が提供されるたびに透明なイベントピクセルを読み込まない点が異なります。 代わりに、クリックデータは広告のクリックスルー URL で追跡されます。 広告は、次のクライアント固有のサブドメインを指します： [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)：ドメインデータ収集サーバーで処理するためのAudience Managerの従来のAudience Managerです。 次に、サーバーは、意図したランディングページにユーザーをリダイレクトします。 この URL には、パラメーターがキー値ペアとして含まれています。

>[!NOTE]
>
>組織が [!DNL Analytics] をトラッキングする場合、Audience Managerクリックの追跡が不要な場合があります。 Adobe Analyticsはクリックシグナルをキャプチャし、を通じてAudience Managerに送信できます。 [サーバー側転送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Advertising DSP Campaigns からクリックおよびインプレッションデータを収集](collect.md)
>* [使用例](use-cases.md)

