# Source catalog / 出典台帳

`catalog.csv` is a **research candidate index**, not a historical-price dataset.

- `source_id`: permanent ID; retain when a URL changes.
- `priority`: order for collecting and validating records.
- `status`: only indicates the source has been identified in the preliminary 2026-10-11 research, not that numerical entries have been verified.
- `reuse_status=unverified`: redistribution and automated collection rights require review before data ingestion/publication.
- `next_action`: the next concrete research step.
- `notes`: provenance, risk, and bibliographic caveats.

Do not enter hypothetical observations into `data/verified/`. Mark a source verified only after accessing the original and recording how it was checked.

## 追加の研究リード

[`price_leads.csv`](price_leads.csv) には、博物館の公開解説・展示から手動で拾った**原史料未照合の調査候補6件**を記録している。価格や賃金の史料上の定義・数量・貨幣単位・年代・場所について確認できていない部分が残る。これは本番用データではなく、利用者向けアプリで表示したり時系列集計したりしてはいけない。

関連：[`docs/RESEARCH_LOG_20261017.md`](../docs/RESEARCH_LOG_20261017.md)。第三者サイトの本文・画像・DB原本は転記・収集せず、最小限の識別情報と再確認のためのリンクを記録する。
