## 環境設定

### Linux(Ubuntu/Debian)

1. 以下のaptパッケージをインストール

    ```bash
    sudo apt update && sudo apt-get install -y vim python3-pip curl git
    pip3 install --upgrade pip
    pip install docker-compose
    ```

2. Dockerをインストール
    ```bash
    sudo curl -sSL get.docker.com | sh
    ```

    こちらも参照 [https://docs.docker.com/install/](https://docs.docker.com/install/)

## インストールする

1. 以下のコマンドを実行してダウンロード＆フォルダに入る

    ```bash
    git clone -b 2.0 https://github.com/edu-ids/OnlineJudgeDeploy.git && cd OnlineJudgeDeploy
    ```

2. 適切にdocker-compose.ymlを書き換える

   一部，CHANGE_THISみたいなやつがあるのでそこら辺は対応したほうがいいと思います．

3. Docker-Composeを立ち上げる

    ```bash
    docker-compose up -d
    ```

5分くらいで完璧になります

 `docker ps -a`を実行して `unhealthy` や `Exited (x) xxx` になってなければOK

## フォーク元

https://github.com/QingdaoU/OnlineJudgeDeploy