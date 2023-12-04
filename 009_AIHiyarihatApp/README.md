# Power AI Chat アプリ

## アプリケーション概要
AIヒヤリハット報告アプリは、生成AIを活用し、ヒヤリハット登録時の支援を行い、過去のヒヤリハットを元に注意すべきポイントの提案を行うアプリです。
過去に登録したヒヤリハットの情報を基に回答を生成するため、自社に適した提案を受けることができます。

## キャプチャ
![キャプチャ](https://github.com/microsoft/PowerApps-Sample-Apps-Japan/blob/main/docs/AIHiyarihatApp.png?raw=true "キャプチャ")

## 構成
- README.md
- hyarihatkaizen_1_0_0_0.zip：アンマネージドソリューション
- hyarihatkaizen_1_0_0_0_managed.zip：マネージドソリューション
- ソリューションインポート手順書.pdf：インストール手順書
- AIヒヤリハット報告アプリ_初期設定&動作確認.pdf：初期設定と動作確認手順書

## 展開・利用に必要な条件
- Power Apps Premium ライセンス（開発者・利用者）
- Azure OpenAI Service

## 対応言語
- 日本語

## 主な機能
- ヒヤリハットの登録
- ヒヤリハット登録時のAI支援
    - カテゴリ提案
    - 危険度提案
    - 対策提案
- ヒヤリハットAI相談窓口

## アプリ利用に必要なコネクタ
- Dataverse
- HTTP

## Azure OpenAI Service 対象モデル
- ChatCompletion API 対応モデル
    - 例：gpt-4、gpt-35-turbo、他　※2023年11月現在

## インストールに必要な権限
- システム管理者（セキュリティロール）

## インストールに必要なソリューション
- 特になし

## インストール方法
- ソリューションインポート手順書.pdf を参照
<br>

## 初期設定方法
- AIヒヤリハット報告アプリ_初期設定&動作確認.pdf を参照
<br>

## マネージドソリューションとアンマネージドソリューション
2種類のソリューションを用意しています。インストールにはマネージドソリューションを使用することをおすすめします。アンマネージドは開発環境への展開や、追加の開発・カスタマイズを実施する環境で展開してください。
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

2023年11月吉日