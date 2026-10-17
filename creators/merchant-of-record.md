# merchant of record: creator is the seller, sculptura facilitates

ruled 2026-10-17: option 1, the etsy-model. the buyer's purchase
contract is with the creator's shop; sculptura runs the rails,
escrow, routing, and fee collection. sculptura is the marketplace
facilitator, not the seller. structured as option 3's platform: if
a house line ever exists, those items are platform-mor separately.

## what this unlocks

- class 40 trademark wording (brand/ip): facilitator language -
  arranging for the manufacture of jewelry for others, not custom
  manufacture
- stripe connect configuration: separate charges and transfers -
  already the escrow architecture (charge on the platform account,
  per-order/milestone transfers to connected accounts, payouts on
  the 15th)
- tax posture: us marketplace-facilitator rules - the platform
  collects and remits sales tax once thresholds hit, while the
  legal seller stays the creator

## the descriptor and privacy answer (why option 1 is safe here)

because separate charges and transfers put the charge on the
platform's stripe account, the buyer's payment descriptor - card
statement, paypal receipt, apple pay record - is **sculptura's**,
configured by the platform. it never carries the creator's legal
name. buyers see the shop handle (trade name) in the receipt ui.

creator legal identity lives only in: stripe connect kyc, payout
and banking records, and private platform records. it never renders
on any buyer-facing surface - consistent with the standing
location-ambiguity and identity rulings: descriptors and receipts
leak neither names nor geographies.

## per-market expansion item

some markets require the seller's legal identity on invoices
(eu-style invoicing rules). handled at market rollout: either the
facilitator invoicing regimes (platform invoices for tax purposes,
which is what marketplace-facilitator vat regimes do) or
market-specific invoice design. the us launch market needs neither;
the invoice question is parked with the market-rollout leg, not
blocking.

## fee model consistency

option 1 is what the financial model already assumes: revenue =
fees (the take breakup stays valid), creator payouts are
pass-through escrow releases, and platform accounts never book
order value as revenue. no model changes.
