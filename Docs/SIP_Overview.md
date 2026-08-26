# Semantic Identity Protocol (SIP)

### A new identity layer for the AI-native internet

---

## The one-line version

SIP gives every resource on the internet a **human-readable, AI-understandable semantic address** — one that expresses *what something means*, not just where it lives.

```
@amazon.cloud.aws        →  https://aws.amazon.com
@google.video.youtube    →  https://youtube.com
@wikipedia.knowledge.apollo11  →  https://en.wikipedia.org/wiki/Apollo_11
```

---

## What problem does SIP solve?

### 1. The internet's address system was built for machines, not meaning

DNS domains (`aws.amazon.com`, `youtube.com`) are transport addresses. They tell a browser *where to go*, but they say almost nothing about *what is there*. An AI assistant reading `aws.amazon.com` has to infer that this is Amazon's cloud computing platform — the domain itself doesn't say so.

SIP fixes this. `@amazon.cloud.aws` encodes the full semantic context directly: **owner → category → service**. No inference required.

### 2. Good names are scarce and expensive

The flat global namespace of `.com` domains turned internet identity into a land grab. Short, meaningful names are hoarded, auctioned, or squatted. A startup launching today may find every reasonable domain taken and face five-figure acquisition costs just to get a credible address.

SIP eliminates this scarcity. Because semantic paths are **hierarchical and contextual**, there is no finite pool of root names to exhaust. `@amazon.bakery.shop` and `@amazon.commerce.marketplace` can coexist without conflict — neither entity owns the root label `amazon` globally. Uniqueness lives at the **full path level**, not the first word.

### 3. URLs are fragile; meaning is stable

A URL is a location. Locations change — routes reorganize, infrastructure migrates, frameworks are replaced. But the *meaning* of a resource rarely changes. Amazon's cloud platform has been AWS for twenty years, even as its URLs have evolved dozens of times.

SIP separates **semantic identity** from **transport location**. The SIP address stays the same; the URL it points to can be updated without breaking every reference that existed before.

---

## How it works (in plain terms)

1. **Semantic Identity Providers (SIPs)** — organizations that host verified mappings from semantic paths to destinations, similar to how DNS registrars host domain records, but federated and open.

2. **Resolvers** — services that query multiple providers, weigh verification quality and cross-provider consensus, and return a ranked destination. No single company controls resolution.

3. **Two modes of identity:**
   - **Discovery paths** like `@video.streaming` are intentionally broad. A resolver returns ranked candidates — Netflix, YouTube, Disney+. The user or AI picks the right one.
   - **Owner-bound identities** like `@stackworks.games.lasca` are specific and verified. A resolver routes deterministically to a single destination.

4. **Trust through consensus, not monopoly** — multiple providers may publish mappings for the same identity. Resolvers prefer mappings where verification exists and trusted providers agree. No single registry can corner the market on semantic meaning.

---

## Why now?

The internet is entering an AI-native era. Billions of people interact with the web through AI assistants that interpret natural language intent and navigate on their behalf. Those systems need an address layer that carries meaning — not just routing instructions.

`aws.amazon.com` is opaque to AI reasoning. `@amazon.cloud.aws` is self-describing. Multiply that difference across every resource on the internet and the gap becomes enormous.

SIP is designed from the ground up for this moment: **semantic-first, AI-native, federated, and scarcity-resistant**.

---

## What it enables

| Capability | What it looks like |
|---|---|
| **Natural language navigation** | "Open Amazon's cloud services" → AI resolves `@amazon.cloud.aws` automatically |
| **Semantic discovery** | Typing `@games.strategy.abstract` surfaces ranked candidates the user can explore |
| **Stable bookmarks** | Save `@amazon.cloud.aws` once; it remains valid even if the URL changes |
| **AI-assisted IntelliSense** | Autocomplete for semantic paths, with synonym awareness and owner-bound suggestions |
| **Shortcut aliases** | `@games.lasca` privately expands to the full canonical path you've chosen |
| **Shareable shortcut collections** | Export and import curated shortcut sets with verified author attribution |
| **Health monitoring** | Providers alert owners when routes break, SSL lapses, or destinations move |
| **Contextual resolution** | The same path can resolve differently based on user history, location, or profile |

## Global SIP Shortcut Registry

A **global SIP shortcut** is a short, public, owner-neutral alias — such as `@games/lasca` or `@games/chess` — that resolves to a semantic discovery path rather than to any private owner's destination. These shortcuts are governed by a **Global SIP Shortcut Registry** managed by namespace stewards (e.g. the *SIP Games Namespace Registry* for `@games`). Acceptance requires a formal process: proposal, public review, conflict check, semantic path assignment, and cryptographic signing. First-come, first-served registration does **not** apply — no individual or company can claim ownership over a public semantic concept simply by registering first. Each accepted entry is a signed JSON record identifying the shortcut, the discovery path it expands to, the steward, and a version stamp.

