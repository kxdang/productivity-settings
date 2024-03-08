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
   {
     "key": "cmd+enter",
     "command": "renameFile",
     "when": "explorerViewletVisible && filesExplorerFocus"
   },
   {
     "key": "enter",
     "command": "-renameFile",
     "when": "explorerViewletVisible && filesExplorerFocus"
   },
   {
     "key": "enter",
     "command": "list.select",
     "when": "listFocus && !inputFocus"
   }

```

# My personal yabai window tiling shortcuts

hyper bound to caps using Karabiner

yabai:
```
yabai -m config layout bsp

# New window spawns to the right if vertical split, or bottom if horizontal split
yabai -m config window_placement second_child


yabai -m config top_padding 4
yabai -m config bottom_padding 4
yabai -m config left_padding 4
yabai -m config right_padding 4
yabai -m config window_gap 4


yabai -m rule --add app="^System Settings$" manage=off
yabai -m rule --add app="^Calculator$" manage=off
yabai -m rule --add app="^Karabiner-Elements$" manage=off

```

skhdrc:
```
# Navigates between open windows
hyper - j: yabai -m window --focus south
hyper - k: yabai -m window --focus north
hyper - h: yabai -m window --focus west
hyper - l: yabai -m window --focus east

# Navigates between external monitors
hyper - s: yabai -m display --focus west
hyper - g: yabai -m display --focus east

# Flips based on axis
hyper - y: yabai -m space --mirror y-axis
hyper - x: yabai -m space --mirror x-axis

# Maximizes the window fullscreen
hyper - m: yabai -m window --toggle zoom-fullscreen

# toggle window float
hyper - t: yabai -m window --toggle float --grid 4:4:1:1:2:2

# rotate 3 windows
hyper - r: yabai -m window first --swap next && yabai -m window first --swap last
hyper - q: yabai -m window first --swap last && yabai -m window first --swap next

```
