<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@100..900&family=Noto+Sans+SC:wght@100..900&display=swap" rel="stylesheet">

# Noto Sans JP SC Priority

フォントファミリーとして Noto Sans JP, SC を指定した簡体字中国語混ざりの日本語のドキュメントにて、簡体字の表示を最適化するための CSS である．

フォントファミリーを `'Noto Sans CJK JP'` や `'Noto Sans JP','Noto Sans SC'` と指定した場合、主に簡体字中国語で用いられる漢字の表示が不適切になる場合がある．

![Noto Sans の比較](https://github.com/user-attachments/assets/6801eeaa-b771-43ff-a616-de69e9f2aa4f)
*Noto Sans の比較 (上から順に日本, 中国大陸, 台湾, 香港)*

私の主観に基づいて、簡体字中国語向けのフォントの表示を優先させるべき漢字を列挙した．

| 漢字 | Unicode  |
| ---- | -------- |
| 迂   | `U+8fc2` |
| 汲   | `U+6c72` |
| 迄   | `U+8fc4` |
| 丫   | `U+4e2b` |
| 芒   | `U+8292` |
| 迁   | `U+8fc1` |
| 剪   | `U+526a` |
| 圾   | `U+573e` |
| 窗   | `U+7a97` |
| 启   | `U+542f` |
| 曾   | `U+66fe` |
| 极   | `U+6781` |
| 适   | `U+9002` |
| 达   | `U+8fbe` |
| 复   | `U+590d` |
| 运   | `U+8fd0` |
| 关   | `U+5173` |
| 类   | `U+7c7b` |
| 门   | `U+95e8` |

```text
迂汲迄丫芒迁剪圾窗启曾极适达复运关类门
```

![SCフォントの表示を優先させるべき漢字](https://github.com/user-attachments/assets/a0e382a0-3faa-4b69-95e9-c892bab0966d)

## 使用方法

1. HTML の `<head>` に次のコードが埋め込まれていることとする．

   ```html
   <link rel="preconnect" href="https://fonts.googleapis.com">
   <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
   <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@100..900&family=Noto+Sans+SC:wght@100..900&display=swap" rel="stylesheet">
   ```

2. 本レポジトリの `noto-sans-sc-partial.css` の内容をコピーし、当該ドキュメントにお使いの CSS に貼り付ける．

3. フォントファミリーは次のように指定する．

   ```css
   font-family: 'Noto Sans SC partial','Noto Sans JP','Noto Sans SC';
   ```

> [!NOTE]
> `noto-sans-sc-partial.css` を `@import` するのではおそらく機能しない．

## 漢字を追加したい場合

1. 当該漢字の Unicode を調べる．
2. https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@100..900&family=Noto+Sans+SC:wght@100..900&display=swap にアクセスする．
3. 調べた Unicode で検索をかける．
4. `font-family: 'Noto Sans SC';` なる `@font-face` を見つけ出し、`src` の `.woff2` の URL をコピーする．
5. `noto-sans-sc-partial.css` に既存の記述に倣ってコードを書く．

> [!NOTE]
> `unicode-range` がハイフン `-` を用いて指定されている場合に注意する．
