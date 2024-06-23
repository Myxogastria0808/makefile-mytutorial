# Makefile入門

## Makefileの構成

1. Makefileの中で用いる変数(マクロ)の設定

```Makefile
変数名 = 定義
```

2. ルールの設定

```Makefile
ターゲット: 依存ファイル名1 依存ファイル名2 ...
  コマンド 1
  コマンド 2
  コマンド 3
```

**コマンドの前は、TABで空ける**

実行時のコマンドは、以下のようになる

```shell
make ターゲット
```

### make-sample

実行コマンド

```shell
make compile -f Makefile
```

makefileのファイル名を指定しない場合は、以下の順番でファイルが探索される。

GNUmakefile → makefile → Makefile

ファイルの内容

```makefile
compile: main.c
　gcc main.c -o hello
```

## 参考サイト

https://ie.u-ryukyu.ac.jp/~e085739/c.makefile.tuts.html

http://www.jsk.t.u-tokyo.ac.jp/%7Ek-okada/makefile/

https://qiita.com/yagiyuki/items/ff343d381d9477e89f3b#%20Makefile%E3%81%AE%E3%82%B5%E3%83%B3%E3%83%97%E3%83%AB

https://qiita.com/mizcii/items/cfbd2aa17f6b7517c37f

# cargo-make 入門

## install

```shell
cargo install --force cargo-make
```

### cargo-make-sample

実行コマンド

```shell
makers COMPILE
```

ファイルの内容

```toml
[tasks.COMPILE]
description = "compile source files"
script = ['''
#!/bin/bash
gcc main.c -o hello
./hello
''']
```

## 参考サイト

https://sagiegurari.github.io/cargo-make/

https://www.tkat0.dev/posts/cargo-make-1/

https://qiita.com/ota42y/items/299197505062d4f7958b
