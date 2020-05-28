**学んだことを記述していく　Udemyでの学習記録その4**

**ES６以降の新しい方法 バッククォートの記号を使う「`」**
**オブジェクト＋メソッド（命令）の処理。windowの処理は隠れている**


**正規表現の処理について**
- 正規表現の記述(郵便番号を例に行う) 学習記録で詳細に記載　/^[0-9]{3}-[0-9]{4}$/;
- また電話番号やクレジットカードの番号なども対応可能。ただし、メルアドに関しては行わないほうがいいらしい
- 例： /^\d{3}-?\d{4}$/g　
- 参考URL https://javascript.programmer-reference.com/js-regexp-sample/
  
**別のwebページへ移動、転送するlocationメソッド**
location.href = 'http://www.yahoo.co.jp/'

**別ファイルとしてimportする場合の記述**
- <script src="timer.js">

**タイマーで時計表示　関数定義 その他**
- - let timer = () => {
- - let now = new Date();
- - document.getElementById('timer').innerHTML = 
- - `${now.getHours()}:${now.getMinutes()}:${now.getSeconds()}`;
- - 関数化しただけの表記→timer();

- リアルタイム表示の処理：setinterval
- 時間を止める場合やストップウォッチなどで利用できる
- - setIntervalとclearInterval


**外部ファイルや関数化したものを読み込む方法と記述方法**
- <script type="module">
- - import {sum} from './math.js' という記述方法

また、練習ファイルではVScodeの拡張機能で「live server」をインストールして実行


**Ajaxと非同期通信の内容**
- 講義内容ではコードをただ書くだけで動いたが、実際には
- 別途jsonファイルを用意し、それが読み込まれるために、決まりごとの記載が必要。
- またその決まりごとには、ネットワーク系の内容が含まれており、根本的な理解はできていない。

**cookieの保存方法などもこれが正しいのかが理解できておらず。**
- 別途、こちらも演習が必要かもしれない

**ローカルストレージでの保存方法**
- ローカルストレージに保存する(HTML5対応ブラウザで動作するため、古いブラウザ対応のためにはcookieはまだ必要)
-document.getElementById('値指定').addEventListener('click',function()

//ローカルストレージ用メソッド
localStorage.setItem('email', document.getElementById('HTMLでの値：emailなど').value);
