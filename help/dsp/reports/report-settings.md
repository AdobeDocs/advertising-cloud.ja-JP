---
title: カスタムレポート設定
description: 「カスタムレポート設定」の説明を参照してください。
feature: DSP Custom Reports
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---


# カスタムレポート設定

**[!UICONTROL Name]** レポート名。最大長は180文字です。

**[!UICONTROL Report Type]** レポートのタイプ： *[!UICONTROL Custom]* （利用可能なオプションの多くを含む）、 *[!UICONTROL Billing]*、 *[!UICONTROL Conversion]*、 *[!UICONTROL Device]*、 *[!UICONTROL Frequency (by Impression)]*、  *[!UICONTROL Frequency (by App/Site)]*、 *[!UICONTROL Geo]*、 *[!UICONTROL Margin]*、 *[!UICONTROL Media Performance]*、  *[!UICONTROL Segment]*、 *[!UICONTROL Site]*。

## [!UICONTROL Apply Filters] セクション

**[!UICONTROL Timezone]:** レポートのタイムゾーン。

**[!UICONTROL Observe Daylight Savings Time]:** 報告された時間に夏時間を考慮します。

**\[日付範囲\]:** データを生成する日付範囲。使用可能な日数は、レポートおよび選択したディメンションによって異なります。 次のいずれかを選択します。

* **[!UICONTROL Previous N days]:** 今日までの特定の日数のデータが含まれます。

* **[!UICONTROL Custom]:** 特定の開始日から終了日までのデータが含まれます。前日までデータをレポートする場合は、「**[!UICONTROL Present]**」を選択します。

* **[!UICONTROL Last Calendar Month]:** 前月のデータが含まれます。

**[!UICONTROL Add Filters]:** （オプション）データをフィルタリングするための追加のディメンション。ディメンションがレポートの列として含まれているかどうかに関わらずです。 *[!UICONTROL Account]*、\*  *[!UICONTROL Advertiser]*、  *[!UICONTROL Campaign]*、  *[!UICONTROL Placement]*、  *[!UICONTROL Ad]*、  *[!UICONTROL Ad Type]*、  *[!UICONTROL Video]*、  *[!UICONTROL Video Duration]*、  *[!UICONTROL Country]*&#x200B;および *[!UICONTROL Package]*。

\* *[!UICONTROL Account]*&#x200B;は、組織が[クロスアカウントレポート](report-about.md#cross-account-reporting)用に設定されている場合にのみ、次のレポートタイプで使用できます。 [!UICONTROL Custom]、[!UICONTROL Site]、[!UICONTROL Segment]、[!UICONTROL Geo]、[!UICONTROL Device]、[!UICONTROL Frequency (by Impression)]、および[!UICONTROL Conversion]です。 クロスAdobeレポートについて詳しくは、アカウントマネージャーにお問い合わせください。

1つ以上のフィルターを適用するには、次の操作を行います。

* ディメンションを選択し、演算子（*equals*&#x200B;または&#x200B;*not equals*）を選択して、適切な値を選択します。 例えば、プリロール広告のデータのみを返すには、「[!UICONTROL Ad Type equals Preroll]」と指定します。
* （オプション）フィルターに条件を追加します。
* （オプション）フィルターを追加し、それぞれに1つ以上の条件を設定します。

## [!UICONTROL Build Your Report] セクション

**[!UICONTROL Select To Add As Report Headers]:**  レポートに含めるデータ列（ヘッダー）。列を追加するには、カテゴリを展開し、列名の横にあるチェックボックスを選択します。 使用できない指標はすべて無効になります。 使用可能なデータカテゴリは次のとおりです。

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] （広告主別に並べ替え）
* [!UICONTROL Custom Goals] （広告主別に並べ替え）

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 列ヘッダーの順序。任意の列をドラッグ&amp;ドロップして順序をカスタマイズできます。

## [!UICONTROL Multi-Touch Conversion Options] セクション

**[!UICONTROL Format]:** レポートを(コンマ区切り値 *[!UICONTROL CSV]* )形式または（タブ区切り値） *[!UICONTROL Tab]* 形式のどちらで生成するか。

