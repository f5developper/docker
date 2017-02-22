# docker

### やること

- [ ] vagrantインストール
- [ ] chefインストール
- [ ] dockerインストール
  - [ ] apacheインストール
  - [ ] php5.6インストール
  - [ ] fuelphpインストール
  - [ ] groongaインストール
  - [ ] mailcatcherインストール

### vagrantインストール

#### virtualboxをインストールする
以下のURLから取得する
　http://www.oracle.com/technetwork/server-storage/virtualbox/overview/index.html

#### vagrantのインストール
以下のURLから取得する。
http://www.vagrantup.com/downloads

##### vagrantのプラグインのインストール
* vagrant-vbguest
virtualboxをvagrantから利用するためのプラグイン
```
$ vagrant plugin install vagrant-vbguest
```
* vagrant-chef-zero

#### osインストール

https://atlas.hashicorp.com/bento/boxes/centos-7.3/ から取得


### dockerをインストール

* dockerインストールスクリプ入手
```
$sudo curl -sSL https://get.docker.com/ | sh
```

* sudoユーザにする
これをやらないとdockerコマンドの度にsudoをつけないといけない
```
$ sudo usermod -aG docker vagrant
```

* docker 再起動
```
sudo service docker restart
```
* インストール確認
```
docker version
```
以下のようになっていること

```
Client:
 Version:      1.13.1
 API version:  1.26
 Go version:   go1.7.5
 Git commit:   092cba3
 Built:        Wed Feb  8 06:38:28 2017
 OS/Arch:      linux/amd64

Server:
 Version:      1.13.1
 API version:  1.26 (minimum version 1.12)
 Go version:   go1.7.5
 Git commit:   092cba3
 Built:        Wed Feb  8 06:38:28 2017
 OS/Arch:      linux/amd64
 Experimental: false
```

* dockerコンテナの全削除
```
docker rm -v $(docker ps -aq -f status=exited)
```
