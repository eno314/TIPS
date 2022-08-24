# Thymeleaf TIPS

## Boolean operations (論理演算)

- and, or, !(not)
- <https://www.thymeleaf.org/doc/tutorials/3.0/usingthymeleaf.html#standard-expression-syntax>

## Expression Utility Objects (ユーティリティオブジェクト)

- There are useful utility object. (便利なユーティリティオブジェクトが用意されている)
- <https://www.thymeleaf.org/doc/tutorials/3.0/usingthymeleaf.html#expression-utility-objects>

## Comment

- Thymeleaf parser-level comment blocks
  - `<!--/*`  `*/-->` : Remove remove everything between this block. (このブロックの中にあるものは全て削除される)
  - <https://www.thymeleaf.org/doc/tutorials/3.0/usingthymeleaf.html#thymeleaf-parser-level-comment-blocks>
- Thymeleaf prototype-only comment blocks
  - `<!--/*/` `/*/-->` : It become comments when the template is open statically, but considered normal markup by Thymeleaf when executing the template. (静的に開いた時はコメントになるが、テンプレートとして実行された場合は通常のマークアップとなる)
  - <https://www.thymeleaf.org/doc/tutorials/3.0/usingthymeleaf.html#thymeleaf-prototype-only-comment-blocks>
