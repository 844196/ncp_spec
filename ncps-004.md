# NCPS-004: CLI暗号化コマンド仕様

ncipher暗号化仕様を実装したCLIコマンドは以下の要件を備える必要があります:

* 平文となるファイルを引数として指定できること
* 鍵および区切り文字を指定できること
* 変換結果を、改行を含め1行にして出力すること
* 引数としてファイルが指定されていない場合は標準入力より読み込むこと

```console
$ echo -e "あいうえお\nかきくけこ\nさしすせそ\n" > FILE

$ execute --key='0123456789abcdef' --sep='.' FILE
3042.3044.3046.3048.304a.a.304b.304d.304f.3051.3053.a.3055.3057.3059.305b.305d.a.
```
