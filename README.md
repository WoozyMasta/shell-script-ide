# Shell script IDE

Set of extensions to convert VSCode to IDE for shell scripting (sh, bash)

Recommended setting:

```json
{
  "files.autoSave": "off",
  "[shellscript]": {
    "files.eol": "\n",
    "files.insertFinalNewline": true,
    "files.trimFinalNewlines": true,
    "files.trimTrailingWhitespace": true,
    "editor.renderWhitespace": "boundary",
    "editor.insertSpaces": true,
    "editor.tabSize": 2,
    "editor.tabCompletion": "on",
    "editor.snippetSuggestions": "top",
    "editor.wordWrap": "off",
    "editor.formatOnPaste": true,
    "editor.rulers": [
      {
        "column": 72,
        "color": "#1e751633",
      },
      {
        "column": 80,
        "color": "#c2790b99",
      },
      {
        "column": 132,
        "color": "#a10d2d99"
      }
    ],
    "editor.minimap.maxColumn": 132,
  },
  // Other settings 
}
```
