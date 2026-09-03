# Glitch Live Wallpaper Thesis

動的グリッチ表現を用いたAndroidライブ壁紙生成システムに関する論文です。

[![論文を読む](https://img.shields.io/badge/PDF-論文を読む-dc2626?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](thesis/main.pdf)

上のボタンを押すと、`thesis/main.pdf` を開けます。

## ソースコード

論文のLaTeXソースは [`thesis/`](thesis/) にあります。

## PDFの更新

リポジトリのルートで次を実行します（LuaLaTeX・Biber・latexmkが必要です）。

```sh
LC_ALL=C latexmk -cd -lualatex -interaction=nonstopmode -halt-on-error thesis/main.tex
```

latexmkがBiberと必要なLaTeXの再実行を行います。`lualatex` のみの実行では、追加した文献がPDFに反映されないことがあります。

更新後は `thesis/main.log` と `thesis/main.blg` に未解決の引用・文献キーの警告がないことを確認し、ソースと **`thesis/main.pdf` も一緒にコミット・push** してください。上のボタンはGitHubに保存されたPDFを開くため、ソースだけ更新しても表示は変わりません。
