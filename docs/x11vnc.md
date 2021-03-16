# x11vnc コマンドの説明

## -display

Usage:
```bash
-display <disp>
```

X11サーバーディスプレイが接続する宛先。デフォルトは`:0`。Xサーバープロセスは同じマシンで実行され、`MIT-SHM`をサポートしている必要がある。`DISPLAY`環境変数を`<disp>`へ設定するのと同じである。

## -auth

Usage:
```bash
-auth <file>
```

起動前に`XAUTHORITY`環境変数を`<file>`に設定するのと同じように、X権限ファイルを`<file>`に設定する。`-xauth`ファイルと同じである。

## -forever

最初のクライアントが切断されたらすぐに終了するのではなく、より多くの接続をリッスンし続ける。`-many`と同じ。


## -loop

x11vncプロセスが終了するたびに再起動する外部ループを形成する。`-bg`と`-inetd`はこのモード内では無視される。

Xサーバーが終了して再起動した場合でも続行するのに便利である(その時点で、プロセスはもちろん新しいXサーバーに再接続するためのアクセス許可が必要になる)。

## -noxdamage

x11vncはDAMAGE拡張を1) 画面があまり変化していないときの負荷を大幅に軽減し、2) 変更された領域(デフォルトでは小さな領域)をより迅速に検出する。

を使わない