# Consolidation Status — BMC-alchemizer

Part of the 2026-08-28 seven-repo BMC consolidation review. The canonical review — audit
verdicts, decisions, and the ordered roadmap — is `docs/REPO_CONSOLIDATION_REVIEW.md` in
`Blackmarket-coa/free-black-market`.

## This repo's verdict: parked (operator decision, 2026-08-28)

- This is an unmodified upstream mirror of Blnk Finance — no Blackmarket commits, no
  EconomicUnit/EconomicPolicy layer, no custom work at all. The plan to build the org's ledger
  here is superseded: **FBM's `hawala-ledger` is the canonical ledger** (10.6k lines, 21 specs,
  audited double-entry with six rails and escrow). Standing Blnk up as the ledger would rewrite
  the most-tested money code in the org for no user value.
- The operator's directive is **harvest, not adopt**: port the useful Blnk capabilities into
  `hawala-ledger` (canonical review §5): (1) an external reconciliation engine — upload external
  records + matching rules, the precondition for Stellar/USDC and ACH confidence; (2) balance
  monitors with threshold alerting on settlement/escrow accounts; (3) transaction/balance
  lineage; (4) first-class point-in-time balances. Blnk's implementations of each are the
  reference material.
- **Keep this mirror only until those harvest items land, then archive the repo on GitHub.**
  Nothing is lost by archiving — there is no custom work here, and upstream remains available.
