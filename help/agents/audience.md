---
title: Audience Agent
description: Audience Agentを使用して、オーディエンスの作成、オーディエンスの変更の表示、重複オーディエンスの検出、オーディエンスインサイトの表示を行う方法について説明します。
TQID: https://experienceleague.adobe.com/574QhqKI0YDoPHD9BFmB6jl-HET3zVom3eD4cJQABSE
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: dd7883d8eccab3b0f006d55a850248e1c347d7e7
workflow-type: tm+mt
source-wordcount: 1242
ht-degree: 2%

---

# Audience Agent

>[!AVAILABILITY]
>
>Audience Agentは、AI アシスタントにアクセスできるすべてのお客様が利用できます。 ただし、Audience Agent機能を完全に使用するには、次の権限が必要です。
>
>**セグメントを表示**：この権限を持つユーザーは、Audience Agentを使用して、AI アシスタントで直接オーディエンスに関するインサイトを表示できます。
>
>**セグメントの管理**：権限を付与するには、Audience Agentを使用して、AI アシスタントで直接、新しいオーディエンスを作成できます。

Audience Agentでは、大幅なオーディエンスサイズの変更の検出、重複するオーディエンスの検出、オーディエンスインベントリの調査、オーディエンスのサイズの取得など、オーディエンスに関するインサイトを表示できます。

>[!SLIDE](audience-agent-overview)

## サポートされるユースケース

AI アシスタント内のAudience Agentは、次のユースケースをサポートしています。

- 会話形式でオーディエンスを探索
   - 既存オーディエンスのオーディエンスサイズの特定
   - 次の名前の完全または部分的な属性に基づいてオーディエンスを検索します
   - 重複オーディエンスの検出
   - オーディエンスの定義に使用できるXDM フィールドの詳細
- オーディエンスサイズの大幅な変化を検出
   - これにより、急激に増加または減少したオーディエンスを発見することができ、潜在的な市場の変化をより適切に分析することができます
- オーディエンスの作成
   - このスキルでは、指定された属性とイベントに基づいてオーディエンスを作成できます
   - さらに、このスキルでは、オーディエンスを構築する前にオーディエンスの潜在的な規模を推定し、最も効果的なオーディエンスをアクティベーションする前に迅速に反復することができます

<!--
  - Find your audience size and detect significant changes in audience size
  - This lets you find audiences that have suddenly grown or shrunk, letting you better analyze potential market changes
- Detect duplicate audiences
  - This lets you reduce redundancies with your created audiences
- Find audiences based on full or partial attributes named
  - This lets you more easily navigate through your audience inventory
- Discover XDM fields you can use to define an audience
  - This skill lets you more easily identify the right fields to use in your audience based on context and relevance 
-->

Audience Agentでは、現在&#x200B;**次の機能はサポートされていません。**

- 目標ベースのオーディエンス探索
   - 目標に基づくオーディエンスの探索により、購買傾向やコンバージョン傾向などのマシンラーニングモデルを適用することで、ビジネス目標に即した関連データセットやプロファイルを発見できます。

さらに、Audience Agentを使用する場合は、次の制約を考慮する必要があります。

- Audience Agentでデータを処理するには、少なくとも24時間が必要です
   - 例えば、**では、過去24時間以内にデータを検索するクエリを**&#x200B;できません。 最低でも過去48時間以内に確認する必要があります。
- Audience Agentでは、次のオーディエンスタイプのみがサポートされます。
   - バッチセグメント化を使用して評価される&#x200B;**人物ベースの** オーディエンス
   - 次の使用例の&#x200B;**アカウントベース**&#x200B;のオーディエンス：
      - 会話型オーディエンスの探索
      - 重複オーディエンス検出

## サンプルプロンプト

次の例は、Audience Agentのプロンプトと応答の例です。

### 会話型オーディエンスの探索

富裕層の購入者向けのフィールドを表示する。

+++ 応答

![AI アシスタントに、裕福な購入者に関連するフィールドを表示するテーブルが表示されます。](./images/audience/affluent-buyers.png)

+++

過去30日間にキャンペーンでアクティブ化または使用されていないオーディエンスは？

+++ 応答

![AI アシスタントには、過去30日間にキャンペーンでアクティブ化または使用されていないオーディエンスを表示するテーブルが表示されます。](./images/audience/not-activated.png)

+++

過去3か月間に新しい宛先にマッピングされたすべてのオーディエンスを一覧表示します。

+++ 応答

![AI アシスタントには、過去3か月間に新しい宛先にマッピングされた1人のオーディエンスが一覧表示されます。](./images/audience/new-destination.png)

+++

オーディエンスサイズが最も大きいアカウントオーディエンスとそのサイズは何ですか？

+++ 応答

![AI アシスタントに、最大のアカウントオーディエンスを表示するテーブルが表示されます。](./images/audience/largest-account-audience.png)

+++

### 重複オーディエンスの検出

同じまたは類似の説明を持つオーディエンスはありますか？

+++ 応答

![AI アシスタントは、セグメント定義と、同じセグメント定義を持つオーディエンスの名前を含むテーブルを表示します。](./images/audience/similar-descriptions.png)

+++

同じルールを持ちながら、名前が異なるオーディエンスを特定できます。

+++ 応答

![AI アシスタントは、同じオーディエンスルールを共有するオーディエンスの名前を含むテーブルを表示します。](./images/audience/same-rules-different-names.png)

+++

同じルールを持つが異なるアクティベーション宛先を持つオーディエンスをすべて表示します。

