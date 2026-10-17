# reverse ip indemnity: the parametric safe harbor

## the problem it answers

a creator can walk into the studio, assemble parameter vectors that
reproduce a cartier love bracelet or a chrome hearts ring, name it
accordingly, and publish. the cease-and-desist arrives at sculptura
because sculptura is the visible platform. the safe harbor is
reverse: sculptura does not warrant non-infringement of anything;
the creator warrants and indemnifies, because the creator is the
one who made the expressive choice.

the architecture makes this fair: the studio is neutral tooling
(the same relationship a cad program has to what its users draw).
paracraft's templates and the engine are platform ip; the specific
configuration a creator deploys is the creator's act. template
provenance (paracraft-side) draws that line in every claim.

## the creator warranty (at publish, structured)

at every design release, the creator explicitly warrants that:

1. the combination of parameters they selected was **not designed
   to replicate a trademarked or trade-dress-protected physical
   asset**, and they are not aware of a protected product the
   design imitates;
2. the listing's textual name does not reference, evoke, or claim
   endorsement by any brand or person;
3. they hold the rights needed for every imported element they
   contributed beyond platform templates.

the warranty is a structured acceptance in the release flow: a
recorded event in the release metadata (append-only, terms of
record), not a scroll-through checkbox. every release carries its
warranty event, so any third-party claim can be answered from the
record: what was warranted, when, by whom.

## the indemnity

the creator indemnifies sculptura (and its partners) against any
third-party trademark, trade dress, patent, or registered-design
claim arising from:

- the specific configuration vectors they deployed in the studio
- the textual names and descriptions of their listings
- imported materials they contributed

the indemnity does not cover platform-owned components: house
templates, engine geometry, and platform copy are sculptura's own
exposure and are not shifted onto creators.

## honest limits (counsel's problem, stated plainly)

- indemnities against individual creators are often uncollectable:
  a solo creator is judgment-proof. the indemnity's real value is
  evidentiary (it proves the platform put the choice, and the
  liability, where the choice was made) and deterrent, not a
  recovery source. the operative protections are the publish-time
  gates and the takedown posture
  ([takedown-and-listing-liability.md](takedown-and-listing-liability.md)).
- the warranty above must survive as the platform's safe-harbor
  argument even if no indemnity dollar is ever collected.

## enforcement hooks

- publish gate: luxury-token scan on names and descriptions
  (deterministic, paracraft-side, blocklist of obvious brand
  tokens; false positives get a human review path)
- release metadata: warranty event attached to every release
- dispute flow: outside-artist claims consume the warranty record
  and provenance lookup as first-class evidence
