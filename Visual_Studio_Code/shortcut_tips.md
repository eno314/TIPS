# shortcut tips of Visual Studio Code

## ショートカットを追加する

1. `fn + F1` でコマンドパレットを開き、`Preference: Open Keyboard Shortcuts (JSON)` を選択する
2. `keybindings.json` を編集する

例えば、`ctrl+down` でエディタからターミナルにフォーカスを変え、`ctrl+up` でターミナルからエディタにフォーカスを変えるような設定をする場合は以下のようにする

```:json
// Place your key bindings in this file to override the defaults
[
    {
        "key": "ctrl+down",         "command": "workbench.action.terminal.focus",
                                    "when": "editorTextFocus"
    },
    {
        "key": "ctrl+up",           "command": "workbench.action.focusFirstEditorGroup",
                                    "when": "terminalFocus"
    }
]
```

- 参考
  - <https://qiita.com/rai_suta/items/05e69f0b9065989b19c1>
