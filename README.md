# 発見ニュースまとめサイト

科学の新発見・考古学的発見・歴史的発見に関するニュースを、タイトル+リンクの一覧としてまとめるだけの静的サイト。GitHub Pagesで公開し、スマホからいつでも見られるようにする。

## 構成

- `index.html` : サイト本体。`data/news.json` を読み込んで一覧表示する。
- `data/news.json` : 記事データ本体。`{ date, category, title, url }` の配列。

## 更新方法

家にいるときにClaude Codeへ「ニュースサイト更新して」のように依頼する。Claudeが以下を行う想定:

1. Web検索で科学・考古学・歴史発見系の新しい記事を探す
2. `data/news.json` に新しいエントリを追加(`date` はYYYY-MM-DD形式)
3. `git add` → `git commit` → `git push`
4. pushするとGitHub Pagesが自動で再ビルドし、数分でサイトに反映される

## ローカルプレビュー

```
cd news-digest
python -m http.server 8000
```

ブラウザで `http://localhost:8000` を開く。
