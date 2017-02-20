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

#### vagrantのプラグインのインストール
* vagrant-vbguest
virtualboxをvagrantから利用するためのプラグイン
```
$ vagrant plugin install vagrant-vbguest
```
* vagrant-chef-zero
