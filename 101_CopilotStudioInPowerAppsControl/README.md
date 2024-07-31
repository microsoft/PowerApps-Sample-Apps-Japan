# CopilotStudioinPowerAppsControl
Copilot Studio で作成したチャットボットをPower Apps のコントロールとして埋め込むアプリです。レスポンシブデザインに対応しています。

## 前提条件

* Power Apps Premium ライセンスが必要です。
* 画面のレイアウトをレスポンシブにするために設定から倍率を変更をオフにします。

![image](https://github.com/geekfujiwara/CopilotStudioinPowerAppsControl/assets/96101315/bd7ce15e-92c7-4105-a994-04fd2c012aac)


## 設定手順

以下のチャットボットコントロールのコードをコピーし、Power Apps キャンバスアプリの作成画面 (Power Apps Studio)にコードとして貼り付けます。

### チャットボットコントロールのコード

```
- Chatbot1:
    Control: Chatbot
    Properties:
      EnvironmentId: =""
      SchemaName: =""
      AlignInContainer: =AlignInContainer.Center
      FillPortions: =1
      Width: =Parent.Width
      Height: =Parent.Width
```

### 貼り付け方法

こちらのようにスクリーン上で右クリックをして貼り付けを行います。

![image](https://github.com/geekfujiwara/CopilotStudioinPowerAppsControl/assets/96101315/be9e67ae-3670-44ab-ba1e-756a7bc68b94)

これによりチャットボットコントロールを埋め込むことができます。

![image](https://github.com/geekfujiwara/CopilotStudioinPowerAppsControl/assets/96101315/f3e5c866-cdc5-4ccb-91b3-15e1023abd79)

### チャットボットの設定

Copilot Studio で作成したキャットボットを選択することで、Power Apps に埋め込むことができます。

![image](https://github.com/geekfujiwara/CopilotStudioinPowerAppsControl/assets/96101315/e1cdc821-089b-4aef-a0f6-458620eab1b8)


## 利用方法

再生するとこちらのように表示されます。

![image](https://github.com/geekfujiwara/CopilotStudioinPowerAppsControl/assets/96101315/b57153d8-8547-44f8-a397-74a84ddb1cff)

スマートフォンのレイアウトにも対応しています。

![image](https://github.com/geekfujiwara/CopilotStudioinPowerAppsControl/assets/96101315/c59f2062-23e3-43b8-9d35-d85278771faa)

もしクイック回答を設定しているとこちらのように表示されますので、選択するだけで利用することができます。

![image](https://github.com/geekfujiwara/CopilotStudioinPowerAppsControl/assets/96101315/1a2db274-9b9f-4435-bac1-51eacdf9b272)

SharePoint の接続は、Microsoft の認証で通過することができます。Entra IDの設定の必要なく利用することができます。

![image](https://github.com/geekfujiwara/CopilotStudioinPowerAppsControl/assets/96101315/6537d658-b5c1-4e15-8f3c-f63129772d6e)



