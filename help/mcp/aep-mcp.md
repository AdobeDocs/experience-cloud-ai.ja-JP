---
title: CX Coworker GatewayのAdobe Experience Platformツール
description: CX Coworker Gatewayを通じて利用できるAdobe Experience Platform ツールについて説明します。
source-git-commit: adb72f43865bee5b2b151a5a75994c5f3939c2d9
workflow-type: tm+mt
source-wordcount: '1372'
ht-degree: 8%

---


# Adobe CX Coworker GatewayのAdobe Experience Platformツール {#aep-mcp}

Adobe Experience Platform製品ツールを使用して、MCP対応クライアントからスキーマ、データセット、データガバナンス設定、クエリサービスリソース、監査イベントを調べることができます。 これらのツールは、組織が有効になっていて、ユーザーアカウントに必要なExperience Platform権限が付与されている場合、[Adobe CX Coworker Gateway](overview.md)から利用できます。

>[!AVAILABILITY]
>
>Experience Platformの製品ツールはBetaに搭載されています。 アクセスは招待状によってのみ行われ、Adobe組織の有効化が必要です。 [CX Coworker Gateway Tools](access.md)へのアクセスを参照してください。

## 概要

| ツール | 説明 | リソース | 機能 | ステータス |
| --- | --- | --- | --- | --- |
| `search_allowed_ip_ranges` | クエリサービス IP アクセス制限の取得 | Data Distiller Auth ・ IP範囲 | リスト | アクティブ |
| `search_audit` | Experience Platform全体のユーザーアクティビティ監査イベントのリスト | 監査クエリ ・監査イベント | リスト、アセットタイプ、アクション、ステータス、時間範囲でフィルタリング | アクティブ |
| `search_datasets` | データセットとバッチ取り込みのメタデータのクエリ | カタログ API ・ データセット、バッチ | リスト、取得、フィルター、リストの最後、リストのファイル | アクティブ |
| `search_class_relations` | Experience Platform ビジネスクラスの関係を検索 | クラスリレーション ・静的YAML インデックス | トークンによる検索、複数用語、部分一致 | アクティブ |
| `search_data_access` | 失敗した取り込みバッチからのファイルのリスト | Data Access API ・失敗したバッチ | 失敗したファイルのリスト | アクティブ |
| `search_data_lake` | データセットのメタデータとバッチの正常性の検査 | データレイク API ・ データセット、バッチ | 取得、サイズ取得、失敗したバッチの一覧表示 | アクティブ |
| `search_dule` | データガバナンスラベル、ポリシー、アクションのクエリ | データガバナンス ・ ラベル、ポリシー、marketing_actions | list, get, list enabled,evaluate | アクティブ |
| `search_query_service` | SQL クエリ、テンプレート、スケジュール、アラートのクエリ | クエリサービス ・ クエリ、テンプレート、スケジュール、アラート | リスト、取得、フィルター、取得の接続パラメーター | アクティブ |
| `search_schema_registry` | XDM スキーマ、フィールドグループ、クラス、タイプのクエリ | スキーマレジストリ ・ スキーマ、フィールドグループ、クラス、data_types、記述子 | リスト、取得、コンテナによるフィルタリング | アクティブ |

## ツールリファレンス

### search_allowed_ip_ranges

**リソース：** Data Distiller認証・ IP範囲
**ステータス：** アクティブ

現在のサンドボックス内のクエリサービスに対して設定されたすべてのIP アクセス制限を取得します。 組織IDと許可されるIP範囲のリストを返します。 Data Distiller アドオンを使用しているお客様のみが利用できます。

**機能：** クエリサービスで許可されているIP範囲のリスト

パラメーターがありません。

### search_audit

**リソース：**監査クエリ ・監査イベント
**ステータス：** アクティブ

Experience Platform サービス全体のユーザーアクティビティのタイムスタンプ付きレコードを一覧表示します。 アクションタイプ、ユーザーの電子メール、アセット情報、イベントステータスを返します。 `asset_type`と`action`を使用して結果を絞り込みます。 時間範囲が指定されていない場合は、デフォルトで過去7日間になります。 過去90日間の過去1000件のレコードとイベントに限定されます。

