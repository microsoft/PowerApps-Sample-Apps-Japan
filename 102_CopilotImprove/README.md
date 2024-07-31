# Copilot 改善アプリの概要

Copilot Studio で作成したCopilot の生成型の回答の実行ログを収集して継続的な改善を行うためのアプリです。

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/56bdc708-8014-42fe-8fdf-2b67b02a6ddb)

Copilot for Microsoft 365 には対応しておりません。

Copilot 改善アプリ(CopilotImprove)はあくまでもDataverse に保存されているCopilot の実行履歴をJSON形式から情報を抽出、さらにUnicodeエスケープシーケンスとなっていしまっている会話内容を読める形式に変換、表示し、さらに改善活動につなげていくワークベンチを実行するアプリです。

参考までに、標準で会話履歴が表示されている`ConversationTranscript` テーブルには以下のように複雑に会話履歴が保存されております。

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/795f1184-9278-4e09-870e-94bcf24d897d)

これを利用しやすくしたい、ということで開発を思いつきました。

> [!Note]
> 動いたよ、できたよという結果は是非、 [ギークフジワラのXアカウント](https://x.com/geekfujiwara/) までメンションしてご報告ください！！

標準のレポートではCopilot 毎の情報は提供してくれますが、こちらのアプリは環境毎のCopilot の情報を提供してくれます。

Copilot の実際の改善活動を行うチームは、環境ごとに配置されている想定で作成しています。

例えば、環境が会社毎などで分けれれている場合、その会社ごとでCopilot の改善活動を行っていくのではないか、として想定しています。

> [!Note]
> テナント全体ではCoE Starter Kit による管理を想定しており、環境はこちらのアプリ、テナントはCoE Starter Kit という分担で考えております。

## 動画
1分程度で実際の改善の流れを紹介してみました。

https://github.com/geekfujiwara/CopilotImprove/assets/96101315/c02b9b4d-cd4f-434c-b596-ac056c78c7aa

# Copilot 改善アプリの利用イメージ

## 各種レポート

Copilot Studio で作成したCopilotの、環境内で生成型の回答(Generative Answers)を行った際、そしてその改善活動の各種レポートを確認することが出来ます。

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/82af7d91-e515-40b7-8b83-4bc29d00a6f8)

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/e101baf2-48f7-4116-a013-1246b8edd772)

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/378675fb-364c-4b39-82a6-981b1db51747)

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/0e685a51-b3fb-4b44-8c52-e74d163bfb36)

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/8dfd2f41-cfe8-4550-9ff3-4f5157b7ef1a)

## 利用イメージ

改善対象のログに対して、バックグラウンドで連携されてきます。

> [!Note]
> Copilot を利用しているユーザーや管理者はデータの収集に関して特に何もする必要がありません。
>
> 一度、このアプリを環境にインポートしたら自動的に収集されるようになります。
>
> ただし、データ収集まで1時間ほどのタイムラグがあります。

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/5f19e192-9b4a-4954-a6c9-1dc4697d5043)

詳細を確認するとメッセージとして送った内容と回答内容、そしてその結果等について確認することが出来ます。

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/682064ee-4660-458d-8a21-d1a601dfb313)

## 改善アクションへの活用

可視化できるだけでなく、担当者の割当や改善アクションにつなげることが出来ます。

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/2a4e2877-a211-4eb3-89fc-1270b7c5adf4)

ビジネスプロセスフローでステージを管理することも出来ます。

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/3a8d3270-0e9f-4d03-ac34-0564e6339b41)

## 生成AIのよる結果の確認

### 成功したパターン

回答の生成に成功した場合は「回答した」という結果となり、その応答も返ってきます。

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/c21b63d5-0337-47b4-9033-7ac9c130c969)

### 返答が実行されなかったパターン

不正なメッセージなどでは「OpenAI によってフィルターされた」などの履歴も確認することが出来ます。

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/d0067d71-7709-47de-892b-6825bdd6ea43)

Copilot Studio 側でコンテンツ モデレーションによってフィルターされた結果も反映されてきます。

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/22d75f3a-3d6f-4d0a-b66b-287e12e31418)

データソースに関連性が高い情報がなかったときには「検索結果なし」として返ってきます。

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/b37278e0-bce8-4bea-8b67-399cc14e2723)

## Power Automate で行っている処理

Power Automate クラウドフローにて各種変換、Dataverse カスタムテーブルである`Copilot 改善` テーブルへ格納処理を行っています。

`ConversationTranscript` テーブルにデータが作成されると、フローが起動します。そして、生成AIでの処理が行われると`GenerativeAnswersSupportData`に関する`Activity`が発生します。これを変換後格納しています。値がないときは`Copilot 改善`テーブルへの値の保存は実行されません。

![image](https://github.com/geekfujiwara/CopilotImprove/assets/96101315/d0638f2b-85af-4a4e-9a3f-5e4b4eb6f747)


# 環境へのインストール

## 前提条件

以下のライセンスが必要です。

* Copilot Studio
* Power Apps Premium またはPower Apps per app

## ソリューションのインポート

ソリューションは[リリース](https://github.com/geekfujiwara/CopilotImprove/releases)に提供されています。不定期でアップデートします。最新のリリースを利用するようにしてください。

> [!Note]
> アップデート情報は [ギークフジワラのXアカウント](https://x.com/Geekfujiwara) でご案内します。
>
> フォローしてお待ち下さい。

ソリューションをダウンロードして、Zip形式のままインポートを行います。

インポート後、カスタマイズをすべて公開し、クラウドフローがオフになっている場合オン(有効)にしてください。

ウイザードに則って行えば問題なくインポートができるはずです。ご不明な方はインポート方法は以下を参考にしてください。

[Power Appsのソリューションのインポート](https://learn.microsoft.com/ja-jp/power-apps/maker/data-platform/import-update-export-solutions)

