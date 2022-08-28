# Cohesion (凝集度)

## Ideal (理想)

- Functional Cohesion (機能的凝集)
  - Handle a single function. (単一の機能を処理する)

## Become good or bad depending on situations (状況によって良いときと悪いときがある)

- Sequential Cohesion (逐次的凝集)
  - Grouped because the output from one part is the input to another part like an assembly line (関連する値を受け渡して処理をするものをまとめる)
- Communicational Cohesion (通信的凝集)
  - Grouped because they operate on the same data (同じデータに対して処理をするものをまとめる)
- Procedural Cohesion (手続き的凝集)
  - Grouped by when they are processed  (実行順序に意味がある処理をまとめる)
- Temporal Cohesion (時間的凝集)
  - Grouped by when they are processed (近い時間で実行する処理がまとまっている)
  - ex. initialize (初期化処理)

## Not so good (あまりよくない、可能な限り避ける)

- Logical Cohesion (論理的凝集)
  - Handle process by flag. (関連のない処理をフラグで切り替える)

## Bad (良くない、避けるべき)

- Coincidental Cohesion. (偶発的凝集)
  - Grouped randomly and non related. (無作為に処理がまとまっている)
  - ex. Utility class which has functions used frequently. (頻繁に使われる関数を持つユーティリティクラス)
