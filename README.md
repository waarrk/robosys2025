# kana-sort

![GitHub Actions Status](https://github.com/waarrk/robosys2025/actions/workflows/test.yml/badge.svg)

`kana-sort` は **標準入力を受け取り、Unicode のデフォルト順で行をソートして返すコマンド**です。
前後の空白は取り除かれ、空行を含む入力はエラーとして終了コード 1 を返します。

人の名前を50音順にソートしたい場合に便利です。

## 動作検証済み環境

- OS: Ubuntu 22.04 / 24.04, macOS 14
- Python: 3.7 〜 3.12（3.7はUbuntu 22.04でのみ動作確認）

Windowsは非対応です

## インストール

```bash
$ git clone https://github.com/waarrk/robosys2025.git
$ cd robosys2025
$ chmod +x kana-sort test.bash
```

## 使い方

標準入力に 1 行ずつ名前などを与えます。

```bash
$ printf "山田\nあいざわ\nたなか\n" | ./kana-sort
あいざわ
たなか
山田
```

既存ファイルをソートする場合はリダイレクトして使います。

```bash
$ ./kana-sort < names.txt
```

## ライセンス

- BSD 3-Clause License

## 謝辞 / 参考資料

- 授業資料: [Ryuichi Ueda (CC-BY-SA 4.0)](https://github.com/ryuichiueda/slides_marp/tree/master/robosys2025) — コードを作成するにあたって参考資料として閲覧しました
- コード: [robosys2025](https://github.com/ryuichiueda/robosys2025) — 本人の許可のもと本コードのベースとして利用しました