# Ubuntu Docker Environment Template

機械学習やPythonを用いた開発のためのUbuntuベースのDocker環境構築テンプレートです．

## Quick Start
### 1. Library
必要なパッケージを`requirements.txt`に入力してください．

### 2. Image Build
`docker` フォルダ内の`build.sh`の`ubuntu_docker_temp`を任意のイメージ名に変更してください．次に，以下のコマンドを実行し，`build.sh`を実行することで，イメージが作成されます．

```bash
cd docker
bash build.sh
```

### 3. Container Run
`run.sh`の`ubuntu_docker_temp`を`build.sh`に入力したのイメージ名に変更してください．次に，`docker`フォルダの1つ上の階層に戻り，以下のコマンドを実行し，コンテナを起動してください．（末尾の 0 は使用するGPUのIDを指定しています）

```bash
bash run.sh 0
```

## Directory Structure
```text
.
├── README.md
├── docker/
│   ├── Dockerfile         # Dockerイメージの構成ファイル
│   ├── build.sh           # イメージ構築用スクリプト
│   └── requirements.txt   # インストールするPythonライブラリの一覧
├── run.sh                 # コンテナ起動用スクリプト
└── .gitignore