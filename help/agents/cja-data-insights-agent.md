---
description: Customer Journey AnalyticsのData Insights Agentを使用して、データを視覚化する方法を説明します
title: Customer Journey AnalyticsのData Insights Agentでデータを視覚化する
role: User, Admin
solution: Customer Journey Analytics
TQID: https://experienceleague.adobe.com/UtKIDlN2x7MOAiHNRRQ8b5OO4fIwzV74r1fnfMwblcQ
product_v2:
  - id: e98b7246-966c-4318-9e95-cad2f7a17dc7
feature_v2:
  - id: b743a5d9-dc51-41ed-8b2f-86a1f8de430f
  - id: c73c4213-d623-4126-81f4-80b42e5e2656
  - id: ce577701-5b9e-4fe4-8fa3-4eedea976da4
subfeature_v2:
  - id: b1f5d324-a668-4e51-a59b-6fc0862d7310
  - id: bc7a5a86-1a70-451f-985c-037b65f091d1
  - id: df7fb1db-aa1b-4314-98ac-59dbfcc3044f
  - id: e44e560d-5e5c-4a5f-9a87-eb8adbb817af
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: dd7883d8eccab3b0f006d55a850248e1c347d7e7
workflow-type: tm+mt
source-wordcount: 2690
ht-degree: 4%

---

# Data Insights Agentでデータを視覚化

>[!AVAILABILITY]
>
>Data Insights Agentは、対象となるお客様が期間限定で利用できます。 Data Insights Agentへのアクセスは、2026年3月31日（PT）まで可能です。 この日付以降も引き続きData Insights Agentを使用する場合は、Adobeのライセンスについて詳しくは、Adobe Experience Platform Agent Orchestratorの担当者にお問い合わせください。

