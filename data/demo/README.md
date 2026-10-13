# デモ用データ(data/demo)

`demo.html` が読み込むサンプルです。ファイルを書き換えて GitHub に上げると、デモに反映されます。

## ファイル

| ファイル | 中身 |
| --- | --- |
| `works.json` | 作品(カバー画像・カテゴリ・設定・メモ) |
| `characters.json` | キャラ(名前・ふりがな・色・タグ・基本情報・サンプルボイス・立ち絵) |
| `chars/○○.txt` | キャラの本文(AI整形後)。`characters.json` の `bodyFile` で指定 |
| `chars/○○.before.txt` | AI整形前の文章。`beforeFile` で指定。あると本文の上に「整形前/整形後」の切り替えが出ます(省略可) |
| `pic/` | 画像。JSON の `path`(例 `pic/mio.svg`)と同じ場所に置きます。svg / png / webp / jpg が使えます |

## 書き方のメモ

- 作成日は `"date": "2026-09-20"` のように書きます。
- キャラを増やすときは、`characters.json` の1人分をコピーして `id` を変えます(例 `cdemo6`)。`workId` は `works.json` の作品の `id` です。
- 本文を `chars/○○.txt` に分けず、JSON の `"body"` に直接書いても動きます。
- 作品の「設定」「メモ」の本文は、`works.json` の中の `body` に入っています。
- 整形前・整形後の文章は、「質問から作る」で出た文章と、AIで整えた文章をそのまま貼れば使えます。
