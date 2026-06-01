# Semantic Identity Protocol: Shortcut Aliases, Domain Bridges, and Global Registry Model

## 1. The Core Problem

A major adoption issue for Semantic Identity Protocol (SIP) is the length of the full owner-bound SIP string path.

A full owner-bound SIP identity may need to be long in order to be precise, portable, and machine-verifiable. For example:

```text
@owner/edbecnel/stackworks/games/strategy/abstract/capture/leaping/stacking/lasca
```

This kind of identifier is useful for machines, registries, verification, and long-term ownership tracking. However, it is not practical as the public-facing name that people are expected to type, remember, print, share, or market.

If SIP requires people to use long owner-bound strings directly, many users will fall back to ordinary `.com` names because domain names are shorter, familiar, and marketable.

Therefore, SIP needs a naming model that gives humans short, memorable identifiers while preserving the long canonical SIP identity underneath.

The solution is to separate:

```text
Human-friendly SIP shortcut
        from
Canonical owner-bound SIP identity
```

The full owner-bound SIP path should be treated like a cryptographic or canonical backend identity. It is the permanent truth, but it should not be the primary human interface.

---

## 2. Three Layers of SIP Identity

SIP should support three distinct layers of identity:

1. **Canonical owner-bound SIP identity**
2. **SIP shortcut string**
3. **Domain-based discovery alias**

These are related, but they are not the same thing.

---

## 3. Canonical Owner-Bound SIP Identity

The canonical owner-bound SIP identity is the full permanent identity used internally by resolvers, software, registries, and verification systems.

Example:

```text
@owner/edbecnel/stackworks/games/strategy/abstract/capture/leaping/stacking/lasca
```

This identity is:

- permanent
- owner-bound
- machine-verifiable
- portable
- explicit
- suitable for long-term registry records
- not dependent on a domain name

This is the identity that SIP software should ultimately resolve to and verify.

However, most users should rarely need to see or type this full string.

---

## 4. SIP Shortcut Strings

A SIP shortcut string is a shorter SIP-native identifier that begins with `@`.

Examples:

```text
@stackworks/lasca
@games/lasca
@edbecnel/lasca
```

These are SIP strings because they follow the SIP shortcut convention:

```text
SIP strings begin with @
```

A shortcut string is a human-friendly SIP identifier. It exists to make SIP practical for everyday use.

However, not all shortcut strings have the same meaning. SIP should distinguish between several types of shortcuts.

---

## 5. Domain-Based Discovery Aliases Are Not SIP Strings

The following are not SIP strings:

```text
stackworks.games/lasca
lasca.stackworks.games
```

They do not begin with `@`, so they should not be described as SIP shortcut strings.

They are better described as:

```text
Domain-based discovery aliases
```

or:

```text
Web entry points into SIP resolution
```

A domain alias can point into SIP, but it is not itself the SIP identity.

Example resolution chain:

```text
lasca.stackworks.games
        ↓
@stackworks/lasca
        ↓
@owner/edbecnel/stackworks/games/strategy/abstract/capture/leaping/stacking/lasca
```

The domain name serves as a familiar web-facing bridge. The SIP string remains the actual SIP identity layer.

---

## 6. Avoid Confusing `sip:` URI Syntax

A URI-style example such as:

```text
sip:stackworks.games/lasca
```

should probably be avoided.

Although it resembles a protocol URI, `sip:` is already strongly associated with the existing internet telephony protocol called SIP, the Session Initiation Protocol. Using `sip:` for Semantic Identity Protocol could create confusion.

If a URI wrapper is needed later, SIP could consider a different scheme such as:

```text
sipi:stackworks.games/lasca
semantic-id:stackworks.games/lasca
sid:stackworks.games/lasca
```

However, the cleanest primary rule is:

```text
SIP strings begin with @.
Domain aliases do not.
```

---

## 7. Corrected Naming Categories

The earlier examples should be categorized like this:

### SIP Shortcut Strings

```text
@stackworks/lasca
@games/lasca
```

These are SIP-native shortcut strings.

### Domain-Based Discovery Aliases