**[!UICONTROL Report Headers]:** 列ヘッダーの *[!UICONTROL Include]* どちら *[!UICONTROL Do Not Include]* を使用するか。

**[!UICONTROL Attribution Rule Settings]:** ( [!UICONTROL Custom]列また [!UICONTROL Conversion]は [!UICONTROL Device]列を含むすべての [!UICONTROL Geo]、 [!UICONTROL Segment]、 [!UICONTROL Site] 、 [!UICONTROL Conversion Metrics] 、 [!UICONTROL Custom Goals] およびレポート。Advertising Cloudコンバージョントラッキングのみを使用する広告主)レポート内で、コンバージョンにつながる一連のイベントのコンバージョンデータの属性を設定する方法を説明します。ルール間の違いを比較する場合は、複数のルールを選択できます。

>[!NOTE]
>
>コンバージョンパスには、Advertising Cloud Searchで設定された、広告主のインプレッションまたはクリックルックバックウィンドウ内のインプレッション数とクリック数が含まれます。 コンバージョン属性の間のインプレッション数に対して、クリック数の方が優先されます。 コンバージョンパスのクリックは、アトリビューションルールに基づいてフルクレジットを受け取ります。 インプレッションは、コンバージョンパスでクリックが追跡されない場合にのみクレジットを受け取ります。

* *[!UICONTROL Last Event]:* コンバージョンパスの最後のクリックまたはインプレッションに対するコンバージョンを関連付けます。

* *[!UICONTROL Weight Last More]:* コンバージョンパス内のすべてのイベントにコンバージョンを関連付けますが、最後のイベントに最も重み付けを適用し、前のイベントに対して順次重み付けを減らします。

* *[!UICONTROL Even Distribution]:* コンバージョン属性は、コンバージョンパスの各イベントに等しくなります。

* *[!UICONTROL Weight First More]:* コンバージョンパス内のすべてのイベントにコンバージョンを関連付けますが、最初のイベントに最も重み付けを適用し、次のイベントに対して順次重み付けを小さくします。

* *[!UICONTROL First Event]:* コンバージョンパスの最初のクリックまたはインプレッションにコンバージョンを関連付けます。

* *[!UICONTROL U-shaped]:* コンバージョンパス内のすべてのイベントにコンバージョンを属性付けしますが、最初と最後のイベントに最も重み付けを適用し、コンバージョンパスの途中にあるイベントに対する重み付けを徐々に軽減します。

* *[!UICONTROL Display Only]:*  コンバージョンパスの最後のDSPクリックまたはインプレッションに対するコンバージョンを属性にします。これには、ビデオおよび接続されたテレビ広告が含まれ、Advertising Cloud Search広告のクリックは除外されます。

* *[!UICONTROL Social Only]:* 旧式

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising Cloud](). -->

**[!UICONTROL Paths as Columns]:**  (同じデバイ [!UICONTROL Custom]スで以前のイベントが発生した場合にレポートするコンバージョンのタイ [!UICONTROL Conversion]プ、  [!UICONTROL Device]、  [!UICONTROL Geo]、  [!UICONTROL Segment]、  [!UICONTROL Site]  [!UICONTROL Conversion Metrics]  [!UICONTROL Custom Goals] 列を含むレポート)。最大3つのタイプを含めることができます。 選択したタイプごとに、各コンバージョン指標に対して個別の列が追加され、指定したサフィックス（[!UICONTROL (tl)]、[!UICONTROL (ct)]または[!UICONTROL (vt)]）が付きます。

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* クリック数（クリックスルーのCT）とインプレッション数（ビュースルーのVT）に起因するコンバージョンが含まれます。インプレッションに関連付けられるコンバージョンに、指定したビュースルーの重み付けを掛けます。 デフォルトのビュースルーの重み付けは100%です。つまり、インプレッションに関連するコンバージョンは、クリックに関連するコンバージョンの値の100%としてカウントされます。

* *[!UICONTROL With Clicks (CT)]:* クリック数に起因するコンバージョンのみを含みます。

* *[!UICONTROL Impressions Only (VT)]:* コンバージョンパスでクリックが追跡されなかったので、インプレッションに起因するコンバージョンのみが含まれます。

