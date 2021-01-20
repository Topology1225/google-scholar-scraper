# sumiyoshi\_demo
Google scholar から論文情報を抽出するツールを作成した。

## 1. スクレイピングの仕組み
1. url をリクエスト
   * （大量にリクエストすると BAN されてしまうので注意）
   * （重要そうな論文順に、1ページ10件並んでいる）
1. html を BeautifulSoup で解析。論文情報抽出。

## 2. 複合キーワード検索
1. 著者、キーワード、出版名、出版年を入力
1. url をリクエストし、上位100件を検索
1. 論文の情報（タイトル、著者、出版年、引用数、url、スニペット）を抽出
1. csv に出力

## 3. ある論文を引用している論文、引用数の推移
1. 著者、キーワード、出版名、出版年を入力
1. url をリクエストし、上位10件を表示・対象論文を選択
1. 選んだ論文を引用している論文を上位100件検索
1. 論文の情報・各年の引用数の推移を抽出し、csv に出力

## 4. 分野のレジェンド論文・バズ論文を可視化
