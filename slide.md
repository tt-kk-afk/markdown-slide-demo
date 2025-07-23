---
marp: true
theme: default
lang: ja
style: |
  h1, h2, h3, h4, h5, h6, p, ul, li, th, td {
    word-break: auto-phrase;
  }

  h1, h2, h3, h4, h5, h6 {
    text-wrap: balance;
  }

  p, ul, li, th, td {
    text-wrap: pretty;
  }

---

# Gemini CLIでGitHub Pagesでスライドを公開してみた話

発表者: 加屋本 風子

---

## 背景・動機

- LLMってスライド作れるのかな？
  - PowerPointは直接無理そう...
  - テキストベースならいけるのでは？
- → マークダウンからスライドが作れる「Marp」を発見！
- **どうせなら、スライド作成から公開まで全部Gemini CLIにやらせてみよう！**

---

## 今回使ったAIアシスタント

**Gemini CLI**

- Google製のAI、Geminiをターミナル上で対話的に使えるツール
- ファイルの読み書き、コマンド実行、Web検索など、PC上の操作をAIに任せられる

---

## 使った技術

- **Gemini CLI**
  - Google製のAIアシスタント
- **Marp**
  - マークダウンからスライドを生成するツール
  - 今回はHTML生成。PowerPoint ファイルやPDFも作成可能。VSCode拡張もある
- **GitHub Pages**
  - GitHubリポジリから静的なWebサイトをホスティングする機能

---

## 普段使っているAI vs 今回のAI

| | **GitHub Copilot** | **Gemini CLI** |
|:---|:---|:---|
| **動作環境** | 主にIDE（VS Codeなど）内 | 主にターミナル/CLI |
| **得意なこと** | IDE内の開発作業支援、コード補完・提案 | ローカルファイルシステム/シェルコマンド操作、システムレベルの自動化 |
| **強み** | 開発者の思考を止めない、IDEとの深い連携 | PC作業全般を任せられる、IDEに依存しない汎用性 |

---

## 手順

1. **Marpのセットアップ**: `npm`でMarp CLIをインストール
2. **スライドの構成案作成**: Geminiと相談して構成を決定
3. **スライドのコンテンツ作成**: マークダウンでスライドを記述
4. **GitHubリポジトリの準備**: `git init` など
5. **MarpでHTMLを生成**: `marp`コマンドでHTML化
6. **GitHub Pagesで公開**: `gh-pages`ブランチにpush

---

## デモ・成果物

実際に公開したスライドがこちらです！

**https://tt-kk-afk.github.io/markdown-slide-demo/**

![width:50%](https://marp.app/assets/marp.svg)

---

## ハマったところ・工夫したところ

- **Gemini CLIへの指示**
  - 曖昧な指示より、具体的なステップを提示する方がスムーズ
  - 「〇〇して」より「〇〇するために△△のコマンドを実行して」
- **デザイン調整の難しさ**
  - GUIツールに比べて、コードベースでのデザイン調整は試行錯誤が大変
- **Gemini CLIの利便性**
  - チャット欄とターミナルを行き来する手間がなく、作業に集中できる

---

## まとめ

- Gemini CLIを使えば、スライド作成から公開まで自動化できる！
- 人間は構成案の確認や、指示の微調整に集中できる

ご清聴ありがとうございました。