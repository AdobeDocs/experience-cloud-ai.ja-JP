---
title: Adobe Marketing Agent for Microsoft 365 Copilot
description: Adobe Marketing Agent for Microsoft 365 Copilotの活用方法を学びましょう。
source-git-commit: c3cb327bb7625ee81f784a1fad740b7b4cbdfb71
workflow-type: tm+mt
source-wordcount: '1843'
ht-degree: 0%

---

# [!DNL Microsoft 365 Copilot]のAdobe Marketing Agent

[!DNL Microsoft 365 Copilot]のAdobe Marketing Agentは、Adobe Experience Platformを[!DNL Microsoft 365 Copilot]に直接接続するAIを活用したツールです。 このエージェントを使用すると、[!DNL Teams]、[!DNL Word]、[!DNL Powerpoint]、[!DNL Excel]などの[!DNL Microsoft 365]個のアプリケーション内で自然言語による質問を行い、ワークフローを中断することなく、Experience Platformからマーケティングインサイトをすばやく取得できます。 同じ担当者が同じアプリで利用でき、Adobe Marketing Agentとのチャット履歴は引き継がれます。たとえば、[!DNL Teams]の[!DNL Copilot]で調査を開始し、キャンペーンの概要を作成したりプレゼンテーションをレビューしたりしながら、[!DNL Word]または[!DNL Powerpoint]で会話を続けることができます。

[!DNL Microsoft 365 Copilot]向けAdobe Marketing Agentを使用すると、マーケティングマネージャー、分析およびインサイト部門、ビジネス関係者は次のことが可能になります。

- より迅速なデータドリブン型マーケティングに取り組む。
- ツール間の切り替えに費やす時間を削減します。
- 部門をまたいでオーディエンスとジャーニーのインサイトへのアクセスを簡素化する。

## エージェントの仕組み

>[!IMPORTANT]
>
>[!DNL Microsoft 365 Copilot]のAdobe Marketing Agentは、現在、Experience Platform Operational Insights、Customer Journey Analytics Data Insights、Audience Agent、およびJourney Agentをサポートしています。

[!DNL Microsoft 365 Copilot]のAdobe Marketing Agentでは、Experience Platformと[!DNL Microsoft 365] アプリケーション間の統合エクスペリエンスが提供されます。

- Adobe Marketing Agentは、[!DNL Teams]、[!DNL Word]、[!DNL Powerpoint]、[!DNL Excel]など、[!DNL Microsoft 365 Copilot]に担当者として表示されます。
- Adobe アカウントでログインし、使用するデータ環境（サンドボックス、データビュー）を選択します。

### データアクセスと権限

受け取る回答は、Adobe IDに関連付けられた&#x200B;**データとアクセスレベル**&#x200B;を反映しています。クエリおよび参照できる内容は、Experience Platformおよびその関連ソリューションで利用できる内容と同じです。 Adobe Marketing Agent **では、これらの権限を**&#x200B;継承し、**not**&#x200B;では、[!DNL Microsoft 365]統合に対して個別の権限を設定する必要があります。 基盤となるExperience Platform AI アシスタント機能およびその他のAdobe AI エージェントの場合、Experience Platformでこれらの機能を使用する際の&#x200B;**権限の要件は変更されません**。

エージェントは、お使いの[!DNL Microsoft 365] インスタンスをExperience Platformとその関連アプリケーション （Real-Time CDP、Adobe Journey Optimizer、およびCustomer Journey Analytics）に接続します。 この統合により、Experience Platform AI アシスタントとエージェントを使用して、関連するインサイトを[!DNL Microsoft 365] インスタンスに直接取得できます。 [!DNL Microsoft 365] インスタンスで返される回答は、会話型および自然言語のテキスト、テーブル、データのビジュアライゼーションとして表示されます。 さらに、同じ[!DNL Copilot] チャット内で、フォローアップの質問と調査のサポートを利用できます。

## 主要なユースケースとシナリオ例

