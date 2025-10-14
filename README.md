---
source-git-commit: e09480184d8d0507ec730f1e3a87c665124c173a
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 33%

---
# 記事への投稿

アドビのコミュニティだけでなく、ドキュメントチーム以外のアドビ従業員からの投稿も歓迎します。

## アドビオープンソース行動規範

このプロジェクトでは、[アドビオープンソース行動規範](code-of-conduct.md)または [.NET Foundation 行動規範](https://dotnetfoundation.org/code-of-conduct)を採用しています。詳しくは、[投稿](contributing.md)の記事を参照してください。

## Adobe コンテンツへの投稿方法

**Adobeの従業員でない場合は** 外部のコミュニティ投稿を送信できます。 コミュニティの投稿は社内システムにインポートされ、編集されてパブリックリポジトリにマージされます。 その後、公開リポジトリが最新の変更と同期され、非公開リポジトリに結合されます。

**Adobeの従業員の場合**、非公開の [Adobe GitHub リポジトリに直接投稿できます &#x200B;](https://git.corp.adobe.com/AdobeDocs/)。 詳しくは、Adobeの社員向けの Adobe Experience League オーサリングガイドを参照してください。

## 外部寄稿者

### 小規模な変更

マイナーアップデートに参加している場合：

1. 編集するトピックに移動します。
1. 「このコンテンツは役に立ちましたか？」 ブラウザーウィンドウの下部に表示されるバナーで、「**詳細フィードバックオプション**」をクリックします。
1. 「**編集の提案**」をクリックし、GitHub UI で変更内容を含むプルリクエスト（PR）を送信します。

   一般的な [Adobe ドキュメント投稿者ガイド &#x200B;](https://experienceleague.adobe.com/docs/contributor/contributor-guide/introduction.html?lang=ja) を参照してください。

このリポジトリのドキュメントやコード例に対して送信する小規模な修正や説明には、アドビの利用条件が適用されます。

### コミュニティからの大きな変更または新しいトピック

Adobe コミュニティのメンバーが新しいトピックを作成したり、大きな変更をコントリビューションしたりする場合は、該当する Git リポジトリーの「**イシュー**」タブを使用してイシューを送信し、ドキュメントチームとのやり取りを開始します。 計画が合意されたら、Adobe ライターと協力してリビジョンを公開します。

**メモ：** ドキュメントおよびコード例に大幅な変更を加えたプルリクエストを送信すると、プルリクエストにオンライン貢献使用許諾契約（CLA）を送信するように求めるメッセージが表示されます。 プルリクエストを確認する前に、オンラインフォームに記入する必要があります。

### ツール

コミュニティの寄稿者は、基本的な編集に GitHub UI を使用したり、リポジトリをフォークして大規模な投稿を行ったりすることができます。

詳しくは、[アドビドキュメントの寄稿者ガイド](https://experienceleague.adobe.com/docs/contributor/contributor-guide/introduction.html?lang=ja)を参照してください。

## 内部寄稿者

Adobe Experience Cloud ソリューションの製品チームのテクニカルライター、プログラムマネージャー、または開発者で技術記事の投稿または作成を担当している場合は、[&#x200B; プライベートリポジトリ &#x200B;](https://git.corp.adobe.com/AdobeDocs) を使用します。

## トピックの書式設定

このリポジトリ内の記事はすべて、GitHub 固有の Markdown を使用しています。 Markdown について詳しくは、以下を参照してください。

* [Markdown の基本 &#x200B;](https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/)
* [&#x200B; 印刷用 Markdown チートシート &#x200B;](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)

## ラベル

パブリックリポジトリでは、プルリクエストのワークフローを管理し、プルリクエストの状況を通知するために、プルリクエストに次の自動ラベルが割り当てられます。

* **変更を作成者に送信**：作者に保留中のプルリクエストが通知されました。
* **結合準備完了**：プルリクエストレビューチームによるレビューの準備が整いました。
