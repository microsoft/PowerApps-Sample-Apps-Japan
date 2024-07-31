# Azure OpenAI GPT-4o を活用した画像認識Power Apps アプリ

マルチモーダルに対応し、応答の精度や速度が格段に向上したGPT-4oをAzureにデプロイして、Power Apps で画像認識アプリを公開しています。

画像を利用したGPTへの依頼が可能になったことにより、より人間に近い依頼ができるようになりました。

![image](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/ad45d7b4-eb9b-4e03-9c4c-a9dceabf5e70)

> [!NOTE]
> 動いたよ、できたよなどのソリューションを利用した感想などはぜひ、[ギークフジワラのX](https://x.com/geekfujiwara/status/1797378518676082839)までお願いいたします！



たとえば以下のような利用シーンが考えられます。

（1）保険、カロリー計算と栄養指導

<img width="896" alt="image" src="https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/a65087db-ce30-42cc-8d66-bc87421c15e2">

（2）OCR、画像から情報抽出

![image](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/2ede4a2f-7b38-44c4-bbb8-3baab60de4d9)

（3）プロジェクト、業務フローの改善点指摘

<img width="901" alt="image" src="https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/fafe2e1d-04b5-458b-84ff-b9fb3078e337">

（4）サポートデスク、スクリーンショットからエラー修復

<img width="897" alt="image" src="https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/bb18ae32-8c6e-4204-9867-8b6cd6ae38da">
[GPT4o_1_0_0_0_managed.zip](https://github.com/user-attachments/files/16435894/GPT4o_1_0_0_0_managed.zip)

（5）Webサイト作成

<img width="896" alt="image" src="https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/bc81512b-7058-44c7-b74c-2363804ad328">

作成したWebサイト

<img width="439" alt="image" src="https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/07fa384f-085c-4b75-bd1a-4df4a29a6dee">

（6）作業上の安全管理

![image](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/5079600c-d201-48ce-a4b4-f7e35e1ebbd7)


これらは全てこちらのアプリで実現可能です。

その他にもいろいろな利用シーンを[私のブログで紹介](https://www.geekfujiwara.com/tech/powerplatform/4778/)しています。

作成方法や利用方法は以下の動画で解説しています。

[YouTubeでの解説](https://youtu.be/aCuqqWYoG9s)

[![Azure OpenAI GPT-4o を活用した画像認識Power Apps アプリ](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/caebc125-3a97-4d83-b966-15d690c7c086)](https://youtu.be/aCuqqWYoG9s)




# 参考情報

[ブログ](https://www.geekfujiwara.com/)

[YouTubeチャンネル](https://www.youtube.com/@geekfujiwara)

[X](https://twitter.com/geekfujiwara)


# アプリの概要

## 機能

* 画像をアップロード
* プロンプトを自由に変更
* クリップボードにコピー
* 結果を保存
* 結果の表示と削除

## OCR2GPTのまさに「進化版」

[OCR2GPTで実現していたこと](https://github.com/geekfujiwara/OCR2GPT)も、GPT-4oの実現方式でよりシンプルに、精度高く実現できます。

# ソリューションのインポート方法

## 前提条件

ソリューションは[リリース](https://github.com/geekfujiwara/GPT-4oPowerApps/releases)からダウンロードできます。


## インポート方法

[公式ドキュメント](https://learn.microsoft.com/ja-jp/power-apps/maker/data-platform/import-update-export-solutions)を参考にZIPファイル形式のままソリューションをインポートしてください。

インポート時に聞かれる環境変数は[Azure OpenAI Studio](https://oai.azure.com/) から取得するようにしてください。

![image](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/a9fce1e9-b2de-44f1-bbb5-030ef2b72aca)

チャットプレイグラウンドからコードの表示と進めると確認できます。

![image](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/6d323025-2202-4ce6-8e8b-b35a98e1fefe)


エンドポイントURLはCurlから取得できます。

![image](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/3a2bb72e-97f5-44ff-bf3d-ed974b3124de)

APIキーはこちらから取得できます。

![image](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/d5ef7dc2-0b13-4855-9828-d9f44d82f9a2)




## インポート後の警告

もし言語ラベルに関する警告が発生したとしても気にせず進めてください。

表示された場合でも基本的にはこのまま利用することができます。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/47bd2f63-fff8-461a-a41e-39e1cb555561)


## カスタマイズをすべて公開

インポート後はカスタマイズをすべて公開します。

もしクラウドフローがオフになっている場合はオンにします。

![image](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/3294ef08-b6e0-4744-95ca-f25f505adba7)


## アプリの実行

アプリを実行できます。Enjoy!

![image](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/0586d0b9-a9b7-40d5-8683-e584317c72ca)




以上、ご参考になれば幸いです。
