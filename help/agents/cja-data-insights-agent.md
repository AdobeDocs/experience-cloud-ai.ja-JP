---
description: Customer Journey AnalyticsのData Insights Agentを使用してデータを視覚化する方法を説明します
title: Customer Journey AnalyticsのData Insights Agentを使用したデータの視覚化
role: User, Admin
solution: Customer Journey Analytics
source-git-commit: 04a73ac0f705cd3a2184fb2f8599aff85b7bb5e5
workflow-type: tm+mt
source-wordcount: '2499'
ht-degree: 5%

---

# Data Insights Agentでのデータの視覚化

>[!AVAILABILITY]
>
>Data Insights Agentは、対象となるお客様が期間限定で利用できます。 Data Insights Agentへのアクセスは、2026 年 2 月 28 日（PT）まで可能です。 Data Insights Agentを引き続き使用するには、Adobe アカウント担当者に連絡して、Adobe Experience Platform Agent Orchestratorのライセンスの詳細を問い合わせてください。

Data Insights Agentは、Customer Journey Analyticsの [AI アシスタント ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant) からアクセスでき、データに関する質問に迅速かつ効率的に回答するジェネレーティブ AI コンバージョンエージェントです。 データビューのコンポーネントと実際のデータを使用して、Analysis Workspace で関連するビジュアライゼーションを作成します。

Data Insights Agentを使用してAnalysis Workspaceのデータ中心の質問に回答すると、Analysis Workspaceでビジュアライゼーションを手動で作成してデータビューコンポーネントに慣れる時間を大幅に節約できます。

