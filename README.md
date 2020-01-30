# MPD Dsiplay on I2C-OLED with isaax IoT

秋月電子のSO1602AW というI2C-OLEDを使ってMPDの曲名を表示するpythonスクリプト...をisaax IoTで制御するやつです。

![http://nw-electric.way-nifty.com/photos/uncategorized/2016/09/14/oled_r3.jpg](http://nw-electric.way-nifty.com/photos/uncategorized/2016/09/14/oled_r3.jpg)



### Volumio2への導入方法

Volumio2のユーザー名とパスワードは共に `volumio` です。

1. `/etc/modules`に`i2c-dev` が記載されていることを確認します。なければ追記してください。
2. `/boot/config.txt`に`dtparam=i2c_arm=on` が記載されていることを確認します。なければ追記してください。
3. `sudo reboot` で再起動します。
4. このリポジトリをforkします。
5. [Isaax IoT](https://isaax.io/)への登録を済ませます。
6. プロジェクトを作成します。リポジトリは先程forkしたリポジトリを指定します。
7. トークンを発行します（トークンの下に書かれてるシェルスクリプトをコピーすると楽です）
8. `sudo apt-get update` でパッケージをアップデートします
9. コピーしたシェルスクリプトを貼り付けて実行します
10. `isaaxd installation complete`と表示されたら完了です。サービスの登録やコードのデプロイはこの時点で完了しています。
