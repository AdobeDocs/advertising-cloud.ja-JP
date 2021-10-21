---
title: カスタムレポート設定
description: カスタムレポート設定の説明を参照してください。
feature: DSP Custom Reports
source-git-commit: d2ad7d47d9cf13411fc831526a6fa4ff698b0a15
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---


# カスタムレポート設定

**[!UICONTROL Name]** レポート名。 最大長は 180 文字です。

**[!UICONTROL Report Type]** レポートのタイプ： *[!UICONTROL Custom]* （利用可能な最も多くのオプションを含む） *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]*&#x200B;または *[!UICONTROL Site]*.

## [!UICONTROL Apply Filters] セクション

**[!UICONTROL Timezone]:** レポートのタイムゾーン。

**[!UICONTROL Observe Daylight Savings Time]:** 報告された時間で夏時間を考慮します。

**\[ 日付範囲\]:** データを生成する日付範囲。 使用できる日数は、レポートおよび選択したディメンションによって異なります。 次のいずれかを選択します。

* **[!UICONTROL Previous N days]:** 今日までの特定の日数のデータが含まれます。

* **[!UICONTROL Custom]:** 特定の開始日と終了日の間のデータが含まれます。 前日までのデータをレポートするには、 **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** 前月のデータが含まれます。

**[!UICONTROL Add Filters]:** （オプション）ディメンションがレポートの列として含まれているかどうかに関係なく、データをフィルタリングする追加のディメンション： *[!UICONTROL Account]*,\* *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Placement]*, *[!UICONTROL Ad]*, *[!UICONTROL Ad Type]*, *[!UICONTROL Video]*, *[!UICONTROL Video Duration]*, *[!UICONTROL Country]*&#x200B;および *[!UICONTROL Package]*.

\* *[!UICONTROL Account]* は、組織が [クロスアカウントレポート](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]および [!UICONTROL Conversion]. お問い合わせ [!DNL Adobe] アカウントマネージャーを参照してください。

1 つ以上のフィルターを適用するには、次の手順を実行します。

* ディメンションを選択し、演算子 (*次と等しい* または *等しくない*) をクリックして、適切な値を選択します。 例えば、プリロール広告のデータのみを返すには、[!UICONTROL Ad Type equals Preroll].」
* （オプション）フィルターに条件を追加します。
* （オプション）フィルターを追加し、それぞれに 1 つ以上の条件を設定します。

## [!UICONTROL Build Your Report] セクション

**[!UICONTROL Select To Add As Report Headers]:**  レポートに含めるデータ列（ヘッダー）。 列を追加するには、カテゴリを展開し、列名の横にあるチェックボックスを選択します。 使用できない指標はすべて無効になります。 使用できるデータカテゴリは次のとおりです。

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] （広告主別に並べ替え）
* [!UICONTROL Custom Goals] （広告主別に並べ替え）

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 列ヘッダーの順序。 任意の列をドラッグ&amp;ドロップして順序をカスタマイズできます。

## [!UICONTROL Multi-Touch Conversion Options] セクション

**[!UICONTROL Format]:** でレポートを生成するかどうか *[!UICONTROL CSV]* （コンマ区切り値）または *[!UICONTROL Tab]* （タブ区切り値）形式

**[!UICONTROL Report Headers]:** 対象 *[!UICONTROL Include]* または *[!UICONTROL Do Not Include]* 列ヘッダー。

**[!UICONTROL Attribution Rule Settings]:** ( すべて [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]および [!UICONTROL Site] レポート [!UICONTROL Conversion Metrics] または [!UICONTROL Custom Goals] 列；Advertising Cloudコンバージョントラッキングのみを使用する広告主 ) レポート内で、コンバージョンにつながる一連のイベントのコンバージョンデータの属性を設定する方法を説明します。 ルール間の違いを比較する場合は、複数のルールを選択できます。

>[!NOTE]
>
>コンバージョンパスには、Advertising Cloud Searchで設定された、広告主のインプレッションまたはクリックルックバックウィンドウ内のインプレッション数とクリック数が含まれます。 コンバージョン属性の間のインプレッション数よりも、クリック数の方が優先されます。 コンバージョンパス内のクリックは、アトリビューションルールに基づいてフルクレジットを受け取ります。 インプレッション数は、コンバージョンパスでクリック数が追跡されていない場合にのみクレジットを受け取ります。

* *[!UICONTROL Last Event]:* コンバージョンパスの最後のクリックまたはインプレッションにコンバージョンを関連付けます。

* *[!UICONTROL Weight Last More]:* コンバージョンパス内のすべてのイベントに対するコンバージョンを属性付けます。ただし、最後のイベントに対する重み付けが最も大きくなり、前のイベントに対する重み付けが連続的に小さくなります。

* *[!UICONTROL Even Distribution]:* コンバージョンの属性は、コンバージョンパスの各イベントに等しくなります。

* *[!UICONTROL Weight First More]:* コンバージョンパス内のすべてのイベントに対するコンバージョンを属性付けますが、最初のイベントに対する重み付けが最も大きく、次のイベントに対する重み付けが連続的に小さくなります。

* *[!UICONTROL First Event]:* コンバージョンパスの最初のクリックまたはインプレッションにコンバージョンを関連付けます。

