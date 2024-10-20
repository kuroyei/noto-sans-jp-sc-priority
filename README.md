<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@100..900&family=Noto+Sans+SC:wght@100..900&display=swap" rel="stylesheet">

# Noto Sans JP SC Priority

フォントファミリーとして Noto Sans JP, SC を指定した簡体字中国語混ざりの日本語のドキュメントにて、簡体字の表示を最適化するための CSS である．

フォントファミリーを `'Noto Sans CJK JP'` や `'Noto Sans JP','Noto Sans SC'` と指定した場合、主に簡体字中国語で用いられる漢字の表示が不適切になる場合がある．

- <span style="font-family: 'Noto Sans JP';">我们必须尽快复习功课。</span>
- <span style="font-family: 'Noto Sans JP';">请记得出门时关灯。</span>

<span style="font-family: 'Noto Sans JP'; font-size: xx-large;">复, 关, 门</span> ではなく <span style="font-family: 'Noto Sans SC'; font-size: xx-large;">复, 关, 门</span> と表示されるべきだ．