**機能：**&#x200B;監査イベントのリスト、アセットタイプ、アクション、ステータス、時間範囲、ページネーションでフィルタリング

**パラメーター：**

| パラメーター | 必須 | 説明 |
| --- | --- | --- |
| `action` | × | アクションタイプでフィルタリング。 共通の値（ORのコンマ区切り）: `Create`、`Delete`、`Update`、`Enable`、`Disable` |
| `asset_type` | × | アセットタイプでフィルタリング。 `Dataset`, `Schema`, `Segment`, `Destination`, `Source Data Flow`, `Merge Policy`, `Identity Namespace`, `Identity Graph`, `Sandbox`, `Role`, `Query`, `Scheduled Query`, `Datastream`, `Computed Attribute`, `Field Group`, `Class`, `Data Types`, `Account`, `Product Profile`, `Query Template`, `Work Order`, `Audit Logs`, `Access Control Policy`のいずれかである必要があります |
| `status` | × | イベントステータスでフィルタリング。 値：`Success`、`Failure`、`Allow`、`Deny`。 OR用のカンマ区切り |
| `start_time` | × | 最も早いタイムスタンプ。 ISO 8601 UTC （ミリ秒） （例：`2024-01-15T00:00:00.000Z`） |
| `end_time` | × | 最新のタイムスタンプ。 ISO 8601 UTC （ミリ秒） |
| `property_filter` | × | 生のフィルター式（例：`action==create`）。 上記の専用パラメーターを優先する |
| `orderby` | × | 並べ替え順序：`timestamp` （asc）または`-timestamp` （desc） |
| `limit` | × | 結果の最大数（3 ～ 1000、デフォルト 50） |
| `start` | × | ページネーションのオフセット 各ページの制限値増分 |
| `query_id` | × | 同じクエリを繰り返す前の応答のクエリ ID |

### search_datasets

**リソース：** カタログ API ・ データセット、バッチ
**ステータス：** アクティブ

Experience Platform カタログサービスの統合ディスパッチツール。 データセットのメタデータ（スキーマ参照、タグ、作成情報）またはバッチ取り込みレコード（ステータス、指標、ファイルリスト）のクエリを実行できます。 `dataset/list`を使用してデータセットを検索し、`batch/list`を使用して取り込みの正常性を確認し、`batch/list_files`または`batch/get_meta_files`を使用して特定のバッチコンテンツを検査します。 すべての操作は読み取り専用です。

**機能：** データセットのリスト、データセットの取得、バッチのリスト、データセットごとの最後のバッチのリスト、バッチファイルのリスト、バッチメタファイルの取得（行エラー、入力ファイル）

**パラメーター：**

| パラメーター | 必須 | 説明 |
| --- | --- | --- |
| `entity_type` | ○ | `dataset` または `batch` |
| `operation` | ○ | `list`, `get`, `list_last`, `list_files`, `get_meta_files`. 有効なコンボ：データセット→リスト、取得、5つすべて→バッチ |
| `resource_id` | × | データセットまたはバッチ ID: `dataset/get`、`batch/get`、`batch/list_files`、`batch/get_meta_files`に必要 |
| `query_params.limit` | × | 1 ページあたりの最大結果（最大100）。 すべてのリスト操作に適用 |
| `query_params.start` | × | ページネーションのオフセット すべてのリスト操作に適用 |
| `query_params.order_by` | × | 並べ替え方向（例：`asc:created,updated`）。 すべてのリスト操作に適用 |
| `query_params.properties` | × | コンマ区切りプロパティの許可リストに加える。 データセット/リスト、データセット/取得、バッチ/リスト、バッチ/リスト_lastに適用 |
| `query_params.name` | × | 名前でデータセットをフィルタリング（データセット/リストのみ） |
| `query_params.tags` | × | タグ別にデータセットをフィルタリング （例：`unifiedProfile:enabled:true`） （データセット/リストのみ） |
| `query_params.property_filter` | × | 応答オブジェクトの正規表現フィルター（データセット/リストおよびバッチ/リスト） |
| `query_params.status` | × | ステータスでバッチをフィルタリング：`success`、`failed`、`loading`、`active` （バッチ/リストのみ） |
| `query_params.dataset_id` | × | バッチを特定のデータセット（batch/listおよびbatch/list_last）にスコープ付けする |
| `query_params.created_after` | × | Unix タイムスタンプの後に作成されたバッチをミリ秒単位でフィルタリングします（バッチ/リストのみ） |
| `query_params.created_before` | × | Unix タイムスタンプの前に作成されたバッチをミリ秒単位でフィルタリングします（バッチ/リストのみ） |
| `query_params.last_batch_status` | × | 最後のバッチステータスでフィルタリング（batch/list_lastのみ） |
| `query_params.aggregate` | × | ルートレベルで集計された指標を返します（バッチ/取得のみ） |
| `query_params.path` | × | ダウンロードするMeta ファイル：`row_errors`、`input_files`、`row_errors_sample.json` （batch/get_meta_filesのみ） |

