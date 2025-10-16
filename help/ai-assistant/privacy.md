---
title: AI アシスタントでのプライバシー、セキュリティ、ガバナンス
description: AI アシスタントのプライバシー、セキュリティ、ガバナンス手法について説明します。
source-git-commit: 4bb6da3fe1abee98446df62c94730274e0931493
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# AI アシスタントでのプライバシー、セキュリティ、ガバナンス

Adobe Experience Platformの AI アシスタントは、プライバシー、セキュリティ、ガバナンスを最前線で考慮して構築されています。

このドキュメントでは、AI アシスタントに期待できる顧客の信頼に焦点を当てた機能について説明します。

* 現在、AI アシスタントは、トレーニング目的であっても、個人データを使用していません。
* AI アシスタントは、消費者データを認識していません。
* 既存のすべての [&#x200B; アクセス制御 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/home) ポリシーは、AI アシスタントによって順守されます。

   * 新しい属性ベースのアクセス制御ポリシーは、最大 24 時間が経過すると AI Assistant に反映されます&ast;

* AI アシスタントとやり取りするための明示的な権限を付与される必要があります。

   * [&#x200B; 権限 UI](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/abac/permissions-ui/browse) を使用して、Experience PlatformとJourney Optimizerに異なる権限を設定したり、[Admin Console](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/ui/browse) を使用してCustomer Journey Analyticsに権限を割り当てたりできます。
   * 権限は粒度が細かく、サンドボックス管理者は、どのユーザーに異なる質問カテゴリ（AI アシスタントを使用した製品ナレッジベースの質問または運用インサイトに関する質問）を依頼できるかを設定できます。

* AI アシスタントは、Adobe Experience Platform Healthcare Shield と組み合わせて使用する場合の、HIPAA 対応の機能です。
* 以前に AI アシスタントとやり取りしたログを 30 日間の保持ポリシーで表示できます。
* AI アシスタントは、ユーザープロンプトに答える際に、サンドボックス固有のデータと公開Adobe ドキュメントに基づいています。 データは、サンドボックス間で共有されません。
* AI アシスタントに指定したプロンプトは、他の顧客とは共有されません。

&ast; *つまり、フィールドやオブジェクトに新しいラベルが追加された場合や、新しいポリシーが作成された場合、AI アシスタントは最長で 24 時間かかるようになります。 この 24 時間、新たにアクセスを制限されたユーザーは、引き続きこれらのフィールドやオブジェクトにアクセスできます。*
