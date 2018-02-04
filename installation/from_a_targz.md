# tar.gz から

何らかの理由で他のインストール方法が採れない / を採らない場合でも、スタンドアロンな .tar.gz ファイルをダウンロードする方法があります。

最新のファイルは GitHub の Releases ページ (<https://github.com/crystal-lang/crystal/releases>) にあります。

自分のプラットフォームに合うファイルをダウンロードして解凍してください。中に `bin/crystal` という実行ファイルがあります。

パスの通った場所にシンボリックリンクを張ると使うのが楽になります。

`ln -s [full path to bin/crystal] /usr/local/bin/crystal`

そうするとただ `crystal` と打つだけでコンパイラを実行できます。
