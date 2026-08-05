### I build AI systems that can be checked.

I work on products where the interesting problem is trust: can a user verify what the system
just told them? That question shows up in ML governance, in retrieval, and in provenance, and
it is most of what I have built.

I decide what gets built and why, I ship it, and I run it against real users and real data.

**Selected work**

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

**How I work**

Build on real data. Live markets, real documents, production lineage. A demo that only works on
fixture data has not been tested.

Prove it. A claim should link to a source or settle on chain. I would rather ship a measured
result that is inconvenient than a confident one I cannot support.

Build for one user first. If it is not useful to a single named person, scale will not save it.

Test on the deployed thing. Localhost agrees with you. Production does not.

Reach me at cnpierrepapi@gmail.com.