* *[!UICONTROL U-shaped]:* コンバージョンパス内のすべてのイベントにコンバージョンをアトリビュートしますが、最初と最後のイベントに最も重みを付け、コンバージョンパスの途中にあるイベントに対する重みを徐々に減らします。

* *[!UICONTROL Display Only]:*  コンバージョンパスの最後のDSPクリックまたはインプレッションにコンバージョンを関連付けます。 これには、ビデオおよび接続されたテレビ広告が含まれ、Advertising Cloud Search広告のクリックは除外されます。

* *[!UICONTROL Social Only]:* 旧式

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising Cloud](). -->

**[!UICONTROL Paths as Columns]:**  ( すべて [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]および [!UICONTROL Site] レポート [!UICONTROL Conversion Metrics] または [!UICONTROL Custom Goals] 列 ) 同じデバイスで以前のイベントが発生した場合にレポートするコンバージョンのタイプ。 最大 3 つのタイプを含めることができます。 選択したタイプごとに、各コンバージョン指標に対して個別の列が追加され、指定したサフィックス ([!UICONTROL (tl)], [!UICONTROL (ct)]または [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* クリック数（クリックスルーの CT）とインプレッション数（ビュースルーの VT）に起因するコンバージョンが含まれます。 インプレッションに起因するコンバージョンに、指定したビュースルーの重み付けを掛けます。 デフォルトのビュースルーの重み付けは 100%です。つまり、インプレッションに関連するコンバージョンは、クリックに関連するコンバージョンの値の 100%としてカウントされます。

* *[!UICONTROL With Clicks (CT)]:* クリックに起因するコンバージョンのみを含みます。

* *[!UICONTROL Impressions Only (VT)]:* コンバージョンパスでクリックが追跡されなかったので、インプレッションに起因するコンバージョンのみが含まれます。

**[!UICONTROL Cross Device Level]:**  ( すべて [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]および [!UICONTROL Site] レポート [!UICONTROL Conversion Metrics] または [!UICONTROL Custom Goals] 列；（クロスデバイスアトリビューションを持つ広告主のみ）コンバージョンを追跡するレベル。 *[!UICONTROL People]* または *[!UICONTROL Household]*.

詳細情報 [クロスデバイスソリューション](/help/dsp/introduction/features/cross-device-solutions.md).

**[!UICONTROL Cross-Device Breakout]:** ( すべて [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]および [!UICONTROL Site] レポート [!UICONTROL Conversion Metrics] または [!UICONTROL Custom Goals] 列；適用できるのは、クロスデバイスアトリビューションを持つ広告主のみ ) レポートに含めるクロスデバイスコンバージョンの詳細。 詳細な分類を行う場合は、最大 3 つのレベルを選択し、各レベルを個別の列に含めます。

* *[!UICONTROL Total People (TP)]:* コンバージョンの合計を含みます。これには、同じデバイスのコンバージョンとクロスデバイスのコンバージョン（該当する場合）の両方が含まれます。 レポートで、「[!UICONTROL (tp)]「 」がコンバージョン指標名とルールタイプに追加されます。

* *[!UICONTROL Same Device (SD)]:* コンバージョンパスで 1 台のデバイスのみがトラッキングされたコンバージョンのみが含まれます。 レポートで、「[!UICONTROL (sd)]「 」がコンバージョン指標名とルールタイプに追加されます。

* *[!UICONTROL Cross Device (XD)]:* コンバージョンパスで複数のデバイスが追跡されたコンバージョンのみが含まれます。 レポートで、「[!UICONTROL (xd)]「 」がコンバージョン指標名とルールタイプに追加されます。

**[!UICONTROL Conversion Reporting Based On]:**  コンバージョンデータのレポート方法：

* *[!UICONTROL Conversion Timestamp]:* （デフォルト）コンバージョンは、コンバージョン日に関連付けられます。

* *[!UICONTROL Event Timestamp]:* コンバージョンは、指定した [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Email Recipients] セクション

**[!UICONTROL Email]:** エラーが原因でレポートがキャンセルされた場合に、完了したレポートまたは通知を送信する電子メールアドレス。 複数のアドレスを指定する場合は、コンマまたはスペースで区切ります。

**[!UICONTROL Frequency]:** レポートの送信頻度： *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*&#x200B;または *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] セクション

**[!UICONTROL Send & Save]:** レポートを送信するタイミング： *[!UICONTROL On Schedule]* または *[!UICONTROL Run Now]*. 予定レポートは、アカウントのタイムゾーンで 09:00 までに配信されます。

>[!NOTE]
>
>次の操作が可能です。 [いつでもカスタムレポートを実行する](report-run-now.md) から [!UICONTROL Reports] 表示

>[!MORELIKETHIS]
>
>* [カスタムレポートについて](/help/dsp/reports/report-about.md)
>* [カスタムレポートの作成](/help/dsp/reports/report-create.md)
>* [カスタムレポートの複製](/help/dsp/reports/report-copy.md)
>* [カスタムレポートの編集](/help/dsp/reports/report-edit.md)
>* [カスタムレポートの実行](/help/dsp/reports/report-run-now.md)
>* [カスタムレポート設定](/help/dsp/reports/report-settings.md)

* [使用可能なレポート列](/help/dsp/reports/report-columns.md)
