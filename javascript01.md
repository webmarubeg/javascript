**学んだことを記述していく　Udemyでの学習記録（）**
- <script> の間に記載

** //オブジェクト＋メソッド（命令）の処理。windowの処理は隠れている**
- docume$nt.write('Javascriptの再学習していくぞ\n');
- alert('ご注意ください。macのフリーズ')

** // 1年が何秒か計算する**
- document.write(60*60*24*365);

**// ユーザーの入力を受け付ける ES2015以降の変数宣言：letを使用**
- let day = window.prompt('何日の秒数を計算しますか？');

**// 指定された日数の計算を行う**
- document.write(60*60*24*day);

**//従来の方法**
- document.write(hour + '時');

**//ES６以降の新しい方法 バッククォートの記号を使う「`」**
- document.write(`${hour}時 ${min}分 ${sec}秒`); //テンプレート表示

**//HTMLの要素を変更、修正する**
- <title>タイトルを変更してみるよ</title>
- let display = document.getElementById('time');
- display.innerHTML = '22時10分12秒';
- document.title = '(1)'+ document.title;
  

- </scirpt>