### search_class_relations

**リソース：** クラス リレーション ・静的YAML インデックス
**ステータス：** アクティブ

静的な`class_relations_v1.yaml` インデックスを使用して、名前でExperience Platform ビジネスクラスの関係を検索します。 Experience Platform API呼び出しは行われません。 1つの用語またはコンマ区切りの用語を受け入れます。各用語は、部分的なトークン照合を使用してクラス名と照合されます。 順方向リレーション（各クラスが指す）と逆方向リレーション（クラスが指す）を持つ一致するクラスを返します。 クエリ、データフロー、スキーマコンポジションを構築する前に、エンティティの関係を把握するために使用します。

**機能：** トークンによる検索、複数用語のコンマ区切り検索、部分的なトークン一致、双方向の同義語拡張

**パラメーター：**

| パラメーター | 必須 | 説明 |
| --- | --- | --- |
| `query` | ○ | 検索するビジネスクラス名またはオブジェクトタイプ。 トークンの一部の一致をサポートしています（`dat`は`dataset`、`data_type`などに一致します）。 複数のコンマ区切りの用語を渡して、一度に複数のクラス （例：`dataset, schema`）を検索します。 |
| `n` | × | 返される一致した結果の最大数（デフォルトは5、最小1） |

### search_data_access

**リソース：** データ アクセス API ・失敗したバッチ
**ステータス：** アクティブ

Experience Platform データ取り込みに失敗したバッチからファイルにアクセスします。 失敗したバッチに属するファイルを一覧表示するには、`failed_batch/list_failed`を使用します。 すべての操作にバッチ IDが必要です。 注意：`file/get`と`dataset/preview`は、実際のレコードデータを公開しているため、無効になっています。 すべての操作は読み取り専用です。

**機能：**&#x200B;失敗した取り込みバッチからのファイルのリスト

**パラメーター：**

| パラメーター | 必須 | 説明 |
| --- | --- | --- |
| `entity_type` | ○ | `failed_batch` – 失敗した取り込みバッチからのファイルのリスト |
| `operation` | ○ | `list_failed` — サポートされている操作は1つだけです |
| `resource_id` | ○ | 失敗したバッチのバッチ ID |
| `query_params.start` | × | ページング開始インデックス （例：`1`） |
| `query_params.limit` | × | ページあたりの結果の数（例：`10`） |
| `query_params.path` | × | ファイル名の完全なフィルター（例：`profiles.csv`） |


### search_data_lake

**リソース：** Data Lake API ・ データセット、バッチ
**ステータス：** アクティブ

データレイク層からデータセットとバッチメタデータを検査します。 完全なメタデータには`get`、ストレージと取り込みサイズの指標には`get_size`、タイムウィンドウ内の取り込み失敗を監視するには`list_failed`を使用します。 `list_failed`に期間が指定されていない場合は、過去7日間がデフォルトになります。 すべての操作は読み取り専用で、リソース IDが必要です。

**機能：** データセット/バッチメタデータの取得、ストレージサイズ指標の取得、失敗したバッチの時間枠内での一覧表示