| ユースケース | 説明 |
| --- | --- |
| オーディエンスとカスタマージャーニーの運用に関するインサイトの取得 | Adobe Marketing Agentを使用すると、オーディエンスやカスタマージャーニーをまたいで、運用上のインサイトを簡単に取得できます。 最もエンゲージメントの高いオーディエンスや大きなオーディエンスを特定することで、集中的に取り組むべき施策を優先できます。 現在アクティブなカスタマージャーニーを確認し、そのパフォーマンスを把握することで、最適化の機会を特定することができます。 また、さまざまなセグメントが時間の経過とともに成長または縮小している状況を追跡し、オーディエンスの変化にタイムリーに対応することもできます。 |
| データの可視化により、カスタマージャーニーや施策をより適切に分析 | ジャーニーのパフォーマンスとドロップオフを確認し、キャンペーンのパフォーマンスを長期的に比較して、コンバージョンを促進するタッチポイントを把握することができます。 さらに、施策のパフォーマンスに関するビジュアルレポートを生成し、チャネル、地域、または異なる期間にわたって比較できます。 また、クエリやダッシュボードを手作業で作成することなく、トレンドを調査することもできます。 |
| コラボレーションと意思決定の強化 | オーディエンス、キャンペーン、web トラフィックを検索するために、提案されたプロンプトを使用します。 自然言語インターフェイスを活用して、Experience PlatformとCustomer Journey Analyticsのコンセプトを簡単に学ぶことができます。 さらに、プランニングミーティング中に[!DNL Teams]個のチャネルまたはチャットに関するインサイトを共有できます。 また、Adobe Marketing Agentを利用して、計画やデッキを確認しながら、リアルタイムで高度な質問に答えることができるため、関係者の足並みを揃え、一連の指標と定義を維持することができます。 |

## 前提条件

[!DNL Microsoft 365 Copilot]でAdobe Marketing Agentを使用する前に、まず次の要件を満たしていることを確認する必要があります。

- [!DNL Microsoft 365] （[!DNL Microsoft Teams]または[!DNL Microsoft Copilot Chat]）。
- Experience Platformと、Real-Time CDP、Adobe Journey Optimizer、Customer Journey Analyticsのいずれか少なくとも1つ。
- Experience Platform Agent Orchestratorとエージェントの使用権限。
- 使用するソリューションとデータに対する組織のAdobe Experience Cloud アカウント（ログインおよび製品の使用権限）へのアクセス。 Adobeへのアクセス権がない場合は、Adobe管理者にお問い合わせください。

## 組織のエージェントを有効にする {#enable-the-agent-for-your-organization}

エンドユーザーがAdobe Marketing Agentを使用できるのは、[!DNL Microsoft 365] テナントで使用できるようになった後だけです。 **組織の[!DNL Microsoft 365] Copilot管理者** （または組織内のCopilot エージェントに対応する管理者）と協力して、組織が必要とするアクセスを有効にし、エージェントを割り当てます。

管理者設定後の一般的な結果には、次のものがあります。

- **[!DNL Agent Store]**&#x200B;を[!DNL Teams]で開き、エージェントのリストから&#x200B;**[!DNL Adobe Marketing Agent]**&#x200B;を見つけ、**[!DNL Add]**&#x200B;を選択してCopilot エージェントに添付できます。
- または、Copilot管理者は、組織内の全員または特定のグループにエージェントを&#x200B;**公開**&#x200B;できるため、ユーザーが個別にエージェントを追加する必要はありません。

[!DNL Microsoft 365]管理センターの管理者の手順とポリシーオプションについては、Microsoft ドキュメントの「[Microsoft 365 Copilotのエージェントを管理](https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/manage)」を参照してください。

## 基本を学ぶ

