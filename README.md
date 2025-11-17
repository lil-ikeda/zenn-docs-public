# Zenn Docs Public

このリポジトリは[Zenn](https://zenn.dev)で公開する技術記事・本を管理するためのものです。

## 📚 ディレクトリ構成

```
.
├── articles/      # 技術記事（.mdファイル）
├── books/         # 技術書籍
└── .github/       # GitHub連携設定
```

## 🚀 セットアップ

### 必要な環境
- Node.js 18.x以上

### インストール

```bash
npm install
```

## 💻 開発コマンド

### プレビュー
ローカルでプレビューサーバーを起動します：

```bash
npx zenn preview
```

ブラウザで http://localhost:8000 にアクセスして記事を確認できます。

### 新規記事作成

```bash
# ランダムなslugで記事を作成
npx zenn new:article

# 特定のslugで記事を作成
npx zenn new:article --slug my-article-slug
```

### 新規書籍作成

```bash
# ランダムなslugで書籍を作成
npx zenn new:book

# 特定のslugで書籍を作成
npx zenn new:book --slug my-book-slug
```

### コンテンツ一覧

```bash
# 記事一覧
npx zenn list:articles

# 書籍一覧
npx zenn list:books
```

## 📝 記事の書き方

### Frontmatter

各記事ファイルの先頭には以下のようなfrontmatterを記述します：

```yaml
---
title: "記事のタイトル"
emoji: "📌"
type: "tech"  # tech: 技術記事 / idea: アイデア記事
topics: ["topic1", "topic2"]  # トピック（最大5つ）
published: true  # 公開設定（trueで公開）
published_at: "2025-01-16 12:00"  # 公開日時（省略可）
---
```

### 本文の書き方

- Markdown形式で記述
- Zenn独自の記法も使用可能（メッセージ、アコーディオンなど）
- 詳細は[ZennのMarkdown記法](https://zenn.dev/zenn/articles/markdown-guide)を参照

## 🚢 公開方法

1. 記事のfrontmatterで `published: true` に設定
2. GitHubにpush

```bash
git add .
git commit -m "記事を公開"
git push
```

GitHubにpushすると自動的にZennに反映されます。

## 🔗 参考リンク

- [📘 Zenn CLIの使い方](https://zenn.dev/zenn/articles/zenn-cli-guide)
- [📘 Zenn CLIのインストール](https://zenn.dev/zenn/articles/install-zenn-cli)
- [📘 ZennのMarkdown記法](https://zenn.dev/zenn/articles/markdown-guide)

## 📄 ライセンス

記事の内容は各記事の著者に帰属します。