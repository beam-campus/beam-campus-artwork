# BEAM Campus — Voice and Writing Guide

*How we sound. Applies to website copy, documentation, proposals, conference decks, social posts.*

## Register

**Engineer-to-engineer.** We assume the reader is a senior technical person who wants specific facts, not motivational framing.

| Situation | Good | Bad |
|-----------|------|-----|
| Describing a product | "Macula is a federated HTTP/3 relay mesh. 300 relays across three countries, 10,000 connected nodes." | "Macula revolutionises sovereign infrastructure with cutting-edge relay technology that unlocks new possibilities." |
| Describing a problem | "The current Kademlia DHT has a 6-minute TTL and no republish schedule, causing record loss in production." | "Current limitations in our infrastructure create sub-optimal user experiences that we are passionate about solving." |
| Describing a solution | "Replace with tier-aware S/Kademlia + proper lifecycle (tReplicate=1h, tRepublish=24h)." | "We're building a game-changing new system that leverages best-in-class technologies to deliver superior results." |
| Describing a goal | "Target €3M ARR by month 18." | "Our ambitious roadmap will drive explosive growth in the coming quarters." |

## Rules

### Use

- Present tense ("Macula supports X," not "Macula will support X")
- Specific numbers ("300 relays" not "many relays")
- Active voice ("We implement X" not "X is implemented")
- Direct statements ("This works" not "This has been shown to potentially work")
- Technical precision (exact protocol names, version numbers, hash algorithms)

### Avoid

- Marketing verbs: disrupt, revolutionise, transform, unlock, empower, elevate
- Vague qualifiers: seamlessly, effortlessly, best-in-class, next-generation
- Corporate hedging: "in the coming weeks," "we are exploring," "leverages"
- Superlatives without backup: "the most advanced," "world-class"
- Acronym soup without definitions ("Deployed via CI/CD in our GitOps-based K8s cluster...") without context
- Exclamation marks in technical contexts

### Balance

Technical accuracy matters, but accessibility matters too. Write so a senior engineer can understand immediately, **without** making a first-year CS student feel lost. Define acronyms on first use. Link to prior work.

## Sentence patterns

### The "evidence-first" pattern

State the fact. Then the implication. Not the other way round.

**Good:** "Paris relay IPv6 outage on 9 April 2026 caused 3,300 nodes to auto-failover in under 10 seconds. This demonstrates resilience works as designed."

**Bad:** "Our infrastructure is exceptionally resilient, as demonstrated by a recent failover event."

### The "comparison" pattern

When positioning vs. alternatives, be specific and fair.

**Good:** "Iroh is Rust-based; Macula is BEAM-native. Iroh targets individual P2P use; Macula targets infrastructure federation with thousands of nodes per realm."

**Bad:** "Unlike other solutions on the market, Macula offers unique advantages."

### The "number" pattern

Anchor claims to numbers whenever possible.

| Instead of | Say |
|------------|-----|
| "Production-deployed" | "300 relay identities across DE/FI/FR, 10,000+ connected nodes" |
| "Well-tested" | "500+ tests across unit, integration, and end-to-end suites" |
| "Community traction" | "10+ hex.pm packages with organic download traffic" |
| "Fast" | "Cross-EU RPC p95 < 200ms, intra-realm p95 < 20ms" |

## Vocabulary

### Our words

- **Sovereign** (not "independent" or "self-hosted")
- **Federated** (not "distributed" when we mean federation specifically)
- **Relay** (the technical term; not "server" or "node" in the relay context)
- **Realm** (our unit of sovereignty; capitalise in product contexts)
- **Mesh** (the topology; not "network" generically)
- **Resilient** / **resilience** (preferred over "reliable" in infrastructure contexts)
- **European** (not "EU" in brand voice; "EU" when citing specific regulation)
- **Open source** (two words; not "opensource")

### Banned words

- "Revolutionary"
- "Cutting-edge"
- "Next-generation"
- "Game-changing"
- "Synergy"
- "Leverage" (as a verb — use "use")
- "Solutioning"
- "Holistic"
- "Ecosystem" in a vague marketing sense (OK when specific: "the BEAM ecosystem")

### Words we're careful with

- **AI** — use sparingly, specifically; never as a grab-bag term
- **Blockchain** / **crypto** — only when specifically relevant, never to seem trendy
- **Disruptive** — only in the precise economics-Clay-Christensen sense, never generically
- **Enterprise** — use when specifically meaning enterprise-scale; avoid as a selling adjective

## Regional register

We are European-based and European-rooted. Our voice is:

- **Quiet confidence** — not American sales energy
- **Direct** — more like German engineering communication than English corporate
- **Fact-based** — claims backed by evidence, not by marketing theatre
- **Slightly formal** — appropriate for B2B, regulatory, technical audiences

When writing for international audiences, use British / European English spellings (colour, centre, realise) for consistency with our Belgian origin, unless the outlet explicitly prefers US spellings.

## Example rewrites

### Before (marketing voice)

> Introducing Macula — the revolutionary new sovereign infrastructure platform that empowers European organisations to seamlessly unlock next-generation digital sovereignty while leveraging best-in-class distributed technologies to transform their operations.

### After (our voice)

> Macula is a federated HTTP/3 relay mesh built on Erlang/OTP. It enables European organisations to operate sovereign infrastructure without depending on US-controlled cloud platforms. Current deployment: 300 relay identities across Germany, Finland, and France; 10,000+ connected nodes.

---

### Before

> We are excited to announce that our team has been working diligently on a game-changing new release that will elevate the user experience and unlock tremendous value for our ecosystem partners.

### After

> Macula v1.2 is released. Three changes: (1) tier-aware S/Kademlia replacing the previous DHT, (2) IPv6-direct routing with 44-byte source-routing header for relay-forward fallback, (3) signed records via PKARR-compatible format. Release notes: [link].

---

### Before

> BEAM Campus is committed to delivering exceptional sovereignty solutions that drive meaningful outcomes for our valued customers through innovative approaches to infrastructure challenges.

### After

> BEAM Campus builds open-source infrastructure for European organisations that need to run software without US legal jurisdiction. Three products: Macula (network), ReckonDB (data), Hecate (runtime).

## Sign-off

When in doubt, the "engineer-to-engineer" test: would a senior engineer respect this sentence, or roll their eyes at it? If they'd roll their eyes, rewrite.
