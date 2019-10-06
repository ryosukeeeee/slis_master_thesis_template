# slis_thesis_template

slisの修論をLaTeXで執筆する人がさくっと作業にとりかかるための雛形

## 使い方

右上の「Clone or donwload」を押して「Download ZIP」を押す。するとダウンロードが始まる
![top-page](https://raw.githubusercontent.com/ryosukeeeee/slis_master_thesis_template/image/image/github_top.png)

ダウンロードが完了したらzipファイルを解凍する。

解凍後のフォルダをVisual Studio Codeで開く。
拡張機能のLaTeX Workshopをまだインストールしていない場合は、左側の丸で囲んだアイコンを選択する。

![vs-code](https://github.com/ryosukeeeee/slis_master_thesis_template/blob/image/image/visual_studio_code.png)

検索フォームに「LaTeX Workshop」と入力すると検索結果のトップに表示されるので選択。
もしすでにインストールされていれば下のように「Disable」「Uninstall」ボタンが表示されている。
まだインストールしていないときは緑色の「install」ボタンが表示されているので、そのボタンを押せばインストールが始まる。

![latex_workshop](https://github.com/ryosukeeeee/slis_master_thesis_template/blob/image/image/latex_workshop.png)

## 構成
```
.
├── Master_ja
│   ├── masterThesisJa-Ja.sty
│   ├── masterThesisJaSample.pdf
│   └── masterThesisJaSample.tex
├── README.md
├── assets
│   └── images
│       └── 163811.png
├── chapter
│   ├── 00_abst.tex
│   ├── 01_intro.log
│   ├── 01_intro.tex
│   ├── 02_method.log
│   ├── 02_method.tex
│   ├── 03_result.tex
│   ├── 04_discussion.tex
│   ├── 05_conclusion.tex
│   └── 99_thanks.tex
├── main.pdf
├── main.tex
└── ref.bib
```

`Master_ja`の下に教務指定のスタイルシートを配置してください。

**※リポジトリに含まれる論文作成テンプレートは2019.3.12版です。最新のスタイルシートを使うようにしてください**

`assets/images`には論文中で使う画像を保存します。

`chapter`には各章のTeXファイルが配置されています。

`main.tex`が起点になります。

`ref.bib`はBibTeXファイルです。

## main.texについて
各章の内容は個別のTeXファイルに書き込む。

例えば、第1章について`main.tex`では

```TeX
% はじめに
\subfile{chapter/01_intro}
```

とあり、`chapter/01_intro.tex`をみてみると

```TeX
% !TEX root=../main.tex
\documentclass[../main]{subfiles}
\begin{document}
\chapter{はじめに}
（中略）
\end{document}
```
となっている。

もちろん`main.tex`に
```TeX
\chapter{はじめに}

\chapter{手法}
```
と書いてもよい。

## 参考

### LaTeX Workshop
- [LaTeX Workshop - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

- [Visual Studio Code/LaTeX - TeX Wiki](https://texwiki.texjp.org/?Visual%20Studio%20Code%2FLaTeX)

### LaTeX一般
- [LaTeXコマンド集](http://www.latex-cmd.com)

- [LaTeX コンパイル・PDF作成](http://www.yamamo10.jp/yamamoto/comp/latex/run/run.php)

- [Create LaTeX tables online](http://www.tablesgenerator.com/latex_tables)

- [LaTeXの表を生成できるサイトTables Generator - muscle_keisukeの日記](http://muscle-keisuke.hatenablog.com/entry/2016/07/02/170205)

### ptex2pdf
- [ptex2pdf – There and back again](https://www.preining.info/blog/software-projects/ptex2pdf/)
- [texjporg/ptex2pdf: Convert Japanese TeX documents to pdf](https://github.com/texjporg/ptex2pdf)

### 修論 論文作成テンプレート配布元
- [教務関係 | 筑波大学 図書館情報メディア系／大学院図書館情報メディア研究科](http://www.slis.tsukuba.ac.jp/grad/students/kyoumu/)
