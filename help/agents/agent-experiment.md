---
title: Experimentation Agent
description: Experimentation Agentの使用方法を学ぶ
source-git-commit: 5694f15d82081eed8e762fea8aabc3da1e265b04
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 3%

---

# Experimentation Agent

>[!AVAILABILITY]
>
>Experimentation Agentは、Journey Optimizer Experimentation Acceleratorの有料ライセンスを購入したお客様が利用でき、Adobe TargetまたはAdobe Journey Optimizerとシームレスに統合されます。
>
>[&#x200B; 詳しくは、Journey Optimizer Experimentation Acceleratorを参照してください &#x200B;](https://experienceleague.adobe.com/ja/docs/experimentation-accelerator/using/overview)

## 概要

**0&rbrace;Experimentation Agent&rbrace; は、Web サイト、メール、プッシュメッセージおよびアプリケーションをまたいでデジタル実験を実行および管理する方法を最新化する、AI を活用したツールです。** Adobe Experience Platform AI プラットフォームと実験ツール上に構築された **Experimentation Agent** は、実験をより効率的に実行し、ビジネス目標を整理し、実用的なインサイトを生み出し、うまくいったこと、うまくいかなかったこと、次に実験する場所を強調表示するのに役立ちます。

Experimentation Agentの機能を完全に使用するには、次の権限が必要です。

* **実験を表示**：この権限を持つユーザーは、Experimentation Agentを使用して AI アシスタントで実験に関するインサイトを直接表示できます。

* **実験メタデータを管理**：この権限を持つユーザーは、Experimentation Agentを使用して AI アシスタントで新しい実験を直接作成できます。

➡️ [&#x200B; 詳しくは、Journey Optimizer Experimentation Accelerator ドキュメントを参照してください &#x200B;](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-access)

Experimentation Accelerator機能の一部として、エージェントは次の機能を提供します。

* **パフォーマンス**：実験で何が起こったかの明確なビュー

* **インサイト**：結果が発生した理由の説明

* **機会**：次に取るべき行動に関するガイダンス

![Experimentation Agentのサンプル &#x200B;](./images/experiment/experiment-agent.png)

## ユースケース

Experimentation Agentは、結果を分析し、コンテンツを解釈し、次のステップを提案することで、実験ワークフローの各フェーズを強化します。

その機能は、次の 5 つの主要な機能にグループ化できます。

* **実験の要約**

  実験結果の明確な非技術的な概要を関係者に提供する。

* **コンテンツ分析**

  処理のメッセージやクリエイティブな要素を調べて、特定の処理が他の処理よりも優れている理由を理解します。

* **属性の識別**

  テーマ、トーン、形式などの主要な属性に基づいて処理を分類し、それらの属性をコンバージョン結果に結び付けます。

* **レコメンデーションの生成**

  以前の実験からのインサイトに基づいて、テストする新しい処理や調整を提案します。

* **商談**

  より広い領域や新しい角度を特定し、未開発の可能性を明らかにします。

## 範囲内および範囲外の機能

### **範囲内**

現在、次の機能がサポートされています。

* パフォーマンス
* Insights
* 機会

### **範囲外**

次の機能は、現在サポートされていません。

* 実験の作成または編集
* レポートのユースケースへの複数の指標の使用

## サンプルプロンプト

Experimentation Agentを使い始める際に役立つプロンプトサンプルを以下に示します。

### 一般的な質問

| プロンプト |
|-|
| 実行されている実験は何ですか？ |
| `<campaign name>` ースに対して実行されている実験は何ですか？ |
| 先月から開始した実験は何ですか？ |
| 過去 1 年間に終了した実験の数 |
| 現在、一時停止/停止/その他しているのはどの実験ですか？ |
| 最近のテストで明らかになっている、一般的なパターンは何ですか。 |
| 前四半期の実験の平均期間はどれくらいですか？ |

### パフォーマンスの質問

| プロンプト |
|-|
| 私の `<experiment name>` にとって、どんな治療が先行していますか？ |
| `<experiment name>` の上昇率はいくらですか。 |
| 統計的に有意な結果が得られた実験はどれですか？ |
| コンバージョン率が最も高かった実験はどれですか？ |

### インサイトの質問

| プロンプト |
|-|
| テスト `<experiment name>` は? |
| 私たちは `<experiment name>` から何を学びましたか？ |
| 治療 A が勝った理由を教えてください。 |
| どのテーマが勝者のバリアントのトレンドですか？ |
| 最近のテストで明らかになっている、一般的なパターンは何ですか。 |
| `<experiment name>` で何か思いがけないことが起こったのですか。 |

### オポチュニティの質問

| プロンプト |
|-|
| この実験の後、次は何をすることをお勧めしますか？ |
| `<experiment name>` を改善する方法はありますか？ |
| どのような機会が明らかになりまし `<experiment name>` か？ |
| `<experiment name>` の仮説を証明するために次にテストできることは何ですか？ |
| その他にどのようなユースケースを実装する必要がありますか？ |
