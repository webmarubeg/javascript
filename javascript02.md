**学んだことを記述していく　Udemyでの学習記録その２**

**ES６以降の新しい方法 バッククォートの記号を使う「`」**
**オブジェクト＋メソッド（命令）の処理。windowの処理は隠れている**

**for文、配列（曜日）**
**曜日を表示するプログラム(日：0、月:1、火:2、など)**
- const today = new Date();  

**ES6以前は、「array」で配列を作る必要があったが、ES6後は、下記のような記載で動作する**
- const week = ['日','月','火','水','木','金','土'];
- let week_jp = week[today.getDay()];
- document.write(`今日は、${week_jp}曜日です。`);
- 例1：document.write(week[today.getDay()]);
- 例2：document.write(today.getDay());

**連想配列（キーワード検索）**
- 連想配列について(pythonだとdictionary型が当てはまる)
- const words = {
    'Apple' : 'りんご',
    'Orange': 'オレンジ',
    'Grapes' : 'グレープ'
-     }
**数字以外のエラー処理など**

**キーワード検索を行うプログラム 例：文章など　「index0f」のメソッドを使う**
- const book = '我輩は猫である';
- let keyword = prompt('検索したい文字は？');
- let posion = book.indexOf(keyword);

**見つけたい文字が０番目以下の場合（見つからない時、「-1」と表示されるので数字で比較）**
- if (posion >= 0) {
- }


**文字ではエラーになるので型変換してから処理されるよう変換。整数にする「parseInt」**
- const cnt = parseInt(prompt('〜〜〜'));

**数字を判断する処理。isfiniteメソッドを使用**
- if (Number.isFinite(cnt)) {
- }

**計算時、四捨五入が必要な場合**
- Math.floor(切り上げ)
- Math.cell(切り下げ)がある

**ランダムな数値をコンピュータで出力させるメソッド**
**ランダム数値は小数点なので切り上げ、かつ１０倍すると整数**
- const q1 = Math.floor(Math.random() * 10)
- 例：ランダムな数値「0.５2242」が出力→数値を１０倍→切り上げする
