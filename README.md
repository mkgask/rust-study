# Rust学習リポジトリ

## 📚 概要
このリポジトリは、Rustプログラミング言語を基礎から応用まで体系的に学ぶための総合教材です。Markdownによる解説と実行可能なサンプルコードを組み合わせ、自己学習に最適な構成となっています。
2025年4月3日にリリースされたRust 1.86.0をターゲットにしています。

## 👥 対象ユーザー
- プログラミング初心者〜中級者（他言語経験者）
- システム言語に興味のあるWeb開発者
- パフォーマンスと安全性を重視するアプリケーション開発者

## 🛠️ 環境構築
各OSごとのRust開発環境構築手順は以下のドキュメントを参照してください：
- [Windows環境構築](./chapters/00-environment-setup/windows-setup.md)
- [macOS環境構築](./chapters/00-environment-setup/macos-setup.md)
- [Linux環境構築](./chapters/00-environment-setup/linux-setup.md)
- [Docker環境](./chapters/00-environment-setup/docker-setup.md)
- [Podman環境](./chapters/00-environment-setup/podman-setup.md)

## 📝 カリキュラム内容
本リポジトリは以下の章構成でRustを学習します：

0. [環境構築](./chapters/00-environment-setup/README.md)
1. [Rustの基礎（変数、データ型、制御フロー）](./chapters/01-rust-basics/README.md)
2. [所有権システムとメモリ管理](./chapters/02-ownership-system/README.md)
3. [構造体とEnumによるデータモデリング](./chapters/03-data-modeling/README.md)
4. [エラーハンドリングの手法](./chapters/04-error-handling/README.md)
5. [ジェネリクスとトレイト](./chapters/05-generics-traits/README.md)
6. [コレクションとイテレータ](./chapters/06-collections-iterators/README.md)
7. [並行処理と非同期プログラミング](./chapters/07-concurrency-async/README.md)
8. [FFIと他言語連携](./chapters/08-ffi-interop/README.md)
9. [マクロとメタプログラミング](./chapters/09-macros-metaprogramming/README.md)
10. [実践的なWebアプリケーション開発](./chapters/10-web-development/README.md)
11. [システムプログラミングとRust](./chapters/11-system-programming/README.md)
12. [組み込み開発とRust](./chapters/12-embedded-development/README.md)

## 📋 リポジトリ構造
各章は以下の構成になっています：
- `README.md` - 章の概要と学習目標
- `contents/` - 解説文書（Markdown）
- `examples/` - 実行可能なサンプルコード
- `exercises/` - 演習問題とその解答例

## 🔧 学習方法
1. 各章のREADME.mdから始め、学習目標を確認
2. `contents/`の解説文書で概念を理解
3. `examples/`のサンプルコードを実行して動作を確認
4. `exercises/`の演習問題に挑戦して理解を深める
5. テストを実行して自分の実装が正しいか確認

## 🔄 進捗管理
各章の最後にはチェックリストと自己評価クイズがあり、理解度を確認できます。
各演習問題には段階的なヒントシステムが用意されているため、つまずいた時も自力で解決する力が身につきます。

## ⚡ Rustの特徴
- 安全性とパフォーマンスの両立
- 強力な型システムと所有権モデル
- コンパイル時の安全性チェック
- ゼロコスト抽象化
- 優れた並行処理サポート

## 🌟 貢献について
このリポジトリへの貢献をお待ちしています。詳細は[CONTRIBUTING.md](./CONTRIBUTING.md)をご覧ください。

## 📜 ライセンス
このプロジェクトは[MITライセンス](./LICENSE)の下で公開されています。