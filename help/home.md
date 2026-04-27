---
title: Experience Cloud アプリケーションの AI
description: Experience Cloud アプリケーションで生成 AI（GenAI）、AI アシスタント、エージェント型 AI がどのように使用されるかについて説明します。
TQID: https://experienceleague.adobe.com/heALjEZbowNaygG24oOM2HSlHa9oYVI5ViUNZDr19Ds
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: dd7883d8eccab3b0f006d55a850248e1c347d7e7
workflow-type: tm+mt
source-wordcount: 846
ht-degree: 4%

---

# Experience Cloud の AI

Adobe Experience Cloudアプリケーション全体のAI能力に関する包括的なガイドへようこそ。 このドキュメントでは、生成AI、AI アシスタント、AdobeエージェントをExperience Cloudワークフローに統合し、生産性を高め、意思決定を強化する方法を説明します。

## このガイドの内容

### AI アシスタント

[AI アシスタント &#x200B;](./ai-assistant/ai-assistant-ui.md)は、Adobe Experience Platform ベースのアプリケーションの生産性を向上させ、作業を再定義する、インテリジェントな会話型の生成AI ツールです。 ユーザーは、自然言語プロンプトを通じて、製品知識を得たり、問題のトラブルシューティングを行ったり、業務インサイトを得たりすることができます。 また、AI アシスタントを使用して、Adobe Experience Platform Agentsやその他のAI機能にアクセスすることもできます。

**主な機能：**

- **対話型インターフェイス**: ワークフローの環境設定に合わせて、フルスクリーンとパネル表示のインターフェイスのいずれかを選択できます。
- **検出プロンプト**: AI アシスタントは、学習、分析、最適化などのカテゴリ別に整理された、事前設定済みのプロンプトを提供します。
- **コンテキスト設定**: アプリケーション、サンドボックス、データビューの設定を設定して、ニーズに合わせた応答を受信できます。
- **データの可視化**：このツールは、インタラクティブなチャートとグラフを提供し、データからインサイトを得ることができます。
- **応答検証**：すべての応答には、ソースの引用、AI推論の説明、フィードバックを提供するためのメカニズムが含まれます。


### Agent Orchestrator

[Adobe Experience Platform Agent Orchestrator](./agents/agent-orchestrator.md)は、Adobe Experience Platformの新しいエージェント レイヤーです。 このプラットフォームの豊富なデータとカスタマーナレッジを活用するように設計されたExperience Platform Agent Orchestratorは、専用に構築されたエキスパートであるAdobe Experience Platform Agentsの背後にあるインテリジェンスと推論を支援します。これにより、人間の監視下で、複雑な意思決定と問題解決のタスクを迅速かつ大規模に実行できます。 AI アシスタントのような会話型インターフェイスを利用して、自然言語で質問したり、サポートを求めたりすると、Agent Orchestratorは専門の担当者を自動的に呼び出して適切な回答を提供します。 Agent Orchestratorは、会話履歴を記憶するため、コンテキストを繰り返すことなく自然に以前の質問を作成でき、複数の担当者からのインサイトを組み合わせて、明確で統一された回答を提供します。

**コアコンポーネント：**

- **推論エンジン**：段階的な計画を作成し、必要に応じてアプローチを調整します
- **専用エージェント**：特定のタスクとドメイン用に構築された専用エージェント
- **ナレッジベース**：ビジネスインテリジェンスとドキュメントへの安全なアクセス

### 専門エージェント

#### Audience Agent

Audience Agentは、次のようなオーディエンスに関するインサイトを提供します。

- オーディエンスサイズの大幅な変更を検出。
- 重複したオーディエンスの特定：
- オーディエンスのインベントリを調べる：
- オーディエンスサイズの取得。

詳しくは、[Audience Agent ドキュメント &#x200B;](./agents/audience.md)を参照してください。

#### Data Insights Agent

Customer Journey AnalyticsのData Insights Agentで利用できます。

- 自然言語を使って、データに関する疑問の答えを提供します。
- Analysis Workspaceで関連するビジュアライゼーションを作成：
- は、データビューと実際のデータのコンポーネントを使用します。

#### ジャーニー分析エージェント

ジャーニー分析エージェントを使用すると、Adobe Journey Optimizer ユーザーは次のことが可能になります。

- 自然言語を使用して、カスタマージャーニーを分析、最適化します。
- スケジュールやオーディエンスの競合を検出して解決。
- パフォーマンスと離脱ポイントを分析：

詳しくは、[Journey Agent ドキュメント &#x200B;](./agents/ajo-agent.md)を参照してください。

#### 製品サポート担当者

セルフサービスのデバッグとトラブルシューティングには、次の製品サポートエージェントを使用します。

- ワークフローから離れることなく、Adobe Experience Platformの機能をトラブルシューティング。
- AI アシスタントとのやり取りのコンテキストに基づいてサポートチケットを作成します。
- AI アシスタントを通じてチケットの更新を確認します。

詳しくは、[製品サポートエージェントのドキュメント &#x200B;](./agents/product-support.md)を参照してください。

<!--
#### Adobe Marketing Agent for [!DNL Microsoft 365 Copilot]

Use the Adobe Marketing Agent for [!DNL Microsoft 365 Copilot] to retrieve marketing insights from Experience Platform in [!DNL Microsoft 365] apps like [!DNL Teams], [!DNL Word], [!DNL Powerpoint], and [!DNL Excel]. With this agent, you can:

- Make faster, data-driven marketing decisions.
- Reduce time spent switching between tools.
- Simplify access to audience and journey insights across teams.

Read the [Adobe Marketing Agent documentation](./agents/ama-ms.md) for more information.
-->

## はじめに

### アクセス要件

AI アシスタントとExperience Platform Agentsを使用するには、Adobe管理者が適切な権限を設定する必要があります。

- Real-Time CDPおよびAdobe Journey Optimizer内でAI アシスタントを使用するには、運用上の質問にアクセスするための「AI アシスタントを有効にする」権限と「運用上のインサイトを表示する」権限が必要です。
- Customer Journey AnalyticsのAI アシスタントへのアクセスは、Customer Journey Analytics Access Controlを通じて管理され、製品情報とデータインサイトの両方に質問することができます。
- Adobe Experience Managerの場合は、Adobe Admin Consoleで設定した権限を使用して、AI アシスタントにアクセスできます。

### プライバシーとセキュリティ

AI アシスタントは、プライバシー、セキュリティ、ガバナンスを最前線に据えて構築されています。

- トレーニングに個人データは使用されません。
- 既存のすべてのアクセス制御ポリシーが尊重されます。
- ADOBE EXPERIENCE PLATFORM Healthcare ShieldでHIPAAに対応。
- インタラクションログの30日間保持ポリシー。
- サンドボックス固有のデータの分離：

## ベストプラクティス

AI アシスタントのエクスペリエンスから最大限の価値を引き出すには、次のベストプラクティスに従ってください。

- AI アシスタントからターゲットを絞った関連性の高いインサイトを取得するには、プロンプトに&#x200B;**具体的な**&#x200B;を入力します。
- **AI アシスタントが提供するソースの引用と説明の理由を確認して、回答**&#x200B;を検証します。
- **コンテキスト設定**&#x200B;を使用して、最も関連性の高いデータソースが質問に使用されるようにします。
- **フィードバック**&#x200B;を提供して、AI アシスタントのパフォーマンスと精度を長期的に向上させることができます。
- **複数のエージェントからのインサイト**&#x200B;を組み合わせて、より包括的で全体的な分析を実現します。

## 法的考慮事項

AI アシスタントを利用する際には、重要な法的および実践的な考慮事項を認識することが重要です。 現在、AI アシスタントは英語での回答のみをサポートしています。 言語モデルが誤りを犯す可能性があるため、提供される情報を常に検証するように注意してください。 回答に含まれる論理的な手順と説明を活用して、回答をより深く理解します。 問題や不正確さが発生した場合は、フィードバックを送信して、AI アシスタントを長期的に改善できるようにしてください。