[AI アシスタント &#x200B;](/help/ai-assistant/ai-assistant-ui.md)からアクセス可能なData Insights Agentは、生成AI会話型エージェントで、データに関する質問に迅速かつ効率的に回答します。 データビューと実際のデータからのコンポーネントを使用して、Analysis Workspaceに関連するビジュアライゼーションを構築します。

Data Insights Agentを使用してAnalysis Workspaceでデータ中心の質問に回答することで、Analysis Workspaceで手動でビジュアライゼーションを作成したり、データビューコンポーネントに慣れたりするのに費やす時間を大幅に節約できます。

![AI アシスタント内のData Insights Agent](/help/agents/images/cja-agent/cja-ai-asst-da.gif)

## スコープ内フィーチャーとスコープ外フィーチャー

| 機能 | スコープ内 | 範囲外 |
| --- | --- | --- |
| **ビジュアライゼーションタイプ** | <ul><li>折れ線グラフ</li><li>複数行</li><li>フリーフォームテーブル</li><li>棒グラフ</li><li>ドーナツグラフ</li><li>概要番号</li></ul> | <ul><li>フロー</li><li>フォールアウト</li><li>コホートテーブル</li><li>エリア、積み重ねエリア</li><li>横向き積み上げ</li><li>箇条書き</li><li>コンボ</li><li>ヒストグラム</li><li>横向き棒グラフ、横向き棒グラフ</li><li>主要指標の概要</li><li>散布図</li><li>変更概要</li><li>テキスト</li><li>ツリーマップ</li><li>ベン</li><li>ガイド付き分析：アクティブな成長，コンバージョントレンド，エンゲージメント，初回使用の影響，頻度，Funnel, ネット成長，リリースの影響，保持，タイムライン，トレンド</li></ul> |
| **Workspaceのアクションとエージェント機能** | <ul><li>ビジュアライゼーションの構築と更新<p>フリーフォームテーブルと関連するビジュアライゼーション（線、棒グラフ、ドーナツなど）を生成します。</p><p>例えば、*2月から5月までのSKU全体の利益は何ですか？*</p></li><li>フォローアップの質問<p>以前のプロンプトからのコンテキストでプロンプトに応答します。 例：</p> <ul><li>プロンプト 1: *3月からのトレンドイベント。*</li><li>プロンプト 2: *3月から4月までのデータを表示する*</li></ul> </li><li>スコープ外プロンプト検出<p>このプロジェクトを書き出す&#x200B;*など、スコープ外のプロンプトを送信すると、Data Insights Agentは、質問がスコープ外であることを通知して応答します。*</p></li></ul> | <ul><li>共有</li><li>書き出し</li><li>ダウンロード</li><li>ユーザー環境設定の管理</li><li>データビューを管理</li><li>Adobe Analytics ダッシュボードアプリ</li><li>アトリビューション</li><li>インラインの要約または応答<p>Data Insights Agentは、ユーザープロンプトの概要回答を使用して、チャットパネルでインラインで応答できません。 スコープ外プロンプトの例としては、*最後のプロンプトのインサイトの概要を表示*&#x200B;および&#x200B;*行のビジュアライゼーションのハイライトを要約*&#x200B;します。</p></li></ul> |
| **質問の明確化** | Data Insights Agentで回答するのに十分なコンテキストがない、または一般的すぎる質問をした場合、Data Insights Agentは明確な質問または提案されたオプションで回答します。 <p>以下の質問は、コンポーネント関連の質問の例です。</p><ul><li>指標：*どの「収益」指標を意味しましたか？*</li><li>Dimension: *次の「リージョン」のうち、どのリージョンに重点を置きますか？*</li><li>セグメント：*適用する「アカウント」セグメントはどれですか？*</li><li>日付範囲：*「先月」とは、最後の1か月または過去30日間を意味していますか？*</li></ul><p>次の明確な質問は、ディメンション項目に関連する質問の例です。</p> <ul><li>「お店の名前」とはどういう意味ですか。 （例：Store #5274、Store #2949など）</li></ul> | 質問の明確化は、コンポーネントとディメンション項目に限定されます。 Data Insights Agentでは、データビュー、ビジュアライゼーション、データの粒度、比較、範囲などを明確にすることはできません。 質問を明確にできない場合、エージェントはデフォルトで、最も可能性の高い質問に従います。 予期せぬビジュアライゼーションやデータの精度が返された場合は、フォローアップで質問するか、ビジュアライゼーションとデータを調整することができます。 |
| **データの検証可能性と正確性** | 生成されたフリーフォームテーブルとデータのビジュアライゼーションを表示することで、データの検証可能性と正確性を確認できます。 <p>例えば、Data Insights Agentに対して&#x200B;*先月*&#x200B;のトレンド注文を求める場合、新しく生成されたパネル、データビジュアライゼーション、フリーフォームテーブルで正しい指標（「注文」）と日付範囲（「先月」）が選択されていることを確認できます。</p> | Data Insights Agentは、追加されたコンポーネントやビジュアライゼーションを通知しても応答しません。 |
| **フィードバックメカニズム** | <ul><li>サムズアップ</li><li>サムズダウン</li><li>フラグ</li></ul> |  |


## Data Insights Agent へのアクセスの管理 {#manage-access}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-enable-data-insights-data-view"
>title="Data Insights Agent を有効にする"
>abstract="このオプションを選択すると、Data Insights Agent で使用するためにこのデータビューが有効になります。 Data Insights Agent は、Customer Journey Analytics の AI アシスタントからアクセスできる生成 AI 会話エージェントです。 テキストプロンプトを使用してデータをすばやく分析するのに役立ちます。 データビューのコンポーネントと実際のデータを使用して、Analysis Workspace で関連するビジュアライゼーションを作成します。"

<!-- markdownlint-enable MD034 -->

次のパラメーターは、Customer Journey AnalyticsのData Insights Agentへのアクセスを管理します。

* **ソリューションへのアクセス**：対象となるお客様は、Data Insights Agentを期間限定で利用できます。 Data Insights Agentへのアクセスは、2026年2月28日（PT）まで可能です。 Adobe Analyticsでは使用できません。

* **契約上のアクセス**: AI アシスタントでData Insights Agentを使用できない場合は、組織の管理者またはAdobe アカウントチームにお問い合わせください。 Data Insights Agentを導入する前に、生成AIに関する特定の法的条件に同意する必要があります。

* **権限**: [!UICONTROL Adobe Admin Console]で必要な権限を付与してから、ユーザーがData Insights Agentにアクセスできるようにする必要があります。

  権限を付与するには、[製品プロファイル管理者](https://helpx.adobe.com/jp/enterprise/using/manage-product-profiles.html)が[!UICONTROL Admin Console]で次の手順を実行する必要があります。
   1. **[!UICONTROL Admin Console]**&#x200B;で、**[!UICONTROL 製品]** タブを選択して、**[!UICONTROL すべての製品とサービス]** ページを表示します。
   1. **[!UICONTROL Customer Journey Analytics]**&#x200B;を選択します。
   1. **[!UICONTROL 製品プロファイル]** タブで、[!UICONTROL AI アシスタント：製品ナレッジ &#x200B;]にアクセスする製品プロファイルのタイトルを選択します。
   1. 特定の製品プロファイルで、「**[!UICONTROL 権限]**」タブを選択します。

      Admin Console![&#128279;](/help/agents/images/cja-agent/ai-assistant-permissions-tab.png)の「権限」タブ

   1. 指定されたテーブルの&#x200B;**[!UICONTROL レポートツール]**&#x200B;行で、編集アイコン ![編集](/help/agents/images/cja-agent/Edit.svg)を選択します。
   1. **[!UICONTROL AI アシスタント：製品ナレッジ]**&#x200B;までスクロールするか検索し、この権限の横にあるプラスアイコン ![AddCircle](/help/agents/images/cja-agent/AddCircle.svg)を選択します。
   1. **[!UICONTROL Data Insights Agent]**&#x200B;にスクロールするか検索し、この権限の横にあるプラスアイコン ![AddCircle](/help/agents/images/cja-agent/AddCircle.svg)を選択します。

      **[!UICONTROL AI アシスタント：製品知識]**&#x200B;権限と&#x200B;**[!UICONTROL Data Insights Agent]**&#x200B;権限が&#x200B;**[!UICONTROL 含まれる権限項目]**&#x200B;列に追加されます。

      ![権限を追加](/help/agents/images/cja-agent/ai-assistant-permissions.png)。

   1. **[!UICONTROL 保存]**&#x200B;を選択して、権限を保存します。

  アクセス制御の詳細については、[&#x200B; アクセス制御](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/technotes/access-control#access-control)を参照してください。

* **データビューへのアクセス**: Data Insights Agentでデータビューを有効にする必要があります。

  >[!IMPORTANT]
  >
  >データビューを有効にする際には、次の点を考慮してください。
  >* IMS組織ごとに最大50個のデータビューを有効にできます。 特定の組織のすべての製品プロファイルで50以上のデータビューを有効にすると、Data Insights Agentで最も使用される50のデータビューが使用されます。
  >  データビュー[&#128279;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-dataviews/manage-dataviews#manage-data-views)のData Insights Agent列の情報を使用して、IMS組織内でData Insights Agentに対して有効になっているデータビューの数を表示できます。
  >* Data Insights Agentでは、含まれるデータビューを、有効にするのと同じ日の任意の時点で参照できます。

  Data Insights Agentのデータビューを有効にするには：

   1. Customer Journey Analyticsで、**[!UICONTROL Data Management]** > **[!UICONTROL Data views]**&#x200B;を選択します。

   1. Data Insights Agentに対して有効にする1つ以上のデータビューを選択し、**[!UICONTROL Data Insights Agentに対して有効]**&#x200B;を選択します。

      ![Data Insights Agentのデータビューを有効にする](/help/agents/images/cja-agent/data-view-enable-dia.png)

      Data Insights Agentのデータビューを有効にする方法について詳しくは、「[&#x200B; データビューのAI設定](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-dataviews/create-dataview#ai-settings/help/data-views/create-dataview.md#ai-settings)」を参照してください。

  IMS組織内でData Insights Agentに対して有効になっているデータビューの数を表示するには：

   1. Customer Journey Analyticsで、**[!UICONTROL Data Management]** > **[!UICONTROL Data views]**&#x200B;を選択します。

   1. **[!UICONTROL Data Insights Agent]**&#x200B;列の上部にある情報アイコンを選択します。

      ![Data Insights Agent情報アイコン &#x200B;](/help/agents/images/cja-agent/data-insights-agent-tooltip.png)


## AI アシスタントでのData Insights Agentへのアクセス

1. [experience.adobe.com](https://experience.adobe.com/)に移動し、Adobe IDでログインします。

2. Experience Cloud ホームから&#x200B;**Customer Journey Analytics**&#x200B;を選択します。

3. プロジェクトページの上部にあるバナーで「**[!UICONTROL 空のプロジェクト]**」を選択して、新しい空のプロジェクトを開きます。

4. パネルに選択したデータビューが、[Customer Journey AnalyticsのData Insights Agentへのアクセスの管理](#manage-access-to-data-insights-agent-in-customer-journey-analytics)で説明されているように、Data Insights Agentで使用できるように有効になっているデータビューであることを確認します。

5. ページの右上領域にあるAI アシスタントのチャットアイコンを選択します。

   チャットアイコンが表示されない場合は、管理者に連絡して、Admin Consoleで次の機能を有効にできるようにしてください。

   * レポートツール：**[!UICONTROL AI アシスタント：製品知識]**

   * データビューツール：**[!UICONTROL Data Insights Agent]**

   詳細については、[Customer Journey AnalyticsでのData Insights Agentへのアクセスの管理](#manage-access-to-data-insights-agent-in-customer-journey-analytics)を参照してください。

   ![AI アシスタント アイコン &#x200B;](/help/agents/images/cja-agent/ai-asst-icon.png)

6. ページ下部の「**[!UICONTROL Customer Journey Analyticsについて質問]**」ダイアログで、Data Insights Agentを使用してデータビジュアライゼーションに関する質問を行います。

   詳しくは、次の例を参照してください。

### 例 1

例えば、7月に自社が受け取った注文に関心があるとします。

**プロンプト：** 「*」 7月のトレンド注文を入力します。&quot;*

![AI プロンプト &#x200B;](/help/agents/images/cja-agent/ai-asst-prompt1.png)

**応答：** Data Insights Agentは、指標とコンポーネントを含むデータビュー内のデータを調べることでインサイトを収集します。 プロンプトをデータ範囲内の適切なディメンションや指標に変換します。

ご覧のとおり、7月の注文を表示するために、折れ線グラフとフリーフォームテーブルが自動的に生成されました。

![&#x200B; プロンプトへの回答 – 折れ線グラフとフリーフォームテーブル &#x200B;](/help/agents/images/cja-agent/ai-asst-result.png)

### 例 2

次に、売上が地域別にどのように比較されているかを確認します。

**プロンプト：** プロンプトウィンドウで、*「地域ごとの収益を表示」と入力します。&quot;*

**回答：** Data Insights Agentは、「地域」とは「お客様の地域」を意味することをインテリジェントに理解しています。 地域ごとの売上を最もよく表示する棒グラフが表示されます。

![棒グラフ &#x200B;](/help/agents/images/cja-agent/ai-asst-result2.png)

### 例 3

次に、地域別の売上を把握するだけでなく、地域別の利益のためのデータも確認する必要があります。 前のプロンプトを繰り返す代わりに、Data Insights Agentに最新のビジュアライゼーションおよびフリーフォームテーブルの更新を依頼できます。

**プロンプト：** プロンプトウィンドウで、*&quot;Add profit.&quot;*&#x200B;と入力します。

**応答：** **[!UICONTROL 棒グラフ]**&#x200B;は、依然として最も簡潔な回答を提供しますが、利益指標はフリーフォームテーブルの列として追加されています。

![棒グラフ &#x200B;](/help/agents/images/cja-agent/ai-asst-result4.png)

### 例 4

最後に、商品カテゴリー別の売上を見てみましょう。

**プロンプト：** プロンプトウィンドウに、*「製品カテゴリ別の収益の割合」と入力します。&quot;*

**応答：**&#x200B;繰り返しますが、Data Insights Agentは最も適切なビジュアライゼーション（この場合は&#x200B;**[!UICONTROL ドーナツ]** ビジュアライゼーション）を選択して、質問に答えます。

![ドーナツ](/help/agents/images/cja-agent/ai-asst-result3.png)

## Experience CloudアプリケーションからのData Insights Agentへのアクセス

Adobe Experience Platform Agent Orchestratorを使用すると、Adobe Journey OptimizerやReal-Time CDPなど、複数のAdobe Experience Cloud アプリケーションでData Insights Agentの機能にアクセスできます。

Agent Orchestratorを利用すれば、顧客のリクエストを解釈し、必要な専門エージェントを特定して、適切な対応を提供できます。 マルチターンのインタラクションをまたいでコンテキストを追跡できるため、以前のクエリをもとに自然に構築することができます。

詳しくは、[Adobe Experience Platform Agent Orchestrator](https://business.adobe.com/jp/products/experience-platform/agent-orchestrator.html)を参照してください。

## データビジュアライゼーションプロンプトの例

次に、一般的なプロンプトの例と、そのプロンプトに対してData Insights Agentが応答するために使用するビジュアライゼーションを示します。

| プロンプト例 | 期待されるビジュアライゼーション |
| --- | --- |
| [か月]に利益を表示 | 折れ線グラフ<p>デフォルトで特定の時間範囲内のトレンドまたは指標を要求すると、行のビジュアライゼーションが返されます。 |
| [か月]のトレンド注文 | 折れ線グラフ |
| [か月]の地域別収益を表示 | 棒グラフ |
| 製品カテゴリ別の収益の割合 | ドーナツ |
| 1月から5月までの曜日ごとの注文 | 棒グラフ |
| 3月から6月までの性別で注文を表示 | 棒グラフ |
| 2月から5月までのSKU全体の利益は | 棒グラフ |
| [か月]のストア名別収益 | 棒グラフ |
| [か月]の利益別の上位10のSKUは何でしたか？ | 棒グラフ |
| 月別購入割合 | ドーナツ |
| [か月]の合計利益 | 概要番号<p>特定の時間範囲の指標の「合計」を要求すると、概要番号のビジュアライゼーションが返されます。 |


## プロンプトのベストプラクティス

Data Insights Agentでは、各ユーザープロンプトから提供されるコンテキストを処理し、フリーフォームテーブル内の最も適切なビジュアライゼーションとコンポーネントを使用して、インテリジェントに対応しようとします。

プロンプトで使用する特定の単語やフレーズによって反応が異なる場合があり、言語が少し変更されると、結果が異なる場合があります。

最適な結果を得るには、次のガイドラインを考慮してください。

* **具体的であること：**&#x200B;回答を絞り込むには、正確な用語を含めます。 次に、特定のプロンプトの例を示します。「先月のカリフォルニアでの販売」

* **明確な指標、ディメンション、セグメントを使用：**&#x200B;特定の指標（「収益」など）、ディメンション（「web サイト名」など）、セグメント（「iPhone ユーザー」など）、日付範囲（「過去3か月」など）を追加すると、Data Insights Agentは適切なデータに集中できるようになります。

* **直接の質問：**&#x200B;直接の質問を言うと、Data Insights Agentが明確で適切なインサイトを提供しやすくなります。 次の例は、「今年の製品カテゴリ別の平均売上は？」というプロンプトで直接質問する例です。

Data Insights Agentのプロンプトで使用できる用語やフレーズの例と、想定される回答の種類を次の表でご確認ください。

これらの例は、特定の単語や構造がData Insights Agentの出力にどのような影響を与えるかを理解できるように設計されており、より正確で価値のあるインサイトを獲得するのに役立ちます。 Data Insights Agentは生成AIを利用しているため、ビジュアライゼーションや選択したデータは、類似のプロンプトによって若干異なる場合があります。

| 望ましい成果 | 用語やフレーズの例 |
| --- | --- |
| 概要数値のビジュアライゼーション | <ul><li>合計</li></ul> |
| コンポーネントを比較 | <ul><li>比較</li><li>VS</li><li>コントラスト</li><li>週単位</li><li>月々プラン</li><li>四半期単位</li><li>前年比</li></ul> |
| ドーナツの可視化 | <ul><li>割合</li><li>共有</li><li>配布</li><li>割合</li><li>貢献度</li><li>部分</li><li>部品</li></ul> |
| 折れ線グラフ | <ul><li>トレンド</li><li>[時間範囲]の[指標]</li></ul> |
| 棒グラフの作成 | <ul><li>[指標] by [Dimension]</li></ul> |

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

以下は、Customer Journey Analytics設定（データビュー、計算指標、セグメントなど）に関するベストプラクティスです。これにより、Data Insights Agentが正しいコンポーネントを見つけ、追加情報の入力を求めずに、よりクリーンな回答を返せるようになります。

* **必要なコンポーネントのバランスを取る**。 データセットのすべてのフィールドを指標またはディメンションコンポーネントとしてデータビューに追加しないでください。特に、分析で使用しないフィールドを追加しないでください。 一方、分析に必要なフィールドのみを厳密に制限しないでください。 データビューが限定的すぎると、AnalyticsとData Insights Agentの機能の柔軟性が制限されます。
* **わかりやすい表示名を常に使用する**。 指標コンポーネントまたはディメンションコンポーネントとしてデータビューで定義するすべてのフィールドに、わかりやすいコンポーネント名が付いていることを確認します。 わかりやすい名前でフィールド名を変更するプロセスは、Adobe Analytics ソースコネクタデータセットのフィールドに特に関連しています。 これらのフィールドには、`eVar41`や`prop25`など、わかりにくい名前が付いていることがよくあります。
* **固有の名前を使用**。 識別名は、データビューで指標とディメンションコンポーネントの両方と同じフィールドを使用する場合に特に関連します。 または、同じタイプの複数のコンポーネント（2つの異なる指標など）でフィールドを使用する場合、各コンポーネント設定が異なります。
* **コンポーネントの命名規則**&#x200B;を使用します。 コンポーネントの命名規則を使用して、コンポーネントをグループ化できます。 例えば、**[!UICONTROL Orders | Product]**&#x200B;と&#x200B;**[!UICONTROL Orders | Customer]**&#x200B;は、データに存在する可能性のある異なる注文指標を区別できます。
* **データ要素を使用**。 データディクショナリのコンポーネントに説明やその他の関連データを追加します。 Data Insights Agentでは現在、データ要素の説明とタグは使用されていませんが、将来は使用される可能性があります。
* **承認済みの計算指標を使用**。 承認済みの計算指標のみをデータビューのコンポーネントとして使用し、実験的な計算指標の使用を避けるプロセスに同意します。
* **必要なセグメントを共有**。 セグメントを共有し、Data Insights Agent プロンプトに必要なセグメントを表示します。
* **データビュー全体でコンポーネント名を標準化**。 複数のデータビューで同じフィールドをコンポーネントとして使用する場合は、そのコンポーネントに対して、わかりやすい名前と識別子を1つ使用してください。 名前と識別子が1つだけあれば、Data Insights Agentはコンテキストを失うことなくデータビューを切り替えることができます。


>[!MORELIKETHIS]
>
>[&#x200B; コンポーネント設定](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-dataviews/component-settings/overview)
>[データ辞書](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-components/data-dictionary/data-dictionary-overview)
>[計算指標を承認](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/cm-approving)
>[セグメントの共有](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-components/segments/seg-share)
