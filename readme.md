## コンペ用のリポジトリ
人に見せるかもしれないし、見せないかもしれないリポジトリ
データ解析コンペで使用したプログラムをプロジェクト別にサブモジュールに分けて保存してある

## 使い方
初回クローン時
```bash
git clone --recursive {URL}
```

更新時
```bash
git submodule update --init --recursive
```

これらによって一連のプロジェクトのファイルがクローンされる。
個別のプロジェクトのディレクトリに移動して、`pipfile`のあるディレクトリで
```bash
pipenv install --dev
```
を実行することで、ディレクトリ内に`.venv`ディレクトリが作成されて、仮想環境のディレクトリが完成する。
下記コマンドを実施することで、ターミナル上で仮想環境が立ち上がる。
VS codeでも同様にディレクトリ内の`.venv`内のpythonをカーネルに設定することで仮想環境が立ち上がる
```bash
.\.venv\Scripts\activate
```
個別のプロジェクトにある各種notebookを開いて実行することで、解析を実施することができる。

- データのダウンロードなどは基本的に下記のコマンドでの利用
詳しい使い方や最新情報は[SIGNATE CLIドキュメント](https://github.com/signatelab/signate-cli)を各自で確認してください
```bash
signate download --competition-id=<id> --path=./data/output
```

## ディレクトリ構造

```bash
├─ README.md
├─ doc
│  └─ setup.md
└─ projects
   ├─ example
   │   ├─ data
   │   │  ├─ input
   │   │  └─ output
   │   ├─ baseline.ipynb
   │   └─ ......
   ├─ ......
   └─ ......
```