Global shortcuts sit in the second of three shortcut tiers. `@games/lasca` is a **global semantic shortcut** that expands to `@games.strategy.abstract.capture.leaping.columns.lasca` and returns ranked owner candidates — any publisher can appear there. `@stackworks/lasca` is an **owner-brand shortcut** controlled by StackWorks that resolves deterministically to their specific record. `@my/lasca` is a **local personal shortcut** stored in the user's trusted context only. This layering ensures that short, memorable paths remain a shared public vocabulary while owner identity and user preferences each have their own distinct, non-competing layer.

---

## Business opportunities

SIP is an open protocol, but open protocols create large ecosystems. The opportunities are substantial at every layer.

### Infrastructure providers

Cloudflare, Fastly, and similar edge-network companies are natural hosts for SIP resolution infrastructure. Offering a managed SIP provider service — verification, mapping hosting, health monitoring, federation APIs — mirrors the business model of managed DNS but for the semantic layer.

### AI companies and browsers

Every AI assistant and every browser needs a resolution layer. SIP gives them a structured, federated, standardized one. Companies that build high-quality resolvers gain a strategic position in how AI systems navigate the web.

### Enterprise identity management

Large organizations need to manage hundreds or thousands of semantic identities, just as they manage domains today — but with richer metadata, semantic health monitoring, AI-assisted repair, and analytics. This is a clear enterprise SaaS opportunity.

### Creator and publisher platforms

Platforms hosting content (Substack, YouTube, Medium, BoardGameGeek) can offer semantic identity registration as a feature, letting creators establish verifiable, meaningful identities that persist independently of the platform's own URL structure.

### Developer tooling

IDE plugins, browser extensions, CLI tools, and API clients that understand SIP syntax create an entire developer tooling ecosystem around semantic identity — much as the npm or package-manager ecosystem built up around software identity.

### Semantic data and analytics

Aggregated, anonymized semantic resolution data represents a rich signal about intent and meaning on the internet — a dataset valuable to search companies, AI model trainers, and market researchers.

### Domain-expert taxonomy services

Specialized communities (medical, legal, academic, gaming) can publish authoritative semantic metadata within SIP — establishing themselves as trusted sources for their domain's semantic relationships and earning resolver reputation accordingly.

---

## What makes SIP different from existing systems?

| | DNS | Search | ENS / Blockchain | SIP |
|---|---|---|---|---|
| **Meaning-encoded** | No | Partially | No | **Yes** |
| **AI-native** | No | Partially | No | **Yes** |
| **Scarcity-resistant** | No | N/A | No | **Yes** |
| **Federated** | Partially | No | Yes | **Yes** |
| **URL-independent** | No | Partially | Yes | **Yes** |
| **No blockchain required** | Yes | Yes | No | **Yes** |
| **Human-readable** | Partially | N/A | No | **Yes** |

SIP does not require a blockchain, a token, or a central authority. It runs on existing internet infrastructure and extends it with a semantic layer governed by open standards and consensus.

---

## The long-term vision

Today, finding something on the internet requires knowing its address, guessing a search query, or hoping an AI assistant gets it right. SIP moves the internet toward a world where:

- **Meaning matters more than memorized addresses**
- **Semantic identity is stable even as infrastructure changes**
- **AI systems can reason about internet identity naturally**
- **Discovery replaces the arbitrary scarcity of flat-name ownership**

SIP doesn't replace the web. It makes the web semantically legible — for humans, and for the AI systems increasingly navigating it on their behalf.

---

## Explore further

- **[Whitepaper](SIP_Whitepaper.md)** — Full architecture, protocol design, governance model, trust and consensus model, resolver specification, semantic aliasing, challenges, and roadmap.
- **[JSON-LD Integration Architecture](SIP_JSON-LD_Integration_Architecture.md)** — How SIP complements JSON-LD, RDF, and Linked Data; representation-independent identity; proposed SIP JSON-LD Profile; progressive adoption model.
- **[Interactive Mockup](../Mockups/sip-intellisense-mockup.html)** — A self-contained browser demo of SIP Semantic IntelliSense: type a semantic path, explore suggestions, resolve to owner-bound identities, save shortcuts, share and import shortcut collections, and manage your shortcut library.
- **[Mockup Help](../Mockups/sip-intellisense-help.html)** — Full guide to every feature in the mockup.
