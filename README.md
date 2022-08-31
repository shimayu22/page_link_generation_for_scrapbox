# Scrapbox用のページリンクを生成してクリップボードにコピーするブックマークレット
Scrapboxを使っていろいろなページのリンクを集めている時にいちいち`[URL タイトル]`を手動とコピペで入力するのが面倒だったので、今開いているページを一括で`[URL タイトル]`の形式でクリップボードに保存してくれるブックマークレットを作成しました。

# 使い方
- 以下をブックマークバーに追加する

```
javascript:(function () {var lines = ['[' + window.location.href + ' ' + document.title + ']'];navigator.clipboard.writeText(lines);})();
```

- リンクを作成したいタブを開き、上記で作成したブックマークバーをクリックする
- Scrapboxの任意の場所でペーストする

# Scrapbox公式ブックマークレットとの違い
- 公式の方は、指定のプロジェクトにページが作成される
- これはただ`[URL タイトル]`の形式でクリップボードに保存される
  - １ページにとにかく情報を集める時を想定している

# ご注意
- Chromeのみ動作確認しています
- Scrapboxの仕様上、タイトルに`[]`がついていると、ペーストした時にリンクが途中で途切れます
  - その場合は手動で修正してください

# 参考
- [Scrapboxに画像付きでWebクリップしたいと思いませんか ScrapClip - W&R : Jazzと読書の日々](https://wineroses.hatenadiary.org/entry/20170320/p1)
- Scrapbox公式のブックマークレット
