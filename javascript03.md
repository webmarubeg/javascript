**学んだことを記述していく　Udemyでの学習記録その3**

**ES６以降の新しい方法 バッククォートの記号を使う「`」**
**オブジェクト＋メソッド（命令）の処理。windowの処理は隠れている**

**ランダムな数値をコンピュータで出力させるメソッド**
**ランダム数値は小数点なので切り上げ、かつ１０倍すると整数**
- const q1 = Math.floor(Math.random() * 10)
- 例：ランダムな数値「0.５2242」が出力→数値を１０倍→切り上げする

**スコープについて（グローバル変数とローカル変数の意味合いも含む）**
- 関数の中の定義は関数内
- var 宣言でグローバル変数として扱える？これ、後で学び直し

**クラス、コンストラクタ、インスタンスについて。javascriptでの定義**
- pythonでは、クラス設計時、self、などが必要だがjavascriptでは要らない
- コンストラクタやインスタンス関連はあまり違いはなさそう（今のところはそんな認識）
- class Item {
- //コンストラクタを定義する
- constructor(price) {
- this.price = price;
**Itemクラスからインスタンスを作成（属性.methodの形）**
- const item = new Item(price);

**setterとgetterについては意味がわからない状況。**
- setterとgetterを使うと、プロパティなどを安全に設定できるらしい。
- 使い方以前に、どこがプロパティとかクラス、methodかを確認しておきたい

**HTMLでのボタン制御を行う処理**
- それぞれのメソッドがどういう制御が可能でどう動くのかを記載したほうがいい？
- getElementById
- - 要素を取得するメソッド
- addEventListener
- -同一のイベントに複数の処理を登録することのできるメソッド
- -addEventListener(イベントのタイプ, 関数, オプション)の三つの引数を指定できる
- querySelector
- -※任意の要素を取得。詳細は後日
- nextElementSibling.innerHTML
- -隣接する次の要素を取得する。上記の場合は「innerHTML」の要素を取得する


- <button id="buy">決済する</button>
- id属性にある「buy」のbutton属性を取得して制御
- const btn = document.getElementById('buy');
- //一度押すと、無効にする このボタンをクリックした時に〜の処理
- btn.addEventListener('click', () =>{btn.disabled = true;});
- 他、dblclick＝ダブルクリックで処理が可能になる


**メールアドレス入力の制御**
- メールアドレス： <input type="email" name="email" id="">
- querySelector('input[name="email"]')
- email.nextElementSibling.innerHTML = '※ メールアドレスをご記入ください';


**チェックボックスの制御**
- <input type="checkbox" name="agree" id="agree">同意する
- <button id="submit" disabled>送信する</button>
- document.getElementById('submit').disabled = !agree.checked;
- -disabled(使用禁止)で送信ボタンのon/offを切り替え可能にできる