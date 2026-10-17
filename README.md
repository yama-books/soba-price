# soba-price｜年代・品目・国別物価計算機

**奈良・平安時代から現代まで、食品・生活用品・賃金等の史料価格を探し、当時の為替・購買力の複数の考え方を比較するWebアプリの研究・開発リポジトリです。**

「江戸のそば1杯はいくら？」を入口にし、そばのない時代には米・布・塩・労働賃金等の記録を参照します。価格の記録と円換算上の推定を分けて表示し、原資料をたどれる設計とします。

> **現在地：M0史料予備調査 ＋ M1 UI操作試作（2026-10-17）**
> 奈良・平安の研究リード6件を登録。画面モデル図・20件のモーション案と単一HTMLの動くUI試作を追加しました。**UIは架空データのみ**。史料レコードの本格収集・検証、価格換算、CI・Web配信・実機ブラウザ検証は未実施です。

## はじめに読む文書

| ファイル | 内容 |
| --- | --- |
| [docs/BASIC_DESIGN.md](docs/BASIC_DESIGN.md) | アプリの基本設計、データモデル、比較手法、品質基準 |
| [docs/DATA_COLLECTION_PLAN.md](docs/DATA_COLLECTION_PLAN.md) | 歴博DB、CiNii、米価・為替統計の収集・照合計画 |
| [docs/DATA_POLICY.md](docs/DATA_POLICY.md) | 出典と利用条件の確認、原資料・未検証データの扱い |
| [sources/catalog.csv](sources/catalog.csv) | 出典候補16件。価格観測値ではありません |
| [sources/price_leads.csv](sources/price_leads.csv) | 奈良・平安の価格・賃金の手掛かり6件。原史料未照合・アプリ表示不可 |
| [docs/RESEARCH_LOG_20261017.md](docs/RESEARCH_LOG_20261017.md) | 2026-10-17の調査結果と残課題 |
| [docs/UI_WIREFRAME.md](docs/UI_WIREFRAME.md) | PC・スマホの画面モデル図と状態遷移 |
| [docs/UI_MOTION_PLAN.md](docs/UI_MOTION_PLAN.md) | Motion Promptを参考にした20件の候補と採用優先度 |
| [docs/IMPLEMENTATION_ROADMAP.md](docs/IMPLEMENTATION_ROADMAP.md) | UI・史料取得・為替換算の分離工程 |
| [docs/UI_TEST_PLAN.md](docs/UI_TEST_PLAN.md) | 実機とキーボード操作のテスト計画 |
| [app/prototype/index.html](app/prototype/index.html) | 7件の架空カードで操作する単一HTML試作（未公開・実機未検証） |
| [docs/STATUS.md](docs/STATUS.md) | 現在の作業状態と次の一手 |
| [AGENTS.md](AGENTS.md) | ChatGPT・Codex・Claude Code等に共通の作業ルール |

## UI操作試作 v0.2

[app/prototype/index.html](app/prototype/index.html) に外部ライブラリ不要の1ファイル試作を追加しています。GitHubのRaw / Download raw fileからHTMLを取得してブラウザで開けば、年代・国・品目の絞り込み、年表/比較/出典の切替、詳細ドロワー、比較追加、空表示とモーションを試せます。現時点でGitHub Pages等の公開処理は行っていません。数値や史料は架空UIのため**歴史物価の確認資料には使えません**。

## フォルダ構成

```text
soba-price/
├── README.md
├── AGENTS.md
├── docs/
│   ├── BASIC_DESIGN.md
│   ├── DATA_COLLECTION_PLAN.md
│   ├── DATA_POLICY.md
│   ├── STATUS.md
│   └── RESEARCH_LOG_20261017.md
├── sources/
│   ├── README.md
│   ├── catalog.csv
│   └── price_leads.csv
├── data/
│   ├── verified/        # 許諾確認・史料照合済みの公開用データ
│   └── derived/         # 為替・購買力の根拠付き計算結果
├── scripts/             # 将来の収集・検証・変換処理
└── app/                 # 将来のPC/スマホ向けWebアプリ
```

## 価格表示の原則

- **原記録**：当時の価格・貨幣・支払物・数量・年月・地域・取引種別・出典を保持します。
- **歴史為替円換算**：適切な同時代の相場が存在する期間だけ表示します。古代や中世に架空の円レートを与えません。
- **現代円の参考相当額**：米価・賃金・物価指数などを使う方法と前提を明示し、それぞれ別の結果とします。
- **欠測は欠測**：価格のない時代を補間で「実測価格」にしません。税・年貢・公定価格・小売価格も混ぜません。

## データの取扱い

`sources/catalog.csv` の候補登録は、各URLの現時点の生存確認や再利用許可を意味しません。著作権や利用規約が未確認の書籍PDF・論文本文・DB一括抽出物・図書館での複写物は、公開GitHubへアップロードしません。非公開保管が必要な場合も適法な取得・保持の確認を先に行います。

本リポジトリには現時点でライセンスを設定していません。コード・研究データの再利用条件は公開内容ごとに検討します。

## 次に取り組むこと

1. 歴博「古代・中世都市生活史（物価）」DBの**利用条件**と実際の検索・書き出し結果を確認します。
2. 700〜1299年の年代別・品目別の実際の収録件数を調べます。
3. 研究リード6件と少数のDB明細を原史料に照合し、権利確認済みの公開可能データに限って `data/verified/` に登録します。
4. 為替統計の取得・年平均・通貨建てを検証してから、換算機能の試作を始めます。

正本GitHub：<https://github.com/yama-books/soba-price>
