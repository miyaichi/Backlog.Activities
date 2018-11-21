# Backlog Activities

Backlog API ( https://developer.nulab-inc.com/ja/docs/backlog/ ) のうち、最低限必要なものだけ実装しています。

認証はAPIキー方式のみをサポートしています。APIの設定( https://backlog.com/ja/help/usersguide/personal-settings/userguide2378/ )を参照し、APIキーを登録してください。

## Get Issues
課題一覧を取得します。（ https://developer.nulab-inc.com/ja/docs/backlog/api/2/get-issue-list/ )

**Input**

| パラメーター名  | 内容 |
| --------------- | ---- |
| SpaceName       | スペースID |
| APIKey          | API キー |
| ProjectIDs      | プロジェクトのID(複数の場合はカンマ区切り) |
| AssigneeIDs     | 担当者のID(複数の場合はカンマ区切り) |
| StatusIDs       | 状態のID(複数の場合はカンマ区切り) |

**Output**

| パラメーター名  | 内容 |
| --------------- | ---- |
| Issues          | 課題一覧（DataTable）|

## Get Issue Data
課題の情報を取得します。（ https://developer.nulab-inc.com/ja/docs/backlog/api/2/get-issue/ )

**Input**

| パラメーター名  | 内容 |
| --------------- | ---- |
| SpaceName       | スペースID |
| APIKey          | API キー |
| IssueId         | 課題のID |

**Output**

| パラメーター名  | 内容 |
| --------------- | ---- |
| IssueData       | 取得した課題の情報(JObject) |


## Update Issue
課題の情報を更新します。( https://developer.nulab-inc.com/ja/docs/backlog/api/2/update-issue/ )

**Input**

| パラメーター名  | 内容 |
| --------------- | ---- |
| SpaceName       | スペースID |
| APIKey          | API キー |
| IssueId         | 課題のID |
| Summary         | 課題の件名 |
| ParentIssueId   | 課題の親課題のID |
| Description     | 課題の詳細 |
| StatusId        | 状態のID |
| ResolutionId    | 完了理由のID |
| StartDate       | 課題の開始日 (yyyy-MM-dd) |
| DueDate         | 課題の期限日 (yyyy-MM-dd) |
| EstimatedHours  | 課題の予定時間 |
| ActualHours     | 課題の実績時間 |
| IssueTypeId     | 課題の種別のID |
| CategoryIds     | 課題のカテゴリーのID(複数の場合はカンマ区切り) |
| VersionIds      | 課題の発生バージョンのID(複数の場合はカンマ区切り) |
| MilestoneIds    | 課題のマイルストーンのID(複数の場合はカンマ区切り) |
| PriorityId      | 課題の優先度のID |
| AssigneeId      | 課題の担当者のID |
| NotifiedUserIds | 課題の登録の通知を受け取るユーザーのID(複数の場合はカンマ区切り) |
| AttachmentIds   | 添付ファイルの送信APIが返すID(複数の場合はカンマ区切り) |
| Comment         | コメント |
