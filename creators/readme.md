# creators: terms of record (legal leg)

the creator-facing terms that sculptura needs from day one, drafted
as product design, not legal advice. counsel review is required
before any of these become enforceable terms (standing rule from
the kirosculp ip docs carries over).

- [ip-indemnity-and-safe-harbor.md](ip-indemnity-and-safe-harbor.md)
  reverse ip indemnity: the creator warrants their parameter
  choices and indemnifies sculptura against claims arising from them
- [manufacturing-warranty-limitation.md](manufacturing-warranty-limitation.md)
  sculptura warrants api-validated geometry, not foundry outcomes;
  sole remedy for foundry-level anomalies is reprint or credit
- [takedown-and-listing-liability.md](takedown-and-listing-liability.md)
  creators own their listing names and visual properties; automated
  dmca/trademark takedown in the dashboard; neutral-engine posture

the engineering hooks for all three live in the kirosculp drafting
repo: the release pipeline (warranty events as release metadata),
paracraft provenance (which side of a claim a design belongs to),
and the outside-artist dispute spec (takedown machinery).
