# Glitch Live Wallpaper Thesis

動的グリッチ表現を用いたAndroidライブ壁紙生成システムに関する論文です。

[![論文を読む](https://img.shields.io/badge/PDF-論文を読む-dc2626?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](thesis/main.pdf)

上のボタンを押すと、`thesis/main.pdf` を開けます。

## ソースコード

論文のLaTeXソースは [`thesis/`](thesis/) にあります。

## PDFの更新

リポジトリのルートで次を実行

```sh
LC_ALL=C latexmk -cd -lualatex -interaction=nonstopmode -halt-on-error thesis/main.tex
```

`lualatex` のみの実行じゃだめ

更新後は `thesis/main.log` と `thesis/main.blg` の引用がいい感じか確認し、ソースと全部 **`thesis/main.pdf` も一緒にコミット&push** 
```sh
git add thesis
git commit -m "論文を更新"
git push
```
上のボタンはGitHubに保存されたPDFを開くため、ソースだけ更新しても表示は変わらない
