# My TeX Template

## 想定の使い方

TeX ファイルがあるリポジトリにおいて submodule として使用する。

```bash
cd <tex-directory-repository>
git submodule add https://github.com/mo-mo-666/tex-template.git
# git submodule add git@github.com:mo-mo-666/tex-template.git
```

TeX ファイル内で例えば以下のようにして使う。

```latex
\documentclass[a4paper,12pt]{article}

\input{../tex-template/general_style}
\input{../tex-template/general_style_en}
```

独自のスタイルを適用したい場合は適宜コピーして使えばよい。
