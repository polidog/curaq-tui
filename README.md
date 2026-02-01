# curaq-tui

<p align="center">
  <img src="assets/curaq-tui-demo.gif" alt="curaq-tui Demo" width="800">
</p>

Ink で構築された CuraQ CLI/TUI クライアント。

## 必要要件

- Node.js 18以上
- CuraQ API トークン

## インストール

### npm でグローバルインストール

```bash
npm install -g curaq-tui
```

### ソースからビルド

```bash
pnpm install
pnpm build
```

## 使い方

### コマンド

```bash
# API トークンの設定（~/.config/curaq-tui/config.json に保存）
curaq-tui setup

# 現在の設定を表示
curaq-tui config

# テーマを設定（インタラクティブ選択または名前指定）
curaq-tui theme
curaq-tui theme dracula

# スタート画面を設定
curaq-tui start-screen unread

# 保存されたトークンをクリア
curaq-tui clear

# ヘルプを表示
curaq-tui help

# TUI アプリケーションを起動
curaq-tui
```

### 環境変数でトークンを設定

環境変数は保存された設定より優先されます：

```bash
CURAQ_MCP_TOKEN=your_token_here curaq-tui
```

### トークンの保存場所

トークンは `~/.config/curaq-tui/config.json` に保存されます。

## キーバインド

### 記事リスト
| キー | アクション |
|-----|--------|
| j/↓ | 下に移動 |
| k/↑ | 上に移動 |
| Enter | 記事を表示 |
| m | 既読にする |
| o | ブラウザで開く |
| a | 記事を追加 |
| T | テーマ選択 |
| ^R | リストを更新 |
| q | 終了 |

### リーダービュー
| キー | アクション |
|-----|--------|
| j/k | スクロール |
| Space/PgDn | ページダウン |
| PgUp | ページアップ |
| o | ブラウザで開く |
| Esc | リストに戻る |

### テーマ選択
| キー | アクション |
|-----|--------|
| j/k | テーマを選択 |
| Enter | 適用 |
| q | キャンセル |

## テーマ

利用可能なテーマ: default, ocean, forest, sunset, mono, sakura, nord, dracula, solarized, cyberpunk, coffee, tokyoMidnight, kanagawa, pc98

## 開発

```bash
pnpm dev
```
