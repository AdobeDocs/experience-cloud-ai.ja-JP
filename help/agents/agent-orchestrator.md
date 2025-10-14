---
title: Adobe Experience Platform Agent Orchestrator
description: Adobe Experience Platform Agent Orchestratorの詳細。
source-git-commit: a77ff0217f91a23c69902f2f48bc2bd399818b6d
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 2%

---

# Adobe Experience Platform Agent Orchestrator

Adobe Experience Platform Agent OrchestratorはAdobe Experience Platformの新しいアジェンティック層です。 Experience Platformの豊富なデータとカスタマーナレッジを活用するように設計されたExperience Platform Agent Orchestratorは、専用のエキスパートであるAdobe Experience Platform Agents の背後にあるインテリジェンスと推論を強化し、複雑な意思決定や問題解決のタスクを人間の監督によって迅速かつ大規模に実行できるようにします。 AI アシスタントなどの会話型インターフェイスで自然言語を使用して質問したり、ヘルプをリクエストしたりすると、Agent Orchestratorは自動的に専門のエージェントを呼び出して、適切な回答を得ます。 Agent Orchestratorは、会話履歴を記憶しているので、コンテキストを繰り返すことなく自然に前の質問に基づいて構築でき、複数のエージェントからのインサイトを組み合わせて、明確で統一された回答を提供します。

複雑なエンドツーエンドのワークフローを、バックグラウンドで動作しているエージェントを把握しなくても、直感的な会話インターフェイスで完了できます。 システムはユーザーの目標を理解し、段階的な計画を作成し、ユーザーのフィードバックに基づいて必要に応じてアプローチを調整します。 AI アシスタントの会話内で、Agent Orchestratorの推論パネルを調べて、段階的な考え方のプロセスを確認し、リクエストの処理方法をより深く理解できます。

Agent Orchestratorについて詳しくは、このドキュメントを参照してください。

## Agent Orchestrator のコンポーネント {#components}

Agent Orchestratorは、AI アシスタントの会話型インターフェイス、意思決定と計画のための推論エンジン、専門のAdobe Experience Platform エージェント、関連情報へのアクセスを提供するナレッジベースなど、いくつかの主要なコンポーネントで構成されています。

