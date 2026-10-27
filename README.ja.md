<div align="center">

<img src="assets/logo.png" width="96" alt="DRVCAM logo">

# DRVCAM

**root化した対応Android端末向けの仮想カメラです。** 写真や動画を選び、選択したアプリのカメラ映像として表示できます。ライブ再生と画角の操作に対応しています。

[English](README.md) | [Español](README.es.md) | [العربية](README.ar.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Italiano](README.it.md) | **日本語** | [简体中文](README.zh-hans.md)

[![最新リリース](https://img.shields.io/github/v/release/Xposed-Modules-Repo/com.droidrooter.virtualcamera?label=最新リリース)](https://github.com/Xposed-Modules-Repo/com.droidrooter.virtualcamera/releases/latest)
[![プラットフォーム](https://img.shields.io/badge/プラットフォーム-Android-3DDC84)](#動作要件)
[![root必須](https://img.shields.io/badge/root-必須-critical)](#動作要件)
[![ライセンス](https://img.shields.io/badge/ライセンス-proprietary-lightgrey)](#ライセンス)

**[⬇ ダウンロード](#ダウンロード)** &nbsp;·&nbsp; **[📦 インストール](#インストール)** &nbsp;·&nbsp; **[💬 サポート](#サポート)** &nbsp;·&nbsp; **[🌐 droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**

</div>

> [!IMPORTANT]
> **ベータ版。** DRVCAMは開発が続いており、動作は端末によって異なる場合があります。 このリポジトリはDRVCAMの**モジュール一覧情報**です。ソースコードは含まれません。製品ページ、料金、詳しいドキュメントはこちら：**[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**。

## 目次

- [スクリーンショット](#スクリーンショット)
- [できること](#できること)
- [動作要件](#動作要件)
- [ダウンロード](#ダウンロード)
- [インストール](#インストール)
- [無料プランと有料プラン](#無料プランと有料プラン)
- [プライバシーの基本](#プライバシーの基本)
- [よくある質問](#よくある質問)
- [免責事項](#免責事項)
- [ライセンス](#ライセンス)
- [サポート](#サポート)
- [変更履歴](#変更履歴)

## スクリーンショット

<div align="center">
<table>
<tr>
<td align="center"><img src="screenshots/screen-home.webp" width="200"><br><sub>ホーム</sub></td>
<td align="center"><img src="screenshots/screen-controller.webp" width="200"><br><sub>フローティングコントローラー</sub></td>
<td align="center"><img src="screenshots/screen-editor.webp" width="200"><br><sub>メディアエディター</sub></td>
<td align="center"><img src="screenshots/screen-presets.webp" width="200"><br><sub>プリセット</sub></td>
</tr>
</table>
</div>

## できること

- 取り込んだ写真や動画を、端末・カメラAPI・アプリが対応している範囲で、選択したアプリのカメラソースとして使用します。
- 対象アプリを選択し、再生、回転、左右反転、ズーム、画角を調整できます。Mainソースと4つのプリセットを保存して切り替えられます。
- 設定済みの対象を、仮想映像と実際の物理カメラの間で切り替えられます。一部のアプリでは切り替えを反映するためにカメラの開き直しが必要で、その場合はDRVCAMが知らせます。
- 使用中のアプリの上に表示される、任意のフローティングコントローラーを利用できます（オーバーレイ権限が必要です）。
- 実際のマイクはそのままです — DRVCAMは音声の置き換えや処理を行いません。

## 動作要件

- root化したAndroid端末（MagiskまたはKernelSU）、Android 9以降。カメラ置き換えにはrootが必要です。rootなしでもアプリは開きますが、置き換えは利用できません。
- libxposed API 102に対応したXposed系フレームワーク — DRVCAMは[Vector](https://github.com/JingMatrix/Vector)（LSPosedの後継）でテストしています。これはZygiskを基盤とするLSPosed系フレームワークです。API 102に対応していないフレームワークではモジュールが読み込まれません。
- 選択するメディアとアプリに十分なデコーダー性能とグラフィック性能。

## ダウンロード

このリストには**Android 9以降向けの電話機用ビルド**（arm64）が掲載されています。エミュレーター用イメージは**[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**にあり、端末に合うものを案内する選択ツールも利用できます。

ここでの各リリースにはリリースノートにSHA-256が記載されています — インストール前にダウンロードを確認してください。

## インストール

1. お使いのAndroidバージョンと端末の種類（上表）に合うAPKをダウンロードしてインストールします。
2. フレームワークのマネージャーを開き、DRVCAMを有効にします。求められたら再起動してください。
3. DRVCAMを開き、求められたらrootを許可します。選択したアプリの範囲はDRVCAM自身のアプリ内で管理されるため、フレームワークのマネージャーで手動設定を追加する必要はありません。
4. ログインするか、**無料で試す**を選びます（[無料プランと有料プラン](#無料プランと有料プラン)を参照）。
5. 写真や動画をライブラリに読み込み、選択し、対象アプリを選んでから**Enable**をタップします。対象アプリのカメラは自分で開いてください。
6. 対象アプリ内で結果を確認します。DRVCAM自体のプレビューはメディア選択の目安であり、それだけでは対象アプリが映像を受け取ったことの証明にはなりません。

**Disable**で対象からDRVCAMの範囲を再び外せます。

## 無料プランと有料プラン

DRVCAMには、ログイン・端末登録・更新のためにDRVCAMアカウントとインターネット接続が必要です。ログイン後は、一定期間オフラインでも動作を続けられます。

- **無料で試す**（無料）：画像ソース、対象アプリ1つ。
- **有料プラン**：動画ソース、複数の対象アプリ、フローティングコントローラー、Camera Sourceの切り替え。

現在のプラン、端末数の上限、料金：**[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/#pricing)**。

## プライバシーの基本

- カメラ機能に関わるメディアは端末内に保存されます — ログインのためにメディアやカメラの映像がアカウントサービスに必要になることはありません。
- アカウントサービスは、ログインとライセンスを機能させるためにアカウント・端末・サブスクリプションのデータを処理します。診断情報は、あなたが要求した場合にのみ送信されます。
- 対象アプリは、そのカメラが映すものを保存・解析・送信する場合があります。これはそのアプリ自体のプライバシー方針によります。
- 詳しいポリシー：[droidrooter.com/privacy](https://www.droidrooter.com/privacy)。

## よくある質問

<details>
<summary><strong>rootは必要ですか？</strong></summary>

はい。カメラ置き換えはシステムレベルのフックで実現しており、rootと対応するXposed系フレームワークが必要です。
</details>

<details>
<summary><strong>自分の端末で動きますか？</strong></summary>

検証済みの組み合わせのみ製品ページに掲載しています。端末・ファームウェア・カメラアプリの組み合わせは非常に多く、事前に動作を保証することはできません。
</details>

<details>
<summary><strong>ログインせずに使えますか？</strong></summary>

はい、**無料で試す**（画像ソース、対象アプリ1つ）で利用できます。動画やその他の機能には有料プランが必要です。
</details>

<details>
<summary><strong>マイクも置き換わりますか？</strong></summary>

いいえ。DRVCAMが置き換えるのはカメラの映像だけです。実際のマイクはどのプランでもそのまま使用されます。
</details>

<details>
<summary><strong>ライブのネットワークストリームをカメラソースとして使えますか？</strong></summary>

はい、有料プランで利用できます。写真や動画を取り込むのと同じ方法でRTSP/RTMPストリームを取り込めます。
</details>

<details>
<summary><strong>カメラ設定はいくつ保存できますか？</strong></summary>

Main設定1つに加えてプリセット4つです。プリセットには有料プランが必要です。Mainは無料プランでも利用できます。
</details>

<details>
<summary><strong>Remote Diagnosisとは何ですか？</strong></summary>

サポートがあなたの端末に接続して問題の診断を手伝う機能です。デフォルトではオフになっており、ヘルプが必要なときだけ設定で自分で有効にします。
</details>

<details>
<summary><strong>パスワードを忘れました。どうすればよいですか？</strong></summary>

現時点でのアカウント復旧は手動対応です。下記の[サポート](#サポート)のリンクをご利用ください。
</details>

<details>
<summary><strong>ソースコードはどこにありますか？</strong></summary>

ここでは公開していません。このリポジトリはモジュール一覧情報であり、署名済みのリリースバイナリのみを配布しています。
</details>


## 免責事項

DRVCAMはベータ版ソフトウェアであり、いかなる保証もなく「現状のまま」提供されます。端末のroot化やシステムレスフレームワークのインストールは自己責任で行う操作であり、端末の保証や安定性に影響する場合があります。

利用する素材、DRVCAMと組み合わせて使用するアプリケーション、そしてご自身に適用される法律や規約の遵守について、責任を負うのは利用者本人です。開発者は、本ソフトウェアの違法、無許可、またはその他の不適切な使用について責任を負いません。

## ライセンス

DRVCAMはクローズドソースの独自ソフトウェアです。アプリケーションの複製、改変、リバースエンジニアリング、再配布のいずれについてもライセンスは許諾されません。ダウンロードとインストールには、製品サイトに掲載の[利用規約](https://www.droidrooter.com/terms)が適用されます。

## サポート

- WhatsApp: [WhatsAppでチャット](https://wa.me/message/RPNSAAK4EPUSC1)
- Telegram：[@DroidRooter](https://t.me/DroidRooter)
- ウェブサイトのお問い合わせフォーム：[droidrooter.com/contact](https://www.droidrooter.com/contact)

## 変更履歴

変更内容は各[リリース](https://github.com/Xposed-Modules-Repo/com.droidrooter.virtualcamera/releases)のノートをご覧ください。
