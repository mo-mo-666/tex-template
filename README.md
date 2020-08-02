# My TeX Template

## 想定の使い方

TeX ファイルがあるリポジトリにおいて submodule として使用する。

```bash
cd <tex-directory-repository>
git submodule add https://github.com/mo-mo-666/tex-template.git
# git submodule add git@github.com:mo-mo-666/tex-template.git
```

TeX ファイル内で例えば以下のようにして使う。

- English article

```latex
\documentclass[a4paper,12pt]{article}
\usepackage[margin=20truemm]{geometry}

\input{../tex-template/general_style}
\input{../tex-template/general_style_en}

\usepackage[dvipdfmx,%
 bookmarks=true,%
 bookmarksdepth=3,%
 bookmarksnumbered=true,%
 colorlinks=false,%
 setpagesize=false,%
 pdftitle={},%
 pdfsubject={},%
 pdfauthor={},%
 pdfkeywords={}]{hyperref}
```

- Japanese article

```latex
\documentclass[uplatex,a4paper,10pt]{jsarticle}
\usepackage[margin=20truemm]{geometry}

\input{../tex-template/general_style}
\input{../tex-template/general_style_ja}

\usepackage[dvipdfmx,%
 bookmarks=true,%
 bookmarksdepth=3,%
 bookmarksnumbered=true,%
 colorlinks=false,%
 setpagesize=false,%
 pdftitle={},%
 pdfsubject={},%
 pdfauthor={},%
 pdfkeywords={}]{hyperref}
% PDFのしおり機能の日本語文字化けを防ぐ
\usepackage{pxjahyper}
```

- Japanese beamer

```latex
\documentclass[aspectratio=169,11pt,dvipdfmx]{beamer}
\input{../tex-template/schoolslide_style_ja}

% \usetheme{Copenhagen}
\usetheme[height=1cm]{Rochester}
\usecolortheme{orchid}
\usefonttheme{professionalfonts}
% \useinnertheme{rectangles}
\useinnertheme{circles}
% \useoutertheme{infolines}
\setbeamertemplate{navigation symbols}{}
\setbeamertemplate{footline}[frame number]
```

独自のスタイルを適用したい場合は適宜コピーして使えばよい。
