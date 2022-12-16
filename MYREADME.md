# 自分流解き方
Dockerで作成したUbuntuの仮想環境上でコマンドを実行する。

# 環境

## Docker image repository
https://hub.docker.com/repository/docker/kr7fl/ubuntu-shellgei

## ローカルにpull
```sh
docker pull kr7fl/ubuntu-shellgei
```

## 起動の仕方
```sh
docker images
```
で上記Docker imageのIMAGE IDを探す。

```sh 
docker run <IMAGE ID> -it bash 
```
でシェルを起動。ここで練習問題、問題を解く。

## imageを更新した場合
コンテナに変更を加えた場合、変更を加えたimageを再度dockerhubにpushする必要がある。

```sh
exit
```

```sh
docker ps -a 
```
でSTATUSが最近終了したCONTAINER IDを探す。

```sh
docker commit <CONTAINER ID> kr7fl/ubuntu-shellgei
```

```sh
docker push kr7fl/ubuntu-shellgei
```