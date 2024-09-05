## 開発用ディレクトリを作成
` npm init -y `

## 関連パッケージをインストール
` npm install --save-dev typescript ts-loader webpack webpack-cli webpack-dev-server `

### # typescript

### # webpack

### # ts-loader
- ts-loaderの主な機能:
    1. tsファイルをコンパイルし、JacaScriptに変換します。
       これによりTypeScriptで書かれたコードをブラウザで実行できます。

### # webpack-cli
- webpack-cliの主な機能:
    1. webpackをコマンドラインで実行できます。
       例えば、ビルドを開始するときは ` webpack `とコマンドを打つだけです。

### # save-dev
- webpack-dev-serverの主な機能:
    1. ローカル開発サーバーの立ち上げ
    2. ホットリロード
         ファイルが変更されるたびブラウザが自動的にリロードされます。
    3. プロキシの設定
         APIリクエストを別のバックエンドサーバーにプロキシする設定が可能になります。

## Web packの設定
` webpackconfig.js `ファイルを作成。

### # entry
- エントリーポイントを指定します。
  パスの指定先のtsファイルを起点にしてコンパイルを行います。
  起点ファイルが依存しているほかのモジュールやファイルすべて辿り、最終的に1つのjsファイルにまとめます。

### # output
- 出力先を指定します。パスで指定した先にコンパイルされたjsファイルが格納されます。
- ファイルネームを指定します。[name]はエントリーポイントで指定された名前を使ってファイル生成します。

### # resolve
- Web packがファイルやモジュールをインポートするときどのようなファイルを見つけるかを定義します。
- 例えば、import文でファイル拡張子を書かなくても指定した拡張子の順に探してくれます。

### # devServer
- staticで静的ファイルのパスを指定します。

### # module
- moduleでモジュールに対してどのように処理を定義します。
- rulesでファイルの種類に応じて適用するルールを定義します。
    - loaderでなんのローダーを使うかを明記します。
    - testでどのファイルにローダーを適用するか指定します。

## TypeScriptの初期設定
` npx tsc --init `
