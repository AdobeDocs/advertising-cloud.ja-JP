---
source-git-commit: d3e36cef27fce533e9435717d428d54b982fd427
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---
# Advertising Cloudのコラボレーションドキュメント

これは、Adobe Advertising Cloudのドキュメントリポジトリで、クロス製品、DSP、TVドキュメントを含みます。 （後で、クリエイティブおよび検索に関するドキュメントが含まれます）。

**注意：このページは、お客様向けドキュメントには公開されていません。**

## 目次

+ `TOC.md` 任意のユーザーガイドのルートに、ガイドに含まれるトピックの構成を指定します。
+ 各ユーザーガイドには固有の`TOC.md`があり、必要に応じてすべてのページ/トピックを並べ替えることができます。


## ユーザーガイド

+ ユーザーガイドの導入部分は、`overview.md`と呼ばれます。
+ ユーザーガイドの各トピックには、独自のディレクトリがあります。
   + *Implementation*&#x200B;という名前のトピックがガイドにある場合、対応するディレクトリは`/implementation`です。
+ すべての画像アセットは、ユーザーガイドのルートの`/assets`に保存されます。
   + `/assets`ディレクトリ内の画像はすべてローカライズされます。
   + `/no-localize`ディレクトリ内の画像はローカライズされません（当然です！）。 これを使用すると、locバージョンで、特定のアセットが不必要に再現されないようにすることができます。

## ユーザーガイドレベルのメタデータ

+ `TOC.md`には、ユーザーガイドを説明するメタデータが格納されています。 これには、以下が含まれます。
   + product — 製品/機能の名前。
   + cloud — この製品が属するクラウド。
   + audience — ガイドのターゲットとなるオーディエンスまたはアーキタイプ。
   + user-guide — ユーザーガイドの名前。

## ページレベルのメタデータ

+ ドキュメントを説明するために必要なメタデータは、個々のページの一部として保存されます。 これには、以下が含まれます。
   + title — ページのタイトル
   + description — ページの説明
   + seo-title - seo代替タイトル
   + seo-description - SEO用の代替タイトル
   + short-title — （オプションのフィールド）
   + index - yes/no — ページをAdobeの検索プラットフォームでインデックス付けするかどうか
   + translate - yes/no — このページがローカライズされるかどうか
   + beta — この製品がベータ版かどうか。
   + redirect — 必要に応じて、新しいページへの参照を作成するために使用できます。
   + doc-type:リファレンス（デフォルト）/トラブルシューティング/開発者/チュートリアル/kb/ホワイトペーパー

## 詳細情報

詳細な公開手順、スタイルガイド、サンプルおよびその他のリソースについては、以下を参照してください。

+ [特にAdvertising Cloud向けの投稿作成者 **のガイドライン**](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=EfficientFrontier&amp;title=Contributing+Author+Guidelines+for+Advertising+Cloud+Help)
+ [すべてのオーサリングAdobe](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/home.html)

関連トピック：

+ contributing.md ：ドキュメントへの投稿方法の概要。

<!-- * guidelines.md For an overview on what is expected in contributions and how to compose your documentation contributions. -->
+ code-of-conduct.md ：このドキュメントプロジェクトへの投稿時に期待される行動の標準の概要。