組織がエージェントを有効にした後（[組織のエージェントを有効にする](#enable-the-agent-for-your-organization)を参照）、選択したアプリケーションの[!DNL Microsoft 365 Copilot]に移動し、左側のナビゲーションを使用して&#x200B;**[!DNL All Agents]**&#x200B;を選択します。

![Microsoft 365 コパイロットの左側のナビゲーションで、すべてのエージェントが選択されています。](../agents/images/ama/all-agents.png)

[!DNL Adobe Marketing Agent]のカードを探すか、検索バーを使用してエージェントを手動で検索します。 担当者が決まったら、カードを選択します。

エージェント ギャラリーの![Adobe Marketing Agent カードまたは検索結果。](../agents/images/ama/select-ama.png)

エージェントの詳細を確認するには、ポップアップウィンドウを使用します。 準備ができたら、**[!DNL Add]**&#x200B;を選択します。

![Adobe Marketing Agentの詳細ポップアップと「追加」ボタンの表示](../agents/images/ama/add-ama.png)

[!DNL Microsoft 365 Copilot] ダッシュボードは、メインページの[!DNL Adobe Marketing Agent] ブランディングで更新されます。

![&#x200B; メインダッシュボードにAdobe Marketing Agentが表示されているMicrosoft 365 Copilot ホームページ。](../agents/images/ama/home.png)

### ログインしてコンテキストを設定します

次に、エージェントにサインインするよう促し、アカウントの認証に必要な手順に従います。 この手順では、エージェントが返す数値コードをコピーしてから、Adobe組織にログインする必要があります。 ログインを完了できない場合、または組織のAdobe ソリューションへのアクセス権がない場合は、**Adobe管理者**&#x200B;にお問い合わせください。

![Adobe ログイン手順で、コピーする数値コードと、Adobe組織で認証する手順が表示されます。](../agents/images/ama/sign-in.png)

成功したら、コンテキストセッターを使用して、クエリに使用するドキュメントソース、サンドボックス、データビューを確立します。

![&#x200B; コンテキストセッターUIで、クエリのドキュメントソース、サンドボックス、データビューを選択します。](../agents/images/ama/context.png)

### エージェントを使用して運用上のインサイトを取得します

ログインしたら、メインページのプロンプトを使用して開始できます。 また、スタータープロンプトを活用して、マーケティングオーディエンスの分析、キャンペーンのパフォーマンスの確認、キャンペーンジャーニーの監視などに分岐することもできます。 例えば、「**[!DNL Review campaign performance]**」を選択してから「**[!DNL Analyze engagement - Show web visitors for top 10 products last week]**」を選択します。

エージェントのホームページに![&#x200B; スタータープロンプトが表示され、キャンペーンのパフォーマンスのレビューとエンゲージメントの分析オプションが表示されます。](../agents/images/ama/starter-guide.png)

担当者がすぐに計算を行い、データを視覚化して回答します。 表示された棒グラフを使用するか、**[!DNL View data]**&#x200B;を選択してテーブルのデータを表示できます。

![上位の製品のweb訪問者を可視化し、データを表示するオプションを示す棒グラフ付きのエージェントの応答](../agents/images/ama/response.png)

![&#x200B; データを表示を選択した後、同じインサイトがデータテーブルとして表示されます。](../agents/images/ama/tables.png)

担当者が推奨するフォローアップの質問を選択して、さらに調査することができます。 別の方法として、別のスタータープロンプトをピボットして試したり、エージェントが参照した情報ソースを確認したり、フィードバックメカニズムを使用してフィードバックを提供したりすることもできます。

![詳しい調査のために、担当者の回答の下にフォローアップの質問を提案しました。](../agents/images/ama/follow-up.png)

AI アシスタント UI機能について詳しくは、[AI アシスタントの使用](../ai-assistant/ai-assistant-ui.md)に関するガイドを参照してください。

## セキュリティ、プライバシー、責任あるAI

**データの処理とガバナンス**

Adobe Marketing Agentは、Experience Platformと[!DNL Microsoft 365]に適用されるのと同じコントロールとガバナンスに依存しています。 組織はデータの所有権と制御を保持します。 エージェントを通じて返されたインサイトは、各ユーザーのAdobe権限およびデータエンタイトルメントに対してスコープが設定されます。Experience Platformおよび関連するAdobe AI エージェントで既に適用されているものを超える追加の権限モデルは、[!DNL Microsoft 365] サーフェスに導入されません。

**責任あるAIの使用**

エージェントは、読み取り専用のインサイトを返すことを目的としており、Experience Platformの顧客データを変更することはありません。 生成された要約と分析は、ビジネス上の意思決定に活用する前に確認する必要があります。

**サポートされている言語とスコープ**

最初のリリースは、英語の体験として利用可能です。 機能は読み取り専用のインサイトに限定され、エージェントはマーケティングアセットや設定を作成または更新しません。

>[!IMPORTANT]
>
>Adobe Marketing Agentは、送信されたプロンプトに応じて、様々なAdobe エージェントとジョブを呼び出します。 この基になるAdobe エージェントは、[Adobe Experience Platform エージェントジョブとAI クレジットの使用](https://experienceleague.adobe.com/en/docs/core-services/interface/features/ai-credit-consumption) ページに示されているAI クレジットを使用します。

## 付録

[!DNL Microsoft 365 Copilot]のAdobe Marketing Agentについて詳しくは、次を参照してください。

### Adobe Marketing Agent [!DNL Microsoft 365 Copilot]の管理者手順

外部プロバイダー（サードパーティ開発者またはMicrosoft Commercial Marketplace）からエージェントを設定するには、まずテナント設定で外部アプリが許可されていることを確認してから、管理センターの「統合アプリ」または「エージェント」セクションで管理する必要があります。

#### テナント設定で外部エージェントを有効にする

外部エージェントをデプロイする前に、組織のポリシーで外部エージェントを許可する必要があります。

- [Microsoft 365管理センター](https://admin.microsoft.com/)にログインします。
- **エージェント** > **設定** > **ユーザーアクセス**&#x200B;に移動します。
- **許可されたエージェントの種類、**&#x200B;では、外部パブリッシャー&#x200B;**によって構築された**&#x200B;許可アプリとエージェントが選択されていることを確認します。

>[!IMPORTANT]
>
>この設定が無効になっている場合、ユーザーの[&#x200B; エージェントストア &#x200B;](https://devblogs.microsoft.com/microsoft365dev/introducing-the-agent-store-build-publish-and-discover-agents-in-microsoft-365-copilot/)に外部エージェントは表示されません。

#### エージェントの取得と承認

通常、[[!DNL Microsoft Commercial Marketplace]](https://appsource.microsoft.com/)で外部エージェントを見つけることができます。

- **マーケットプレイスから**：必要なエージェントを見つけて、**今すぐ入手**&#x200B;を選択します。 これは、多くの場合、管理者センターの&#x200B;**統合アプリ** ページにリダイレクトされます。
- **権限を確認**: [統合アプリ &#x200B;](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide) リストで、外部エージェントを選択します。
- **データとツール**&#x200B;と&#x200B;**セキュリティとコンプライアンス**&#x200B;のタブを確認して、外部プロバイダーがどのデータにアクセスするかを確認します。
- 「**承認**」または「**アクティブ化**」を選択して、組織のインベントリに移動します。

#### 特定のユーザーへのデプロイ

承認されると、Copilot サイドバーにエージェントを表示するユーザーを正確に制御できます。

- [[!DNL Microsoft 365] 管理センター](https://admin.microsoft.com/)で、**エージェント** > **すべてのエージェント**&#x200B;に移動します。
- リストから外部エージェントを選択します。
- **デプロイ** （または&#x200B;**割り当てを編集**）を選択します。
- **特定のユーザー/グループ**&#x200B;を選択し、それを持つ必要がある個人または[!DNL Entra ID] グループを検索します。
- 「**デプロイメントを完了**」を選択します。 これにより、エージェントがそれらのユーザーに「プッシュ」され、Copilot インターフェイスに自動的に表示されます。

#### 更新を管理

外部プロバイダーは、頻繁にエージェントを更新します。 これらの更新を管理するには、次のベストプラクティスに従います。

- [[!DNL Agent Registry]](https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-registry?view=o365-worldwide)を定期的に確認してください。
- 更新に新しい権限が必要な場合、エージェントは&#x200B;**保留中の更新**&#x200B;のステータスを表示する場合があります。
- 新しいバージョンを割り当てられたユーザーにロールアウトする前に、手動で&#x200B;**更新を承認**&#x200B;する必要があります。