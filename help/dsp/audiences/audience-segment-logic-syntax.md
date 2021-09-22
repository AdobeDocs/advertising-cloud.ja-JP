---
title: オーディエンスセグメントロジックの構文
description: オーディエンスセグメントのロジックを定義するために使用できる構文を参照します。
feature: DSP Audiences
exl-id: 3a51b1b5-1eef-453b-9be5-0694e27491a8
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# オーディエンスセグメントロジックの構文

再利用可能なオーディエンスを作成する場合は、英数字のセグメントIDと次の構文を使用して、セグメントロジックを手動で定義できます。

* ()をクリックして、グループを指定します。
* `||` for  [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; for [!DNL AND]
* ! [!DNL NOT] （除外）

>[!NOTE]
>
>* 前にが付いていない限り、指定されたすべてのセグメントグループが含まれます。 （これらを除く）。


例えば、次のロジックがあります。

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

（平易な英語で）を意味する

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>配置設定では、保存したオーディエンスをオーディエンスとして使用して明示的にターゲット設定をおこなうか、ターゲティングから除外する個別のオーディエンスとして使用できます。 セグメントのロジックに、オーディエンスを使用する目的が反映されていることを確認します。

>[!MORELIKETHIS]
>
>* [Audience Managementについて](audience-about.md)
>* [再利用可能なオーディエンスの作成](reusable-audience-create.md)
>* [オーディエンス設定](audience-settings.md)
>* [使用可能なサードパーティデータプロバイダー](third-party-data-providers.md)

