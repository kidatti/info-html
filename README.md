# Info Dashboard

ニュース・天気・為替・マーケット情報をリアルタイムに表示するPWAダッシュボード。

## Quick Start

### GitHub Pages で開く

- Dashboard: https://kidatti.github.io/info-html/
- Clock: https://kidatti.github.io/info-html/clock.html

## 表示内容

- **IP Address** - ヘッダーにIPアドレスと位置情報を表示
- **Weather** - IPジオロケーションによる現在地対応（フォールバック: 東京）+ 12時間先の時間別予報
- **News** - Yahoo! / ロイター / 日経 / 読売 / 産経 / Impress系の日本語ニュースをRSSから取得・マージ表示
- **Tech News** - 日経テクノロジー / Yahoo! IT / Impress系 + Hacker News をマージ表示
- **Exchange Rates** - 主要5通貨の対円レートと前日比
- **Market** - 主要暗号資産の円建て価格と24h変動率
- **Clock** - フルスクリーンデジタル時計ページ（clock.html）

## 機能

- **Dark / Light Theme** - ダーク・ライトテーマの切り替え対応
- **Auto Refresh** - セクションごとに更新間隔を個別設定可能（1分〜手動）
- **Settings** - フィード選択・表示件数・更新間隔をlocalStorageに自動保存、設定の初期化機能
- **Keyboard Shortcuts** - `r` で全更新、`1`-`5` でカードにスクロール（input / select フォーカス中は無効）

## 操作

| キー | 動作 |
|------|------|
| `r` | すべて更新 |
| `1`-`5` | 対応するカードにスクロール |

※ input / select にフォーカス中は無効。

## データ保存

localStorage に以下のデータを保存。設定画面から初期化可能。

| キー | 内容 |
|------|------|
| `dashSettings` | フィード選択・表示件数・更新間隔 |
| `proxyUrl` | Proxy URL |
| `proxyKey` | Proxy API Key |
| `theme` | テーマ（dark / light） |

## Data Sources

すべて無料API（APIキー不要）:

| データ | ソース |
|--------|--------|
| IP / 位置情報 | a.apiless.com |
| 天気 | Open-Meteo |
| 為替 | Frankfurter (frankfurter.dev) |
| マーケット | CoinGecko |
| ニュース | Yahoo! RSS / assets.wor.jp (日経, ロイター, 読売, 産経) / Impress Watch系 |
| テックニュース | Hacker News API / assets.wor.jp (日経テクノロジー) / Yahoo! IT / Impress Watch系 |
