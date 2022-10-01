---
title: オーディエンスセグメントロジックの構文
description: オーディエンスセグメントのロジックを定義する際に使用できる構文を参照します。
feature: DSP Audiences
exl-id: 3a51b1b5-1eef-453b-9be5-0694e27491a8
source-git-commit: efd04189de975f8f075dec7851a3a06d2d647ded
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# オーディエンスセグメントロジックの構文

再利用可能なオーディエンスを作成する場合、英数字のセグメント ID（キー）と次の構文を使用して、セグメントロジックを手動で定義できます。

* ()：グループを示します。
* `||` 対象 [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; for [!DNL AND]
* ! 対象 [!DNL NOT] （除外）

>[!NOTE]
>
>* 指定したセグメントグループは、前にが付いていない限り、すべて含まれます。 （これらを除く）。
>* 以下が可能です。 [オーディエンスのセグメント ID を見つける](reusable-audience-clipboard.md) から [!UICONTROL Audiences] > [!UICONTROL All audiences].


例えば、次のロジックがあるとします。

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

（平易な英語で）を意味する

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>配置設定では、保存したオーディエンスをオーディエンスとして使用して、明示的にターゲティングするか、別のオーディエンスとして使用して、ターゲティングから除外することができます。 セグメントのロジックに、オーディエンスを使用する目的が反映されていることを確認します。

>[!MORELIKETHIS]
>
>* [再利用可能なオーディエンスのセグメントキーをクリップボードにコピーする](reusable-audience-clipboard.md)
>* [Audience Management について](audience-about.md)
>* [再利用可能なオーディエンスを作成](reusable-audience-create.md)
>* [オーディエンス設定](audience-settings.md)
>* [利用可能なサードパーティデータプロバイダー](third-party-data-providers.md)