**パラメーター：**

| パラメーター | 必須 | 説明 |
| --- | --- | --- |
| `entity_type` | ○ | `dataset` または `batch` |
| `operation` | ○ | `get`, `get_size`, `list_failed`. `list_failed`は`batch` エンティティ型のみをサポートしています |
| `resource_id` | ○ | データセット IDまたはバッチ ID。 `list_failed`の場合：スコープを設定するためのデータセット IDが失敗しました |
| `query_params.created_after` | × | 時間ウィンドウの開始。 Unix タイムスタンプ （ミリ秒） |
| `query_params.created_before` | × | 時間ウィンドウの終了。 Unix タイムスタンプ （ミリ秒） |
| `query_params.limit` | × | 1 ページあたりの最大結果（最大100） |
| `query_params.order_by` | × | 並べ替え方向（例：`desc:created`） |

### search_dule

**リソース：** データガバナンス ・ ラベル、ポリシー、marketing_actions
**ステータス：** アクティブ

Policy Service APIに対して、データ使用ラベル、ポリシー、マーケティングアクションをクエリします。 `marketing_action/evaluate`を使用して、特定のラベルを持つデータに対するマーケティングアクションがガバナンスポリシーに違反するかどうかをテストします。 すべての操作は読み取り専用です。

**機能：** データ使用ラベルのリスト/取得、ポリシーのリスト/取得、有効なポリシーのリスト、マーケティング アクションのリスト/取得、ラベルに対するマーケティング アクションの評価

**パラメーター：**

| パラメーター | 必須 | 説明 |
| --- | --- | --- |
| `entity_type` | ○ | `label`、`policy`または`marketing_action` |
| `operation` | ○ | `list`、`get`、`list_enabled` （ポリシーのみ）、`evaluate` （marketing_actionのみ）。 `list_enabled`には範囲が必要ありません |
| `scope` | × | `core` （Adobe定義）または`custom` （組織定義）です。 `list`、`get`、`evaluate`には必須です。`list_enabled`には使用されません |
| `resource_id` | × | ラベル名、ポリシーID、またはマーケティングアクション名。 `get`および`evaluate`に必要 |
| `query_params.dule_labels` | × | コンマ区切りのラベル （例：`C1,C3`）。 `marketing_action/evaluate`には必須です。`policy/list`にはオプションのフィルターがあります |
| `query_params.limit` | × | 最大結果 |
| `query_params.start` | × | 以前の応答の`_page.next`値からのページネーション カーソル |
| `query_params.orderby` | × | コンマ区切りのソートフィールド |
| `query_params.property_filter` | × | フィルター式（例：`name==C1`） |
| `query_params.marketing_action` | × | このマーケティングアクションを参照するポリシーにポリシーリストを制限する（ポリシー/リストのみ） |
| `query_params.include_draft` | × | `marketing_action/evaluate`にドラフトポリシーを含める（デフォルト：ENABLED ポリシーのみ） |

### search_query_service

**リソース：** クエリサービス ・ クエリ、テンプレート、スケジュール、スケジュール実行、接続、アラートサブスクリプション
**ステータス：** アクティブ

Query Serviceのリソース向けの統合ツール。 アドホッククエリ、保存されたSQL テンプレート、スケジュールされたクエリとその実行、インタラクティブ接続パラメーター（psql/JDBC クライアント用）、アラートサブスクリプションのリストと取得。 クエリリストの場合は、デフォルトで`isService==false,isParentLevel==true`に設定して、内部トラフィックを除外します。 すべての操作は読み取り専用です。

**機能：** リスト/取得クエリ、リスト/取得テンプレート、リスト/取得スケジュール、リスト/取得スケジュール実行、接続パラメーターの取得、アラート サブスクリプションのリスト

**パラメーター：**

| パラメーター | 必須 | 説明 |
| --- | --- | --- |
| `entity_type` | ○ | `query`, `query_template`, `schedule`, `schedule_run`, `connection`, `alert_subscription` |
| `operation` | ○ | `list`, `get`, `get_connection_params`, `list_by_u...` |
