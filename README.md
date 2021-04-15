# etrob

[ETロボコン](https://etrobo.jp/)のEV3/シミュレータ双方に対応する開発環境のインストール方法を説明します.


【インストール手順】

まず, シミュレータと開発環境のインストールにはにはVisual Studio Codeをインストールする必要があります.

https://azure.microsoft.com/ja-jp/products/visual-studio-code/

上記のURLからVisual Studio Codeをダウンロードし, インストールしてください.

Visual Studio Codeのインストールが終わったら, シミュレータと開発環境のインストールを行います. 

ターミナルでルートディレクトリに移動し, 以下のコマンドを入力してください. 


```
echo 'name=startetrobo_mac.command; if [ ! -f $name ]; then curl -O https://raw.githubusercontent.com/ETrobocon/etrobo/master/scripts/$name; chmod +x ~/$name; fi; ~/$name' > "Start ETrobo.command"; chmod +x "Start ETrobo.command"
```

コマンドを入力すると, ルートディレクトリ内に`Start ETrobo.command`が作成されるのでダブルクリックしてください.　自動的にインストールが開始されます.

インストールは1時間ほどかかりますが, 途中で`Password:`と入力を求められることがあります. その際はMacのパスワードを入力してください.ただし, `cybozu`の`UserName`と`Password`の組を求められた際には, ETロボコンの参加者専用ページのユーザ名とパスワードを入力します. インストールする際にはまだ登録していないと思うので, 何も入力せずにエンターを押してください.

ネットワークの環境が悪いと, 回線の接続が途中で切れることがあります. その場合にインストールが途中で止まってしまい失敗した場合は, 以下のコマンドで途中のインストールデータを削除しもう一度`Start ETrobo.command`をダブルクリックし, インストールをやり直してください.

```
./startetrobo clean
```


インストールが完了すると, 自動的にVSCodeが立ち上がります.
立ち上がったVSCode内で`Ctrl+Shift+@`を入力すると下の方にターミナルタブが開きます. そこで`make sample`と入力し, サンプルが立ち上がれば成功です.

エラーが出た場合, Mattermostの`@e175708`かこちらのgitのページのIssuesに連絡お願いします. 
