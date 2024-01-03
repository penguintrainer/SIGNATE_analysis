## 環境構築に関するメモ書き
新しいPCで作業を始めるとすると、私だったらこうやって環境構築するぞ
というメモ書き

---
### 開発環境のインストール
### VS code のインストール
多機能なテキストエディタ
[VS code](https://code.visualstudio.com/)

### gitのインストール
ソフトウェアのバージョン管理ソフト
後々使う、ソースコード共有に使われる[github](https://github.com/)を使うときにも使われる
[git](https://git-scm.com/downloads)

---
### pythonの実行環境のインストール
PCの本体へのインストールは下記の2つのみ
- penvのインストール
- pipenvのインストール

その他のライブラリの導入などは各仮想環境毎に実行する

### pyenvのインストール
一つのPCで複数のバージョンのpythonの実行環境を構築してくれるツール

[pyenv-win](https://github.com/pyenv-win/pyenv-win/blob/master/docs/installation.md#powershell)
インストールコマンドはドキュメントを確認してほしいが、下記の通り
```bash
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine
```
```bash
Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"
```

[公式サイト](https://www.python.org/)を使ってpythonのインストールも可能であるが、pythonのバージョン違いによるエラーが発生した場合に、個別に入れ直さないと行けないので少し面倒。


### pipenvのインストール
一つのPCで複数の仮想環境を構築してくれるライブラリ
プロジェクト毎に実行環境を構築してくれる
[pipenv](https://pipenv-ja.readthedocs.io/)

仮想環境関係のフォルダをプロジェクトフォルダに格納するための設定
よくわからない場所()に、おっきなファイルが生成されるのを防ぐ
[PIPENV_VENV_IN_PROJECT](https://pipenv-ja.readthedocs.io/ja/translate-ja/advanced.html#pipenv.environments.PIPENV_VENV_IN_PROJECT)

---