# markdown tips of Visual Studio Code

## 拡張機能

- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)

## settings.json

```:json
    # mdファイルを開いたときに、プレビューも表示する
    "markdown.extension.preview.autoShowPreviewToSide": true,
    # markdownのLintで、親の見出しが異なる場合は、重複したタイトルがあってもOKにする
    "markdownlint.config": {
        "MD024": {
            "siblings_only": true
        }
    }
```
