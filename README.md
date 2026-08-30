# Atsuhiro Yamamoto — University Application Portfolio

GitHub Pages で公開できる、日英切替対応の静的ポートフォリオです。ビルド工程や外部サービスは不要です。

## ファイル構成

```
portfolio-site/
├── index.html            # レイアウト・スタイル・表示処理
├── data/
│   └── portfolio.js      # 活動、受賞、年表などの編集用データ
└── README.md             # この手順書
```

## ローカルで確認する

`index.html` をブラウザで開くだけで表示できます。より実際の公開環境に近い形で確認したい場合は、任意のローカル静的サーバーを使ってください。

## 内容を編集する

### 日本語・英語の文章

活動カードや年表は `data/portfolio.js` にあります。各テキストは必ず次の形で、両言語を同時に編集します。

```js
title: {
  ja: "日本語の見出し",
  en: "English heading"
}
```

### 新しい Project を追加する

`portfolio.js` の目的に合う配列（例：`research`、`impact`、`technology`）へ、既存と同じ形式のオブジェクトを追加します。

```js
{
  meta: "Project category",
  status: "[Status to be confirmed]", // 不要なら削除
  title: { ja: "プロジェクト名", en: "Project title" },
  text: { ja: "説明", en: "Description" },
  tags: ["Field", "Tool"]
}
```

より詳細なプロジェクト記録には、Title、Period、Role、Status、Description、Question、Approach、Outcome、What I Learned、Related Fields、Links、Images を追加しておくことを推奨します。公開前に、本文へ反映する内容とリンクを確認してください。

### Award を追加する

`awards` 配列へ以下の形式で追加します。証明書や主催団体のページがある場合は、公開前に出典リンクも本文または別ページへ追加してください。

```js
{
  title: { ja: "賞の名称", en: "Award name" },
  detail: { ja: "受賞内容", en: "Recognition detail" }
}
```

### 不明な実績の扱い

参加・応募・選考通過・受賞のいずれかが確定していない場合は、断定せず `status: "[Status to be confirmed]"` を使ってください。構想段階の活動には `Concept stage` などを付け、実施済みと区別します。

## GitHub Pages で公開する

1. GitHub で新しい **Public** リポジトリを作成します（例：`atsuhiro-yamamoto-portfolio`）。
2. このフォルダ内の `index.html`、`data`、`README.md` をリポジトリの最上位へアップロードしてコミットします。
3. リポジトリの **Settings → Pages** を開きます。
4. **Build and deployment** の Source を **Deploy from a branch** にし、`main` / `root` を選んで保存します。
5. 表示された GitHub Pages URL を確認します。公開反映には数分かかる場合があります。

公開前に、連絡先、個人情報、すべての受賞・参加ステータス、外部リンクの正確性を必ず確認してください。
