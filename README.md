### I build AI systems that can be checked.

I work on products where the interesting problem is trust: can a user verify what the system
just told them? That question shows up in ML governance, in retrieval, and in provenance, and
it is most of what I have built.

I decide what gets built and why, I ship it, and I run it against real users and real data.

Open to remote roles and contract work. The titles that fit are AI product manager, customer
centric engineer, forward deployed engineer. Reach me at cnpierrepapi@gmail.com.

## Selected work

**[Ariadne](https://github.com/cnpierrepapi/ariadne)** answers a question production ML teams
ask constantly and answer slowly: when a model starts behaving badly, what upstream change
caused it? It walks data lineage to the root cause instead of guessing, and it carries policy
packs so one warehouse can be checked against several regulatory regimes at once.

The result I care about most is a negative one. Testing whether protected attributes could be
reconstructed from a "clean" dataset, sex came back at 0.813 AUC and race at 0.73, while
geographic region carried almost nothing. The lesson is that removing a column is not the same
as removing the information, and the useful product is the one that measures the gap rather
than asserting compliance. [Live](https://ariadne-five.vercel.app).

**[Warmleads](https://warmleads.app)** scores local businesses on how badly they need what an
agency sells, so outreach starts from evidence instead of a list. It runs about 10,675 scored
businesses with live billing through Stripe and Paystack. Building it taught me more about
pricing and unit economics than about code: the first pricing model needed roughly 1,400
subscribers to work, and the fix was the customer, not the feature set.

**[Doc-chat](https://github.com/cnpierrepapi/doc-chat)** is retrieval over your own documents
with inline citations, so an answer links back to the passage it came from. Voyage embeddings,
pgvector, streaming responses. Built because an AI answer you cannot check is worth very little
in any setting where being wrong is expensive. [Live](https://doc-chat-beige-beta.vercel.app).

**[Hallmark](https://github.com/cnpierrepapi/hallmark)** stamps generated media with a record of
how it was made, and keeps that record attached through conversion so it survives the edit.
[Live](https://hallmark-rust.vercel.app).

**[Solana Error Doctor](https://github.com/cnpierrepapi/solana-error-doctor)** turns an opaque
chain error into a root cause and a verified fix. Shipped as a public skill for coding agents.

## Upstream contributions

One thread, running since July, on how DataHub models incidents. DataHub could raise an incident
on a table but not on a column, so the metadata model and the docs disagreed about which entity
types were actually supported. I picked up the column case and the documentation.

- [datahub-project/datahub#19115](https://github.com/datahub-project/datahub/pull/19115),
  **merged 20 Aug 2026.** Incident support for schemaField, so a data quality problem can be
  attached to the column it belongs to instead of the whole dataset.
- [datahub-project/datahub#18685](https://github.com/datahub-project/datahub/pull/18685), open.
  Generates the supported-entity table from the metadata model at build time, rather than asking
  someone to remember to update a page. Three backend surfaces are parsed; the two frontend ones
  are named in prose, because reaching into the web app from a model generator is a scope
  violation waiting to happen.
- [datahub-project/datahub#18684](https://github.com/datahub-project/datahub/pull/18684), open.
  Two self-hosted MCP troubleshooting entries, both from problems I hit myself.
- [datahub-project/datahub-skills#66](https://github.com/datahub-project/datahub-skills/pull/66),
  open. A skill that traces which models and dashboards a dataset change is about to break.

## How I work

Build on real data. Live markets, real documents, production lineage. A demo that only works on
fixture data has not been tested.

Prove it. A claim should link to a source or settle on chain. I would rather ship a measured
result that is inconvenient than a confident one I cannot support.

Build for one user first. If it is not useful to a single named person, scale will not save it.

Test on the deployed thing. Localhost agrees with you. Production does not.
