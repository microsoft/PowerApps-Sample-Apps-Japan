# SupportCopilot 問合せCopilot

Copilot からDataverse に問合せを登録、更新、削除を行うことが出来ます。また、自動的にカテゴリ分類を実施するAI Builder のAIプロンプトのモデルも含まれております。

![image](https://github.com/geekfujiwara/SupportCopilot/assets/96101315/09550b06-f342-41ff-a34e-984fd1c9ca1b)

デモ動画を作成しています。以下のようにCopilot とPower Apps を統合的に利用することが出来ます。

https://github.com/geekfujiwara/SupportCopilot/assets/96101315/143bfca0-e0df-4821-8641-1a5e824600a0

# ソリューション

[リリース](https://github.com/geekfujiwara/SupportCopilot/releases)ページからソリューションを取得することが出来ます。


# 前提条件

* Copilot Studio スタンドアローンライセンスが必要です。
* Power Apps Premium ライセンスが必要です。
* AI Builder のクレジットが必要です。


# 詳細

Power Apps モデル駆動型アプリで問合せを受付、クローズまで管理することが出来ます。

![image](https://github.com/geekfujiwara/SupportCopilot/assets/96101315/d6d00836-e161-4f18-ba0e-11174071cdb0)


Copilot により Dataverse に登録、更新、削除を行うことが出来ます。

![image](https://github.com/geekfujiwara/SupportCopilot/assets/96101315/3bb58822-4479-488c-beae-a44b570da957)

問合せを行うと、その結果として内容やDataverse で自動採番された番号を返します。

![image](https://github.com/geekfujiwara/SupportCopilot/assets/96101315/8d5db0b1-ba2c-4f9b-9ecf-14ab1bb37cdd)


クラウドフローは以下のようなフローが含まれています。

![image](https://github.com/geekfujiwara/SupportCopilot/assets/96101315/69a569d9-0607-4463-b970-4186e98e432e)

起票するときのフローは以下のようなフローになっています。

![image](https://github.com/geekfujiwara/SupportCopilot/assets/96101315/c5a90526-d170-48bb-b5b5-3c3c06967e86)


起票してみたが、問合せを変更したくなったり、取り消ししたいときの処理を行うフローも用意されており、会話フローに接続されています。

トピック内の会話のフローは以下のようになっています。

![image](https://github.com/geekfujiwara/SupportCopilot/assets/96101315/0f42249a-375c-48b4-a687-8c2e6fb080ae)

アクションに接続されているフローは以下のとおりです。

![image](https://github.com/geekfujiwara/SupportCopilot/assets/96101315/f40120de-cfe2-46a9-a9a4-a334827eb08a)

![image](https://github.com/geekfujiwara/SupportCopilot/assets/96101315/e88b4347-7d1f-46da-972d-a18990a479d7)


起票された、あるいは問合せ内容が変更されたときに起動するフローとして、自動的にカテゴリ分類を実施するAI Builder のAIプロンプトが含まれているフローもあります。

![image](https://github.com/geekfujiwara/SupportCopilot/assets/96101315/8acc8312-b071-442b-b5b5-10392ea9fb53)

カテゴリ分類を行うAIプロンプトは以下のようなプロンプトで構成されています。

![image](https://github.com/geekfujiwara/SupportCopilot/assets/96101315/e59f0b4a-639a-4466-babe-ae932ccd5b1d)

ビジネスプロセスフローで問合せへの回答を行うことが出来ます。

![image](https://github.com/geekfujiwara/SupportCopilot/assets/96101315/22aec125-bcd2-424f-b7ca-ae5930d77b32)

# ソリューション

[リリース](https://github.com/geekfujiwara/SupportCopilot/releases)ページからソリューションを取得することが出来ます。