+++ 応答

![AI アシスタントは、異なる宛先に対するセグメント定義が重複していないことを示します。](./images/audience/same-rules-different-destinations.png)

+++

同じルールを持ちながら、名前が異なるアカウントオーディエンスを特定します。

+++ 応答

![AI アシスタントは、同じオーディエンスルールを共有するアカウントオーディエンスの名前とIDを含むテーブルを表示します。](./images/audience/duplicate-account-audience.png)

+++

### オーディエンスサイズの取得

オーディエンス「California_f153e1のゴールドスター会員」の現在のサイズはどのくらいですか？

+++ 応答

![AI アシスタントは、質問されたオーディエンスの現在のサイズを示します。](./images/audience/current-size.png)

+++

最大のオーディエンスは何か？

+++ 応答

![AI アシスタントは、名前とオーディエンス IDを含む、最も多くのプロファイルを持つオーディエンスに関する情報を提供します。](./images/audience/largest-audience.png)

+++

### オーディエンスサイズの大幅な変化を検出

先週20%以上増加したオーディエンスはどれですか？

+++ 応答

![AI アシスタントは、クエリに一致するすべてのオーディエンスの名前を一覧表示するテーブルを表示します。 また、増加率、現在のオーディエンスサイズ、および以前のオーディエンスサイズも表示されます。](./images/audience/increase-past-week.png)

+++

先月10%以上減少したオーディエンスはどれですか？

+++ 応答

![AI アシスタントは、クエリに一致するすべてのオーディエンスの名前を一覧表示するテーブルを表示します。 現在のオーディエンスサイズ、以前のオーディエンスサイズ、および古いオーディエンスサイズの日付も表示されます。](./images/audience/decrease-month.png)

+++

「最も急成長しているオーディエンスは何か？」

+++ 応答

![AI アシスタントは、最も急速に成長しているオーディエンスの名前と、現在のサイズと成長の割合を示します。](./images/audience/fastest-growing.png)

+++

### オーディエンスの作成

>[!AVAILABILITY]
>
>Agent Orchestrator エクスプローラープログラムの一部である場合にのみ、オーディエンスを作成スキルを使用できます。 詳しくは、Adobe カスタマーケアにお問い合わせください。

Audience Agentでオーディエンスを構築する場合、AI アシスタントがプランを案内します。 例えば、「カリフォルニア在住の人で構成されるオーディエンスを作成する」と依頼できます。 次に、AI Assistantは、オーディエンスの作成に着手する計画をリストします。

+++ 応答

![AI アシスタントは、オーディエンスを作成する計画を表示します。](./images/audience/audience-create-plan.png)

+++

この計画は、次の3つのステップで構成されています。

1. [オーディエンス特性の特定](#identify)
2. [オーディエンスサイズの推定](#estimate)
3. [新しいオーディエンスの作成と維持](#create)

#### オーディエンス特性の特定 {#identify}

![&#x200B; オーディエンスの特徴を特定するための計画の手順1。](./images/audience/plan-step-1.png){align="center" width="80%"}

プランを承認すると、AI アシスタントは、最初のクエリにもとづいてオーディエンスの特徴を取得します。

+++ 応答

![&#x200B; ユーザークエリに基づくオーディエンス定義。](./images/audience/audience-create-definition.png)

このクエリでは、AI Assistantがカリフォルニア州に住む人物を探す関連するProfile Query Language（PQL）を生成します。 このユースケースでは、PQL クエリは次のようになります。

```sql
homeAddress.state.equals("California", false)
```

PQLについて詳しくは、[PQLの概要](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/pql/overview)を参照してください。

+++

AI アシスタントのオーディエンス定義が正しい場合は、承認して次のステップに進むことができます。

#### オーディエンスサイズの推定 {#estimate}

![潜在的なオーディエンスのサイズを見積もるプランの手順2。](./images/audience/plan-step-2.png){align="center" width="80%"}

特定されたオーディエンスの特性を承認すると、AI アシスタントは、潜在的なオーディエンスのサイズとオーディエンス定義の詳細を推定します。

+++ 応答

![潜在的なオーディエンスのサンプル推定値が表示されます。 推定サイズとセグメント定義が表示されます。](./images/audience/audience-create-estimate.png)

+++

見積もりが正しく見える場合は、承認して次のステップに進むことができます。

#### 新しいオーディエンスの作成と維持 {#create}

![&#x200B; オーディエンスの作成を完了するプランの手順3。](./images/audience/plan-step-3.png){align="center" width="80%"}

最後に、オーディエンスの特徴とサイズが正しく見える場合は、オーディエンスの作成を承認または却下できます。

+++ 応答

まず、提供されたデータグリッドを通じて、提案されたオーディエンスを確認できます。

![&#x200B; レビュー画面が表示されます。](./images/audience/audience-create-review.png)

オーディエンスが正しく見える場合は、**[!UICONTROL 作成]**&#x200B;を選択して提案を承認し、オーディエンスの作成を完了できます。

![&#x200B; オーディエンスに対する完全な提案が表示されます。](./images/audience/audience-create-proposal.png)

+++

これでオーディエンスが作成されました。

![&#x200B; オーディエンスの提案が承認され、オーディエンスが作成されました。](./images/audience/audience-finish-create.png){align="center" width="80%"}

## 次の手順

このガイドを読めば、Audience Agentとそのサポートする機能について理解を深めることができます。 Adobe Experience Platformのエージェントについて詳しくは、[Agent Orchestratorの概要](./agent-orchestrator.md)を参照してください。

