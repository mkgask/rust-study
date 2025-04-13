# Windows環境でのRust開発環境構築

## 📋 前提条件
- Windows 10または11（64ビット推奨）
- 管理者権限のあるユーザーアカウント
- インターネット接続

## 🚀 Rustのインストール

### rustupを使用したインストール

1. [Rustの公式サイト](https://www.rust-lang.org/tools/install)にアクセスします。
2. 「RUSTUP-INIT.EXE」（64ビット版）をダウンロードします。
3. ダウンロードしたファイルを実行します。
4. デフォルト設定でインストールする場合は、表示されるプロンプトで `1) Proceed with installation (default)` を選択します。
5. インストールが完了すると、コマンドプロンプトかPowerShellを再起動する必要があります。

インストールが成功したか確認するには、新しくコマンドプロンプトかPowerShellを開いて以下のコマンドを実行します：

```powershell
rustc --version
cargo --version
```

バージョン情報が表示されれば、インストールは成功しています。

### Visual Studio Build Toolsのインストール

Rustでネイティブライブラリをビルドするためには、Visual C++ビルドツールが必要です：

1. [Visual Studio Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/)をダウンロードします。
2. インストーラーを実行し、「C++によるデスクトップ開発」ワークロードを選択します。
3. 右側のオプションパネルで、以下のコンポーネントが選択されていることを確認します：
   - Windows 10 SDK
   - MSVC - 最新のC++ビルドツール
   - C++ CMake Tools for Windows
4. 「インストール」をクリックして、選択したコンポーネントをインストールします。

## 🖥️ 開発環境のセットアップ

### Visual Studio Codeのインストールと設定

1. [Visual Studio Code](https://code.visualstudio.com/)をダウンロードしてインストールします。
2. VSCodeを起動し、拡張機能（Extensions）タブを開きます。
3. 次の拡張機能を検索してインストールします：
   - **rust-analyzer**: 高度なコード補完と解析
   - **CodeLLDB**: Rustプログラムのデバッグ
   - **Even Better TOML**: Cargo.tomlの編集サポート
   - **crates**: Rust依存関係の管理と更新
4. VSCodeの設定（File > Preferences > Settings）で、自動フォーマットを有効にします：
   ```json
   {
     "editor.formatOnSave": true,
     "rust-analyzer.checkOnSave.command": "clippy"
   }
   ```

## 🔧 追加ツールのインストール

### Rustコンポーネントの追加

以下のコマンドを実行して、便利なRustツールをインストールします：

```powershell
# コード整形ツール
rustup component add rustfmt

# 高度なlintツール
rustup component add clippy

# Rust言語サーバー（IDEサポート用）
rustup component add rust-analyzer

# ドキュメント生成ツール
rustup component add rust-docs
```

### Cargo拡張のインストール

```powershell
# cargo-editで依存関係管理を簡単に
cargo install cargo-edit

# cargo-watchでファイル変更を監視
cargo install cargo-watch

# cargo-expandでマクロ展開を確認
cargo install cargo-expand

# cargo-updateでプロジェクトの依存関係を更新
cargo install cargo-update
```

## 📱 Rustのバージョン管理

### バージョンアップ

rustupを使用すると、Rustツールチェーンを簡単に最新バージョンにアップデートできます：

```powershell
# rustup自身をアップデート
rustup self update

# Rustを最新版にアップデート
rustup update
```

### 複数バージョンの管理

プロジェクトごとに異なるRustバージョンを使いたい場合：

```powershell
# 利用可能なバージョンを確認
rustup toolchain list

# 特定のバージョンをインストール（例：1.86.0）
rustup toolchain install 1.86.0

# デフォルトのバージョンを切り替え
rustup default 1.86.0

# 特定のディレクトリで特定のバージョンを使用
cd プロジェクトディレクトリ
rustup override set 1.86.0
```

## 🚀 Hello Worldプロジェクトの作成

新しいRustプロジェクトを作成し、動作を確認しましょう：

```powershell
# 新しいプロジェクトを作成
cargo new hello_world
cd hello_world

# プロジェクトをビルドして実行
cargo run
```

`Hello, world!`と表示されれば、環境構築は成功です！

## 🔍 トラブルシューティング

### パスの問題

環境変数の設定が正しく行われていない場合は、手動でRustのbinディレクトリをPATHに追加します：

1. Windowsの検索で「環境変数」と入力し、「システム環境変数の編集」を選択
2. 「環境変数」ボタンをクリック
3. 「ユーザー環境変数」セクションで「Path」を選択し、「編集」をクリック
4. 「新規」をクリックし、`%USERPROFILE%\.cargo\bin`を追加
5. 「OK」を3回クリックして保存

### ビルドエラー

Visual C++ビルドツールが正しくインストールされていない場合、ビルド時にエラーが発生することがあります。その場合は、Visual Studio Build Toolsを再インストールしてみてください。

### rust-analyzerが動作しない

VSCodeを再起動しても問題が解決しない場合は、以下を試してください：

1. コマンドパレット（Ctrl+Shift+P）を開く
2. `Rust Analyzer: Restart Server`を実行

## 📚 参考リソース

- [Rust公式ドキュメント](https://doc.rust-lang.org/)
- [The Rust Programming Language (Book)](https://doc.rust-lang.org/book/)
- [Rust by Example](https://doc.rust-lang.org/rust-by-example/)
- [rustup ドキュメント](https://rust-lang.github.io/rustup/)

以上の手順で、Windowsに完全なRust開発環境が構築できます。次のステップは、[Rustの基礎](../01-rust-basics/README.md)に進んでRustプログラミングを学んでいきましょう！
