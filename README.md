## 開発セットアップ手順

Svelteでの開発を開始するためのセットアップ手順です。前提条件は

- yarn または npmがインストールされていること

です。またコマンドはyarnに合わせて記述していきますので、npmを使っている方は適宜読み替えてください。まずSvelteアプリケーションの雛形をcloneしてくるためにdegitをインストールします。
```
$ yarn global add degit
```
インストールが完了したらプロジェクトを作成したい場所で以下のコマンドを入力します。
```
$ degit sveltejs/template my-svelte-project
```
my-svelte-projectの部分には自分がつけたい好きなプロジェクト名を入れます。できたら、作成されたプロジェクトのディレクトリに移動して
```
$ yarn install
$ yarn run dev
```
とコマンドを打つと、デフォルトで`localhost:5000`でサーバーが立ち上がります。ブラウザのURLにこれを入力して更新したときに以下のようなページが表示されていれば成功です。

[![Image from Gyazo](https://i.gyazo.com/724959a130f39331abd37225be65b54a.png)](https://gyazo.com/724959a130f39331abd37225be65b54a)

これだけでSvelteで開発する準備は完了です。

## サーバー起動手順

package.jsonに何かしらの変更がある場合は

```
$ yarn install
```

を叩いてください。そのあと、もしくは変更がないという場合は

```
$ yarn run dev
```

で`localhost:5000`でサーバーが立ち上がります。
