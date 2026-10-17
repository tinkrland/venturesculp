# manufacturing warranty: what sculptura warrants, and caps

## the warranty, scoped

sculptura's manufacturing responsibility is strictly limited to
generating geometry files that pass the approved automated api
geometric validation (sculpteo and the other providers on the
routing list). a validation pass means: the file is geometrically
castable per the validation provider's automated checks, per the
design rules paracraft enforces. that is what is warranted. nothing
metallurgical, nothing cosmetic, nothing foundry-operational.

the terms must state what validation does and does not check:
geometry, wall thicknesses, closure, castability per the api. it
does not check foundry conditions, alloy behavior at pour, thermal
anomalies, or finishing outcomes.

## foundry-level anomalies: the sole remedy

if a file passes api validation but the physical casting run fails
due to anomalies at the foundry level (porosity, shrink, mold
failure, casting accident, finishing damage), the creator's **sole
and exclusive remedy** is, at sculptura's election:

- a **reprint** of the same file at no charge, or
- a **manufacturing credit** to the creator wallet (manufacturing
   side), equal to the failed run's manufacturing cost

explicitly excluded, forever and plainly stated: consequential,
incidental, and reputational damages; lost storefront revenue;
sales momentum; downtime; opportunity costs. the exclusions are
rendered in plain language at commission/order time, not buried.

## the deliberate carve-out: our own validation errors

the cap covers foundry-level anomalies. it does not cover sculptura
getting the geometry wrong: if paracraft released geometry that
**should have failed** validation (a defect in our rules or
validation mapping), that is sculptura's bug and is not capped by
this section; the design is re-done at no cost, and the failure
feeds the regression harness. this is the deterministic-engine
promise: we stand behind our validation absolutely, and behind the
foundry's melt not at all.

the line between the two is drawn by evidence: the validation
record for the release (what passed, against which rules version)
plus the foundry's failure report. both are part of the order's
append-only record.

## buyer-side interaction

a buyer's order that fails at the foundry follows the order-side
refund path, not this doc: the buyer is made whole (refund or
reorder), the creator's exposure is the reprint/credit remedy here.
the two flows never cross: buyer refunds do not come out of creator
wallets except where a creator-side cause is substantiated.
