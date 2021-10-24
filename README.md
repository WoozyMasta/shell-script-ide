# Shell script IDE

Set of extensions to convert VSCode to IDE for shell scripting (sh, bash)

## Install binary dependencies

For the extensions to work correctly, you need to install binary dependencies
into your operating system.

Install utilities from the release pages:

* <https://github.com/koalaman/shellcheck/releases>
* <https://github.com/hadolint/hadolint/releases>
* <https://github.com/mvdan/sh/releases>

Install bashdb:

```bash
BASDB_VERSION=5.0-1.1.2
curl -Lo "bashdb-$BASDB_VERSION.tar.gz" \
  "https://sourceforge.net/projects/bashdb/files/bashdb/$BASDB_VERSION/bashdb-$BASDB_VERSION.tar.gz/download"
tar xf "bashdb-$BASDB_VERSION.tar.gz"
cd "bashdb-$BASDB_VERSION/"
./configure
make
sudo make install
```

## Recommended VSCode setting

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

## Links

* [Подготовка эффективной среды для написания bash сценариев][habr] - an article
  in Russian about preparing an effective environment for developing
  bash scripts

[habr]: https://habr.com/ru/post/583320/
