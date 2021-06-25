# このアプリケーションについて

## 名称

OJM-Drone

## 概要

ドローンを遠隔操作するためのサービス（アプリケーション）。
現時点ではベータ版（今後大幅なバグ修正、機能追加、変更の可能性がある）

![overview_1](/ja/images/overview_1.png)



## 使用するアプリケーション

### OJM-Drone (remote)

ドローンを操作する側のアプリケーション。**インターネット上のサーバーにブラウザからアクセスするため、インストールなどは不要。**

サーバーは当アプリケーション製作者が管理している

![run_1](/ja/images/run_1.png)


### OJM-Drone (local)

ドローンと接続し、`OJM-Drone (remote)`とデータ送受信をするアプリケーション。以下に示す手順に従い、**ダウンロード、セットアップが必要。**

![run_8](/ja/images/run_8_.png)

# OJM-Drone (local) のセットアップ方法

## 必要なディバイス

### ドローン

[Tello/Tello EDU](https://www.ryzerobotics.com/jp/tello)
  
### PC

#### OS

以下のいづれか

  - Windows 10 (64bit)
  - mac OS (amd)
  
#### ブラウザ

以下のいづれか

 - Google Chrome
 - Microsoft Edge
 - Safari (mac OSのみ)

### その他


ドローンに接続するPCには、以下2つのネットワークインターフェースが必要

- ドローンに接続するためのWi-Fi用のネットワークインタフェース
- インターネットに接続するためのネットワークインターフェース


## 方法 - Windows 


### 1. ダウンロード

1. 以下のURLからzipファイルをダウンロードする(zipなどのファイル名は本アプリのバージョンにより若干異なる)

URL: https://drive.google.com/drive/folders/1Skjsp83Klaewc2UoEX8JWCGnkMBmdChz


![download_1](/ja/images/download_1_.png)

2. ダウンロードしたzipを右クリック＞「すべて展開」

![download_2](/ja/images/download_2_.png)


3. 任意のフォルダを指定し、「展開」

![download_3](/ja/images/download_3_.png)


以下の様に展開される

![download_4](/ja/images/download_4_.png)
![download_5](/ja/images/download_5_.png)






### 2. アプリケーションの起動と初期設定

1. `ojm-drone.exe`をダブルクリックする

**NOTE:**

「指定されたデバイス、パス、またはファイルにアクセスできません」というエラーメッセージが表示される場合、再起動すると直る場合がある。

![setup_1](/ja/images/setup_1_.png)

2. 以下の様なコマンドプロンプトが起動する。5秒ほど待機するとブラウザが起動し、以下の様な画面になる

**NOTE:**

起動するブラウザが、Google Chrome / Microsoft Edge / Safariのいづれでもない場合、一度ブラウザを閉じ、改めて左記のいづれかのブラウザを起動し、アドレスバーに`http://localhost:8000`を入力し、画面を開く


![setup_2](/ja/images/setup_2.png)
![setup_3](/ja/images/setup_3.png)

3. 前手順で起動したブラウザの画面で、「continue」を押下すると、以下の様な「set up」画面に遷移する

![setup_4](/ja/images/setup_4_.png)

4. 別途配布された、アクセストークンをテキストボックスに貼り付ける

**NOTE:**

アクセストークンはユーザーに毎に異なるため、実際に入力する文字列の長さ、及び「Saved access token:」の見え方は、本イメージのものと異なる。

アクセストークンは本アプリケーションを使用するための**パスワードのようなもの**のため、むやみに他者に教えたりしてはならない。


![setup_5](/ja/images/setup_5_.png)

5. 「update」を押下する。更新が完了するまで待つ（プログレスバーが消えるまで）。更新が完了すると以下の様になる

![setup_6](/ja/images/setup_6_.png)






### 3. ドローンとPCとの接続

#### ファイアーウォールの設定

通常のPCでは、ウィルスソフトの設定やOS自体のファイアウォールの設定により、ドローンとのデータ送受信が遮断される。
一時的にファイアウォールをOFFにするか、ルールを追加することにより、ドローンとのデータ送受信を可能とする

例1： AVG(Internet Security)で、ファイアーウォール自体をOFFにする

![fw_1](/ja/images/fw_1.png)


例2：AVGで、ファイアーウォールのルールを追加する

![fw_2](/ja/images/fw_2.png)


#### ドローンとの接続、インターネット接続


![connect_1](/ja/images/connect_1_.png)


### 4. アプリケーションの開始

1. 「run」タブに遷移する

![run_2](/ja/images/run_2_.png)

2. 「Generate」を押下する

![run_3](/ja/images/run_3_.png)


3. 「START」を押下する(Start Codeをコピーしておく。後続の手順で使用する）


**NOTE:**

実際に本アプリケーションを使用する際は「Start Code」を、ドローンをリモートで操作する人（友人、知人etc)に、共有する必要がある。

この「Start Code」は、あなたのドローンに、他者がアクセスするための一時的なパスワードのようなもののため、メール、チャットツールなどのある程度クローズドなチャネルで共有する必要がある。


![run_4](/ja/images/run_4_.png)

4. **ブラウザの別のタブを開き**、`https://ojm-drone.ajizablg.com`にアクセスする

![run_1](/ja/images/run_1.png)


5. 前までの手順で記録したStart Codeをテキストボックスに貼り付ける

![run_5](/ja/images/run_5_.png)


6. 「START」を押下する 

![run_6](/ja/images/run_6_.png)


7. 以下の様なダイアログが出てきたら、「パブリックネットワーク....」にチェックをし、アクセスを許可する 

![run_7](/ja/images/run_7.png)

8. ドローンとの接続などが正常であれば以下の様になる。

- `http://localhost:8000`のほうで、「Drone's status」の「connection」がOKになる
- `http://localhost:8000`のほうで、「Takeoff」を押下すると離陸、「Land」を押下すると着陸する
- `https://ojm-drone.ajizablg.com`で、ドローンを操作できる

 ![run_8](/ja/images/run_8_.png)
 ![run_9](/ja/images/run_9__.png)




### 5. アプリケーションの停止

 - 画面右上の「terminate」を押下する

![end_1](/ja/images/end_1_.png)

 - または、`ojm-drone.exe`ダブルクリック時に起動したコマンドプロンプト上で「Ctrl+c」を、コマンドプロンプトが閉じるまで連打する

![end_3](/ja/images/end_3.png)


## 使用方法 - mac OS

TBD
