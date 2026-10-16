# Collaboration notes

Repository of record: `yama-books/soba-price`.

1. Read `docs/BASIC_DESIGN.md`, `docs/DATA_COLLECTION_PLAN.md` and `docs/DATA_POLICY.md` before making data or application changes.
2. Historical observations, currency conversion rates, purchasing-power anchors and derived estimates are distinct datasets. Never fabricate missing prices or linearly interpolate absent records as actual prices.
3. Confirm license/terms and provenance prior to uploading any source files or raw data to this public repository. Keep unreviewed transcriptions and source PDFs out of it.
4. Verify original units, date conventions, region and transaction type before normalizing. Preserve uncertainty and use an explicit 'not calculable' state.
5. The source catalog records research candidates, not verified market price points. Add publication/re-use status only after checking.
6. Track milestones (design, GitHub save, CI, deployment, device checks) separately in `docs/STATUS.md`. Update on meaningful changes, not every chat turn.
7. Do not create a second public repository for the same app. Avoid competing modifications by concurrent agents; read current main before writing and read back the changed files afterward.
