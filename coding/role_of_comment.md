# Rule of Comment

## Interface

- What
  - Write information when user need to use at Interface Comment.(インタフェースのコメントには、ユーザーが利用するのに必要な情報を書く)
- Why
  - Make module available to user without reading implementation.(実装を読まなくても、ユーザーがモジュールを利用できるようにする)
- How
  - Overview (概要)
  - What to do (何をするか)
  - input and output (入出力)
  - cautions (注意事項)

## In Implementation

- No Comment is ideal. (実装中にコメントが無いのが理想)
  - Code should be understandable easily without comment.(コメントが無くても何をしているのかがすぐに分かるようにコードにする)
- If you'd like to write comment, It's sign to refactor. (コメントを書きたくなったら、それはリファクタリングのサイン)
- (コメントを書いた方がいいケース)
  - It's hard to understand intent. (コードの意図が分かりにくい)
  - It's easy to mistake during fixing. (コード修正時にミスが起こりやすい)
  - It's difficult to refactor. (リファクタリングしにくい)

## HTML

- Pay attention to content of Comment, because Anyone can see Comment. (誰でもみることが可能なので、コメントの内容は気を付ける)
  - Javascript Comments are able to be disappear with minifying.
