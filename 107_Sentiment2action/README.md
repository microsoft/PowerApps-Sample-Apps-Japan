# Sentiment2action 感情分析からアクション

Power Apps + AI Builderで作成した、アンケートやレビュー等の文章に対して感情分析を行い、ケース管理するアプリ。
例えば肯定的な感情のものはそのままとし、否定的なものは対処を検討するために担当者を割り当て、期限管理をする使い方を想定しています。

![image](https://github.com/geekfujiwara/Sentiment2action/assets/96101315/36865503-5285-4d43-9175-172107ff0c78)


ちなみにこの緑色のバーのところはPCFを使っています。

![image](https://github.com/geekfujiwara/Sentiment2action/assets/96101315/4c77ef79-c659-48c5-a4c8-734a8522f93d)



> [!NOTE]
> 動いたよ、できたよという結果は是非、 [ギークフジワラのXアカウント](https://x.com/Geekfujiwara) までメンションしてご報告ください！！


https://github.com/geekfujiwara/Sentiment2action/assets/96101315/535767b8-5498-4865-a1c9-249f4b67b163

## 仕組み

Dataverse の詳細列にデータが追加されたら、Power Automate が起動してAI Builder のモデルにより感情分析が行われます。

感情分析モデルは[事前構築済みモデル](https://learn.microsoft.com/ja-jp/ai-builder/prebuilt-sentiment-analysis)を利用しています。


## AI Builder 感情分析

テキストを渡すと以下の値を返します。

センチメント:
* ポジティブ
* ネガティブ
* ニュートラル
* 混在

信頼度スコア: 
0 から 1 の範囲の値。 値が 1 に近いと、識別されたセンチメントが正確であるという、より高い信頼度を示します。

### サポートされている言語とデータ形式

言語: 
ドイツ語、スペイン語、英語、フランス語、ヒンズー語、イタリア語、日本語、韓国語、オランダ語、ノルウェー語、ポルトガル語 (ブラジル)、ポルトガル語 (ポルトガル)、トルコ語、中国語 (簡体字)、中国語 (繁体字)

文字制限:
5,120 文字を超えることはできません。


## 参考
[ブログ](https://www.geekfujiwara.com/)

[YouTubeチャンネル](https://www.youtube.com/@geekfujiwara)

[X](https://twitter.com/geekfujiwara)


## 前提条件

### ライセンス

AI Builder を利用するアプリです。そのため、Power Apps Premium ライセンスが必要です。

モデル駆動型アプリはPower Apps Premium ライセンスに利用券が含まれています。

詳しいライセンスについては以下をご覧ください。

[Power Apps](https://www.microsoft.com/ja-jp/power-platform/products/power-apps)

### PCF ギャラリー

一部コントロールとして、PCF ギャラリーの[Progress Bar](https://pcf.gallery/progressbar/) を利用しています。

そのためPCFギャラリーから[ソリューション](https://github.com/365lyf/PCFControls/blob/master/ProgressBar/Solution.zip)のダウンロードとインポートを先に行ってください。


![image](https://github.com/geekfujiwara/Sentiment2action/assets/96101315/68e16462-1962-41f2-b3e4-f1df525b3d2d)

## 環境へのインポート

### ソリューションファイルを入手

本ソリューションのファイルは[こちらから入手](https://github.com/geekfujiwara/Sentiment2action/releases)できます。

最新版を入手するようにしてください。

### インポート作業

[公式ドキュメント](https://learn.microsoft.com/ja-jp/power-apps/maker/data-platform/import-update-export-solutions)を参考にZIPファイル形式のままソリューションをインポートしてください。

以上
