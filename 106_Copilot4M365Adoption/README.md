# Copilot4M365Adoption

Copilot Adoption Platform (以下CAP)は、Copilot for M365 の活用促進を支援するゲーミフィケーションプラットフォームです。

CAP はPower Platform をベースとしています。

![image](https://github.com/user-attachments/assets/ee1f2cb7-2533-452c-9447-7963da4d2966)

レスポンシブデザインに対応しています。

![image](https://github.com/user-attachments/assets/e1f51730-b21b-45e4-9d72-a855e43fce3a)

アクションに活用するため利用状況が可視化でき人気コンテンツから必要なコンテンツを確認することができます。

![image](https://github.com/user-attachments/assets/5e1996c7-7f7e-4ace-85a2-6fc411b5ac86)

> [!Note]
> 動いたよ、できたよという結果は是非、 [ギークフジワラのXアカウント](https://x.com/geekfujiwara/status/1816394470998626456) までメンションしてご報告ください！！

## アーキテクチャ

CAP は2種類のPower Apps で作成されています。

* モデル駆動型アプリ: CoE チーム
* キャンバスアプリ: 利用者

アーキテクチャはこちらのようになっており、データは一つのDataverse で共有されています。

先にモデル駆動型アプリで設定をして、利用者の方々にご利用いただきます。

![image](https://github.com/user-attachments/assets/ad133dc6-d393-468e-8108-554be5bf71e7)

# コンポーネント別の説明

## CoEチーム向けアプリ

https://github.com/user-attachments/assets/16fab13c-f386-4c75-8f01-7124d3186cb4

### 可視化

学習リソースの視聴やイベント参加などでもらえるポイントをランキング形式で可視化

![image](https://github.com/user-attachments/assets/c70ded54-befc-4a95-9847-faea308ae6e0)

ユーザーがよく利用しているイベントや学習リソース、プロンプトを可視化

![image](https://github.com/user-attachments/assets/1afdaf16-b633-4baa-a4f4-0cae3082881b)

イベントや学習リソース、プロンプトのカテゴリ別の数量を表示

![image](https://github.com/user-attachments/assets/77d0ef6e-e173-4f3a-bb13-3ef217d6296d)

### トレーニングの提供やプロンプトのテンプレート化

ユーザーに提供したいプロンプトを追加することができます。

![image](https://github.com/user-attachments/assets/a7f65693-920d-49e0-91b5-0e4f4d0b2470)

ユーザーに提供したいイベントを追加することができます。

![image](https://github.com/user-attachments/assets/a1c96660-f959-4da0-9431-40fd483c1d1e)

ユーザーに提供したい学習リソースを追加することができます。

![image](https://github.com/user-attachments/assets/2c910626-198b-439d-8e0a-1ce2000baad8)

### ゲーミフィケーションの設定

イベントや学習リソース、プロンプトを利用するとその種類によって付与されるポイントが異なります。その設定を行うことができます。

![image](https://github.com/user-attachments/assets/47d26e6e-af4f-4d8f-98ec-3084b5f0af18)

ポイントが貯まると、バッジを取得することができます。

![image](https://github.com/user-attachments/assets/8c1f5856-ee28-421b-aeff-3b4ad5c89377)


バッジはぽポイント到達だけではなく、特定のイベントに参加したユーザーに与えることもできます。

![image](https://github.com/user-attachments/assets/75849c93-3de0-4b70-9c46-e5ff56572b3f)

## 利用者向けのアプリ

https://github.com/user-attachments/assets/d78dc3fc-a16f-44c3-9cc1-281129e3c0cb

### イベント

![image](https://github.com/user-attachments/assets/a5db0ae9-e3af-4cb8-ac00-105522421487)

詳細のリンクに遷移することができます。

![image](https://github.com/user-attachments/assets/ead359a6-c8ac-4835-bf2f-c15350a658b2)


### 学習リソース

![image](https://github.com/user-attachments/assets/5b6f973c-f4b0-45cc-9f11-bd868a3d7bae)

学習リソースの詳細の確認ができます。

![image](https://github.com/user-attachments/assets/cf62b07d-558f-4887-ae3d-8663df1ec919)


### ポイント申請

![image](https://github.com/user-attachments/assets/72924323-9ddd-493e-a01b-aaf0f8dac3bb)

ポイント申請する際には承認ワークフローが起動されます。

![image](https://github.com/user-attachments/assets/b361dcf1-1058-40a3-8cd8-b4db07997ff7)


### ポイント獲得履歴

![image](https://github.com/user-attachments/assets/740d8815-e9a8-4f79-9161-9948ea645050)

### プロンプト

![image](https://github.com/user-attachments/assets/bc869128-a76a-4b37-8748-5760e25ef566)

### ランキング

![image](https://github.com/user-attachments/assets/a0305664-28d6-4a7c-9d01-d908e1125258)

### バッジ

![image](https://github.com/user-attachments/assets/28addb0c-a109-455e-81da-4013769fe86f)



## インストール方法

### 前提条件

* ライセンスは、管理者及び利用者にPower Apps Premium ライセンスが必要です。
* 言語ラベルは日本語で利用できます。

### ソリューションの取得

ソリューションを取得します。

[こちら](https://github.com/geekfujiwara/Copilot4M365Adoption/releases)から取得することができます。


[Power Apps ポータル](https://make.powerapps.com/)にアクセスします。

ソリューションに移動します。

![image](https://github.com/user-attachments/assets/8f4f0f73-088d-49b3-aa68-80d3bbf14564)


取得したソリューションをPower Apps ポータルにインポートします。

![image](https://github.com/user-attachments/assets/45b42639-a985-4a89-94ac-6293d8b827ad)

ソリューションを参照からZip形式のままインポートします。

![image](https://github.com/user-attachments/assets/85211ab5-7c2a-45e5-bb92-20a8bd9a6775)

次へをクリックして、接続情報が更新されるのを街、インポートへ進みます。

![image](https://github.com/user-attachments/assets/8037bf94-94fb-4662-88ca-f82de6ba09ae)

インポートには数分かかります。

![image](https://github.com/user-attachments/assets/396a66e8-27bf-4188-829e-3ec00981cf8a)


> [!NOTE]
> 以下のように警告が表示されたとしてもラベルの問題のため問題ありません。
> ![image](https://github.com/user-attachments/assets/0d264880-d39b-489e-8e54-08489e46da01)


インポートが完了し次第、ソリューションに移動します。

![image](https://github.com/user-attachments/assets/fda9e6d3-06c6-4854-870a-87cd5a95bced)

管理者向け(CoEチーム)のアプリと、利用者向けアプリ(Copilot 活用アプリ)の2種類が提供されています。、

![image](https://github.com/user-attachments/assets/71aaaa5c-ccf0-4ea3-8cfd-34c45fcd8a3d)

ソリューションのインポートは完了です。

### セキュリティロール

利用者向けに必要な最低限のセキュリティロールとして「CAP Basic User」というセキュリティロールが提供されています。

Copilot 活用アプリを共有するにはこちらのセキュリティロールを共有するようにしてください。

Copilot 活用アプリを共有するには、まずアプリを選択して共有します。

![image](https://github.com/user-attachments/assets/f6d7389a-9593-4f99-be88-a148848ac745)

共有先のユーザーを選択します。

![image](https://github.com/user-attachments/assets/4d5bf525-bdbb-4c17-84f0-c1f18785b4b2)

> [!NOTE]
> セキュリティグループに対して共有することもできます。
> ![image](https://github.com/user-attachments/assets/d6aa6496-65a1-4df5-9fbd-1d9bff3db331)

Dataqverseテーブルを選択して、ユーザーへのリソースの共有と同時にセキュリティロールを付与します。

![image](https://github.com/user-attachments/assets/52a8740d-a45b-4615-a4b2-0ab2516b0135)

CAP Basic User を探して選択して、共有します。

![image](https://github.com/user-attachments/assets/e3e63318-d990-4056-bc8a-3a47bb179b5c)

### データの追加

ソリューションをインポートしただけではデータは追加されていません。

![image](https://github.com/user-attachments/assets/b5239267-89a4-4f67-b653-ed84cf1c6558)


モデル駆動型アプリを開いて、データを入力していきます。

> [!NOTE]
> データ登録を行うユーザーは、Dataverse セキュリティロールとして、システム管理者またはSystem customizer で行うようにしてください。

モデル駆動型アプリはこのようにして開きます。

![image](https://github.com/user-attachments/assets/62c60ffc-a315-400e-9f07-88090b478d2c)

データの登録は以下の順番で行います。

1. バッジ
2. ポイント種類
3. イベントカテゴリ
4. 学習リソースカテゴリ
5. プロンプトカテゴリ
6. イベント
7. 学習リソース
8. プロンプトテンプレート

以下よりサンプルデータをダウンロードすることができます。

> [!NOTE]
> ポイント種類について、`プロンプトテンプレート登録`というタイトルのポイント種類は必ず登録するようにしてください。
> アプリ内部で予約しています。
> ![image](https://github.com/user-attachments/assets/45911283-4025-449d-8f11-932e0c40ba9b)

1. [バッジ.xlsx](https://github.com/user-attachments/files/16371990/default.xlsx)
2. [ポイント種類.xlsx](https://github.com/user-attachments/files/16371991/default.xlsx)
3. [イベントカテゴリ.xlsx](https://github.com/user-attachments/files/16371992/default.xlsx)
4. [学習リソースカテゴリ.xlsx](https://github.com/user-attachments/files/16371993/default.xlsx)
5. [プロンプトカテゴリ.xlsx](https://github.com/user-attachments/files/16371994/default.xlsx)
6. [イベント.xlsx](https://github.com/user-attachments/files/16372107/default.xlsx)
7. [学習リソース.xlsx](https://github.com/user-attachments/files/16372108/default.xlsx)
8. [プロンプトテンプレート.xlsx](https://github.com/user-attachments/files/16372110/default.xlsx)

ダウンロードが完了しましたら、一つずつ上から順番にデータを登録していきます。

バッジを例にして説明します。バッジ以外のデータは同じ作業のため同様にして実行してください。

![image](https://github.com/user-attachments/assets/58ee985c-1508-49f3-ba30-038e39d79c8c)

Excel Online で開くとします。

![image](https://github.com/user-attachments/assets/f086d811-2894-4962-bec0-81180032070a)

赤枠の範囲をコピーして、同じ領域にペーストします。

![image](https://github.com/user-attachments/assets/0aeac83f-354b-4e22-854c-e2b40d4340de)

ペーストしたら保存します。

![image](https://github.com/user-attachments/assets/040dff58-9d2a-43a0-9542-d6d0b35d38df)

進行状況を追跡します。

> [!NOTE]
> 進行状況の追跡は任意です。バックグラウンドで処理されますので、必要に応じて確認してください。

![image](https://github.com/user-attachments/assets/c733a863-120c-426c-aebd-78300230b08b)

すべて成功していたらOKです。

![image](https://github.com/user-attachments/assets/4e8a309b-7996-4bc8-b7e7-0745d025cfc8)

最新の情報に更新します。

![image](https://github.com/user-attachments/assets/afd64613-4118-4359-a70c-58f0ff3837cc)

バッジが登録されたことがわかります。

![image](https://github.com/user-attachments/assets/f7fb502d-27e5-43c1-88aa-c3e4c9bbf114)

同じようにして、他のテーブルについてもExcel Online より登録していきます。

次に、`ポイント種類`を、`イベント`及び`学習リソース`に連携させるようにしてください。

こちらのようにポイント種類を設定します。

#### イベントの場合

![image](https://github.com/user-attachments/assets/9a44dadf-1ca8-4ea4-b8bf-8b72e753ce4f)

#### 学習リソースの場合

![image](https://github.com/user-attachments/assets/434d67ac-effd-429a-abbc-10f1760b3453)


#### プロンプトテンプレート

プロンプトテンプレートは、`ポイント種類`のタイトルが`プロンプトテンプレート登録`となっているもののポイントを採用しますので、特段連携する設定をする必要はありません。

> [!NOTE]
> データはあくまでサンプルなので、必要に応じて変更するようにしてください。


## 免責事項

    MITライセンス

    このソフトウェアは無償で提供され、使用や複製、変更、出版、頒布、販売など自由に行うことができます。
    しかし、「現状のまま」提供されるため、いかなる種類の保証もなく、著作者または著作権所有者は一切の責任を負いません。
    使用する際には本ドキュメントを確認し、問題が生じても著作者や著作権所有者に責任を求めることはできません。

    バグや改善に関するリクエストはGitHub からIssue またはPull request を送信してください。

    Copyright (c) Geek Fujiwara.   

以上


