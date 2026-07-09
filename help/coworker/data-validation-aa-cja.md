---
title: Adobe AnalyticsからCustomer Journey Analyticsにアップグレードする際に、Coworkerでデータを検証する
description: Adobe Analyticsの管理者がCX Enterprise Coworker Data validation skillを使用して、移行中にAdobe AnalyticsとCustomer Journey Analytics データを比較する方法について説明します。
hold: true
source-git-commit: 850bfef76e3c3e081f9860b9757e5e5128383f76
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# Adobe AnalyticsからCustomer Journey Analyticsにアップグレードする際に、Coworkerでデータを検証する

CX Enterprise Coworkerには、Adobe AnalyticsからCustomer Journey Analyticsにアップグレードする際にデータを検証できる検証スキルが含まれています。 データ検証は、1回の会話で完了します。

このスキルは自動的に比較されます：

* 実装全体で個別に行うことができます。

* すべてのAdobe Analytics データビューに対するすべてのCustomer Journey Analytics レポートスイート。

これらの比較を行った後、AI主導のインサイトとレコメンデーションを生成し、Customer Journey Analyticsへのアップグレードを促進します。

## 始める前に

アップグレードの一環としてデータを検証するには、次のものが必要です。

* 検証するAdobe Analytics レポートスイート。

* 同じデータを含むCustomer Journey Analytics データビュー。

実装がどのように構築されているかを事前に知る必要はありません。 このスキルは、データがAnalytics ソースコネクタを介してマッピングされているか、2つの並列実装を介してマッピングされているかを自動的に検出するため、自身でそのコンテキストを提供する必要はありません。

## 検証セッションを開始

1. CX Enterprise Coworkerにログインします。

1. [!UICONTROL **新規チャット**]&#x200B;を選択します。

1. テキストフィールドで、担当者に対して、Adobe AnalyticsからCustomer Journey Analyticsへの移行を検証するように求めます。

   **プロンプト**

   > Adobe AnalyticsからCustomer Journey Analyticsへの自社のアップグレードの検証を支援します。

   リクエストはデータ検証スキルにルーティングされ、インタラクティブなセットアッププロセスが開始されます。

1. 設定プロセスには、次の表に示す質問が含まれます。 質問ごとに回答を選択し、[!UICONTROL **送信**]&#x200B;を選択します。

   | 質問 | その他のコンテキスト |
   |---------|----------|
   | [!UICONTROL **Analytics会社を選択**] | これがAdobe Analyticsのログイン会社です。 |
   | [!UICONTROL **レポートスイートを選択**] <!--In the UI, recommend change to "Select your Adobe Analytics report suite"--> | これは、Customer Journey Analytics データに対して検証するデータを含むAdobe Analyticsのレポートスイートです。 |
   | [!UICONTROL **Customer Journey Analytics データビューを選択**] | これは、選択したAdobe Analytics レポートスイートと同じデータを含むCustomer Journey Analyticsのデータビューです。 |

1. 続行する前に、セットアップの概要を確認して、適切なデータを検証していることを確認してください。 概要には、選択した会社、レポートスイート、データビュー、各システムの上位の指標とディメンションのプレビューが含まれます。

1. 次のセクションに進みます。[検証するデータを選択](#choose-the-data-to-validate)。

## 検証するデータの選択

個々の指標またはディメンションを検証することも、レポートスイートとデータビューに含まれるすべての指標とディメンションを検証することもできます。

1. 次のオプションから選択します。

   | 検証オプション | 説明 |
   |---------|----------|
   | [!UICONTROL **単一の指標の比較**] | Adobe AnalyticsとCustomer Journey Analyticsにおける1つの指標の傾向を比較します。 ページビューや訪問数など、特定の指標を素早く確認したい場合に使用します。 |
   | [!UICONTROL **単一ディメンションの比較**] | Adobe AnalyticsとCustomer Journey Analyticsのディメンションの内訳を比較します。 これは、特定のディメンションのマッピングまたは分類の違いを疑う場合に使用します。 |
   | [!UICONTROL **完全なレポートスイートとデータビュー監査**] | 1回の実行で最大20の指標とディメンションを比較できます。 移行の全体的な健全性を包括的に把握する場合に使用します。 |

1. 次のセクションに進みます。[分析を確認](#review-the-analysis)。

## 分析の確認

1. 分析を確認するには、次の各タブを選択します。

   | 「分析レビュー」タブ | 説明 |
   |---------|----------|
   | [!UICONTROL **全体的な一致率**] | Adobe Analytics レポートスイートのデータがCustomer Journey Analytics データビューのデータとどの程度一致しているかを示すパーセンテージ。 |
   | [!UICONTROL **重要なインサイト**] | 分析中に発見された重要なインサイト。 |
   | [!UICONTROL **概要**] | Adobe Analytics totals、Customer Journey Analytics totals、total variance、days passing、およびdays critical.<!--what are these?--> |
   | [!UICONTROL **日次トレンド**] | Adobe AnalyticsとCustomer Journey Analyticsのデータを並べて比較したグラフ。 |
   | [!UICONTROL **日別詳細**] | <!--what goes here?--> |

1. 分析を下にスクロールして、分析中に検出された追加のパターン、それらのパターンの原因、データの不一致を解決するために実行できるアクションを表示します。

1. 提案されたアクションが有効であることを確認してから、Adobe Experience PlatformまたはAdobe Analyticsで解決します。

1. （オプション）別の指標を分析するか、別のディメンションを分析するか、[検証するデータを選択](#choose-the-data-to-validate)で説明されているように、最大20個の指標とディメンションの別のレポートを実行して、分析を続行します。

