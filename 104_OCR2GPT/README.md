# OCR2GPT

Power Apps キャンバスアプリのAI Builder テキスト認識エンジン(OCR) とGPT でテキストを作成する アクションを組み合わせたドキュメントOCRソリューションです。

> [!NOTE]
> AI Builder AI プロンプトとして、[GPT の機能が日本でも利用できるようになりました](https://learn.microsoft.com/ja-jp/ai-builder/availability-region)ので、AI Builder AI プロンプトのバージョンにアプリを更新しました。
> 日本でのAI プロンプトの利用は[地域間のデータ移動を有効化する](https://learn.microsoft.com/ja-jp/power-platform/admin/geographical-availability-copilot#enable-data-movement-across-regions)必要があります。
> また、動いたよ、できたよという結果は是非、 [ギークフジワラのXアカウント](https://x.com/Geekfujiwara) までメンションしてご報告ください！！

# 参考
[ブログ](https://www.geekfujiwara.com/)

[YouTubeチャンネル](https://www.youtube.com/@geekfujiwara)

[X](https://twitter.com/geekfujiwara)


# アプリの概要


以下の3オブジェクトで構成されています。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/3ef55726-3a6b-4585-a53e-6c1d681a8c6a)


```mermaid
flowchart TD
    GeekOCR2GPT --> プロンプトテンプレート
```

## 用意されている機能

* AI Builder テキスト認識エンジンによるOCR でドキュメントの全文テキスト化
* AI Builder 'formatGPT' でテキストから必要なデータを抽出またはフォーマットに変換
* プロンプトテンプレートのデータ登録、更新


## サンプルで用意されているプロンプトテンプレート

プロンプトを変更することで任意のフォーマットに対応することができます。

サンプルのプロンプトとして以下の5件が用意されています。

> [!NOTE]
> こちらを参考に他のドキュメントにも適用してみてください。
> 他のフォーマットにも対応できた結果についても是非、 [ギークフジワラのXアカウント](https://x.com/Geekfujiwara) までメンションしてご報告ください！！

### ガソリン給油レシート

ガソリンの給油レシートから必要な情報を抽出します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/a3e9d93f-9bd3-4146-a572-ab4fdd878a41)


### 家系図提案
[GeekOCR2GPT_1_0_0_3_managed.zip](https://github.com/user-attachments/files/16435897/GeekOCR2GPT_1_0_0_3_managed.zip)

戸籍謄本から家系図の提案を行います。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/cf4fea70-7e8b-4907-a841-8a17b35c0562)


### NDA

機密保持契約書から保持期間などの契約情報を抽出します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/91cbc4cf-292c-4037-9779-d403c9e58aba)


### 請求書

請求書から明細も含めて必要な情報を抽出します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/89d78993-e36c-41e9-b432-b86a74af71e5)




### 検査成績表

仕入先から届いた検査成績表から必要な情報を抽出します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/d8372904-5352-42f0-99d9-9b8cbef41314)


#### JSON 形式に出力

それぞれの出力結果は、プロンプトにjsonと加えるだけでjson形式に出力することができます。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/27dfeb9b-4562-4dd3-ae43-fd2360288214)

> [!NOTE]
> 下流の連携先システムに対して構造化したデータとして利用することができます。


### 英語のドキュメントも日本語で回答

英語のドキュメントなど他言語であっても取り込みが可能

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/bb2603cf-c669-4702-ae46-ffe2275191d3)



# ソリューションのインポート方法

## 前提条件

ソリューションは[リリース](https://github.com/geekfujiwara/OCR2GPT/releases)からダウンロードできます。


## インポート方法

[公式ドキュメント](https://learn.microsoft.com/ja-jp/power-apps/maker/data-platform/import-update-export-solutions)を参考にZIPファイル形式のままソリューションをインポートしてください。


## インポート後の警告

この警告は表示言語に関するものです。表示された場合でも基本的にはこのまま利用することができます。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/47bd2f63-fff8-461a-a41e-39e1cb555561)




## データインポート

ソリューションをインポートした時点ではオブジェクトのみが環境に展開されます。

> [!NOTE]
> アプリを開くことはできますが、ソリューションをインポートしただけではプロンプトテンプレートテーブルにはデータが含まれていません。
> 
> ![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/3a244b44-6261-4183-9130-a73700f8b597)
> 

データは移行されませんので、データのインポートを行う必要があります。

以下よりプロンプトのサンプルデータをダウンロードしてください。


[mskk_prompttemplates.xlsx](https://github.com/geekfujiwara/OCR2GPT/files/15104945/mskk_prompttemplates.xlsx)



テーブルを開きます。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/ea7eca85-fba3-4e63-a16b-e46ea34a7015)



「Excel からデータをインポートする」を選択します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/1785ce2f-bcc8-4e7e-a59c-5a4da1866071)



サンプルデータをアップロードします。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/b5325198-77bb-416d-9375-758edc812a7a)


正常にマッピングが完了したら右上のインポートボタンを押します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/e40627d4-b6dd-4540-bf77-1e474a1ef078)

完了しますと以下のようになります。右上のXボタンから閉じます。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/b1bb7fb4-6ff2-44b9-aa66-dfc2b6288a48)


データのインポート確認のため、ブラウザを一度更新します。

プロンプト名、プロンプトテンプレートを表示します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/d2947f40-876c-4bef-8e64-452152ac39f7)

マウスオーバーして以下のように表示されていたらデータのインポートに成功しています。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/c364eb40-08c9-4ef2-acd0-7186eb0d3d9b)

## アプリの実行

キャンバスアプリを開きます。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/5cf02878-f962-463d-907d-314b49f8605f)


プロンプトテンプレートのデータがインポートされていることがわかります。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/69fcfe7e-81cb-4621-a870-882f51bad73e)


> [!NOTE]
> ガソリン給油レシートの場合は以下のように選択できます。
> 
> ![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/b5bdd35e-8618-412c-8474-4b3cbc4c93c3)

### テストドキュメントの読み込み

レシートから情報を取得してみます。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/2ffe354e-4a6c-4a0e-9c6f-fc2378b5c100)

以上、ご参考になれば幸いです。
