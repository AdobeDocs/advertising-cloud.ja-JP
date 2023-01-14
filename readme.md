---
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---
# Adobe広告のコラボレーションドキュメント

これは、クロスAdobeおよびDSPドキュメントを含む、製品広告のドキュメントリポジトリです。 ( 後で、検索用のドキュメントが含まれ、場合によっては (?) クリエイティブの場合 )

**注意：このページは、お客様向けドキュメントには公開されていません。**

## 目次

+ `TOC.md` ユーザーガイドのルートにあるは、ガイドに含まれるトピックの構成を示します。
+ 各ユーザーガイドには、 `TOC.md`：必要に応じて、すべてのページ/トピックの順序を変更できます。


## ユーザーガイド

+ ユーザーガイドの導入部分は、と呼ばれます。 `overview.md`
+ ユーザーガイドの各トピックには、独自のディレクトリがあります。
   + ガイドの *実装*&#x200B;に設定されている場合、対応するディレクトリは `/implementation`
+ すべての画像アセットは、 `/assets` を設定します。
   + 内のすべての画像 `/assets` ディレクトリがローカライズされます。
   + 画像 `/no-localize` ディレクトリはローカライズされません（当然です。） これを使用すると、loc バージョンで、特定のアセットを不必要に複製しないようにすることができます。

## ユーザーガイドレベルのメタデータ

+ ユーザーガイドを説明するメタデータは、 `TOC.md`. これには以下が含まれます。
   + product — 製品/機能の名前。
   + cloud — この製品が属するクラウド。
   + audience — ガイドをターゲットとするオーディエンスまたはアーキタイプ。
   + user-guide — ユーザーガイドの名前。

## ページレベルのメタデータ

+ ドキュメントの説明に必要なメタデータは、個々のページの一部として保存されます。 これには以下が含まれます。
   + title — ページのタイトル
   + description — ページの説明
   + seo-title - seo 代替タイトル
   + seo-description - SEO 用の代替タイトル
   + short-title — （オプションのフィールド）
   + index - yes/no — ページをAdobeの検索プラットフォームでインデックス付けするかどうか
   + translate - yes/no — このページをローカライズするかどうか
   + beta — この製品がベータ版かどうか。
   + redirect — 必要に応じて、新しいページへの参照を作成するために使用できます
   + doc-type:reference（デフォルト）、troubleshooting、developer、tutorial、kb、whitepaper

## 詳細情報

その他の公開手順、スタイルガイド、サンプルおよびその他のリソースについては、以下を参照してください。

+ [投稿作成者のガイドライン **特にAdobe広告用**](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=EfficientFrontier&amp;title=Contributing+Author+Guidelines+for+Advertising+Cloud+Help)
+ [すべてのオーサリングAdobe](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/home.html)

関連項目：

+ contributing.md ：ドキュメントへの投稿方法の概要。

<!-- * guidelines.md For an overview on what is expected in contributions and how to compose your documentation contributions. -->
+ code-of-conduct.md ：このドキュメントプロジェクトへの投稿時に期待される行動の基準の概要。
