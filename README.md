# reversi_typescript
簡単リバーシアプリをTypeScriptで作成。各開発工程の復習も兼ねる。

## 環境構築

### Typescriptを実行するためのnodejsをインストール

- asdfのインストール
    - https://asdf-vm.com/guide/getting-started.htmlにアクセス
    - brew install asdf
        - homebrewがない場合はインストールしておく
    - bash＆homebrewを使用している場合
        - echo -e "\n. \"$(brew --prefix asdf)/libexec/asdf.sh\"" >> ~/.bash_profile
        - echo -e "\n. \"$(brew --prefix asdf)/etc/bash_completion.d/asdf.bash\"" >> ~/.bash_profile
- nodejsをインストール
    - brew install gpg gawk
    - asdf plugin add nodejs https://github.com/asdf-vm/asdf-nodejs.git
    - asdf list all nodejs
    - 使いたいバージョンを選定
    - 作業ディレクトリを作成、移動
    - ターミナルで`. code`を実行し、VScodeを開く
    - ディレクトリ配下に`.tool-versions`というファイルを作成
    - 1行目に`nodejs 16.17.1`を記述
    - VScodeのターミナルを開く
    - `asdf install`と入力
    - `node -v`を入力してバージョン情報が表示されれば完了

### ts-nodeでTypeScriptのHello Worldを実行

- ts-nodeは、Node.jsを使ってTypeScriptを簡単に実行できるツール
- ターミナルを開く
- `npm init`を入力
- package.jsonが出来る
- ターミナルで`npm install --save-dev typescript@4.8.3 ts-node@10.9.1`を実行
- hello.tsというファイルを作り、`console.log('Hello TypeScript')`と記述
- ターミナルで`npx ts-node hello.ts`を実行