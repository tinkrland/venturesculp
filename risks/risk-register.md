# sculptura financial risk register

first pass 2026-10-17. each risk: severity x likelihood, the model
number it threatens, and a concrete shield. sources: the repo
grounded model (tier-schedule, buildup, zero-sales, take breakup)
plus the cfo.ai mirror; ari's monthly trigger ("risk gap analysis")
re-fires on the 1st as a standing cross-check - its output is
evidence, never the register itself.

## already shielded (not repeated below)

zero-sales dead zone (~30 creators breakeven), power-user
utilization tail (pro 29% ceiling), support $6/order placeholder
with measurement, payout side ($0.40/order), chargeback buffer in
escrow, ip indemnity + takedown posture, foundry anomaly caps
(reprint-or-credit), cancellation ladder, promo draw caps, retro
horizon, prohibited-market banking checks, agents never move money.

## new, ranked

### 1. processor reserve holds (severity: high, likelihood: medium)

stripe commonly imposes rolling reserves (5-25% of processed funds
held 30-90 days) or ad-hoc balance holds on new marketplaces. the
15th-payout model assumes the stripe balance is fully available; a
reserve breaks payout timing for escrowed creator money even when
orders are healthy.

- threatens: the payout schedule itself (not a number - a promise)
- shields: (a) payout terms state payouts run "net of processor
  holds" so the obligation is never unfunded; (b) a reserve buffer
  line in the model: assume 10% of active escrow is frozen for
  planning until stripe history is established; (c) track the
  reserve % from the first month live - it is one number.

### 2. correlated foundry failure (severity: high, likelihood: low-medium)

escrow is per-order, which treats manufacturing failures as
independent. they are not: one bad casting run, a bad alloy batch,
or one partner's QC lapse can hit dozens of orders at once, and
per-order escrow does not cover a correlated refund wave plus
buyer goodwill.

- threatens: refund liability far beyond the 0.75% chargeback tail
- shields: (a) an incident reserve line: hold 5% of active escrow
  as foundry-incident reserve until a partner has 3 clean months;
  (b) per-partner exposure caps at launch (no single foundry carries
  >50% of live orders); (c) the failure report + validation record
  already in the order event chain determines liability per the
  warranty doc.

### 3. cross-border payout corridor costs (severity: medium, likelihood: high)

creators are international; stripe connect cross-border payouts
cost meaningfully more than domestic (cross-border fee + fx spread,
commonly 0.5-1%+ on top). the payout side assumed $0.25/payout
domestic-style.

- threatens: the $0.40 payout-side line; real blended cost likely
  higher with international creators
- shields: (a) per-corridor payout cost is exactly the payoutrails
  leg (kirosculp) - parameterize payout cost by corridor and blend
  by creator geography; (b) revisit the take breakup with a
  corridor-weighted payout side once the launch creator roster
  exists; (c) never net these against creator payout amounts
  silently - costs are the platform's side of the ledger.

### 4. metal price drift between listing and order (severity: medium, likelihood: high)

listings carry fixed retail prices; manufacture happens at order
time against live quotes. silver/gold spot can move enough between
listing and purchase that either the fee_base shrinks or the
creator margin does. checkout re-quotes ($0.25/order) exists; a
stale-listing policy does not.

- threatens: fee_base and creator margin on older listings
- shields: (a) price refresh policy: listings older than a
  threshold (hypothesis: 30 days or spot move >4%) auto-pause for
  re-quote rather than selling at a loss; (b) the checkout quote
  revalidation stays authoritative regardless.

### 5. fraud rings / chargeback waves (severity: medium, likelihood: medium)

high-aov, resellable goods attract stolen-card rings; the 0.75%
tail assumes ambient fraud, not a campaign. correlated, so it
compounds with risk 2.

- threatens: chargeback tail, refund_source
- shields: velocity checks at checkout, stripe radar, the tell
  adapters (address shape, email eligibility), and payout holds on
  first orders for new buyer accounts (short window). mostly
  exists; the missing piece is a fraud-spike scenario in the model
  (e.g. one month at 3% chargeback rate) to size the buffer.

### 6. api pricing drift on the budget lane (severity: low-medium, likelihood: medium)

the $0.05/turn cost basis assumes current nano-class pricing and
that free tiers (groq, gemini) stay free. providers have killed
free tiers before.

- threatens: free-tier inference cost ($1.50/mo worst case per free
  creator), the whole backtier thesis economics
- shields: byok adoption (the off-ramp exists by design), a
  quarterly re-check of the nano lane price, and the credit grant
  sizes are the tuning knob (30 turns/mo is cheap to trim).

### 7. key-person risk (severity: high, likelihood: certain-but-unquantified)

solo founder; banking is human-gated by rule (correct), which
makes founder availability the single point of failure for
payroll-scale obligations later.

- threatens: everything
- shields: repos are the source of truth (any future human or
  agent can reconstruct state); runbooks live in venturesculp
  branches; add an emergency-access procedure (a trusted contact +
  documented recovery path for mercury/stripe) as a legalops item.
  not solvable with money at this stage; solvable with documentation.

### 8. money-transmitter characterization (severity: medium, likelihood: low)

holding buyer funds for weeks could be argued as money
transmission in some markets. the architecture already mitigates:
stripe is the custodian (funds sit in the stripe balance), never
sculptura accounts, never mercury.

- threatens: market expansion sequencing
- shields: keep custody with stripe verbatim in the terms; counsel
  confirms per market at rollout (legalops, already on the pattern).

## standing notes

- risks 1 and 2 change the payout/take numbers the most; both get
  model lines (reserve buffer, incident reserve) rather than
  prose-only treatment
- the monthly ari trigger cross-checks this register; disagreements
  come to the register as proposals, never as auto-edits
