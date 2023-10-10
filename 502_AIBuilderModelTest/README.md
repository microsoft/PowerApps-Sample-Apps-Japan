# AI Builder モデル検証アプリ（実装サンプル）

## アプリケーション概要
本アプリは、AI BuilderをPower Appsで利用する際の実装サンプルです。
<br>
AI Builderの事前構築済みモデル11種類を簡単に試していただくことができます。
<br>

## キャプチャ
![キャプチャ](https://github.com/microsoft/PowerApps-Sample-Apps-Japan/blob/main/docs/AIBuilderModelTest.png?raw=true "キャプチャ")
<br>

## 構成
- README.md
- AIBuilderAllApp_1_0_0_1.zip：アンマネージドソリューション
- AI Builder モデル検証アプリ_ソリューションインポート手順書.pdf：インストール手順書
- AI Builder モデル検証アプリ_動作確認.pdf：動作確認手順書
- AI Builder モデル検証アプリ_使用方法.pdf:アプリの操作方法
- テスト用画像データ.zip
<br>

## 展開・利用に必要な条件
- Power Apps 有償ライセンス（開発者・利用者）
- AI Builderキャパシティアドオン（※ こちらは実行数に応じて必要）
<br>

## 主な機能
- 請求書処理
- テキスト認識
- 領収書処理
- IDリーダー
- 名刺リーダー
- 感情分析
- カテゴリ分類
- エンティティ抽出
- キーフレーズ抽出
- 言語検出
- テキスト翻訳
<br>

## 対応環境
テキスト翻訳モデル以外は日本環境に対応しています。テキスト翻訳モデルを含めたすべてのモデルを使用したい場合はUS環境にインポートお願いいたします。

<br>

## 対応言語
- 日本語対応しているモデルは日本語で使用できるようご用意しています。
- モデルごとの対応言語は以下をご参照ください。
    - 請求書処理
    https://learn.microsoft.com/ja-jp/ai-builder/prebuilt-invoice-processing#supported-languages-and-files
    - テキスト認識
    https://learn.microsoft.com/ja-jp/ai-builder/prebuilt-text-recognition#supported-language-format-and-size
    - 領収書処理
    https://learn.microsoft.com/ja-jp/ai-builder/prebuilt-receipt-processing#supported-languages-markets-and-files
    - IDリーダー
    https://learn.microsoft.com/ja-jp/ai-builder/prebuilt-id-reader#supported-language-format-and-size
    - 名刺リーダー
    https://learn.microsoft.com/ja-jp/ai-builder/prebuilt-business-card#supported-language-format-and-size
    - 感情分析
    https://learn.microsoft.com/ja-jp/ai-builder/prebuilt-sentiment-analysis#supported-language-and-data-format
    - カテゴリ分類
    https://learn.microsoft.com/ja-jp/ai-builder/prebuilt-category-classification#supported-data-format-and-languages
    - エンティティ抽出
    https://learn.microsoft.com/ja-jp/ai-builder/prebuilt-entity-extraction#supported-data-format-and-languages
    - キーフレーズ抽出
    https://learn.microsoft.com/ja-jp/ai-builder/prebuilt-key-phrase#supported-language-and-data-format
    - 言語検出
    https://learn.microsoft.com/ja-jp/ai-builder/prebuilt-language-detection#supported-language-and-data-format
    - テキスト翻訳
    https://learn.microsoft.com/ja-jp/ai-builder/prebuilt-text-translation#supported-language-and-data-format
<br>

## アプリ利用に必要なコネクタ
- AI Builder
    - 請求書処理
    - テキスト認識
    - 領収書処理
    - IDリーダー
    - 名刺リーダー
    - 感情分析
    - カテゴリ分類
    - エンティティ抽出
    - キーフレーズ抽出
    - 言語検出
    - テキスト翻訳
- Dataverse
<br>

## インストールに必要な権限
- システム管理者（セキュリティロール）
<br>

## インストールに必要なソリューション
- 特になし
<br>

## インストール方法
- AI Builder モデル検証アプリ_ソリューションインポート手順書.pdf を参照
<br>

## AI Builderキャパシティアドオン取得方法
- [AI Builderアドオン購入方法](https://qiita.com/skuramoto/items/36fc75d9223db5d8feda#ai-builder%E3%82%A2%E3%83%89%E3%82%AA%E3%83%B3%E8%B3%BC%E5%85%A5%E6%96%B9%E6%B3%95)を参照
<br>

## 動作確認方法
- AI Builder モデル検証アプリ_動作確認.pdf を参照
- 画像認識モデル（請求書処理・テキスト認識・領収書処理・IDリーダー・名刺リーダー）に関しては、テスト用として「テスト用画像データ.zip」 の画像もお使いください。
<br>

## 操作方法
- AI Builder モデル検証アプリ_使用方法.pdf を参照
<br>

## FAQ
* Q. 内容や機能をカスタマイズすることは可能ですか？
    * A. 可能です。カスタマイズすることを前提にシンプルで汎用的な作りになっています
* Q. 展開パートナーはどのように見つけることができますか？
    * A. 日本マイクロソフト営業担当者までお問い合わせください
<br>

## 免責事項
本アプリ集は日本マイクロソフトが提供する無償のサンプル群です。本アプリ集をダウンロードされた方は、以下の免責事項を承諾したものとみなされます。

1.　本アプリ集（本アプリ集に付属するドキュメント及びReadmeに記載されている技術情報を含みます。以下、本「免責事項」において同じ。）は利用者に対して「現状のまま」提供されるものであり、日本マイクロソフトは、本アプリ集にプログラミング上の誤りその他の瑕疵のないこと、本アプリ集が利用者の目的に適合すること、並びに本アプリ集及びその使用が利用者または利用者以外の第三者の権利を侵害するものでないこと、その他のいかなる内容についての明示または黙示の保証を行うものではありません。

2.　日本マイクロソフトは、本アプリ集の使用に起因して、利用者に生じた損害または第三者からの請求に基づく利用者の損害について、原因の如何を問わず、一切の責任を負いません。日本マイクロソフトは、本アプリ集に関連して利用者と第三者との間に発生するいかなる紛争について、一切責任を負わないものとします。本アプリ集の利用は、利用者の責任のもとで行ってください。

3.　日本マイクロソフトは、本アプリ集の全部または一部の提供を廃止することがあります。提供の廃止によって利用者に発生した損害について、日本マイクロソフトは一切責任を負いません。

4.　日本マイクロソフトは、本アプリ集のバグ修正、補修、保守、機能追加その他のいかなる義務も負いません。本アプリ集は、不定期に更新される可能性がありますが、バグ修正等が保証されているわけではありません。本アプリ集の安定した動作を確保するためには、利用者自身が適切なテストや検証を行ってください。

5.　日本マイクロソフトは、本アプリ集に関するお問い合わせにはお答えできません。ご利用にあたっては、提供された手順書を参照し、ご自身でのインストールや利用を行ってください。

2023年10月吉日