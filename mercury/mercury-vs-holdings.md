# mercury vs holdings (getholdings.com): account comparison

working doc, 2026-10-16. sources: mercury's support pages (see the
mercury checklist) and getholdings.com (banking + homepage).
features change fast on both sides; re-check at application time.

## what each is

**mercury** (mercury.com): startup banking, fintech rails, funds
held at choice financial group and column n.a. (members fdic).
built for us-registered companies including international-founder
owned. free checking + savings, treasury yield, cards, team spend,
loans, international wires.

**holdings** (getholdings.com): banking + invoicing + books in one
account, positioned as software an ai agent can run (chatgpt /
claude integration: draft quotes and invoices, chase payments,
record deposits; human approves sends). ruling: the agent-executed
side is a non-starter for our banking; agents never move money. funds at i3 bank + partner
banks, fdic up to $3m. 1.75% apy on all balances, unlimited
sub-accounts, no monthly fees, no minimums. matched lending
network. positioned at freelancers, nonprofits, e-commerce.

## side by side (for our use case)

| dimension | mercury | holdings |
|---|---|---|
| international founder, non-us resident | documented, explicit support; thousands of solo non-us founders onboard pre-launch | not documented either way in what we could find; needs a pre-application check |
| eligibility test | us entity + planned us operations + real ppob + not prohibited region | unclear; banking partner (i3) requirements unknown to us |
| yield on idle cash | treasury by mercury (opt-in, historically ~4%), savings | 1.75% apy on all balances, no tiers |
| sub-accounts | yes | unlimited, free |
| agent automation | api + integrations, but banking itself is not agent-operable by design | the whole pitch: invoicing, payment chasing, books runnable by an ai agent with approval gates |
| invoicing/books | not included; export to accounting tools | integrated (paid invoice auto-posts, deposit auto-reconciles) |
| startup ecosystem (cards, loans, treasury, wires) | strong, mature | matched lender network; younger product |
| fees | no monthly, no minimums | no monthly, no minimums |

## what actually matters for sculptura, now

1. **the documented international path.** mercury's criteria are
   published, their international-founder support is explicit, and
   the application runs on exactly the documents in our
   checklist (formation doc, ein, passport). holdings' eligibility
   for a non-us-resident solo founder is not documented anywhere we
   could find; that alone makes it the riskier first account.
2. **our money flow does not need invoicing/books from the bank.**
   revenue arrives via stripe, not customer invoices; creator
   payouts leave via stripe connect. mercury holding company
   operating funds is the right shape for launch.
3. **the holdings "agent-operable banking" angle: not for us.**
   ruled 2026-10-16: agents never execute banking actions. money
   movement stays human-gated at every layer - same discipline as
   the ticketing spec (support proposes, payments executes, a human
   approves). agents may draft, prepare, and surface information;
   a human sends. so the chatgpt/claude integration is a non-feature
   for our banking account, and holdings' remaining case rests on
   apy and invoicing workflows only.
4. **sub-account discipline.** both support sub-accounts; we want
   dedicated sub-accounts from day one (operating, tax set-aside,
   reserve) regardless of which bank. note: creator escrow lives in
   stripe, never in the bank account, so sub-accounts are for
   company funds only.

## recommendation

mercury first, holdings on watch. apply to mercury once the ein
lands (their path is proven for exactly our profile). before any
holdings move: email their support asking two questions - do they
support non-us-resident founders with a us llc, and do they expose
the agent integration via api (not just chat plugins). keep their
answer with this doc if we ever revisit.

## sources

- mercury eligibility: support.mercury.com/hc/en-us/articles/28770467511060
- mercury documents: support.mercury.com/hc/en-us/articles/28770957425172
- holdings: getholdings.com and getholdings.com/banking
