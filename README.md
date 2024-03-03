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
    }
  ],
  "vim.hlsearch": true,
  "vim.handleKeys": {
    "<C-c>": false,
    "<C-v>": false,
    "<C-x>": false,
    "<C-a>": false,
    "<C-d>": false
  },


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
