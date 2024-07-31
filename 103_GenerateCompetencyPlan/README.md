# 資格取得計画提案ソリューション

以下は資格取得ソリューションのデモ動画です。

https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/91d1cf29-834c-4fe0-80fc-84e3f2ad9fa1


> [!Note]
> ソリューションを利用した感想などはぜひ、[ギークのXアカウント](https://x.com/geekfujiwara/status/1797815867021131979)までお寄せください！


## 主要機能のご紹介

### キャンバスアプリ

簡単に資格、期間、受験者のレベルを選択するだけで、資格取得計画を生成AIが立案し、資格取得日をOutlookに登録することができます。

#### 計画の立案

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/0a588dda-cd0b-4195-9810-998e90be0e68)

#### 立案した計画の保存とOutlook予定表連携

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/f733cb66-66c8-42cf-bcea-94b45b1c01f7)

保存するタイミングでOutlookにイベントが登録されます。

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/c8ec3866-26e7-428a-a3c5-05e3cc315dfa)

[TrainingPlan_1_0_0_0_managed.zip](https://github.com/user-attachments/files/16435899/TrainingPlan_1_0_0_0_managed.zip)

### AI Builder 

生成AIのモデルは GPT-4を利用しています。

以下のようなプロンプトを記述しています。

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/df73dba6-550e-4e00-be12-521b2b70a24a)

```
学習の概要と、概算費用を含む必要な教材のリスト、最初に試験を申し込むなどの注意事項を説明してから、次に1週間毎の目標, タスク, 日本語の教材を含む学習計画を可能な限り詳細に生成してください。前提条件として、資格を取得する人のレベルはLevel であり、資格を取得する期間はTargetDuration であり、取得したい資格はCompetencyNameです。
```

### モデル駆動型アプリ

また、その生成した計画を一覧することができます。

#### ビュー

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/95959c11-756c-4644-a65e-6ac01d96ec40)

#### フォーム

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/c14061cd-94ff-46bf-a75c-d1a5d1c69061)

### Power Automate 

資格取得日が近づいたら、自動的に本人にリマインドされます。

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/4869fd19-e0a6-46d1-b4ef-13d03a744b73)

何日前にリマインドするのかは[環境変数](https://learn.microsoft.com/ja-jp/power-apps/maker/data-platform/environmentvariables)で設定することができます。

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/e2878ca6-8fa6-4b98-9daa-fac4928070a1)


## アーキテクチャ

仕組みとしては以下のコンポーネントが使われています。

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/b396e5fc-3ec9-4f64-b91c-f4d838e4532a)

## 前提条件

### 環境

環境にはDataverseが必要です。

### ライセンス

Power Apps Premium ライセンスが必要です。

## インポート手順

### 公式手順

[Microsoft 公式サイト](https://learn.microsoft.com/ja-jp/power-apps/maker/data-platform/import-update-export-solutions)にもソリューションのインポート方法が説明があります。

## ソリューションのインポート方法

### ソリューションの取得

[ソリューションはリリース](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/releases)から入手することができます。

### インポート手順


ソリューションをアップロードしてインポートします。

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/cc07158c-2cf2-47b8-a9c6-42ebca992536)


接続を作成します。

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/0b5dc8f7-d7e3-497b-9da2-9e0b10e26eb0)


資格を取得予定日に対して何日前にリマインドするかを環境変数で設定することができます。

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/bc1e6b11-5181-41ed-9965-d281200e2913)

インポートを実施します。

### データの作成

資格のデータを作成する必要があります。

会社で取得するべき資格の一覧などをExcel Onlineで開く機能などから一括で取り込むとよいでしょう。

モデル駆動型アプリの資格を開きます。

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/0baff0fe-2e58-494b-b23e-dfbf3a17c060)

「>」を選択します。
![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/01cf8774-a566-47f9-abb7-d2f08d2727a4)

Excel Onlineで開きます。

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/aeae12ee-aecd-4177-be53-4aee573b76a9)

こちらから一括で入力することができます。

![image](https://github.com/geekfujiwara/GenerateCompetencyPlanPowerApps/assets/96101315/186ab31e-a1c7-4fff-a4f2-59b30c04a822)

資格マスターを更新後、キャンバスアプリから資格を選択できるようになり、アプリを利用できるようになります。


以上、ご参考になれば幸いです。



