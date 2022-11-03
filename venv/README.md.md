# venv setup

## セットアップコマンド

`Python 3.9.6`であることを確認します。

```bash
python -V
```

Virtual Environmentを構築します。

```bash
python venv venv
 ```

ディレクトリを移動します。

```bash
cd venv
```

pipをアップグレードします。

```bash
./bin/python3 -m pip install --upgrade pip
```

パッケージリストを取得します。

```bash
./bin/python3 -m pip freeze > requirements.txt
```

環境を起動していない場合は環境を起動します。

```bash
. ./bin/activate
```

## パッケージ管理の手順

### 新規にパッケージをインストール(保守)

何かしらのパッケージをインストールしたら、パッケージリストを更新します。

```bash
./bin/python3 -m pip install pandas
```

パッケージインストールを実行後は以下のコマンドを実行します。

```bash
./bin/python3 -m pip freeze > requirements.txt
```

## パッケージリストの復元方法

ディレクトリを移動していない場合はディレクトリを移動します。

```bash
cd venv
```

環境を起動していない場合は環境を起動します。

```bash
. ./bin/activate
```

`requirements.txt` を元にパッケージをインストールします。

```bash
./bin/python3 -m pip install -r requirements.txt
```