![Agent Orchestratorのマーケティングアーキテクチャ &#x200B;](./images/agent-orchestrator/agentic-architecture.png)

### AI アシスタントの会話型インターフェイス {#ai-assistant}

AI アシスタントは、インテリジェントな自然言語による対話型エクスペリエンスで、Experience Cloudが有効になっているアプリケーションを使用している実務担当者が、GenAI 機能と Agentic AI 機能を活用できます。これらの機能は、お客様がライセンスを取得したExperience Cloud アプリケーションによって幅広く利用できます。 アクセスのロックを解除するには、[AI アシスタントへのアクセスに関するガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/access) を参照してください。

詳しくは、[AI アシスタント UI ガイド &#x200B;](../ai-assistant/ai-assistant-ui.md) を参照してください。

### 推論エンジン {#reasoning-engine}

推論エンジンは、自然言語プロンプトに基づいて目標を解釈し、制限や要件を確認し、目的を達成するのに役立つ段階的な計画を作成します。 単純な質疑応答システムとは異なり、状況の変化に応じてプランを調整でき、必要に応じて元に戻って異なるアプローチを試すことができます。 作成したプランは AI アシスタントの会話用インターフェイスに表示されるので、プロセスを確認およびフォローしたり、必要に応じて介入したりできます。

### Adobe Experience Platform エージェント {#agents}

Adobe Experience Platform エージェントは、カスタマーエクスペリエンスの領域全体で共通のジョブを提供できるスキルを持つ AI エージェントをグループ化した専用のツールです。 以下は、現在Experience Cloud アプリケーションで使用できるAdobe Experience Platform エージェントのリストです。

| 代理人 | 詳細 | サポートされるアプリケーション |
| --- | --- | --- |
| [Audience Agent](audience.md) | Audience Agentでは、オーディエンスサイズの大きな変化の検出、重複するオーディエンスの検出、オーディエンスインベントリの調査、オーディエンスのサイズの取得など、オーディエンスに関するインサイトを表示できます。 | <ul><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | Data Insights Agentは、Customer Journey Analyticsの AI アシスタントからアクセスでき、データに関する質問に迅速かつ効率的に回答するジェネレーティブ AI コンバージョンエージェントです。 データビューのコンポーネントと実際のデータを使用して、Analysis Workspaceで関連するビジュアライゼーションを作成します。 | Customer Journey Analytics |
| 実験エージェント | 実験エージェントは、実験結果を分析し、影響を予測し、新しい実験を提案することで、チームがより迅速に学習するのに役立ちます。 過去の実験とアクティブな実験を一元化するので、既に学んだことに基づいて構築し、ギャップを見つけ、次にテストする項目を優先させることができます。 | Adobe Journey OptimizerExperimentation Accelerator |
| [Journey Agent](./ajo-agent-analyze.md) | Journey Agentを使用すると、Adobe Journey Optimizer ユーザーは、自然言語インターフェイスを使用してジャーニーを作成、分析および最適化できます。 Journey Agentを使用すると、ジャーニーをすばやく構築し、スケジュールやオーディエンスの競合を検出および解決し、パフォーマンスとドロップオフポイントを分析し、今後のキャンペーンにレプリケートするパフォーマンスの高いジャーニーを特定することができます。 データに基づく意思決定を行い、顧客エンゲージメントを向上させ、ジャーニーオーケストレーションを合理化するのに役立ちます。 | Adobe Journey Optimizer |
| [&#x200B; 製品サポート担当者 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/ai-assistant/new-features/customer-support) | 製品サポートエージェントは、セルフサービスのデバッグおよびトラブルシューティング機能で、ワークフローから離れることなくAdobe Experience Platformの機能やアプリケーションをトラブルシューティングするのに役立ちます。 サポート管理者は、AI アシスタントのインタラクションからコンテキストを使用してカスタマーサポートチケットを作成し、AI アシスタントを通じてチケットの更新を確認できます。 | <ul><li>Adobe Experience Platform</li><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li><li>Adobe Journey OptimizerB2B edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul> |

Experience Cloud アプリケーションでのエージェントの使用について詳しくは、[Experience Cloudの Agentic AI ドキュメント &#x200B;](https://experienceleague.adobe.com/ja/docs/core-services/interface/features/agentic-ai) を参照してください。

### ナレッジベース {#knowledge-base}

ナレッジベースは、Adobe製品ドキュメント、ビジネスオブジェクトに関するお客様のメタデータ、分析データなど、構造化されたデータソースや構造化されていないデータソースを通じて、お客様のビジネスインテリジェンスへの安全なアクセスをエージェントに提供します。

## アクセス {#access}

AI アシスタントのリクエストは、Adobe Identity Management サービスを使用して認証されます。 権限は、Adobe Experience Platform アクセス制御およびCustomer Journey Analytics アクセス制御によって適用されます。

AI Assistant の会話インターフェイスにアクセスして 1 つ以上のExperience Platform Agent を使用するには、Adobe管理者が権限 UI またはAdobe Admin Consoleで関連する権限を付与する必要があります。

* **Real-Time CDP** および **Adobe Journey Optimizer**:AI アシスタントにアクセスできるようにするには、管理者から **AI アシスタントを有効にする** 権限を付与されている必要があります。 また、管理者は、AI アシスタントで運用インサイトに関する質問をできるように、**運用インサイトを表示** 権限をユーザーに付与する必要があります。 どちらの権限も、管理者によって権限 UI で設定されます。

* **Customer Journey Analytics**：管理者から、[Customer Journey Analytics アクセス制御 &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/technotes/access-control) を通じて AI アシスタントにアクセスする権限を付与してもらう必要があります。 これにより、製品に関する知識やデータインサイトを得ることができます。

>[!NOTE]
>
>オペレーショナルインサイトの質問はCustomer Journey Analyticsでは使用できないので、追加の権限は適用されません。

* **Adobe Experience Manager**：管理者から、[Adobe Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html) 経由で AI アシスタントにアクセスする権限を付与されている必要があります。