![AI アシスタント内のData Insights Agent](images/cja-agent//cja-ai-asst-da.gif)

## 範囲内の機能と範囲外の機能

| 機能 | 範囲内 | 範囲外 |
| --- | --- | --- |
| **ビジュアライゼーションのタイプ** | <ul><li>折れ線グラフ</li><li>複数行</li><li>フリーフォームテーブル</li><li>棒グラフ</li><li>ドーナツ</li><li>概要番号</li></ul> | <ul><li>フロー</li><li>フォールアウト</li><li>コホートテーブル</li><li>面グラフ、積み重ね面グラフ</li><li>積み重ね棒グラフ</li><li>箇条書き</li><li>コンボ</li><li>ヒストグラム</li><li>横棒グラフ、積み重ね横棒グラフ</li><li>主要指標の概要</li><li>散布図</li><li>変更の概要</li><li>テキスト</li><li>ツリーマップ</li><li>ベン図</li><li>ガイド付き分析：アクティブな増加率、コンバージョンのトレンド、エンゲージメント、初回使用の影響、頻度、Funnel、純増加率、リリースの影響、リテンション、タイムライン、トレンド</li></ul> |
| **Workspaceのアクションとエージェントの機能** | <ul><li>ビジュアライゼーションの作成と更新<p>フリーフォームテーブルおよび関連するビジュアライゼーション（線、棒グラフ、ドーナツなど）を生成します。<p>例：*2 月から 5 月の SKU での利益は何ですか？*</p></li><li>フォローアップの質問をする<p>以前のプロンプトからコンテキスト内のプロンプトに応答します。 例：</p> <ul><li>プロンプト 1:*3 月からのトレンドイベント*</li><li>プロンプト 2:*代わりに 3 月から 4 月のデータを表示する*</li></ul> </li><li>範囲外のプロンプト検出<p>*このプロジェクトを書き出す* などの範囲外のプロンプトを送信すると、Data Insights Agentは応答として、質問が範囲外であることを通知します。</p></li></ul> | <ul><li>共有</li><li>書き出し</li><li>ダウンロード</li><li>ユーザー環境設定の管理</li><li>データ表示の管理</li><li>Analytics ダッシュボードアプリ</li><li>アトリビューション</li><li>インラインの概要または応答<p>Data Insights Agentが、ユーザーからのプロンプトに対する概要の回答でチャットパネルのインラインで応答できません。 範囲外プロンプトの例としては、*前回のプロンプトのインサイトの概要を入力* や *折れ線グラフのビジュアライゼーションのハイライトをまとめる* などがあります。</p></li></ul> |
| **質問の明確化** | Data Insights Agentが回答するのに十分なコンテキストがない、または一般的すぎる質問をした場合、Data Insights Agentは、明確な質問または推奨されるオプションを使用して回答します。 <p>以下の明確な質問は、コンポーネント関連の質問の例です。</p><ul><li>指標：*具体的に「売上高」指標はどれですか？*</li><li>Dimension:*注目したい「地域」は、以下のうちどれですか？*</li><li>セグメント：*適用した「アカウント」セグメント*</li><li>日付範囲：*「先月」とは、過去 1 か月を意味していますか？過去 30 日を意味していますか？*</li></ul><p>次の明確な質問は、ディメンション項目に関する質問の例です。</p> <ul><li>「店名」って、どういう意味？ （例えば、Store #5274、Store #2949 など）。</li></ul> | 質問を明確にするのは、コンポーネントとディメンション項目に限られます。 Data Insights Agentでは、データビュー、ビジュアライゼーション、データの精度、比較、範囲などを明確にすることはできません。 質問を明確にできない場合、エージェントは、要求する可能性が最も高い質問にデフォルトで対応します。 予期しないビジュアライゼーションまたはデータの精度が返された場合は、フォローアップの質問をしたり、ビジュアライゼーションとデータを調整したりできます。 |
| **データの検証可能性と正確性** | データの検証可能性と正確性は、生成されたフリーフォームテーブルとデータビジュアライゼーションを表示することで確認できます。 <p>例えば、Data Insights Agentに *先月の注文のトレンド* を依頼すると、新しく生成されたパネル、データビジュアライゼーションおよびフリーフォームテーブルで正しい指標（「注文」）と日付範囲（「先月」）が選択されたことを確認できます。 | Data Insights Agentは、追加されたコンポーネントやビジュアライゼーションをユーザーに通知しても応答しません。</p> |
| **フィードバック機構** | <ul><li>親指を上に向ける</li><li>サムズダウン</li><li>フラグ</li></ul> |  |


## Data Insights エージェントへのアクセスの管理 {#manage-access}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-enable-data-insights-data-view"
>title="Data Insights エージェントを有効化"
>abstract="このオプションを選択すると、Data Insights エージェントで使用するためにこのデータビューが有効になります。Data Insights エージェントは、Customer Journey Analytics の AI アシスタントからアクセスできる生成 AI 対話型エージェントです。テキストプロンプトを使用してデータをすばやく分析するのに役立ちます。データビューのコンポーネントと実際のデータを使用して、Analysis Workspace で関連するビジュアライゼーションを作成します。"

<!-- markdownlint-enable MD034 -->

次のパラメーターは、Customer Journey AnalyticsのData Insights Agentへのアクセスを制御します。

* **ソリューションアクセス**:Data Insights Agentは、2025 年 11 月 30 日（PT）まで、限定アクセスプログラムの一環として、すべてのCustomer Journey Analyticsのお客様が利用できます。 Adobe Analyticsでは使用できません。

* **契約によるアクセス**:AI アシスタントでData Insights Agentを使用できない場合は、組織の管理者またはAdobe アカウントチームにお問い合わせください。 組織がData Insights Agentを使用する前に、生成 AI に関連する特定の法的条項に同意する必要があります。

* **権限**: ユーザーがData Insights Agentにアクセスするには、必要な権限が [!UICONTROL 2}Adobe Admin Console} で付与されている必要があります。]

  権限を付与するには、[ 製品プロファイル管理者 ](https://helpx.adobe.com/jp/enterprise/using/manage-product-profiles.html) が [!UICONTROL Admin Console] で次の手順を実行する必要があります。

   1. **[!UICONTROL Admin Console]** で、「**[!UICONTROL 製品]**」タブを選択して **[!UICONTROL すべての製品とサービス]** ページを表示します。
   1. 「**[!UICONTROL Customer Journey Analytics]**」を選択します。
   1. 「**[!UICONTROL 製品プロファイル]**」タブで、[!UICONTROL AI アシスタント：製品ナレッジ ] へのアクセス権を付与する製品プロファイルのタイトルを選択します。
   1. 特定の製品プロファイルで、「**[!UICONTROL 権限]**」タブを選択します。

      ![Admin Consoleの「権限」タブ ](images/cja-agent/ai-assistant-permissions-tab.png)

   1. 提供されたテーブルの **[!UICONTROL レポートツール]** 行で、編集アイコン ![ 編集 ](images/cja-agent/Edit.svg) を選択します。
   1. スクロールして「**[!UICONTROL AI Assistant: Product Knowledge]**」を選択または検索し、この権限の横にあるプラス アイコン ![AddCircle](images/cja-agent/AddCircle.svg) を選択します。
   1. スクロールして **[!UICONTROL Data Insights Agent]** を検索し、この権限の横にあるプラスアイコン ![AddCircle](images/cja-agent/AddCircle.svg) を選択します。

      **[!UICONTROL AI アシスタント：製品ナレッジ]** 権限と **[!UICONTROL Data Insights Agent]** 権限が **[!UICONTROL 含まれる権限項目]** 列に追加されます。

      ![ 権限を追加 ](images/cja-agent/ai-assistant-permissions.png).

   1. 「**[!UICONTROL 保存]**」を選択して、権限を保存します。

  アクセス制御について詳しくは、[ アクセス制御 ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/access-control#access-control) を参照してください。

* **データビューアクセス**:Data Insights Agentでデータビューを有効にする必要があります。

  >[!IMPORTANT]
  >
  >データビューを有効にする場合は、次の点を考慮してください。
  >* IMS 組織ごとに最大 50 個のデータビューを有効にできます。 特定の組織のすべての製品プロファイルで 50 を超えるデータビューを有効にした場合、Data Insights Agentは最も使用されている 50 のデータビューを使用します。
  >* Data Insights Agentは、含まれているデータビューを、ユーザーが有効にしている日と同じ日にいつでも参照できます。

  Data Insights Agentのデータビューを有効にするには：

   1. Customer Journey Analyticsで、**[!UICONTROL データ管理]**/**[!UICONTROL データビュー]** を選択します。
   1. Data Insights Agentに対して有効にする 1 つ以上のデータビューを選択し、次に **[!UICONTROL Data Insights Agentに対して有効にする]** を選択します。

      ![Data Insights Agentのデータビューの有効化 ](images/cja-agent/data-view-enable-dia.png)

  IMS 組織でData Insights Agentが有効になっているデータビューの数を表示するには：

   1. Customer Journey Analyticsで、**[!UICONTROL データ管理]**/**[!UICONTROL データビュー]** を選択します。
   1. **[!UICONTROL Data Insights Agent]** 列の上部にある情報アイコンを選択します。

      ![Data Insights Agent情報アイコン ](images/cja-agent/data-insights-agent-tooltip.png)

## AI アシスタントでData Insights Agentにアクセスする

1. [experience.adobe.com](https://experience.adobe.com/) に移動し、Adobe IDでログインします。
1. Experience Cloud ホームから **0}Customer Journey Analytics} を選択します。**
1. プロジェクトページ上部のバナーで **[!UICONTROL 空のプロジェクト]** を選択して、新しい空のプロジェクトを開きます。
1. [Customer Journey AnalyticsでのData Insights Agentへのアクセスの管理 ](#manage-access-to-data-insights-agent-in-customer-journey-analytics) で説明されているように、パネル用に選択したデータビューが、Data Insights Agentで使用できるようになっていることを確認します。
1. ページの右上にある AI Assistant チャットアイコンを選択します。

   チャットアイコンが表示されない場合は、管理者に問い合わせて、管理者が Admin Console で次の機能を有効にできるようにします。

   * レポートツール：**[!UICONTROL AI アシスタント：製品知識]**
   * データ ビューツール：**[!UICONTROL Data Insights Agent]**

   詳しくは、[Customer Journey AnalyticsでのData Insights Agentへのアクセスの管理 ](#manage-access-to-data-insights-agent-in-customer-journey-analytics) を参照してください。

   ![AI アシスタント アイコン ](images/cja-agent/ai-asst-icon.png)

1. ページ下部の **[!UICONTROL Customer Journey Analyticsについて尋ねる]** ダイアログで、Data Insights Agentを使用してデータビジュアライゼーションに関する質問をします。

   詳しくは、次の例を参照してください。

### 例 1

例えば、7 月にビジネスが受け取った注文に興味があるとします。

**プロンプト：** 「7 月のトレンド受注 *を入力します*。

![AI プロンプト ](images/cja-agent/ai-asst-prompt1.png)

**回答：** Data Insights Agentは、指標やコンポーネントを含むデータビューでデータを調べることでインサイトを収集します。 これにより、プロンプトがデータ範囲内の適切なディメンションと指標に変換されます。

ご覧のように、7 月の注文を表示する折れ線グラフとフリーフォームテーブルが自動的に生成されました。

![ プロンプトに対する回答 – 折れ線グラフとフリーフォームテーブル ](images/cja-agent/ai-asst-result.png)

### 例 2

次に、売上高を地域別に比較した結果を確認します。

**プロンプト：** プロンプトウィンドウで、「*地域ごとの売上高を表示」と入力します*。

**回答：** Data Insights Agentは、「地域」とは「お客様の地域」を意味することをインテリジェントに理解しています。 次のように、地域別の売上高が最もよく表示される棒グラフが生成されます。

![ 棒グラフ ](images/cja-agent/ai-asst-result2.png)

### 例 3

次に、地域別の売上高を把握するだけでなく、地域別の利益のデータも確認する必要があります。 前のプロンプトを繰り返す代わりに、最新のビジュアライゼーションとフリーフォームテーブルを更新するようにData Insights Agentに依頼できます。

**プロンプト：** プロンプトウィンドウに *「Add profit.」と入力します*

**応答：** **[!UICONTROL 棒グラフ]** は引き続き最も簡潔な回答を提供しますが、利益指標はフリーフォームテーブルの列として追加されています。

![ 棒グラフ ](images/cja-agent/ai-asst-result4.png)

### 例 4

最後に、売上高を製品カテゴリ別に見てみましょう。

**プロンプト：** プロンプトウィンドウで、「*製品カテゴリ別売上高の割合」と入力します。*

**Response:** Data Insights Agentでは、最も適切なビジュアライゼーション（この場合は **[!UICONTROL ドーナツ]** ビジュアライゼーション）を選択して、質問に回答します。

![ドーナツ](images/cja-agent/ai-asst-result3.png)

## Experience Cloud アプリケーションをまたいだData Insights Agentへのアクセス

Adobe Experience Platform Agent Orchestratorを使用すると、Adobe Journey OptimizerやReal-Time CDPなど、複数のAdobe Experience Cloud アプリケーションでData Insights Agentの機能にアクセスできます。

Agent Orchestratorはリクエストを解釈し、必要な専門エージェントを判断し、適切な対応を提供するように調整します。 マルチターンインタラクションのコンテキストを追跡するので、以前のクエリに自然に基づいて構築できます。

詳しくは、[Adobe Experience Platform Agent Orchestrator](/help/agents/agent-orchestrator.md) を参照してください。

## データビジュアライゼーションプロンプトの例

以下に、一般的なプロンプトと、Data Insights Agentがプロンプトに応答するために使用するビジュアライゼーションの例を示します。

| プロンプトの例 | 期待されるビジュアライゼーション |
| --- | --- |
| [ 月 ] の利益を表示する | 折れ線グラフ<p>デフォルトでは、特定の期間内のトレンドや指標を尋ねると、折れ線グラフのビジュアライゼーションが返されます。 |
| [ 月 ] の注文のトレンド | 折れ線グラフ |
| 地域別の収益を [ 月 ] に表示 | 棒グラフ |
| 製品カテゴリ別売上高のシェア | ドーナツ |
| 1 月から 5 月までの曜日ごとの注文 | 棒グラフ |
| 3 月から 6 月の間、性別ごとに注文を表示 | 棒グラフ |
| 2 月から 5 月の SKU での利益 | 棒グラフ |
| [ 月 ] の店舗名別の売上高 | 棒グラフ |
| [ 月 ] の利益別の上位 10 個の SKU は何でしたか？ | 棒グラフ |
| 月別の購入率 | ドーナツ |
| [ 月 ] の合計利益 | 数値の概要<p>特定の時間範囲にわたる指標の「合計」を求めると、数値の概要ビジュアライゼーションが返されます。 |

## プロンプトのベストプラクティス

Data Insights Agentは、各ユーザープロンプトから提供されるコンテキストを処理し、フリーフォームテーブル内の最も適切なビジュアライゼーションとコンポーネントでインテリジェントな応答を試みます。

回答は、プロンプトで使用された特定の単語やフレーズによって異なる場合があり、言語がわずかに変更されただけで結果が異なる場合があります。

最適な結果を得るには、次のガイドラインを考慮してください。

* **具体的：** 回答を絞り込むために、正確な用語を含めます。 次に、「カリフォルニアでの先月の売上」という特定のプロンプトの例を示します。

* **明確な指標、ディメンション、セグメントの使用：** 特定の指標（「売上高」など）、ディメンション（「web サイト名」など）、セグメント（「iPhone ユーザー」など）、および日付範囲（「過去 3 か月」など）を追加すると、Data Insights Agentが適切なデータに焦点を当てるのに役立ちます。

* **直接質問する：** 直接質問すると、Data Insights Agentが明確で関連性の高いインサイトを提供しやすくなります。 次に、「今年の製品カテゴリ別平均売上高は何ですか？」というプロンプトで直接質問した例を示します。

Data Insights Agentのプロンプトで使用できる用語とフレーズの例を、想定される応答のタイプと共に、次の表で確認します。

これらの例は、特定の単語や構造が Data Insight Agent の出力に与える影響を理解し、より正確で価値のあるインサイトを確実にすることを目的としています。 Data Insights Agentは生成 AI を使用するので、類似のプロンプト間でビジュアライゼーションや選択したデータが若干異なる場合があります。

| 望ましい結果 | 用語とフレーズの例 |
| --- | --- |
| 数値の概要ビジュアライゼーション | <ul><li>合計</li></ul> |
| コンポーネントの比較 | <ul><li>を比較</li><li>比較対象</li><li>コントラスト</li><li>週ごと</li><li>前月比</li><li>前四半期比</li><li>前年比</li></ul> |
| ドーナツビジュアライゼーション | <ul><li>割合</li><li>シェア /</li><li>配分</li><li>割合</li><li>貢献度</li><li>部分</li><li>部品</li></ul> |
| 線のビジュアライゼーション | <ul><li>トレンド</li><li>[ 時間範囲 ] の [ 指標 ]</li></ul> |
| 棒グラフビジュアライゼーション | <ul><li>[ 指標 ] （[Dimension] による）</li></ul> |

<!--

## Beta testing expectations and requested feedback

After posing each question, carefully review the assistant's provided answer. It's crucial to evaluate the generated visualizations comprehensively before providing feedback. 

Consider the following when evaluating a response from Data Insights Agent: 

* Chat rail response or template: Evaluate the textual response provided. Is the response appropriate given the context of your prompt? 

* Visualization/chart: Evaluate the visualization. Is it the appropriate or expected visualization for your question, or would you have expected a different visualization?  

* Freeform table: Evaluate the freeform table. Is the freeform table data correct? Is it breaking down data where requested? Are the applied segments those that you requested or expected? 

* Error Message / Out-of-Scope: If a generic error message is given stating the question is out of scope, provide feedback on whether you think the out-of-scope message is appropriate, given your prompt. Was your prompt actually in scope? 

**For every response, give a thumbs up or thumbs down, based on the response.**

Following the thumbs up or thumbs down selection, please make a selection for the relevant multi-select feedback boxes. If you want to provide additional feedback, add notes in the open text box.

## Questions and Contact

* Send questions and feedback in the Beta Slack channel: #data-insights-agent-in-cja-beta

-->


## 設定のベストプラクティス

以下は、Customer Journey Analyticsの設定（データビュー、計算指標、セグメントなど）に関するベストプラクティスで、Data Insights Agentが正しいコンポーネントを見つけて、追加情報を求められることなく、より明確な回答を返せるようにします。

* **必要なコンポーネントのバランスを取**。 データセットのすべてのフィールドを指標またはディメンションコンポーネントとしてデータビューに追加しないでください。 特に、あなたが最も確かに分析で使用しないもの。 一方、分析に必要なフィールドのみに厳密に制限しないでください。 データビューが制限されすぎると、分析の柔軟性やData Insights Agent機能が制限されます。
* **常にわかりやすい表示名を使用する**。 指標またはディメンションコンポーネントのいずれかとしてデータビューで定義するすべてのフィールドに、わかりやすいコンポーネント名があることを確認します。 わかりやすい名前を付けてフィールドの名前を変更するプロセスは、特にAdobe Analytics ソースコネクタデータセットのフィールドに関連します。 多くの場合、これらのフィールドには、`eVar41` や `prop25` など、わかりやすい名前は付けられていません。
* **独特の名前を使用**。 独特の名前は、データビューで指標とディメンションコンポーネントの両方と同じフィールドを使用する場合に特に関連します。 または、同じタイプの複数のコンポーネント（2 つの異なる指標など）でフィールドを使用する場合、それぞれのコンポーネント設定が異なります。
* **コンポーネントの命名規則を使用** します。 コンポーネント命名規則を使用して、コンポーネントをグループ化できます。 例：**[!UICONTROL Orders |製品]** および **[!UICONTROL 注文 |顧客]** は、データに存在する可能性のある様々な注文指標を区別できます。
* **データディクショナリの使用**。 データ要素でコンポーネントの説明やその他の関連データを追加します。 Data Insight Agent は現在、データ要素の説明とタグを使用していませんが、将来の使用になる可能性があります。
* **承認済みの計算指標を使用** します。 承認された計算指標のみをデータビューのコンポーネントとして使用するプロセスに同意し、実験的な計算指標を使用しないようにします。
* **必要なセグメントを共有**. セグメントを共有し、Data Insights Agent プロンプトに必要なセグメントを表示します。
* **データビュー間でコンポーネント名を標準化する**。 複数のデータビューでコンポーネントと同じフィールドを使用する場合は、そのコンポーネントに対して単一のわかりやすい名前と単一の識別子を必ず使用してください。 単一の名前と識別子を使用すると、Data Insights Agentはコンテキストを失うことなくデータビューを切り替えることができます。

>[!MORELIKETHIS]
>
>[ コンポーネント設定 ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/overview)
>[データディクショナリ ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/data-dictionary/data-dictionary-overview)
>[計算指標を承認 ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/cm-approving)
>[セグメント ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/segments/seg-share) 共有
