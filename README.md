# vim-keybindings
my personal vim keybinding settings in vscode


settings.json
```json
 "vim.easymotion": true,
  "vim.insertModeKeyBindings": [{
    "before": ["k","j"],
    "after" : ["<Esc>"]
  }],
  "vim.normalModeKeyBindingsNonRecursive": [
    {
      "before": [" "],
      "after": ["leader", "leader", "leader", "b", "d", "w"]
    },
      // NAVIGATION
    // switch b/w buffers
    { "before": ["<S-h>"], "commands": [":bprevious"] },
    { "before": ["<S-l>"], "commands": [":bnext"] },

    // splits
    { "before": ["leader", "v"], "commands": [":vsplit"] },
    { "before": ["leader", "s"], "commands": [":split"] },

    // panes
    {
      "before": ["leader", "h"],
      "commands": ["workbench.action.focusLeftGroup"]
    },
    {
      "before": ["leader", "j"],
      "commands": ["workbench.action.focusBelowGroup"]
    },
    {
      "before": ["leader", "k"],
      "commands": ["workbench.action.focusAboveGroup"]
    },
    {
      "before": ["leader", "l"],
      "commands": ["workbench.action.focusRightGroup"]
    },
  ],
  ],

  "vim.hlsearch": true,
  "vim.handleKeys": {
    "<C-c>": false,
    "<C-v>": false,
    "<C-x>": false,
    "<C-a>": false,
    "<C-d>": false,
    "<C-w>": false,
  },
 "editor.wordSeparators": "`~!@#$%^&*()=+[{]}\\|;:'\",.<>/?",
```


keybinds.json

```json
   {
        "key": "tab",
        "command": "tab",
        "when": "editorTextFocus && !editorTabMovesFocus"
    },
    {
        "key": "shift-tab",
        "command": "outdent",
        "when": "editorTextFocus && !editorTabMovesFocus"
    }, 

```
