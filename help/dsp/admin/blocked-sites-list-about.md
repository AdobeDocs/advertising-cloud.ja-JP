---
type: Documentation
cloud: Experience Cloud
solution: Advertising Cloud
product: advertising cloud
title: アカウントレベルおよび広告主レベルのブロック済みサイトリストについて
description: アカウントレベルおよび広告主レベルのブロック済みサイトリストについて
source-git-commit: ac35677ef4832177b7a7e735bbbbf24454371496
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# アカウントレベルおよび広告主レベルのブロック済みサイトリストについて

<!-- Can you just add domains for your acct profile or advertiser to which you have access? It doesn't look like you can remove or edit any existing domains. Or can you with a specific syntax? -->

<!-- For domains, sub-domains,...? Specify what is valid. -->
Advertising Cloudアカウント全体に使用されるブロックされたサイトリストと、アカウント内の個々の広告主用の追加リストを編集できます。

ブロックされたサイトリストは、配置に除外するターゲットのセットを定義します。 各リストは、トップレベルの Web サイトドメインと任意のレベルで構成できます <!--- verify --> サブドメイン（example.com、my.example.com、my.new.example.com など）およびモバイルアプリ名 (???など )<!-- package names/app IDs, the full URL in Google Play/iTunes? Specify what is valid. -->.

広告主レベルのリストは、アカウントレベルのリストを上書きします。

>[!NOTE]
>
>* アカウントレベルおよび広告主レベルのブロックサイトリストは、Advertising Cloud DSP [グローバルブロックサイトリスト](/help/dsp/introduction/features/brand-safety-media-quality.md)：広告で安全でないと見なされるサイトを含みます。
>* また、ユーザーは任意のプレースメントにターゲットサイトを追加できます。
>* ブロックされたサイトリストは、常にターゲットサイトリストを上書きします。 配置が広告の同じターゲットを除外して含む場合、そのターゲットは除外されます。 <!-- Verify -->


>[!MORELIKETHIS]
<!--
>* [Edit an Account-level or Advertiser-level Blocked Site List](/help/dsp/admin/blocked-sites-list-edit.md)
[Brand Safety and Media Quality](/help/dsp/introduction/features/brand-safety-media-quality.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
-->
