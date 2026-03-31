---
title: Adobe Experience Platform Agent Orchestrator
description: Adobe Experience Platform Agent Orchestrator について説明します。
source-git-commit: ec03f46b5d80558b683f6cd4330f51258b7378a1
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 10%

---

# Adobe Experience Platform Agent Orchestrator

Adobe Experience Platform Agent Orchestratorは、Adobe Experience Platformの新しいエージェント層です。 Experience Platformの豊富なデータとカスタマーナレッジを活用するように設計されたExperience Platform Agent Orchestratorは、専用に構築されたエキスパートであるAdobe Experience Platform Agentsの背後にあるインテリジェンスと推論を支援します。これにより、人間の監視下で、複雑な意思決定と問題解決のタスクを迅速かつ大規模に実行できます。 AI アシスタントのような会話型インターフェイスを利用して、自然言語で質問したり、サポートを求めたりすると、Agent Orchestratorは専門の担当者を自動的に呼び出して適切な回答を提供します。 Agent Orchestratorは、会話履歴を記憶するため、コンテキストを繰り返すことなく自然に以前の質問を作成でき、複数の担当者からのインサイトを組み合わせて、明確で統一された回答を提供します。

直感的な会話型インターフェイスを利用して、複雑なエンドツーエンドのワークフローを完了できます。その際、舞台裏でどのエージェントが機能しているのかを知る必要はありません。 目標を理解し、ステップバイステップの計画を作成し、フィードバックにもとづいて必要に応じてアプローチを調整します。 AI アシスタントの会話では、Agent Orchestratorの推論パネルを利用して、ステップバイステップの思考プロセスを確認し、リクエストの処理方法をより詳細に把握できます。

>[!SLIDE](agent-orchestrator-overview)

Agent Orchestratorについて詳しくは、このドキュメントを参照してください。

## Agent Orchestrator のコンポーネント {#components}

Agent Orchestratorは、AI アシスタントの会話インターフェイス、意思決定と計画の推論エンジン、Adobe Experience Platformのエージェント、関連情報へのアクセスを提供するナレッジベースなど、いくつかの重要な要素で構成されています。

![Agent Orchestratorのマーケティングアーキテクチャ。](./images/agent-orchestrator/agentic-architecture.png)

### AI アシスタントの会話型インターフェイス {#ai-assistant}

AI アシスタントは、インテリジェントかつ自然言語による会話体験を提供します。これにより、実務担当者は、有効なExperience Cloudアプリケーションを使用して、生成AIとエージェンティック AIの機能を活用できます。これらの機能の幅広さは、お客様がライセンスを取得しているExperience Cloudアプリケーションに依存します。 アクセスを解除するには、[AI アシスタントへのアクセスに関するガイド ](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/access)を参照してください。

詳しくは、[AI アシスタント UI ガイド ](../ai-assistant/ai-assistant-ui.md)を参照してください。

### 推論エンジン {#reasoning-engine}

推論エンジンは、自然言語プロンプトに基づいて目標を解釈し、制限や要件を確認し、目標達成に役立つステップバイステップの計画を作成します。 単純な質疑応答システムとは異なり、状況の変化に応じて計画を調整し、必要に応じて別のアプローチを試すことができます。 作成された計画はAI アシスタントの会話型インターフェイスに表示されるため、プロセスを確認および追跡できるだけでなく、必要に応じて介入することもできます。

### Adobe Experience Platform Agents {#agents}

Adobe Experience Platform Agentsは、顧客体験の領域をまたいで共通のジョブを提供するスキルを持つ、AI エージェントの専用グループです。 以下は、現在Experience Cloud アプリケーションで使用可能なAdobe Experience Platform Agentsのリストです。

| エージェント | 詳細 | サポートされているアプリケーション |
| --- | --- | --- |
|  [!DNL Microsoft 365 Copilot]](ama-ms.md)の[Adobe Marketing Agent | [!DNL Teams]、[!DNL Word]、[!DNL Powerpoint]、[!DNL Excel]などの[!DNL Microsoft 365] アプリで、Adobe Experience Platformからマーケティングインサイトをすばやく取得できます。 このエージェントを利用すれば、アプリ間でチャット履歴を管理し、作業中でもシームレスに会話を続けることができます。 | |
| [Audience Agent](audience.md) | Audience Agentを利用すれば、オーディエンスの大幅な変化の検出、重複するオーディエンスの検出、オーディエンスインベントリの調査、オーディエンスのサイズの取得など、オーディエンスに関するインサイトを取得できます。 | <ul><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | Data Insights Agentは、Customer Journey AnalyticsのAI アシスタントからアクセス可能な生成AI会話型エージェントで、データに関する疑問に迅速かつ効率的に回答します。 データビューのコンポーネントと実際のデータを使用して、Analysis Workspace で関連するビジュアライゼーションを作成します。 | Customer Journey Analytics |
| [Experimentation Agent](./agent-experiment.md) | Experimentation Agentは、実験結果の分析、影響の予測、新しい実験の提案などにより、より迅速な学習を支援します。 過去と現在のテストを一元管理することで、すでに学んだことを基に構築し、ギャップを発見し、次にテストすべきことを優先することができます。 | Adobe Journey Optimizer Experimentation Accelerator |
| [Journey Agent](./ajo-agent.md) | Journey Agentなら、自然言語のインターフェイスを利用して、カスタマージャーニーを構築、分析、最適化できます。 Journey Agentなら、ジャーニーの迅速な構築、スケジュールやオーディエンスの競合の検出と解決、パフォーマンスと離脱ポイントの分析などを実現し、今後のキャンペーンに向けて再現する最もパフォーマンスの高いジャーニーを特定できます。 データにもとづく意思決定、顧客エンゲージメントの向上、ジャーニーオーケストレーションの合理化に役立ちます。 | Adobe Journey Optimizer |
| [製品サポートエージェント ](product-support.md) | Product Support Agentは、セルフサービス型のデバッグおよびトラブルシューティング機能で、ワークフローから離れることなくAdobe Experience Platformの機能とアプリケーションをトラブルシューティングするのに役立ちます。 サポート管理者は、AI アシスタントとのやり取りのコンテキストからカスタマーサポートチケットを作成でき、AI アシスタントを通じてチケットの更新を確認することができます。 | <ul><li>Adobe Experience Platform</li><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li><li>Adobe Journey Optimizer B2B edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul> |

Experience Cloud アプリケーションでのAgentsの利用について詳しくは、[Experience Cloud ドキュメント ](https://experienceleague.adobe.com/ja/docs/core-services/interface/features/agentic-ai)のAgentic AIを参照してください。

### ナレッジベース {#knowledge-base}

ナレッジベースでは、Adobeの製品ドキュメント、ビジネスオブジェクトに関する顧客メタデータ、分析データなどの構造化および非構造化データソースを通じて、担当者は顧客ビジネスインテリジェンスに安全にアクセスできます。

## アクセス {#access}

利用者は誰でも、AI アシスタントと関連するExperience Platformエージェントにアクセスできます。

* **Adobe Experience Manager**：管理者は、[Adobe Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)を通じてAI アシスタントにアクセスする権限を付与する必要があります。

* **Customer Journey Analytics**：管理者は、[Customer Journey Analytics アクセス制御](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/technotes/access-control)を通じてAI アシスタントにアクセスする権限を付与する必要があります。 これにより、製品知識やデータインサイトにもとづいた質問が可能になります。

>[!NOTE]
>
>Operational insightsの質問はCustomer Journey Analyticsでは利用できません。そのため、追加の権限は適用されません。
