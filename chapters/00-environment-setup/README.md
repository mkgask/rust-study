# 第0章: Rust開発環境構築

## 📚 この章の概要
Rustプログラミングを始めるために必要な開発環境の構築方法を解説します。OSごとの手順、推奨ツール、環境構築後の確認方法までをカバーします。

## 🎯 学習目標
- Rustの開発環境を自分のマシンに構築できるようになる
- rustupによるRustツールチェーンの管理方法を理解する
- 基本的なRust開発ツールの使い方を習得する
- コードエディタ/IDEの設定と拡張機能を活用できるようになる

## 🧩 環境構築の基本要素
Rust開発環境は主に以下の要素で構成されています：

1. **Rustツールチェーン**: rustc（コンパイラ）、cargo（パッケージマネージャ兼ビルドツール）など
2. **rustup**: Rustのバージョン管理ツール
3. **コードエディタ/IDE**: Visual Studio Code、IntelliJ IDEA、Vimなど
4. **拡張機能**: rust-analyzer、Rustfmtなど

## 💻 OS別セットアップガイド
お使いのOSに合わせて以下のガイドを参照してください：

- [Windows環境構築](./windows-setup.md)
- [macOS環境構築](./macos-setup.md)
- [Linux環境構築](./linux-setup.md)
- [Docker/Podman環境](./docker-podman-setup.md)

## ✅ 環境構築の確認

環境構築が完了したら、以下のコマンドで正しくインストールされているか確認しましょう：

```bash
# Rustコンパイラのバージョン確認
rustc --version

# Cargoのバージョン確認
cargo --version

# rustupのバージョン確認
rustup --version
```

## 🔄 Rustの更新とメンテナンス

rustupを使用して、Rustを最新バージョンに更新できます：

```bash
# Rustを最新版に更新
rustup update

# 特定のコンポーネントの追加
rustup component add clippy rustfmt

# クロスコンパイル用のターゲットを追加（例：WebAssembly）
rustup target add wasm32-unknown-unknown
```

## 🛠️ 推奨開発ツール

### IDE/エディタ
- **Visual Studio Code + rust-analyzer拡張機能**
  - 高機能な補完とコード解析
  - デバッグ機能
  - Rustfmtによるコード整形

- **IntelliJ IDEA + Rust Plugin**
  - JetBrains IDEに慣れている方向け
  - 充実したリファクタリング機能

- **Vim/Emacs + LSP連携**
  - 軽量で高速
  - カスタマイズ性が高い

### その他の便利ツール
- **clippy**: 高度なlintツール
- **rustfmt**: コード整形ツール
- **cargo-edit**: 依存関係管理を簡単にするツール
- **cargo-watch**: ファイル変更を監視して自動的にビルド/テスト実行

## 📝 次のステップ
環境構築が完了したら、[第1章：Rustの基礎](../01-rust-basics/README.md)に進んで、Rustプログラミングを始めましょう！
