# Shell script IDE

Set of extensions to convert VSCode to IDE for shell scripting (sh, bash)

## Install binary dependencies

For the extensions to work correctly, you need to install binary dependencies
into your operating system.

---

Install **hadolint**:

* Download the [latest binary release][hadolint-releases] and install it on
  your system, or use the official [installation guide][hadolint-install].

---

Install **bashdb**:

Download [bashdb source][bashdb] files and install it:

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

---

Optionally you can also install binaries for [**shellcheck**][shellcheck] and
[**shfmt**][shfmt]. But in most cases this is not necessary, they are installed
automatically when the extension is installed.

* [github.com/koalaman/shellcheck][shellcheck]
* [github.com/mvdan/sh][shfmt]

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

<!-- links -->

[hadolint-releases]: https://github.com/hadolint/hadolint/releases
[hadolint-install]: https://github.com/hadolint/hadolint#install
[bashdb]: https://sourceforge.net/projects/bashdb/files/bashdb/
[shellcheck]: <https://github.com/koalaman/shellcheck/releases>
[shfmt]: <https://github.com/mvdan/sh/releases>
[habr]: https://habr.com/ru/post/583320/