```text
stackworks.games/lasca
lasca.stackworks.games
```

These are not SIP strings. They are ordinary domain-style names that can resolve into SIP.

---

## 8. Semantic Discovery Paths

A shortcut such as:

```text
@games/lasca
```

should not necessarily resolve directly to one owner-bound identity.

Instead, it should first resolve to a fuller semantic discovery SIP path.

Example:

```text
@games/lasca
        ↓
@games.strategy.abstract.capture.leaping.stacking.lasca
```

or, if slash-separated paths are preferred:

```text
@games/lasca
        ↓
@games/strategy/abstract/capture/leaping/stacking/lasca
```

The full discovery path identifies the semantic category or concept. It says:

```text
Find the thing called Lasca in the semantic category of abstract strategy games involving capture, leaping, and stacking.
```

It does not yet identify a specific owner, implementation, website, ruleset document, or application.

---

## 9. Discovery Path Versus Owner-Bound Identity

This distinction is critical.

A semantic discovery path identifies a concept or category.

An owner-bound SIP identity identifies a specific owner-controlled record, implementation, document, product, or service.

Example:

```text
@games/lasca
```

is a public semantic shortcut.

```text
@games.strategy.abstract.capture.leaping.stacking.lasca
```

is a fuller semantic discovery path.

```text
@owner/edbecnel/stackworks/games/strategy/abstract/capture/leaping/stacking/lasca
```

is an owner-bound SIP identity.

A proper SIP resolution chain might look like this:

```text
@games/lasca
        ↓
@games.strategy.abstract.capture.leaping.stacking.lasca
        ↓
matching verified owner-bound SIP records
        ↓
@owner/edbecnel/stackworks/games/strategy/abstract/capture/leaping/stacking/lasca
```

This keeps the shortcut useful without pretending that a global semantic concept belongs to one owner.

---

## 10. Why `@games/lasca` Should Not Directly Identify One Owner

The string:

```text
@games/lasca
```

should mean:

```text
Find the global semantic concept Lasca.
```

It should not mean:

```text
Find Ed Becnel's Lasca implementation.
```

For an owner-specific identity, use something like:

```text
@stackworks/lasca
```

or:

```text
@owner/edbecnel/stackworks/games/lasca
```

This prevents public semantic concepts from being captured by private owners.

---

## 11. Three Kinds of SIP Shortcuts

SIP should formally distinguish at least three shortcut types:

1. **Global semantic shortcuts**
2. **Owner or brand shortcuts**
3. **Local or private shortcuts**

---

## 12. Global Semantic Shortcuts

Global semantic shortcuts are public, owner-neutral shortcuts.

Examples:

```text
@games/lasca
@games/chess
@games/checkers
@music/snare-drum
@recipes/jambalaya
```

These resolve to discovery paths, not directly to one owner.

Example:

```text
@games/lasca
        ↓
@games.strategy.abstract.capture.leaping.stacking.lasca
```

This means:

```text
Find the semantic concept Lasca.
```

Global semantic shortcuts should be controlled by recognized namespace stewards or registry processes, not by private individuals or companies.

---

## 13. Owner or Brand Shortcuts

Owner or brand shortcuts are controlled by a verified owner, person, organization, project, or brand.

Examples:

```text
@stackworks/lasca
@edbecnel/recipes/jambalaya
```

These can resolve to owner-bound SIP identities.

Example:

```text
@stackworks/lasca
        ↓
@owner/edbecnel/stackworks/games/lasca
```

This means:

```text
Find StackWorks' Lasca implementation, document, ruleset, service, or related owned record.
```

Unlike global semantic shortcuts, owner or brand shortcuts may belong to a specific verified owner.

---

## 14. Local or Private Shortcuts

Local or private shortcuts are user-defined or organization-defined aliases.

Examples:

```text
@my/lasca
@favorites/jambalaya
@test/game1
```

These are useful inside a local workspace, application, private organization, or personal knowledge base.

They are not globally authoritative unless registered through the global SIP shortcut system.

A local shortcut may be convenient, but it should not be confused with a globally accepted SIP shortcut.

