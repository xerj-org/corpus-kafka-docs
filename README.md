# Kafka protocol documentation — scoped mirror (kafka-protocol corpus)

Mirror of [apache/kafka-site](https://github.com/apache/kafka-site) scoped to the
CURRENT documentation: `content/en/43/` (the current version's docs, design and
implementation notes, and the generated wire-protocol reference) plus the
current docs served at `content/en/` root (protocol.md, design.md, intro.md,
uses.md, quickstart.md and siblings).

Dropped from the corpus — with reasons, measured on the pre-registered G7 run
of 2026-10-04 that scored 2/5:
- `static/` (750 MB): ~20 versioned copies of the Kafka javadoc. They are not
  protocol docs and they outranked the answer on every miss.
- `content/en/<old-versions>/` (0100…42): the Q2 miss retrieved `upgrade.md`
  from three different old versions ahead of the current protocol reference;
  version clones of near-identical docs dilute current-doc queries.
- hugo machinery (layouts, assets, scripts, Dockerfiles) and site noise
  (blog, testimonials, community pages).

Pinned upstream commit: 7bf6e996d33183683add594d7ef76a6f1fc7ca1a (2026-10-01)
Licence: Apache-2.0 (LICENSE, verbatim from upstream — unchanged by scoping).
Regeneration: clone kafka-site at the pinned commit, `cp -r content/en/43 43`,
`cp content/en/*.md .`, `cp LICENSE .`.

Corpus slug: `kafka-protocol` — the G7 wave-1 suite re-runs unchanged
(expect_files under content/en/43/ suffix-match the 43/ paths here).
