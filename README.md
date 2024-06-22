# Makefile入門

## Makefileの構成

1. Makefileの中で用いる変数(マクロ)の設定

```Makefile
変数名 = 定義
```

2. ルールの設定

```Makefile
ターゲット: 依存するファイル名
  コマンド
```

実行時のコマンドは、以下のようになる

```shell
make ターゲット
```

### level1

実行コマンド

```shell
make compile
```

ファイルの内容

```shell
compile: main.c
	gcc main.c -o hello
```

### level2

## 参考サイト

http://www.jsk.t.u-tokyo.ac.jp/%7Ek-okada/makefile/

https://qiita.com/yagiyuki/items/ff343d381d9477e89f3b#%20Makefile%E3%81%AE%E3%82%B5%E3%83%B3%E3%83%97%E3%83%AB

https://qiita.com/mizcii/items/cfbd2aa17f6b7517c37f