---

## 15. The Governance Problem

SIP shortcut strings are only valuable if they are not random private abbreviations.

If anyone can casually declare:

```text
@games/lasca
```

then the shortcut has no global meaning.

For shortcuts to work globally, SIP needs a registry or governance model that determines which shortcut paths are officially accepted and what they resolve to.

The key question is:

```text
How does a SIP shortcut path string become the accepted global SIP shortcut path string?
```

The answer is:

```text
It must be registered as an official alias in a recognized SIP shortcut registry.
```

---

## 16. Global SIP Shortcut Registry

SIP should define a formal registry layer, possibly called:

```text
SIP Global Shortcut Registry
```

This registry would define accepted shortcut paths such as:

```text
@games/lasca
@games/chess
@games/checkers
@music/snare-drum
@recipes/jambalaya
```

Each shortcut would be a signed registry entry, not merely a piece of text.

Example registry record:

```json
{
  "shortcut": "@games/lasca",
  "resolvesTo": "@games.strategy.abstract.capture.leaping.stacking.lasca",
  "status": "accepted",
  "namespace": "@games",
  "type": "semantic-discovery-shortcut",
  "description": "Lasca / Laska family of stacking capture board games",
  "steward": "SIP Games Namespace Registry",
  "created": "2026-06-01",
  "version": "1.0"
}
```

This makes the shortcut auditable, verifiable, and stable.

---

## 17. Namespace Stewardship

The root namespace:

```text
@games
```

should not be privately owned by one commercial entity.

Major public semantic namespaces such as:

```text
@games
@music
@recipes
@books
@software
@people
@places
@products
```

should be managed by recognized namespace stewards or working groups.

For example:

```text
@games
        stewarded by SIP Games Namespace Registry
```

The `@games` namespace steward would be responsible for reviewing and approving global shortcuts inside that namespace.

Therefore:

```text
@games/lasca
```

would be approved by the `@games` namespace authority.

But:

```text
@stackworks/lasca
```

would be controlled by StackWorks.

Those are different authority models.

---

## 18. First Use Should Not Automatically Win

SIP should avoid domain-name-style squatting.

If someone attempts to register:

```text
@games/chess
```

that person should not own the public semantic concept of chess.

They may own something like:

```text
@somecompany/chess
```

or:

```text
@owner/somecompany/games/chess
```

But the global semantic shortcut:

```text
@games/chess
```

should be treated as a public controlled vocabulary entry, not private property.

Global semantic shortcuts should not be allocated by simple first-come, first-served registration.

---

## 19. Suggested Acceptance Process for Global Shortcuts

A global SIP shortcut should go through a process similar to this:

```text
1. Proposal
2. Public review
3. Conflict check
4. Semantic path assignment
5. Shortcut approval
6. Signed registry publication
7. Versioned updates over time
```

For example, someone proposes:

```text
@games/lasca
```

The registry or namespace steward reviews questions such as:

```text
Is "Lasca" the common name?
Is it ambiguous?
Does it conflict with another game, product, person, or brand?
Should the shortcut be @games/lasca or @games/laska?
What full discovery path should it resolve to?
Are there known synonyms?
```

The registry may then approve:

```text
@games/lasca
        →
@games.strategy.abstract.capture.leaping.stacking.lasca
```

It may also approve synonyms:

```text
@games/laska
        →
@games.strategy.abstract.capture.leaping.stacking.lasca
```

This gives SIP a stable, curated, globally meaningful shortcut system.

---

## 20. Signed Registry Entries

A shortcut should not be trusted merely because it appears in text.

It should be backed by a signed registry entry.

A signed shortcut record should include:

```text
shortcut
canonical discovery path
namespace
status
description
steward
version
creation date
signature
```

The signature ensures that a resolver can verify that the shortcut record came from the accepted namespace authority or registry.

---

## 21. Practical Bootstrap Strategy

At first, SIP does not need a complex distributed registry.

It could begin with a simple official registry file such as:

```text
sip-shortcuts.json
```

or:

```text
registry.sip/.well-known/global-shortcuts.json
```

