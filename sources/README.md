# Source catalog / 出典台帳

`catalog.csv` is a **research candidate index**, not a historical-price dataset.

- `source_id`: permanent ID; retain when a URL changes.
- `priority`: order for collecting and validating records.
- `status`: only indicates the source has been identified in the preliminary 2026-10-11 research, not that numerical entries have been verified.
- `reuse_status=unverified`: redistribution and automated collection rights require review before data ingestion/publication.
- `next_action`: the next concrete research step.
- `notes`: provenance, risk, and bibliographic caveats.

Do not enter hypothetical observations into `data/verified/`. Mark a source verified only after accessing the original and recording how it was checked.