**[!UICONTROL Cross Device Level]:**  ( [!UICONTROL Custom]列また [!UICONTROL Conversion]は [!UICONTROL Device]列を含むすべての [!UICONTROL Geo]、 [!UICONTROL Segment]、 [!UICONTROL Site] 、 [!UICONTROL Conversion Metrics] 、 [!UICONTROL Custom Goals] およびレポート。（クロスデバイスアトリビューションを持つ広告主のみ）コンバージョンを追跡するレベル。 *[!UICONTROL People]* または *[!UICONTROL Household]*。

[クロスデバイスソリューション](/help/dsp/introduction/features/cross-device-solutions.md)の詳細をご覧ください。

**[!UICONTROL Cross-Device Breakout]:** ( [!UICONTROL Custom]列また [!UICONTROL Conversion]は [!UICONTROL Device]列を含むすべての [!UICONTROL Geo]、 [!UICONTROL Segment]、 [!UICONTROL Site] 、 [!UICONTROL Conversion Metrics] 、 [!UICONTROL Custom Goals] およびレポート。クロスデバイスアトリビューションを持つ広告主のみに適用)レポートに含めるクロスデバイスコンバージョンの詳細レベル。詳細な分類が必要な場合は、最大3つのレベルを選択でき、各レベルを個別の列に含めます。

* *[!UICONTROL Total People (TP)]:* コンバージョンの合計を含みます。これには、同じデバイスでのコンバージョンとクロスデバイスでのコンバージョンの両方が含まれます（該当する場合）。レポートでは、コンバージョン指標名とルールタイプに「[!UICONTROL (tp)]」が追加されます。

* *[!UICONTROL Same Device (SD)]:* 1台のデバイスのみがコンバージョンパスで追跡されたコンバージョンのみが含まれます。レポートでは、コンバージョン指標名とルールタイプに「[!UICONTROL (sd)]」が追加されます。

* *[!UICONTROL Cross Device (XD)]:* コンバージョンパスで複数のデバイスがトラッキングされたコンバージョンのみが含まれます。レポートでは、コンバージョン指標名とルールタイプに「[!UICONTROL (xd)]」が追加されます。

**[!UICONTROL Conversion Reporting Based On]:**  コンバージョンデータのレポート方法：

* *[!UICONTROL Conversion Timestamp]:* （デフォルト）コンバージョンは、コンバージョン日に関連付けられます。

* *[!UICONTROL Event Timestamp]:* 指定したに基づいて、コンバージョンを引き起こしたインプレッションまたはクリックの日付に基づいて、コンバージョンがレポートされま [!UICONTROL Attribution Rule Settings]す。

## [!UICONTROL Add Email Recipients] セクション

**[!UICONTROL Email]:** エラーが原因でレポートがキャンセルされた場合に完了したレポートまたは通知を送信する電子メールアドレス。複数のアドレスを指定する場合は、コンマまたはスペースで区切ります。

**[!UICONTROL Frequency]:** レポートの送信頻度： *[!UICONTROL Once]*、 *[!UICONTROL Daily]*、 *[!UICONTROL Weekly]*&#x200B;または *[!UICONTROL Monthly]*。

## [!UICONTROL Save Report] セクション

**[!UICONTROL Send & Save]:** レポートを送信するタイミング： *[!UICONTROL On Schedule]* または *[!UICONTROL Run Now]*。予定レポートは、アカウントのタイムゾーンで09:00までに配信されます。

>[!NOTE]
>
>[[!UICONTROL Reports]ビューからは、いつでも](report-run-now.md)カスタムレポートを実行できます。

>[!MORELIKETHIS]
>
>* [カスタムレポートについて](/help/dsp/reports/report-about.md)
>* [カスタムレポートの作成](/help/dsp/reports/report-create.md)
>* [カスタムレポートの複製](/help/dsp/reports/report-copy.md)
>* [カスタムレポートの編集](/help/dsp/reports/report-edit.md)
>* [カスタムレポートの実行](/help/dsp/reports/report-run-now.md)
>* [カスタムレポート設定](/help/dsp/reports/report-settings.md)

* [使用可能なレポート列](/help/dsp/reports/report-columns.md)
