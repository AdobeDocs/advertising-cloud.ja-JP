---
title: の使用 [!DNL Last Event Service] を使用した JavaScript ライブラリ [!DNL Web SDK]
description: を使用してから切り替える手順を説明します。 [!DNL Analytics] [!DNL visitorAPI] library to the [!DNL Experience Platform] [!DNL Web SDK] library for your [!DNL Analytics for Advertising Cloud] 実装。
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 966a7d64c0a2c1ce6d26ff25f6a57384e527625a
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# の使用 [!DNL Last Event Service] Adobe Experience Platformを使用した JavaScript ライブラリ [!DNL Web SDK]

*Advertising CloudとAdobe Analyticsの統合のみの広告主*

組織が従来のAdobe Analytics `visitorAPI.js` データ収集用のライブラリでは、オプションで [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) ライブラリ (`alloy.js`) を使用して、 [!DNL Edge Network].

この [!DNL Analytics for Advertising Cloud] [!DNL Last Event Service] JavaScript ライブラリは、そのまま、追加の ID(`SDID`) をクリックします。 この [!DNL Web SDK] ただし、ライブラリでは [!DNL stitch ID]. 次の手順で [!DNL Web SDK] 対象 [!DNL Analytics for Advertising Cloud](1) [!DNL Last Event Service] のタグを Web ページで使用し、2) を使用して [!DNL Web SDK] `sendEvent` 適切なコマンド

## 手順 1:を編集 [!DNL Last Event Service] タグを生成して `[!DNL StitchID]`

内 [!DNL Analytics for Advertising Cloud] [!DNL Last Event Service] タグを追加して、 `[!DNL StitchID]` ライブラリにバンドルされているランダム ID ジェネレーターを使用する。

**レガシータグ：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**新しいタグ：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

## 手順 2:用途 [!DNL Web SDK] を [!DNL StitchID] を XDM データとして使用 [!DNL Analytics]

次のプロパティを [!DNL Web SDK] `sendEvent` コマンドを使用して [!DNL StitchID] から [!DNL Experience Edge] as [!DNL Experience Data Model] (XDM) データ [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] は値を `SDID`.

**追加するプロパティ：**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**例：**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [用 JavaScript コード [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/javascript.md)

