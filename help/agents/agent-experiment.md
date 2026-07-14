---
title: Experimentation Agent
description: Experimentation Agentについて詳しく見る
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: fddbc156de78cc72bcc1ed4906be6e089191f5b0
workflow-type: tm+mt
source-wordcount: 555
ht-degree: 5%

---

# Experimentation Agent

<!--
TQID: https://experienceleague.adobe.com/ARh16ylmUDrp%2D%2D%2Dg8KuYNyewIv54IQ53pxoE2g700o0
-->

>[!AVAILABILITY]
>
>Experimentation Agentは、Journey Optimizer Experimentation Acceleratorの有料ライセンスを購入したすべてのお客様が利用でき、Adobe TargetまたはAdobe Journey Optimizerとシームレスに統合できます。
>
>[Journey Optimizer Experimentation Acceleratorについて詳しく見る](https://experienceleague.adobe.com/ja/docs/experimentation-accelerator/using/overview)

## 概要

**Experimentation Agent**&#x200B;は、Web サイト、電子メール、プッシュメッセージ、およびアプリケーションをまたいだデジタル実験を実行および管理する方法を最新化するAIを活用したツールです。 Adobe Experience Platform AI プラットフォームと実験ツールに基づいて構築された&#x200B;**Experimentation Agent**&#x200B;は、実験をより効率的に実行し、ビジネス目標を整理し、実用的なインサイトを生成するのに役立ち、何が機能し、何が機能しなかったか、次に実験すべき場所を強調します。

Experimentation Agentの機能を完全に使用するには、次の権限が必要です。

* **実験を表示**：この権限を持つユーザーは、Experimentation Agentを使用して、AI アシスタントで実験に関するインサイトを直接表示できます。

* **実験メタデータの管理**：この権限を持つユーザーは、Experimentation Agentを使用して、AI アシスタントで新しい実験を直接作成できます。

➡️ [詳しくは、Journey Optimizer Experimentation Accelerator ドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-access)を参照してください

Experimentation Accelerator機能の一部として、Agentは次の機能を提供します。

* **パフォーマンス**：実験で何が起こったのかを明確に把握する

* **インサイト**：結果が発生した理由の説明

* **商談**：次に実行するアクションに関するガイダンス

![Experimentation Agentのサンプル &#x200B;](./images/experiment/experiment-agent.png)

## ユースケース

Experimentation Agentは、結果の分析、コンテンツの解釈、次のステップの提案をおこない、検証ワークフローの各フェーズを強化します。

その能力は、次の5つの主要な機能に分類できます。

* **実験の要約**

  関係者に、実験結果を技術的な知識なしに明確に説明します。

* **コンテンツ分析**

  特定の治療法が他の治療法よりも優れている理由を理解するために、治療法のメッセージやクリエイティブな要素を調べます。

* **属性識別**

  テーマ、トーン、フォーマットなどの主要属性ごとに処理を分類し、そうした属性をコンバージョン結果に結び付けることができます。

* **推奨事項の生成**

  過去の実験から得たインサイトにもとづき、新しい治療法や調整を提案してテストします。

* **商談**

  未開拓の可能性を明らかにするために、実験の対象となるより広い領域や新しい角度を特定します。

## インスコープ機能とアウトオブスコープ機能

### **範囲内**

現在、次の機能がサポートされています。

* パフォーマンス
* Insights
* 機会

### **範囲外**

次の機能は、現在サポートされていません。

* 実験の作成または編集
* レポートのユースケースに複数の指標を使用する

## サンプルプロンプト

Experimentation Agentの使用を開始するためのプロンプトサンプルの一覧を以下に示します。

### 一般的な質問

| プロンプト |
|-|
| どの実験が行われていますか？ |
| `<campaign name>`に対してどの実験が実行されていますか？ |
| 先月はどんな実験が始まったのでしょうか？ |
| 過去1年間に終了した実験の数は？ |
| どの実験が現在一時停止/停止されていますか？ |
| 最近のテストでどのような一般的なパターンが見られるのでしょうか？ |
| 前四半期の平均実験期間は？ |

### パフォーマンスに関する質問

| プロンプト |
|-|
| `<experiment name>`の場合、どのような処理が行われていますか？ |
| `<experiment name>`の上昇率を選択してください。 |
| 統計的に有意な結果を示した実験はどれか？ |
| どの実験が最もコンバージョン率が高かったか？ |

### インサイトに関する質問

| プロンプト |
|-|
| `<experiment name>` テストとは何ですか？ ? |
| `<experiment name>`から何を学びましたか？ |
| なぜA治療が成功したのか教えていただけますか？ |
| どのようなテーマが勝利のバリエーションでトレンドですか？ |
| 最近のテストでどのような一般的なパターンが見られるのでしょうか？ |
| `<experiment name>`で予期しない事態が発生しましたか？ |

### オポチュニティに関する質問

| プロンプト |
|-|
| この実験の次におすすめすることは何ですか？ |
| `<experiment name>`を改善する方法はありますか？ |
| `<experiment name>`後に明確になった商談は何ですか？ |
| `<experiment name>`からの仮説を証明するために、次に何をテストできますか？ |
| 追加のユースケースは何か？ |
