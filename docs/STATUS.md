# プロジェクト現在地

- 最終確認：2026-10-17
- 正本：https://github.com/yama-books/soba-price
- 段階：調査・設計（M0：史料予備調査を進行）
- 実施済：基本設計書・収集計画・公開方針を登録し、出典候補16件を整理。歴博DBの公式概要・検索画面・公開されているダウンロード項目を確認。斎宮歴史博物館の996年盗品評価額と貨幣博物館の奈良時代の展示から価格・賃金の研究リード6件を登録。
- 原資料との照合：**未実施**。6件のリードは資料に関するメモであり、本番用の観測データではない。
- 歴博DB：700〜1299年の年代別・品目別の検索件数は未取得。DB全件数の過去の公表値と混同しない。
- 利用条件：歴博DBの大量取得・再配布条件は未確認。第三者が作成した本文・画像・DB原データのコピーは未登録。
- `data/verified/`：検証済みレコード0件。
- 為替レート：年次実数データのダウンロード・照合は未着手。
- CI：未構築
- Web公開：未実施
- 実機検証：未実施
- 根拠：[`docs/RESEARCH_LOG_20261017.md`](RESEARCH_LOG_20261017.md)、[`sources/price_leads.csv`](../sources/price_leads.csv)、[`sources/catalog.csv`](../sources/catalog.csv)
- 次の作業：歴博DBの利用条件と検索結果件数を実測 → 少数レコードの原資料照合 → 元の単位・用途別に整理 → 公開可否を確認してから `data/verified/` に登録。


## 2026-10-17 追加：UI v0.2

- 画面構成：[UI_WIREFRAME.md](UI_WIREFRAME.md)（PC・モバイル、状態図）
- モーション候補：[UI_MOTION_PLAN.md](UI_MOTION_PLAN.md)（20件、A/B/C、公式Motion PromptのIDと独自補完を区分）
- 開発計画：[IMPLEMENTATION_ROADMAP.md](IMPLEMENTATION_ROADMAP.md) / [UI_TEST_PLAN.md](UI_TEST_PLAN.md)
- ソース：[app/prototype/index.html](../app/prototype/index.html)（外部依存なしの架空カード7件によるフィルタ、比較、詳細、タブ、トースト、スケルトンのUIデモ）
- 保存・静的確認：GitHub mainへ保存し、HTMLの読み戻し、JavaScriptの構文パース、主要UIコード・縮小モーション対応の存在を確認。スマホ用フィルターCSSと詳細内フォーカス移動の実装を修正。
- 未確認：実際のPC/スマホブラウザ操作、アクセシビリティ検証、CI、Webデプロイ。価格記録・換算値は実装していない。
- 次の作業：試作UIをブラウザ実機でテスト（docs/UI_TEST_PLAN.md）→ D0歴博DBの史料収集・権利確認 → D1検証済みレコードを接続。

このファイルは意味のある進捗変化時だけ更新する。未確認の内容を確認済みとしない。