The important requirements are that registry entries should be:

```text
public
versioned
signed
auditable
not silently changeable
```

Over time, the registry could become distributed, mirrored, cryptographically signed, or governed by multiple independent stewards.

---

## 22. Domain Discovery Manifests

Domain names can still be useful as discovery entry points.

For example:

```text
stackworks.games/lasca
```

could resolve to:

```text
@stackworks/lasca
```

which then resolves to:

```text
@owner/edbecnel/stackworks/games/lasca
```

A domain could publish a SIP manifest at a conventional metadata location such as:

```text
https://stackworks.games/.well-known/sip.json
```

Example manifest:

```json
{
  "sipManifest": "1.0",
  "domain": "stackworks.games",
  "aliases": [
    {
      "alias": "@stackworks/lasca",
      "canonical": "@owner/edbecnel/stackworks/games/strategy/abstract/capture/leaping/stacking/lasca",
      "title": "Lasca",
      "type": "game.ruleset",
      "fingerprint": "7K3Q-9M2A"
    }
  ],
  "signedBy": "@owner/edbecnel",
  "signature": "..."
}
```

This lets ordinary domains participate in SIP without becoming the root identity.

The domain is a doorway. The SIP identity remains the verified canonical record.

---

## 23. Recommended User-Facing Display

Most users should not see the full canonical SIP string unless they expand details.

A user interface might show:

```text
Lasca
Verified by StackWorks
Shortcut: @stackworks/lasca
Fingerprint: 7K3Q-9M2A
```

An expanded technical view might show:

```text
Canonical SIP:
@owner/edbecnel/stackworks/games/strategy/abstract/capture/leaping/stacking/lasca

Discovery Path:
@games.strategy.abstract.capture.leaping.stacking.lasca

Global Shortcut:
@games/lasca

Owner Shortcut:
@stackworks/lasca
```

This keeps the everyday interface short while preserving full technical transparency.

---

## 24. Final Resolution Model for Lasca

The clean Lasca model would look like this:

```text
User-facing global shortcut:
@games/lasca

Resolves through the global shortcut registry to:
@games.strategy.abstract.capture.leaping.stacking.lasca

Discovery finds verified owner records such as:
@stackworks/lasca
@owner/edbecnel/stackworks/games/strategy/abstract/capture/leaping/stacking/lasca
```

The full chain:

```text
@games/lasca
        ↓
@games.strategy.abstract.capture.leaping.stacking.lasca
        ↓
matching verified owner-bound SIP records
        ↓
@stackworks/lasca
        ↓
@owner/edbecnel/stackworks/games/strategy/abstract/capture/leaping/stacking/lasca
```

A domain bridge could also enter the chain:

```text
lasca.stackworks.games
        ↓
@stackworks/lasca
        ↓
@owner/edbecnel/stackworks/games/strategy/abstract/capture/leaping/stacking/lasca
```

---

## 25. Key Design Principle

A global SIP shortcut is not merely an abbreviation.

It is an officially accepted public semantic alias.

Therefore:

```text
@games/lasca
```

means:

```text
The SIP @games namespace registry has accepted "lasca" as the short global discovery alias for the Lasca semantic concept.
```

This design gives SIP short, usable identifiers without surrendering the system to `.com` names or private ownership of public concepts.

---

## 26. Summary

SIP should solve the long-path problem by using a layered identity model:

```text
Domain alias
        ↓
SIP shortcut string
        ↓
Semantic discovery path
        ↓
Owner-bound canonical SIP identity
```

The most important rules are:

```text
1. SIP strings begin with @.
2. Domain aliases do not begin with @ and are not SIP strings.
3. Global semantic shortcuts resolve to discovery paths, not directly to private owners.
4. Owner or brand shortcuts resolve to owner-bound records.
5. Global shortcuts must be accepted through a registry or namespace steward process.
6. First use should not automatically win for public semantic concepts.
7. Shortcut records should be signed, public, versioned, and auditable.
```

This makes SIP practical for humans while preserving the deeper semantic and ownership guarantees that make SIP valuable.
