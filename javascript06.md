**学んだことを記述していく　Udemyでの学習記録その6**

**ES６以降の新しい方法 バッククォートの記号を使う「`」**
**オブジェクト＋メソッド（命令）の処理。windowの処理は隠れている**

これまでの過程で思ったのは、その都度小さく動くプログラムを確認しながら、
作ったら動かす→動かなかったら修正→また作って動くようになったら進む、を繰り返すしかないね

**よくある間違いとして**
- スペルの書き間違いが多い。英語の学びも同時行う動機で進めていこう

**vue.jsについて**
javascriptのフレームワークで比較的簡易に利用可能
- 記載方法、コードの書き方がHTMLとCSSと同じファイル内で記述できる
- 公式サイト：https://jp.vuejs.org/
- HTML内には、<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>で読み込み


**vue.js CLIのインストールについて**
- node.jsがインストールされている前提で行う
- node.jsのインストール状況は、「node -v」コマンドで確認できる。
- 公式サイト「」から、さらに「Installation」のページへ移動
- npm install -g @vue/cli　のコマンドが記載されている
- ※npm「node package manager」の略
- プラスアルファとして「@vue/cli-init」を付加してインストールする
- インストール時は、node.jsと同じく管理者用の「sudo」も必要。
- インストール時間は環境によりけりだが、およそ３分弱
- ────────────────────────────────────────────────────────────────╮
   │                                                                │
   │      New patch version of npm available! 6.14.4 → 6.14.5       │
   │   Changelog: https://github.com/npm/cli/releases/tag/v6.14.5   │
   │               Run npm install -g npm to update!                │
   │                                                                │
   ╰────────────────────────────────────────────────────────────────
- インストール後、確認として「vue -V」コマンドを実行(大文字の「V」注)
- Windows環境ではエラーがでる模様。

**vue.jsでのプロジェクト環境構築**
- 作業予定フォルダに「cd(changedirectory)」でターミナルコマンドから移動
- vue create notepad のコマンドを実行
- 実行後、さらに必要なコマンドを促される
- → cd notepadでフォルダ移動、続いてnpm run serve(ローカルサーバ起動コマンド)
- 更に、GUI(webページ上)で操作できるようにするコマンドが「vue ui」
- URLは「http://localhost:8000/project/select」。dashboardもあり

**vue.jsでの環境構築その２**
- 別途SinglePageApplicationで動かすために、環境構築
- routerプラグインを実装する必要あり
- コマンドは「vue add @vue/router」を実行

**vue.jsで新しいページを作成する手順**
- routerフォルダ内の「index.js」をカスタマイズ。その際、定型コードを記載
-   path: '/new',
    name: 'New',
    component: () => import('../views/ファイル名.vue')

- 上記ファイルを設定した後は、viewsフォルダ内に新規ファイルを作成
- 「新規ファイル名.vue」として、新しいページを作成していく
- このファイルでは、HTML,CSS,javascript(vue.js)を設定できる
- 更に必要なプラグインインストール時は「npm install vuex」のコマンドを実行
- また、googlechrome拡張機能も追加→「vuedeveloper」というもの
- ローカルストレージ保存用のプラグイン「npm install　--save vuex-persistedstate」を実行
- ローカルで開発した内容をサーバにアップするために、（配布用）アプリケーションのビルドコマンドが必要
- npm run build　のコマンドを実行。実行後は「dist」フォルダ内に作成される