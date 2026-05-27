# Semantic Identity Protocol (SIP)

## White Paper, Architecture Overview, and Documentation Roadmap

Version: Draft 0.9 - Semantic Path Search and Boolean Query Expressions  Revision Date: May 27, 2026  Status: Conceptual Proposal

# Executive Summary

The Semantic Identity Protocol (SIP) proposes a new AI-native semantic identity and resolution layer for the internet.

SIP does NOT replace DNS.

Instead, SIP introduces a semantic identity overlay above existing web infrastructure that enables:

* Human-readable semantic identities
* AI-native routing and discoverability
* Contextual identity resolution
* Semantic discovery instead of flat-name scarcity
* Stable semantic identities independent of URL structure
* Federated semantic identity providers
* Consensus-driven semantic resolution
* Reputation-backed trust systems
* Semantic identity monitoring and management

Example semantic identities:

@amazon.commerce.marketplace
@amazon.cloud.aws
@google.video.youtube
@wikipedia.knowledge.apollo11

Example destination mappings:

@amazon.commerce.marketplace
→ https://amazon.com

@amazon.cloud.aws
→ https://aws.amazon.com

Example recognizable destination mappings:

@amazon.cloud.aws
→ https://aws.amazon.com

@google.video.youtube
→ https://youtube.com

@wikipedia.knowledge.apollo11
→ https://en.wikipedia.org/wiki/Apollo\_11

@reddit.community.programming
→ https://reddit.com/r/programming

Unlike DNS, semantic identities are:

* Meaning-oriented
* Contextual
* Hierarchical
* Discoverable
* AI-interpretable
* Non-exclusive at the root level

SIP is designed for:

* AI assistants
* Browsers
* Search systems
* Creator platforms
* Web applications
* Semantic discovery
* Future internet identity systems

# The Problem

## DNS Scarcity

The modern internet relies heavily on globally unique flat namespace ownership.

Examples:

example.com
example.org
example.io

This creates:

* Domain scarcity
* Domain squatting
* Artificial pricing inflation
* Branding exhaustion
* Poor discoverability
* Weak semantic meaning

Good names become expensive and difficult to obtain.

Startups are increasingly forced into:

* awkward spellings
* invented names
* expensive acquisitions
* undesirable TLDs

## AI-Native Navigation Requires Semantic Meaning

Modern domains are poorly suited for AI reasoning.

Example:

aws.amazon.com

contains some brand information, but does not explicitly express the full semantic context: Amazon → cloud computing → AWS.

By contrast:

@amazon.cloud.aws

contains:

* organization context: Amazon
* category context: cloud computing
* service/platform context: AWS
* semantic hierarchy

This pairing is intentionally matched: the traditional URL and the SIP identity point to the same real-world target, but the SIP expression makes the contextual meaning more explicit.

This is far more useful for:

* AI assistants
* semantic discovery
* intent resolution
* contextual navigation

## URLs Represent Locations, Not Meaning

URLs are transport-layer destinations.

They change frequently:

* route changes
* SPA routing changes
* infrastructure migrations
* framework migrations
* hosting changes

But semantic meaning changes much more slowly.

SIP separates:

* semantic identity from:
* transport location

# Core Principles

## Principle 1 — Semantic Identity Does Not Replace DNS

SIP uses existing internet infrastructure.

DNS remains:

* transport infrastructure
* routing infrastructure
* compatibility infrastructure

SIP introduces:

* semantic identity
* semantic discovery
* AI-native routing

above DNS.

## Principle 2 — Semantic Identity Does Not Equal URL Structure

Semantic identities identify meaning.

URLs identify transport locations.

Example:

@amazon.cloud.aws

may map to:

https://aws.amazon.com
https://console.aws.amazon.com
https://aws.amazon.com/console/
awsconsole://cloud/aws

without changing the semantic identity.

## Principle 3 — Specific Identities Resolve

Example:

@amazon.cloud.aws

is sufficiently specific to resolve directly.

## Principle 4 — General Identities Discover

Example:

@video.streaming

may resolve to multiple destinations.

Resolvers return ranked discovery results.

## Principle 5 — Root Semantic Names Are NOT Globally Owned

SIP intentionally avoids recreating DNS-style global scarcity.

Example:

@music

is NOT globally owned territory.

Semantic identities are:

* contextual
* federated
* reputation-based
* consensus-driven

This prevents semantic namespace speculation.

## Principle 6 — Consensus Matters More Than Ownership

Multiple Semantic Identity Providers (SIPs) may publish mappings.

Resolvers evaluate:

* verification
* provider reputation
* consensus agreement
* semantic relevance
* user trust

Truth emerges from:

* verification
* consensus
* reputation

not exclusive ownership.

## Principle 7 — Semantic Identities Are Managed Assets

Semantic identities are living resources.

They require:

* monitoring
* verification
* routing updates
* notifications
* health management

SIP therefore includes:

* dashboards
* APIs
* notifications
* health monitoring

# Semantic Identity Syntax

## Basic Syntax

@owner.category.project

Examples:

@amazon.commerce.marketplace
@amazon.cloud.aws
@wikipedia.knowledge.apollo11
@google.video.youtube.creators

## Hierarchical Structure

Semantic identities support arbitrary hierarchy depth.

Examples:

@amazon.cloud.aws.console
@wikipedia.knowledge.apollo11
@google.video.youtube.creators

## Semantic Categories

Categories provide contextual meaning.

Examples:

.games
.recipes
.school
.projects
.music
.video

These are semantic concepts, not DNS ownership layers.

# Resolution Model

## Exact Resolution

Input:

@amazon.cloud.aws

Result:

https://aws.amazon.com

## Discovery Resolution

Input:

@video.streaming

Result:

1. Netflix streaming video
2. YouTube streaming video
3. Disney+ streaming video

## Personalized Resolution

Resolvers may personalize results using:

* user history
* location
* preferences
* language
* trust settings

# Semantic Identity Providers (SIPs)

## Definition

A Semantic Identity Provider (SIP) is an organization or service that:

* hosts semantic identity mappings
* verifies identity ownership
* publishes semantic metadata
* participates in federation
* exposes standardized APIs

## SIP Responsibilities

### Identity Verification

Examples:

* DNS TXT verification
* HTTPS challenge verification
* OAuth verification
* signed manifests

### Mapping Publication

Example:

@amazon.cloud.aws
→ https://aws.amazon.com

### Health Monitoring

SIPs monitor:

* route validity
* SSL validity
* redirects
* content reachability
* manifest integrity

### Owner Notifications

Website owners receive notifications when:

* mappings fail
* URLs change
* SSL expires
* redirects break
* AI detects likely route changes

# Federation Model

## Open Protocol

SIPs interoperate through:

* shared APIs
* shared metadata schemas
* shared verification standards
* shared federation protocols

No single organization owns SIP.

## Federated Ecosystem

Possible SIP providers:

* Cloudflare SIP
* Mozilla SIP
* Cloudflare SIP
* self-hosted SIPs
* open-source SIPs

## Resolver Aggregation

Resolvers query multiple SIPs.

Resolvers rank results using:

* provider reputation
* consensus agreement
* verification confidence
* semantic relevance

# Resolver Architecture

## Resolver Responsibilities

Resolvers:

* query SIPs
* aggregate mappings
* evaluate consensus
* apply reputation weighting
* resolve ambiguity
* return ranked destinations

## Example Resolution Request

GET /resolve?identity=@amazon.cloud.aws

## Example Resolver Response

{
 "identity": "@amazon.cloud.aws",
 "results": [
 {
 "destination": "https://aws.amazon.com",
 "confidence": 0.98,
 "verified": true,
 "provider": "Cloudflare SIP"
 }
 ]
}

# Consensus and Reputation

## Consensus-Driven Resolution

Resolvers prefer mappings where:

* multiple trusted SIPs agree
* ownership verification exists
* semantic relevance is high

## Reputation System

SIPs earn reputation through:

* mapping accuracy
* uptime
* anti-spam enforcement
* verification quality
* consensus consistency

Resolvers may reduce trust for:

* spam mappings
* malicious redirects
* deceptive content
* broken mappings

# Semantic Identity Health Monitoring

## Managed Semantic Infrastructure

SIP introduces:

* semantic identity health
* active monitoring
* AI-assisted repair
* continuity tracking

## Example Health Record

{
 "identity": "@amazon.cloud.aws",
 "status": "healthy",
 "lastVerified": "2026-05-22T08:15:00Z",
 "destination": "https://aws.amazon.com"
}

## AI-Assisted Route Repair

If routes change:

* AI may detect likely replacements
* owners may approve updates
* semantic identity remains stable

# AI Integration

## AI-Native Navigation

Users may interact using natural language.

Examples:

Open Amazon AWS cloud services.
Find reliable Apollo 11 information.
Open YouTube video platform.

AI systems resolve semantic identities automatically.

## Semantic Advantage

Semantic identities provide:

* hierarchical meaning
* contextual meaning
* category meaning
* owner meaning

This is significantly more useful for AI systems than traditional domains.

# Browser and Application Integration

## Chrome Extension MVP

The SIP Chrome extension should:

* detect semantic identities
* resolve identities
* redirect to destinations
* display ambiguity choices
* expose verification metadata

## Future Browser Integration

Future browser support may allow:

@amazon.cloud.aws

directly in the address bar.

# Trust, Verification, and Anti-Impersonation

SIP recognizes that an open federated semantic identity ecosystem must prevent impersonation, phishing, namespace abuse, and malicious semantic mappings.

Trust within SIP is not based solely on name claims or provider authority. Instead, SIP combines:

* ownership verification
* provider reputation
* cross-provider consensus
* semantic relevance
* user trust signals

to establish semantic identity credibility.

## Verification Philosophy

Semantic identities are not automatically trusted simply because they are registered.

For example:

@google.video.youtube

must not automatically be treated as authoritative unless the publisher can prove control or authorization associated with the mapped destination.

Verification mechanisms may include:

* DNS TXT verification
* HTTPS challenge verification
* signed manifests
* OAuth identity verification
* organization email verification
* cryptographic signatures
* institutional verification

## Trust Levels

Resolvers may expose semantic identity trust levels such as:

Unverified
Domain Verified
Organization Verified
Consensus Verified

Highly verified semantic identities may auto-resolve.

Weakly verified or ambiguous semantic identities may instead trigger discovery mode or user confirmation.

## Consensus-Driven Trust

Multiple SIP providers may publish mappings for the same semantic identity.

Resolvers evaluate:

* provider reputation
* verification quality
* consensus agreement
* semantic relevance
* historical accuracy

before selecting the most trusted destination.

This prevents any single provider from monopolizing semantic identity authority while also discouraging impersonation and malicious mappings.

## Resolver Behavior

Resolvers should clearly distinguish between:

* strongly verified semantic identities
* ambiguous semantic identities
* weakly verified semantic identities
* suspicious or conflicting mappings

Resolvers may:

* request user confirmation
* show ranked alternatives
* suppress low-trust mappings
* warn users about suspicious destinations

## Federation Philosophy

SIP intentionally avoids centralized ownership of semantic identity.

Trust emerges through:

* interoperable verification standards
* federated providers
* reputation systems
* consensus-driven resolution
* open protocols

rather than exclusive namespace ownership.

This architecture enables SIP to remain open, federated, and interoperable while still supporting strong trust and anti-impersonation protections.

# Governance

## Open Standards

SIP should be governed through:

* open standards
* public specifications
* interoperable protocols
* multi-provider federation

## Anti-Monopoly Design

SIP intentionally avoids:

* centralized ownership
* global namespace monopolization
* single-provider control

No single company owns semantic identity.

# Economic Model

## Incentives For Providers

SIPs may monetize:

* hosting
* monitoring
* analytics
* enterprise verification
* AI routing APIs
* semantic discovery services
* premium management tools

## Incentives For AI Companies

AI companies benefit from:

* semantic navigation
* improved intent resolution
* richer identity graphs
* structured internet meaning

# Future Vision

SIP represents a transition from:

* location-oriented internet identity

Toward:

* meaning-oriented internet identity

The long-term internet may evolve toward:

* semantic navigation
* AI-assisted discovery
* contextual identity resolution
* federated identity graphs

rather than flat global domain ownership.

# Required Documentation Roadmap

## 1. SIP White Paper

Purpose:

* vision
* architecture
* economic model
* governance model
* AI integration

Audience:

* AI companies
* browser vendors
* standards communities
* investors
* developers

## 2. SIP Core Protocol Specification

Purpose:

* define APIs
* define federation
* define schemas
* define verification

Audience:

* protocol engineers
* browser developers
* SIP providers

Sections:

* syntax specification
* resolution protocol
* federation protocol
* metadata schema
* verification rules
* security model
* trust model

## 3. SIP Resolver Specification

Purpose:

* resolver architecture
* ranking algorithms
* consensus logic
* ambiguity handling

Topics:

* provider aggregation
* reputation scoring
* confidence calculation
* personalization
* caching
* failover

## 4. SIP Federation Specification

Purpose:

* provider interoperability
* federation discovery
* metadata exchange

Topics:

* SIP discovery
* federation registration
* provider trust
* synchronization
* distributed resolution

## 5. SIP Verification Specification

Purpose:

* ownership proof
* identity validation
* anti-hijacking

Topics:

* DNS verification
* HTTPS verification
* signed manifests
* OAuth verification
* cryptographic signing

## 6. SIP Security Architecture

Purpose:

* threat modeling
* abuse prevention
* anti-spam
* anti-phishing

Topics:

* malicious mappings
* spoofing
* replay attacks
* resolver poisoning
* provider compromise

## 7. SIP Reputation and Consensus Model

Purpose:

* provider reputation
* trust weighting
* consensus algorithms

Topics:

* confidence scoring
* provider trust
* ranking logic
* consensus thresholds
* spam suppression

## 8. SIP Semantic Identity Schema

Purpose:

* define semantic metadata structures

Topics:

* identity records
* destination records
* tags
* categories
* ownership metadata
* health metadata

## 9. SIP Dashboard and Management UX

Purpose:

* owner workflows
* management interfaces
* notifications

Topics:

* mapping management
* alerts
* AI-assisted repair
* analytics
* verification workflows

## 10. SIP AI Integration Specification

Purpose:

* define AI interaction model

Topics:

* semantic resolution
* natural language integration
* LLM APIs
* AI confidence handling
* ambiguity dialogue

## 11. SIP Browser Integration Proposal

Purpose:

* future browser support

Topics:

* address bar handling
* UI/UX
* ambiguity prompts
* trust indicators
* browser APIs

## 12. SIP Chrome Extension MVP Specification

Purpose:

* initial working prototype

Features:

* semantic identity parsing
* resolver calls
* redirects
* ambiguity popup
* verification display

## 13. SIP Manifest Specification

Purpose:

* self-hosted semantic identity publishing

Example:

/.well-known/semantic-identities.json

Topics:

* manifest structure
* signatures
* verification
* synchronization

## 14. SIP API Reference

Purpose:

* developer implementation reference

Topics:

* REST APIs
* response schemas
* federation APIs
* resolver APIs
* authentication

## 15. SIP Governance Charter

Purpose:

* long-term ecosystem governance

Topics:

* standards body
* interoperability requirements
* anti-monopoly protections
* open governance principles

## 16. SIP Reference Implementation

Purpose:

* prove feasibility

Components:

* sample SIP server
* sample resolver
* sample dashboard
* sample federation
* sample AI integration

## 17. SIP Demonstration Scenarios

Purpose:

* explain user experience

Examples:

Open @amazon.cloud.aws
Open @video.streaming
Find reliable Apollo 11 information

## 18. SIP Business and Monetization Strategy

Purpose:

* explain ecosystem sustainability

Topics:

* provider business models
* AI integration opportunities
* enterprise opportunities
* hosting opportunities

# Conclusion

SIP proposes:

* semantic identity above DNS
* AI-native internet navigation
* contextual semantic discovery
* federated semantic identity providers
* consensus-driven trust
* stable meaning independent of URLs

SIP does not replace the web.

SIP makes the web semantically understandable for both humans and AI systems.

The long-term vision is an internet where:

* meaning matters more than memorized addresses
* semantic identity matters more than domain scarcity
* AI systems can reason about internet identity naturally
* semantic discovery replaces flat-name ownership limitations

# Semantic Confidence and Ambiguity Resolution

SIP recognizes that not all semantic identities possess sufficient semantic specificity to function as deterministic globally resolvable identities.

For example:

@music

contains very little semantic information and may correspond to thousands or even millions of possible identities across the internet.

SIP therefore distinguishes between:

* semantic handles
* contextual aliases
* discovery-oriented identities
* strongly resolvable semantic identities

## Semantic Entropy and Identity Strength

Semantic identities possess varying levels of semantic entropy and contextual specificity.

Examples:

| Semantic Identity | Relative Semantic Strength |
| --- | --- |
| @music | Extremely Weak |
| @amazon.commerce | Weak |
| @amazon.cloud.aws | Strong |
| @google.video.youtube | Very Strong |

Higher semantic specificity generally produces:

* lower ambiguity
* higher resolver confidence
* stronger consensus stability
* improved deterministic resolution

## Discovery-Oriented Identities

Low-specificity semantic identities should generally behave as discovery identities rather than authoritative routing identities.

Example:

@music

may produce:

* ranked identity candidates
* profile suggestions
* organizations
* semantic categories
* contextual search-style results

rather than immediately resolving to a single destination.

This behavior intentionally discourages DNS-style root-name speculation.

## Deterministic Resolution Thresholds

Resolvers may calculate semantic confidence scores using factors including:

* hierarchy depth
* semantic uniqueness
* verification quality
* provider consensus
* contextual specificity
* historical resolution stability
* user context

Example conceptual confidence levels:

| Semantic Identity | Example Confidence |
| --- | --- |
| @music | 0.08 |
| @amazon.commerce | 0.42 |
| @amazon.cloud.aws | 0.96 |

Resolvers may refuse deterministic automatic resolution below configurable confidence thresholds.

## Contextual Resolution

Certain semantic identities may resolve differently depending on:

* user history
* organization membership
* browser profile
* local social graph
* resolver preferences
* geographic context

For example:

@music

inside a user’s personal environment may resolve successfully due to contextual familiarity while remaining globally ambiguous.

## Human Semantic Parallel

Human communication already behaves similarly.

Example:

Open music.

often requires additional contextual clarification.

By contrast:

Open Amazon cloud services for AWS.

contains significantly stronger semantic specificity.

SIP intentionally embraces this semantic reality rather than forcing artificial global uniqueness.

## Architectural Implications

SIP therefore does not attempt to replicate deterministic DNS-style exact global resolution for all semantic identities.

Instead, SIP supports:

* probabilistic semantic resolution
* confidence-aware routing
* ambiguity-aware discovery
* contextual resolution
* consensus-assisted ranking

This distinction represents one of the fundamental architectural differences between SIP and traditional DNS systems.

## Anti-Speculation Implications

Because low-specificity semantic identities possess limited deterministic routing value, short semantic handles such as:

@music
@news
@video

provide reduced monopolistic value compared to traditional domain names.

This naturally discourages semantic namespace speculation and artificial semantic scarcity.

# Challenges, Risks, and Open Questions

SIP acknowledges that semantic identity resolution introduces significant technical, governance, economic, and security challenges that must be addressed through open standards, interoperable protocols, and ongoing ecosystem collaboration.

The following areas represent critical architectural considerations for long-term SIP viability.

## Resolver Centralization Risk

Even in a federated ecosystem, dominant resolver operators could potentially centralize influence over semantic discovery and navigation.

Examples include: - AI assistant providers - browser vendors - search companies - operating system vendors

Resolvers may therefore require: - transparent ranking principles - resolver interoperability - user-selectable resolvers - open ranking signals - resolver neutrality guidelines

to reduce ecosystem capture risk.

## Reputation System Abuse

Consensus and reputation systems may be vulnerable to: - sybil attacks - coordinated spam - malicious providers - consensus manipulation - semantic SEO abuse

SIP therefore requires: - provider reputation scoring - trust weighting - anti-spam systems - abuse detection - verification requirements - adversarial threat modeling

## Ambiguity Explosion

General semantic identities may become highly ambiguous.

Example:

@video.minecraft

may refer to: - official game publishers - fan communities - servers - videos - educational content - malicious impersonators

Resolvers must therefore support: - ambiguity-aware ranking - confidence thresholds - contextual resolution - explicit disambiguation flows - user confirmation workflows

## Namespace Pollution

Open semantic registration may encourage: - meaningless identities - spam identities - keyword stuffing - semantic abuse - deceptive categorization

SIP providers and resolvers may require: - semantic quality policies - moderation systems - trust-based ranking - anti-spam heuristics - abuse penalties

## Privacy Concerns

Resolvers may learn: - browsing intent - semantic interests - organizational relationships - navigation behavior - discovery preferences

SIP therefore requires consideration of: - private resolution - encrypted queries - local caching - anonymous resolution - resolver minimization - privacy-preserving federation

## AI Hallucination Risk

AI-assisted semantic resolution introduces the possibility of: - incorrect inference - hallucinated destinations - false semantic relationships - incorrect routing

SIP therefore distinguishes between: - authoritative verified mappings - AI-assisted suggestions - semantic inference - discovery recommendations

AI systems may assist with ranking and discovery, but verified mappings remain authoritative.

## Competing and Related Systems

SIP overlaps conceptually with several existing technologies and standards including: - DNS - search engines - ActivityPub - Mastodon federation - ENS (Ethereum Name Service) - Handshake - Namecoin - package manager namespaces - knowledge graphs - OAuth identity systems

SIP differs by focusing specifically on: - semantic identity - AI-native navigation - federated meaning resolution - consensus-driven trust - stable meaning independent of URLs - non-scarce semantic hierarchy

without requiring blockchain ownership models or centralized identity monopolies.

## Governance Challenges

SIP introduces governance questions including: - trusted provider policies - resolver neutrality - semantic abuse handling - identity disputes - trademark conflicts - provider interoperability - federation standards

Long-term SIP governance may require: - open standards organizations - multi-stakeholder governance - interoperability requirements - transparent dispute procedures - anti-monopoly protections

## Trademark and Identity Conflicts

Conflicts may arise involving: - @apple.devices - @google.search - @microsoft.cloud

SIP therefore requires: - identity dispute frameworks - trademark handling procedures - organization verification - provider-level moderation - transparent appeal processes

## Performance and Scalability

Federated semantic resolution may create: - high query volumes - provider synchronization complexity - latency concerns - distributed caching challenges

SIP therefore requires: - edge caching - resolver optimization - federation indexing - distributed metadata synchronization - scalable reputation systems

## Open Questions

Several long-term questions remain intentionally open for ecosystem evolution: - How should resolver neutrality be standardized? - How should provider reputation be calculated? - What governance body should oversee SIP standards? - How should semantic abuse be moderated? - How should privacy-preserving resolution operate? - How should semantic ranking transparency be handled? - How should enterprise and institutional verification evolve?

SIP intentionally treats these areas as ongoing ecosystem and standards challenges rather than assuming all issues are permanently solved in the initial protocol design.

# AI-Mediated Semantic Resolution and Persistent Semantic Favorites

SIP recognizes that many users may never manually type semantic identities directly.

Instead, AI systems, browsers, applications, and semantic resolvers may generate SIP identity candidates automatically in response to natural language intent.

Example:

User request:

Find me a reliable cloud computing platform.

AI-generated semantic candidates:

@amazon.cloud.aws
@microsoft.cloud.azure
@google.cloud.platform
@oracle.cloud.infrastructure

Resolvers and AI systems may then: - rank semantic candidates - evaluate trust and reputation - infer contextual relevance - explain recommendations - ask disambiguation questions

This allows SIP to function as an AI-native semantic identity layer rather than merely a manual address-entry system.

## Semantic Favorites and Persistent Semantic Identity Memory

Once users identify preferred semantic identities, browsers, AI systems, applications, and operating systems may allow users to save semantic identities as persistent favorites.

Examples:

Favorite:
@amazon.cloud.aws

This allows future requests such as:

Open my favorite cloud platform.

or:

Open AWS.

to resolve using: - personal semantic preferences - user trust history - semantic favorites - local semantic memory - AI personalization

## Browser and AI Semantic Memory

Future semantic-aware systems may maintain:

* semantic favorites
* semantic bookmarks
* trusted semantic identities
* contextual semantic history
* AI-assisted semantic preferences

This creates a semantic identity layer that behaves more naturally like human memory and relationships rather than requiring memorization of exact URLs or globally unique identifiers.

## Architectural Implications

This architecture further reinforces that SIP is:

* AI-native
* semantic-first
* context-aware
* probabilistic rather than purely deterministic
* meaning-oriented rather than location-oriented

SIP therefore functions both as:

* a semantic identity system and:
* an AI-readable semantic knowledge and navigation layer.

## Relationship To Traditional Bookmarks

Traditional bookmarks save transport locations such as URLs.

SIP semantic favorites instead save:

* semantic meaning
* contextual identity
* trusted semantic relationships

This allows semantic favorites to remain stable even when: - URLs change - applications migrate - infrastructure changes - SPA routes evolve - transport mechanisms change

while still preserving the user’s semantic intent and trusted destination preferences.

# Semantic Aliasing and Multi-Path Identity

SIP recognizes that human semantic organization is not rigid, singular, or universally hierarchical.

The same resource may validly belong to multiple semantic pathways depending on: - culture - terminology - context - geography - cuisine style - user intent - organizational preference - AI semantic interpretation

SIP therefore supports semantic aliasing and multi-path semantic identity relationships.

## Example - Apollo 11 Knowledge Semantic Aliases

A single Wikipedia article about Apollo 11 may validly exist under multiple semantic identities such as:

@wikipedia.history.space.apollo11
@wikipedia.knowledge.apollo11
@wikipedia.science.space.apollo11
@wikipedia.education.space.apollo11
@wikipedia.astronomy.moon.apollo11

while all mapping to the same underlying semantic resource and destination.

For example:

https://en.wikipedia.org/wiki/Apollo\_11

This is not considered a conflict within SIP.

Instead, these represent multiple valid semantic pathways to the same semantic object.

## Canonical Identities and Semantic Aliases

SIP resources may define:

* canonical semantic identities
* semantic aliases
* contextual semantic aliases
* AI-generated semantic associations

Example conceptual model:

{
 "canonical": "@wikipedia.knowledge.apollo11",
 "aliases": [
 "@wikipedia.history.space.apollo11",
 "@wikipedia.space.apollo11",
 "@wikipedia.astronomy.moon.apollo11"
 ]
}

## Semantic Pathways vs Strict Taxonomy

SIP intentionally avoids rigid taxonomy requirements.

Semantic hierarchy within SIP represents:

* contextual meaning pathways rather than:
* strict ownership trees or:
* rigid classification systems

This allows SIP to more naturally model: - human language - semantic relationships - overlapping categories - contextual discovery - AI semantic reasoning

## AI-Assisted Semantic Enrichment

AI systems may assist with semantic enrichment by suggesting additional semantic aliases based on:

* content analysis
* topic analysis
* subject matter
* geography
* semantic similarity
* user behavior
* contextual relationships

Example AI-generated suggestions:

@wikipedia.nasa.apollo11
@wikipedia.moonlanding.apollo11
@wikipedia.knowledge.apollo11

Owners may approve, reject, or modify these semantic associations.

## Multi-Path Discovery

Users searching for:

Apollo 11 moon landing information

may still discover:

@wikipedia.history.space.apollo11

through semantic alias relationships and AI-assisted semantic graph traversal.

This significantly improves semantic discovery compared to rigid URL or DNS hierarchies.

## Semantic Graph Architecture

SIP identities therefore increasingly resemble semantic graph relationships rather than traditional filesystem-style paths.

This allows:

* many-to-one semantic mappings
* contextual discovery
* overlapping semantic organization
* AI-assisted relationship inference
* semantic continuity independent of URL structure

## Architectural Implications

This architecture further reinforces that SIP is:

* semantic-first
* AI-native
* graph-oriented
* context-aware
* meaning-oriented

rather than a simple replacement for hierarchical DNS naming.

SIP therefore functions as both:

* a semantic identity system and:
* a federated semantic knowledge routing layer.


# Semantic Synonyms and Equivalent Path Segments

SIP should support semantic synonyms: different path segments or semantic phrases that represent the same meaning within a given context.

Synonyms are related to semantic aliases, but they operate at a more granular level.

A semantic alias may describe an alternate full SIP path.

A semantic synonym may describe an equivalent segment or partial path inside a larger SIP expression.

For example:

@games.strategy.abstract.capture.leaping.columns

and:

@games.strategy.abstract.capture.leaping.stacking

may be treated as equivalent because, in this game taxonomy, "columns" and "stacking" describe the same core mechanic.

In this context:

columns ⇄ stacking

means:

A game where captured pieces are stacked into columns, towers, or layered piece structures.

## Segment-Level Synonyms

Segment-level synonyms allow a SIP resolver, provider, or IntelliSense system to recognize that two terms can occupy the same semantic position in a path.

Example:

@games.strategy.abstract.capture.leaping.columns.lasca

may be equivalent to:

@games.strategy.abstract.capture.leaping.stacking.lasca

Both expressions describe Lasca through the same semantic structure:

games → strategy → abstract → capture → leaping → stacking/columns → lasca

This does not necessarily mean that every use of "columns" and "stacking" is globally identical.

It means they are equivalent within this semantic context.

## Context-Bound Meaning

Synonyms should be context-bound rather than globally absolute.

For example, "stacking" may mean one thing in abstract strategy games, another thing in software architecture, and another thing in logistics or warehousing.

Therefore, synonym equivalence should usually be scoped to a semantic path or domain.

Example scoped synonym rule:

Within:

@games.strategy.abstract.capture.leaping

the segment:

columns

may be treated as equivalent to:

stacking

But outside that context, the same terms may not necessarily be equivalent.

## Canonical Paths and Synonym Paths

SIP may allow one path to be treated as canonical while other paths are treated as equivalent synonym paths.

Example canonical path:

@games.strategy.abstract.capture.leaping.columns.lasca

Equivalent synonym path:

@games.strategy.abstract.capture.leaping.stacking.lasca

The canonical path is the preferred stored or published identity.

The synonym path remains valid for discovery, IntelliSense, search, and AI-assisted navigation.

This allows SIP to support natural language variation without requiring every equivalent phrase to become a separate competing identity.

## Synonyms Are Not Ownership Claims

A synonym does not assign ownership.

For example:

@games.strategy.abstract.capture.leaping.stacking.lasca

may be equivalent to:

@games.strategy.abstract.capture.leaping.columns.lasca

But neither expression is owner-bound.

Both remain unbound discovery paths until the user selects a specific owner-qualified identity such as:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

or:

@stackworks.games.strategy.abstract.capture.leaping.stacking.lasca

if the owner has also published that synonym path.

The synonym relationship improves discovery and navigation.

It does not determine the authoritative owner.

## IntelliSense Behavior for Synonyms

Semantic IntelliSense should expose synonyms clearly without confusing them with ordinary child categories or owner-bound identities.

When the user types:

@games.strategy.abstract.capture.leaping.

IntelliSense may show:

Continue semantic discovery path:

columns  
stacking  
checkers  
dama  
draughts

The interface may indicate that:

columns

and:

stacking

are equivalent semantic choices.

For example:

columns  
Equivalent: stacking

stacking  
Equivalent: columns

If the user selects:

stacking

then the active SIP string may become:

@games.strategy.abstract.capture.leaping.stacking

and the system should still offer the same next-level continuations that would have appeared under:

@games.strategy.abstract.capture.leaping.columns

For example:

lasca  
damasca  
columns-draughts

If the user continues to:

@games.strategy.abstract.capture.leaping.stacking.lasca

the resolver may understand this as equivalent to:

@games.strategy.abstract.capture.leaping.columns.lasca

and may show the same owner-bound candidates.

## Synonym Selection and Canonicalization

When a user selects a synonym path, SIP-aware interfaces may either preserve the user’s chosen wording or show the canonical equivalent.

Two possible UX modes are valid:

1. Preserve user wording

Input:

@games.strategy.abstract.capture.leaping.stacking.lasca

Display remains:

@games.strategy.abstract.capture.leaping.stacking.lasca

Resolver understands it as equivalent to:

@games.strategy.abstract.capture.leaping.columns.lasca

2. Canonicalize visibly

Input:

@games.strategy.abstract.capture.leaping.stacking.lasca

Interface shows:

Equivalent canonical path:
@games.strategy.abstract.capture.leaping.columns.lasca

In either case, the interface should make clear that the expressions are semantically equivalent in the current context.

## Synonym Metadata

SIP identity records, semantic manifests, or provider APIs may define synonym relationships using metadata.

Example conceptual metadata:

{
 "canonical": "@games.strategy.abstract.capture.leaping.columns.lasca",
 "synonyms": [
   "@games.strategy.abstract.capture.leaping.stacking.lasca"
 ],
 "segmentSynonyms": [
   {
     "context": "@games.strategy.abstract.capture.leaping",
     "canonical": "columns",
     "equivalent": "stacking"
   }
 ]
}

This allows resolvers, IntelliSense systems, AI assistants, and browsers to understand equivalent semantic paths consistently.

## Relationship to Shortcut SIPs

Synonyms are different from shortcut SIPs.

A shortcut SIP compresses a longer path.

Example:

@games.lasca

may expand to:

@games.strategy.abstract.capture.leaping.columns.lasca

A synonym SIP expresses the same path using equivalent wording.

Example:

@games.strategy.abstract.capture.leaping.stacking.lasca

may be equivalent to:

@games.strategy.abstract.capture.leaping.columns.lasca

Both features improve usability, but they solve different problems.

Shortcuts reduce typing.

Synonyms support natural language variation.

## Core Synonym Rule

The core synonym rule is:

Synonyms may express equivalent meaning.  
They do not assign ownership.  
They do not eliminate the need for canonical identity resolution.

This allows SIP to support flexible human language while still preserving deterministic owner-bound resolution when a specific verified identity is selected.

## Broad Semantic Facets and Non-Exclusive Path Expansion

Some SIP expressions represent broad semantic facets rather than strict hierarchical paths or one-to-one aliases.

For example:

@games.strategy.abstract.stacking

does not necessarily mean:

@games.strategy.abstract.capture.leaping.columns

Although leaping column-capture games may involve stacking, stacking may also appear in other abstract strategy contexts, such as:

@games.strategy.abstract.capture.displacement.columns
@games.strategy.abstract.capture.rotation.columns
@games.strategy.abstract.movement.stacking
@games.strategy.abstract.placement.stacking

Therefore, broad semantic facet paths should generally behave as discovery expressions rather than canonical aliases.

The expression:

@games.strategy.abstract.stacking

means:

Find abstract strategy games involving stacking mechanics.

It does not by itself specify the exact capture method, movement method, or structural mechanic.

Semantic IntelliSense may respond by showing possible refinements, narrower semantic branches, and matching owner-bound identities.

A resolver should not collapse a broad semantic facet into a single canonical path unless the relationship is explicitly defined as one-to-one within a specific context.

Core rule:

Broad facets discover.
Specific aliases canonicalize.
Owner-bound identities resolve.

# Semantic Definition Authority and Governance

SIP does not require a single global authority to define every synonym, shortcut, facet, category, or semantic relationship.

Instead, SIP uses a multi-authority semantic definition model.

The SIP protocol defines the structure and rules for semantic relationships, but the actual semantic meaning of those relationships may come from verified owners, Semantic Identity Providers, resolvers, domain experts, communities, users, organizations, and AI-assisted semantic systems.

This distinction is important because SIP is not intended to become one universal centralized taxonomy.

SIP should define how semantic claims are expressed, verified, ranked, disputed, personalized, and resolved.

It should not require one central party to dictate every possible semantic meaning.

## Protocol-Defined Relationship Types

The SIP core specification should define the formal relationship types that the ecosystem may use.

Examples include:

- canonical identity
- semantic alias
- synonym
- equivalent path segment
- shortcut
- broad semantic facet
- owner-bound identity
- discovery path
- broader-than relationship
- narrower-than relationship
- related-to relationship
- personalized shortcut binding
- AI-suggested semantic association

These relationship types are part of the protocol grammar.

They define how semantic relationships are represented and interpreted.

For example, SIP may define that:

- a synonym expresses equivalent meaning within a context
- a shortcut compresses a longer semantic path
- a broad semantic facet discovers multiple narrower paths
- an owner-bound identity may resolve deterministically
- a personalized shortcut applies only within a user’s trusted context

The protocol defines these categories of relationship.

It does not centrally define every individual semantic fact.

## Owner-Defined Semantic Identities

Verified owners, publishers, organizations, creators, and providers may define semantic identities inside their own owner namespace.

For example, StackWorks may define:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

and may publish destination mappings such as:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca  
→ https://stackworks.games/lasca

StackWorks may also publish owner-bound aliases or shortcuts such as:

@stackworks.games.lasca

or:

@stackworks.games.abstract.lasca

Because these identities exist inside the StackWorks owner namespace, StackWorks may act as the authoritative publisher for those mappings, subject to verification, trust, and anti-impersonation requirements.

However, StackWorks should not automatically control broad unbound expressions such as:

@games.lasca

or:

@games.strategy.abstract.stacking

Those expressions exist in broader semantic discovery space and should not be globally owned by one publisher.

## Provider-Published Semantic Metadata

Semantic Identity Providers may publish semantic metadata, identity records, aliases, categories, facets, synonyms, and relationship claims.

Examples of provider-published semantic claims may include:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca  
is related to:  
@games.strategy.abstract.stacking

or:

@games.strategy.abstract.capture.leaping.columns  
has equivalent segment:  
@games.strategy.abstract.capture.leaping.stacking

or:

@games.strategy.abstract.stacking  
matches narrower paths including:  
@games.strategy.abstract.capture.leaping.columns  
@games.strategy.abstract.capture.displacement.columns  
@games.strategy.abstract.capture.rotation.columns

Such claims should be treated as semantic metadata.

They may be authoritative when published inside a verified owner namespace.

They may be consensus-ranked when published in broader public semantic space.

## Resolver-Ranked Consensus Relationships

For broad public semantic concepts, no single owner should automatically define the global meaning.

Examples:

@games.strategy.abstract.stacking  
@music.jazz  
@recipes.gumbo  
@video.minecraft

These expressions may be influenced by many sources, including:

- verified owner metadata
- Semantic Identity Providers
- community taxonomies
- domain experts
- trusted registries
- resolver ranking systems
- user behavior
- semantic popularity
- AI-assisted analysis
- cross-provider consensus

Resolvers should evaluate these claims using factors such as:

- provider reputation
- verification quality
- semantic relevance
- source credibility
- cross-provider agreement
- abuse resistance
- user trust settings
- historical accuracy
- contextual relevance

In this model, broad public semantic meaning emerges from federated metadata, domain knowledge, reputation, and consensus.

It is not dictated by a single central authority.

## Domain Expert and Community Contributions

Certain semantic areas may benefit from domain-specific taxonomies or expert-maintained semantic maps.

Examples:

- board game mechanics
- medical terminology
- legal terminology
- academic fields
- software package ecosystems
- music genres
- culinary traditions
- scientific classifications

For example, the relationship between:

@games.strategy.abstract.stacking

and narrower paths such as:

@games.strategy.abstract.capture.leaping.columns

may be informed by game designers, game historians, rules databases, gaming communities, and board game taxonomy providers.

SIP should allow these communities to publish semantic relationship claims, but resolvers should still evaluate those claims through reputation, verification, and consensus.

## User-Defined Personal Semantics

Users may define personal shortcuts, preferred identities, semantic favorites, and context-specific meanings.

For example, a user may choose:

@games.lasca

to mean:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

within that user’s trusted resolver context.

This creates a personal semantic binding.

It does not imply that StackWorks globally owns:

@games.lasca

Nor does it prevent another user from binding:

@games.lasca

to a different Lasca-related identity.

Personal semantic definitions may come from:

- explicit user choice
- saved semantic favorites
- browser profile settings
- organizational profile settings
- AI-assisted semantic memory
- trusted local resolver preferences

Personal semantic definitions should remain scoped to the user, organization, device, browser profile, or resolver context in which they were created.

## AI-Suggested Semantic Relationships

AI systems may suggest semantic relationships, but AI suggestions should not automatically be treated as authoritative.

AI may suggest that:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

is related to:

@games.strategy.abstract.stacking

or that:

columns

and:

stacking

may be equivalent within a particular game-mechanics context.

However, such suggestions should be treated as provisional unless they are:

- accepted by an owner
- confirmed by a trusted provider
- supported by domain expertise
- reinforced by resolver consensus
- approved by a user for personal use
- verified through reliable metadata

AI can assist discovery, enrichment, classification, and ranking.

It should not silently create authoritative semantic truth without verification or acceptance.

## Semantic Claims vs Semantic Authority

SIP should distinguish between publishing a semantic claim and having semantic authority.

A semantic claim says:

This relationship may be meaningful.

Semantic authority says:

This relationship is trusted enough to affect resolution, ranking, display, or deterministic behavior.

For example, any provider may claim:

@games.strategy.abstract.stacking  
is related to:  
@games.strategy.abstract.capture.leaping.columns

But a resolver may decide whether that claim is trusted based on:

- who published it
- whether it is verified
- whether reputable sources agree
- whether it matches user context
- whether it conflicts with better evidence
- whether it appears abusive or misleading

This distinction allows SIP to remain open while still resisting spam, abuse, and semantic manipulation.

## Authority Levels

SIP semantic definitions may be understood across several authority levels.

### Protocol Authority

The SIP specification defines the relationship types, metadata structures, verification models, and resolver behavior.

Example:

A broad semantic facet discovers multiple narrower paths.

### Owner Authority

A verified owner defines identities, aliases, and destination mappings inside its own namespace.

Example:

@stackworks.games.lasca  
→ https://stackworks.games/lasca

### Provider Authority

A Semantic Identity Provider publishes semantic metadata and verified records.

Example:

A provider publishes that Lasca belongs under abstract strategy games.

### Consensus Authority

Resolvers rank broad public semantic relationships based on multiple trusted sources.

Example:

@games.strategy.abstract.stacking

matches several narrower stacking-game branches.

### Personal Authority

A user defines private or contextual shortcut meanings.

Example:

For this user:

@games.lasca  
→ @stackworks.games.strategy.abstract.capture.leaping.columns.lasca

### AI-Assisted Authority

AI suggests relationships for review, enrichment, discovery, or personalization.

Example:

AI suggests that “stacking” may be a broad game mechanic facet.

## Example: StackWorks and Lasca

StackWorks may authoritatively define:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

and map it to:

https://stackworks.games/lasca

StackWorks may also define:

@stackworks.games.lasca

as an owner-bound shortcut.

However, broader unbound expressions such as:

@games.lasca

or:

@games.strategy.abstract.stacking

should remain public semantic discovery expressions.

They may return StackWorks as a highly relevant candidate, but they should not be globally owned by StackWorks.

A resolver may show:

StackWorks — Lasca  
@stackworks.games.strategy.abstract.capture.leaping.columns.lasca  
Maps to: https://stackworks.games/lasca

Wikipedia — Lasca  
@wikipedia.games.boardgames.lasca

BoardGameGeek — Lasca  
@boardgamegeek.games.boardgames.lasca

The user may then select StackWorks and optionally save:

@games.lasca

as a personal shortcut.

This gives the user convenience without creating global ownership over the shorthand.

## Core Semantic Authority Rule

The core rule is:

The SIP protocol defines relationship types.  
Owners define their verified identities.  
Providers publish semantic metadata.  
Resolvers rank and reconcile claims.  
Users define personal preferences.  
AI suggests relationships, but does not automatically make them authoritative.

This keeps SIP open, federated, contextual, and AI-native without allowing any one organization to define the entire semantic universe.

# Shortcut SIPs and Semantic Shortcut Aliases

SIP recognizes that highly descriptive semantic identities may become too long for frequent manual use.

For example, a fully descriptive Lasca discovery path might be:

@games.strategy.abstract.capture.leaping.columns.lasca

This expression is semantically rich because it describes Lasca as:

games → strategy → abstract → capture → leaping → columns → lasca

However, users may reasonably expect to type a shorter expression such as:

@games.lasca

SIP therefore supports shortcut SIPs, also called semantic shortcut aliases.

A shortcut SIP is a compact semantic expression that expands to a longer semantic discovery path or an owner-bound canonical identity.

Shortcut SIPs improve usability without removing the richer semantic structure behind the shortcut.

## Discovery Shortcut SIPs

A discovery shortcut SIP is a compact expression that expands to a longer unbound semantic discovery path.

Example:

@games.lasca

may expand to:

@games.strategy.abstract.capture.leaping.columns.lasca

This does not automatically bind the identity to a specific owner, publisher, organization, or destination.

Instead, it means:

Find resources semantically associated with Lasca within the games category.

The expanded path remains discovery-oriented unless the user selects a specific owner-bound result.

For example, after typing:

@games.lasca

Semantic IntelliSense may show:

Shortcut expansion:

Lasca game classification  
@games.strategy.abstract.capture.leaping.columns.lasca

Matching owner-bound identities:

StackWorks — Lasca  
@stackworks.games.strategy.abstract.capture.leaping.columns.lasca  
Maps to: https://stackworks.games/lasca

Wikipedia — Lasca  
@wikipedia.games.boardgames.lasca

BoardGameGeek — Lasca  
@boardgamegeek.games.boardgames.lasca

In this model, selecting the shortcut expansion keeps the user in semantic discovery mode.

Selecting an owner-bound candidate commits the expression to a specific owner-qualified identity.

## Owner-Bound Shortcut SIPs

An owner-bound shortcut SIP includes the owner namespace and therefore has stronger identity meaning.

Example:

@stackworks.games.lasca

may expand to:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

This expression is different from:

@games.lasca

because the owner is already specified.

The shortcut:

@stackworks.games.lasca

means:

Open or resolve the StackWorks-owned Lasca identity.

It may therefore resolve deterministically when verification, trust, and confidence thresholds are satisfied.

Example mapping:

@stackworks.games.lasca  
→ @stackworks.games.strategy.abstract.capture.leaping.columns.lasca  
→ https://stackworks.games/lasca

## Personalized Shortcut SIPs

Some shortcuts may be personalized by user preference, semantic favorites, browser profile, organization membership, or AI-assisted semantic memory.

For example:

@games.lasca

may normally behave as an unbound discovery shortcut.

However, if a user has previously selected and saved:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

as their preferred Lasca destination, then the user’s resolver may treat:

@games.lasca

as a personalized shortcut to the StackWorks Lasca identity.

This personalized behavior should be clearly distinguished from global deterministic resolution.

The shortcut is deterministic only within that user’s trusted context.

It should not imply that StackWorks globally owns:

@games.lasca

unless the owner-bound form is explicitly used.

## Resolver-Assisted Shortcut Binding

Users should not be required to know a full canonical SIP identity before creating a useful personal shortcut.

A user may begin with a compact shorthand expression such as:

@games.lasca

Before personalization, this expression behaves as an unbound shortcut discovery query.

The resolver may interpret it as:

Find likely SIP identities, semantic expansions, owner-bound candidates, and trusted destinations associated with games and Lasca.

The resolver may then return candidate identities such as:

StackWorks — Lasca  
@stackworks.games.strategy.abstract.capture.leaping.columns.lasca  
Maps to: https://stackworks.games/lasca

Wikipedia — Lasca  
@wikipedia.games.boardgames.lasca

BoardGameGeek — Lasca  
@boardgamegeek.games.boardgames.lasca

Generic semantic expansion  
@games.strategy.abstract.capture.leaping.columns.lasca

The user may then choose the desired identity and optionally save that choice as a personal shortcut.

For example, if the user selects:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

and saves it as the preferred meaning of:

@games.lasca

then the user’s trusted resolver context may store:

@games.lasca  
→ @stackworks.games.strategy.abstract.capture.leaping.columns.lasca  
→ https://stackworks.games/lasca

This creates a personalized shortcut binding.

The binding applies only within that user’s trusted context, browser profile, organization profile, or semantic memory environment.

It does not imply that StackWorks globally owns:

@games.lasca

Nor does it prevent other users from binding:

@games.lasca

to a different preferred Lasca-related identity.

Core rule:

A shorthand SIP may begin as discovery.  
After user selection, it may become a personal shortcut.  
Personal shortcut binding does not create global ownership.

## Shortcut SIP Types

SIP therefore distinguishes between at least three shortcut types:

1. Discovery shortcut

Example:

@games.lasca

Expands to:

@games.strategy.abstract.capture.leaping.columns.lasca

Behavior:

Unbound semantic discovery path.

2. Owner-bound shortcut

Example:

@stackworks.games.lasca

Expands to:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

Behavior:

Owner-qualified identity that may resolve deterministically.

3. Personalized shortcut

Example:

@games.lasca

May resolve for a specific user to:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

Behavior:

Personal or contextual shortcut based on saved preference, semantic favorite, or trusted resolver memory.

## IntelliSense Behavior for Shortcut SIPs

Semantic IntelliSense should visibly distinguish shortcut expansion from owner binding.

When the user types:

@games.lasca

the IntelliSense panel may display:

Shortcut expansion:

Lasca game classification  
@games.strategy.abstract.capture.leaping.columns.lasca  
Discovery shortcut. Expands meaning but does not bind an owner.

Matching owner-bound identities:

StackWorks — Lasca  
@stackworks.games.strategy.abstract.capture.leaping.columns.lasca  
Maps to: https://stackworks.games/lasca

Wikipedia — Lasca  
@wikipedia.games.boardgames.lasca

BoardGameGeek — Lasca  
@boardgamegeek.games.boardgames.lasca

If the user selects the shortcut expansion, the active SIP string becomes:

@games.strategy.abstract.capture.leaping.columns.lasca

The expression remains unbound and discovery-oriented.

If the user selects:

StackWorks — Lasca

the active SIP string becomes:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

The expression becomes owner-bound and may resolve to:

https://stackworks.games/lasca

## Shortcut Expansion Should Not Silently Assign Ownership

A shortcut SIP may expand semantic meaning, but it should not silently assign ownership.

This rule is important:

A shortcut may expand meaning, but it should not silently bind ownership unless the shortcut itself is owner-qualified or the user has selected a trusted owner-bound result.

For example:

@games.lasca

should not automatically become:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

unless one of the following is true:

- the user explicitly selects StackWorks as the owner-bound result
- the user has saved StackWorks Lasca as a semantic favorite
- the resolver is operating inside a trusted personalized context
- the SIP expression itself is owner-qualified, such as @stackworks.games.lasca

This protects SIP from recreating DNS-style ownership fights over short semantic expressions.

## Anti-Scarcity Implication

Shortcut SIPs preserve usability without creating artificial scarcity.

Broad shortcuts such as:

@games.lasca
@recipes.gumbo
@music.jazz
@video.minecraft

should generally remain discovery-oriented unless owner-qualified or personalized.

This prevents short semantic expressions from becoming globally monopolized assets.

At the same time, SIP still supports convenient owner-qualified shortcuts such as:

@stackworks.games.lasca
@amazon.cloud.aws
@google.video.youtube
@wikipedia.knowledge.apollo11

These owner-bound shortcuts may resolve deterministically when supported by verification, consensus, reputation, and resolver confidence.

## Core Shortcut Rule

The core shortcut rule is:

Shortcuts make SIP easier to type.  
They do not erase the distinction between discovery and ownership.

Discovery shortcut:

@games.lasca

means:

Explore Lasca-related game identities.

Owner-bound shortcut:

@stackworks.games.lasca

means:

Resolve the StackWorks-owned Lasca identity.

Canonical owner-bound identity:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

means:

Resolve the fully descriptive StackWorks Lasca semantic identity.

This allows SIP to remain both practical for everyday use and semantically precise for AI-native identity resolution.


# Identity–Discovery Spectrum

SIP recognizes that semantic pathways exist along a spectrum between:

* deterministic semantic identity and:
* semantic discovery intent

Not all SIP expressions represent authoritative globally resolvable semantic identities.

Many SIP expressions instead function as:

* semantic discovery pathways
* semantic search intent
* contextual semantic exploration
* AI-assisted semantic queries

## Deterministic Semantic Identities

Highly specific semantic identities may support deterministic resolution.

Example:

@wikipedia.knowledge.apollo11

This semantic identity strongly implies:

* creator or owner context
* knowledge category
* historical/scientific context
* specific topic identity

Such identities may resolve directly to a trusted semantic destination.

## Ambiguous Semantic Pathways

Partially specific semantic pathways may represent ambiguous semantic discovery.

Example:

@wikipedia.knowledge.apollo11

This may correspond to:

* multiple publishers
* encyclopedia articles
* educational sources
* videos
* educational pages
* AI-generated knowledge indexes

Resolvers may therefore return:

* ranked semantic candidates
* contextual recommendations
* trusted semantic sources
* discovery interfaces

rather than deterministic routing.

## Semantic Discovery Queries

Generalized SIP expressions may function primarily as semantic search intent.

Example:

@wikipedia.knowledge.apollo11

does not uniquely identify:

* a creator
* a publisher
* an organization
* a specific knowledge resource

Instead, it semantically represents:

Find information about Apollo 11.

Such expressions should therefore behave more like semantic discovery queries than authoritative semantic identities.

## Discovery and Ranking Behavior

Expressions such as:

@wikipedia.knowledge.apollo11

may discover or rank resources including:

@wikipedia.history.space.apollo11
@nasa.history.apollo11
@history.space.apollo11

based on:

* semantic relevance
* user preferences
* trust history
* contextual relationships
* AI-assisted ranking
* semantic alias relationships

rather than deterministic ownership mapping.

## Semantic Specificity Spectrum

SIP semantic behavior generally correlates with semantic specificity.

Examples:

| Semantic Pathway | Typical Behavior |
| --- | --- |
| @video | broad semantic discovery |
| @video.streaming | semantic discovery with ranking |
| @amazon.cloud.aws | likely deterministic resolution |
| @google.video.youtube | highly deterministic resolution |

## AI-Native Semantic Navigation

This architecture allows SIP to unify:

* semantic identity
* semantic discovery
* AI-assisted navigation
* semantic memory
* semantic personalization
* contextual semantic reasoning

within a single interoperable semantic framework.

## Architectural Implications

SIP therefore differs fundamentally from DNS.

DNS primarily performs:

* exact deterministic location resolution

SIP instead supports:

* probabilistic semantic resolution
* semantic ranking
* ambiguity-aware discovery
* contextual interpretation
* AI-assisted semantic navigation

This distinction represents one of the central architectural principles of SIP.

Integrated Real-World URL → SIP Mapping Examples

The following examples demonstrate how SIP identities expose semantic meaning far more clearly than many modern URLs, shortened links, opaque IDs, and technical routing structures.

|  |  |  |
| --- | --- | --- |
| Traditional URL | SIP Equivalent | Semantic Advantage |
| aws.amazon.com | @amazon.cloud.aws | Clearly communicates Amazon cloud services and AWS platform identity. |
| youtube.com/@mkbhd | @mkbhd.video.tech | Represents creator identity, media type, and technology content category. |
| youtu.be/dQw4w9WgXcQ | @rickastley.video.nevergonnagiveyouup | Represents the actual artist, media type, and specific video identity rather than an opaque shortlink. |
| discord.gg/python | @discord.community.python | Represents a Python programming community rather than a random invite code. |
| aka.ms/vscode | @microsoft.developer.vscode | Represents Microsoft's VS Code developer platform rather than a generic shortlink. |
| npmjs.com/package/react | @meta.code.react | Clearly communicates organization, software category, and framework identity. |
| github.com/openai/gym | @openai.code.gym | Represents OpenAI software project identity and category. |
| reddit.com/r/machinelearning | @reddit.community.machinelearning | Represents a machine learning discussion community. |
| docs.google.com/document/d/abc123 | @google.docs.collaboration.projectproposal | Represents collaborative document purpose rather than opaque document IDs. |
| substack.com/profile/ai-insights | @writer.newsletter.ai | Represents AI-focused newsletter publishing identity. |

Key Observation

Traditional URLs primarily expose transport and infrastructure structure. SIP identities instead expose semantic meaning, contextual relationships, content type, creator identity, organizational identity, and AI-readable intent.

---

# Semantic IntelliSense and Guided Semantic Navigation

SIP recognizes that manually typing and memorizing deeply structured semantic identities may become impractical as semantic ecosystems grow.

SIP therefore supports Semantic IntelliSense — an AI-assisted semantic autocomplete and guided navigation system similar to modern IDE code completion systems.

## Semantic IntelliSense

As users type semantic identities beginning with the @ symbol, SIP-aware browsers, AI assistants, operating systems, and applications may provide contextual semantic suggestions dynamically at each hierarchy level.

Example:

User types:

@games.

Suggested semantic continuations:

@games.minecraft
@games.chess
@games.lasca
@games.strategy
@games.boardgames

As the user continues typing:

@games.lasca.

Suggested semantic continuations:

@games.lasca.online
@games.lasca.rules
@games.lasca.community
@games.lasca.tournaments

This allows users to navigate semantic knowledge structures interactively rather than memorizing exact semantic identities.

## AI-Assisted Semantic Completion

Semantic IntelliSense suggestions may be generated using:

- AI semantic reasoning
- semantic graph relationships
- trust and reputation scoring
- user preferences
- semantic favorites
- contextual relevance
- organization membership
- historical usage
- semantic popularity
- semantic similarity analysis

This creates AI-assisted semantic navigation rather than simple static autocomplete.

## Semantic Exploration

Low-specificity semantic identities may naturally function as semantic exploration nodes.

Example:

@games

may expose semantic discovery suggestions including:

@games.minecraft
@games.chess
@games.strategy
@games.simulation

rather than behaving as a single deterministic destination.

This allows SIP to support semantic exploration and contextual discovery naturally.

## Deterministic Semantic Resolution

Higher-specificity semantic identities may increasingly support deterministic routing.

Example:

@openai.code.gym

contains significantly greater semantic specificity and may therefore resolve directly to a trusted semantic destination.

This creates a natural spectrum between:

- semantic discovery
and:
- deterministic semantic identity resolution

## Semantic Navigation UX

SIP-aware interfaces may provide:

- dropdown semantic suggestions
- AI-assisted semantic ranking
- contextual semantic completion
- semantic favorites
- semantic bookmarks
- semantic history
- semantic recommendation systems
- trust-ranked semantic navigation

This allows semantic navigation to behave more like intelligent knowledge exploration than traditional URL entry.

## Owner-Bound Identity Selection in Semantic IntelliSense

Semantic IntelliSense should distinguish between:

- unbound semantic discovery paths
- owner-bound semantic identities

This distinction is important because users may begin semantic navigation from a broad conceptual category rather than from a known owner, publisher, organization, or verified semantic namespace.

For example, a user may begin typing:

@games.

Semantic IntelliSense may then suggest broad game categories such as:

@games.action
@games.strategy
@games.rpg
@games.adventure
@games.narrative
@games.puzzle
@games.casual

If the user selects:

@games.strategy

and continues navigating through additional semantic levels, the resulting expression may become:

@games.strategy.abstract.capture.leaping.columns.lasca

This expression should be treated as an unbound semantic discovery path.

It semantically means:

Find identities, resources, games, communities, rule systems, or destinations associated with:

games → strategy → abstract → capture → leaping → columns → lasca

It does not yet assert a specific owner or authoritative publisher.

By contrast, an owner-bound semantic identity includes a verified or selected owner namespace, such as:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

This expression identifies a specific StackWorks-owned semantic identity that may resolve deterministically to a destination such as:

https://stackworks.games/lasca

or another current StackWorks Lasca destination.

### Discovery Path Mode

When the user is navigating an unbound path such as:

@games.strategy.abstract.capture.leaping.columns.lasca

Semantic IntelliSense should treat the expression as discovery-oriented.

At this stage, the resolver or IntelliSense engine may return ranked candidate identities such as:

StackWorks — Lasca  
@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

BoardGameGeek — Lasca  
@boardgamegeek.games.strategy.abstract.capture.leaping.lasca

Wikipedia — Lasca  
@wikipedia.games.boardgames.lasca

Other Lasca-related communities, rule references, tournaments, variants, or educational resources may also appear depending on resolver confidence, user context, semantic relevance, provider reputation, and trust signals.

### Owner-Bound Identity Mode

Owner-bound identity mode begins when the user selects a specific authoritative or preferred candidate.

For example, if the user selects:

StackWorks — Lasca

then the semantic expression may be completed or rewritten as:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

At that point, the expression is no longer merely an exploratory semantic pathway. It has become a specific owner-qualified semantic identity.

This owner-qualified form may be eligible for deterministic resolution if verification, trust, consensus, and confidence thresholds are satisfied.

### Owner Names Should Not Be Treated as Ordinary Child Categories

Owner or publisher names should not normally be inserted as ordinary dot-level continuations at the end of an exploratory semantic path.

For example, after:

@games.strategy.abstract.capture.leaping.columns.lasca.

the owner name:

stackworks

should not normally appear as if it were a subcategory of Lasca.

This would blur the distinction between semantic classification and identity ownership.

Instead, Semantic IntelliSense should present owner-bound results in a separate suggestion group.

Example:

Continue semantic path:

@games.strategy.abstract.capture.leaping.columns.lasca.rules  
@games.strategy.abstract.capture.leaping.columns.lasca.online  
@games.strategy.abstract.capture.leaping.columns.lasca.tournaments  
@games.strategy.abstract.capture.leaping.columns.lasca.history  
@games.strategy.abstract.capture.leaping.columns.lasca.variants  

Matching owner-bound identities:

StackWorks — Lasca  
@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

Wikipedia — Lasca  
@wikipedia.games.boardgames.lasca

BoardGameGeek — Lasca  
@boardgamegeek.games.boardgames.lasca

This allows the user to either:

- continue exploring the semantic graph
- choose a concrete owner-bound semantic identity
- select a trusted destination
- save the selected identity as a semantic favorite

### Completion Behavior

Semantic IntelliSense should follow this general rule:

Typing categories explores meaning.  
Choosing an owner-bound result commits identity.

In practical terms:

- selecting a semantic continuation extends the discovery path
- selecting an owner-bound candidate completes or rewrites the SIP expression as a canonical owner-qualified identity
- deterministic resolution should generally occur only after an owner-bound identity is selected or inferred with high confidence
- ambiguous discovery paths should continue to return ranked results rather than automatically redirecting

### IntelliSense Panel Layout and Selection Behavior

Semantic IntelliSense should appear visually near the active SIP string, similar to an IDE autocomplete menu or browser address-bar suggestion panel.

When the user is typing a SIP expression, the active text field remains the primary focus.

Example active input:

@games.strategy.abstract.capture.leaping.columns.

Directly below or alongside the active SIP string, the interface may display an IntelliSense panel grouped into separate suggestion sections.

Example:

Current SIP input:

@games.strategy.abstract.capture.leaping.columns.

IntelliSense suggestions:

Continue semantic discovery path:

  lasca
  damasca
  columns-draughts

Matching owner-bound identities:

  StackWorks — Lasca
  @stackworks.games.strategy.abstract.capture.leaping.columns.lasca

  StackWorks — Damasca
  @stackworks.games.strategy.abstract.capture.leaping.columns.damasca

  BoardGameGeek — Lasca
  @boardgamegeek.games.boardgames.lasca

The key UX principle is that semantic continuations and owner-bound identities are visually distinct choices.

A semantic continuation is a category, concept, game type, mechanic, topic, or descriptive path segment.

An owner-bound identity is a specific candidate destination associated with an owner, publisher, organization, creator, provider, or verified semantic namespace.

Selecting a semantic continuation extends the discovery path.

Selecting an owner-bound identity commits the expression to a specific owner-qualified SIP identity.

### Discovery Subcategory Selection

If the user selects a semantic continuation such as:

lasca

then the active SIP string is extended in place:

@games.strategy.abstract.capture.leaping.columns.lasca

The expression remains discovery-oriented.

It does not yet represent a specific owner, publisher, or authoritative destination.

The user may continue typing:

@games.strategy.abstract.capture.leaping.columns.lasca.

and Semantic IntelliSense may then offer additional semantic continuations such as:

rules
online
history
variants
tournaments
strategy
tutorials

It may also continue to show matching owner-bound identities in a separate section.

### Owner-Bound Candidate Selection

If the user selects an owner-bound candidate such as:

StackWorks — Lasca

then the active SIP string is completed or rewritten as:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

This is a different kind of selection.

The user is no longer merely extending a semantic discovery path.

The user has selected a specific owner-qualified semantic identity.

At this point, the interface may:

- resolve the identity directly
- show the destination URL
- show trust and verification indicators
- allow the user to open the destination
- allow the user to save the identity as a semantic favorite
- allow the user to continue editing the SIP string manually

### Visual Grouping

Semantic IntelliSense should avoid presenting all suggestions as a flat list.

Instead, suggestions should be grouped by intent.

Possible groups include:

- Continue semantic discovery path
- Matching owner-bound identities
- Trusted or verified identities
- Recently used identities
- Semantic favorites
- Related aliases
- Broader or narrower concepts

This avoids confusing a semantic category with an identity owner.

For example:

lasca

and:

StackWorks — Lasca

should not appear as equivalent choices.

The first choice extends the semantic path.

The second choice binds the path to a specific owner-qualified identity.

### Keyboard and Mouse Behavior

SIP-aware interfaces may support both mouse and keyboard selection.

Typical behavior may include:

- Arrow keys move through suggestions
- Enter selects the highlighted suggestion
- Tab accepts the currently highlighted completion
- Escape closes the IntelliSense panel
- Typing more characters filters the suggestions
- Clicking a suggestion selects it directly

When a semantic continuation is selected, only the next path segment is inserted.

When an owner-bound identity is selected, the entire SIP string may be replaced with the canonical owner-qualified identity.

Example:

Before selection:

@games.strategy.abstract.capture.leaping.columns.

User selects semantic continuation:

lasca

After selection:

@games.strategy.abstract.capture.leaping.columns.lasca

But:

Before selection:

@games.strategy.abstract.capture.leaping.columns.

User selects owner-bound candidate:

StackWorks — Lasca

After selection:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

This difference should be intentional and visible to the user.

### Preview and Confirmation Behavior

For owner-bound candidates, the IntelliSense panel may show additional metadata before selection.

Example:

StackWorks — Lasca
@stackworks.games.strategy.abstract.capture.leaping.columns.lasca
Verified owner: StackWorks
Destination: https://stackworks.games/lasca
Trust level: Domain Verified
Resolution type: deterministic candidate

This allows the user to understand that selecting this item is not merely choosing another category.

It is choosing a specific semantic identity owned or published by a specific party.

For weakly verified or ambiguous candidates, the UI may display a warning, lower confidence score, or require confirmation before resolving.

### Core UX Rule

The IntelliSense panel should make this distinction clear:

Selecting a category continues exploration.

Selecting an owner-bound result commits identity.

This allows SIP to support natural semantic browsing without forcing the user to know the owner at the beginning of the expression.

It also allows SIP to preserve owner-qualified deterministic resolution once the user chooses a specific trusted candidate.

### Example Flow

User begins with:

@games.

Semantic IntelliSense suggests:

action  
strategy  
rpg  
adventure  
narrative  
puzzle  
casual  

User selects:

strategy

The expression becomes:

@games.strategy

User continues:

@games.strategy.

Semantic IntelliSense suggests:

abstract  
rts  
tbs  
grand  
tactical  
moba  
tower  

User selects:

abstract

The expression becomes:

@games.strategy.abstract

User continues:

@games.strategy.abstract.

Semantic IntelliSense suggests:

capture  
annihilation  
territory  
grid-control  
connection  
stacking  
3d-spatial  
mancala  
counting  

User selects:

capture

The expression becomes:

@games.strategy.abstract.capture

User continues:

@games.strategy.abstract.capture.

Semantic IntelliSense suggests:

displacement  
leaping  

User selects:

leaping

The expression becomes:

@games.strategy.abstract.capture.leaping

User continues:

@games.strategy.abstract.capture.leaping.

Semantic IntelliSense suggests:

columns  
checkers  
dama  
draughts  

User selects:

columns

The expression becomes:

@games.strategy.abstract.capture.leaping.columns

User continues:

@games.strategy.abstract.capture.leaping.columns.

Semantic IntelliSense suggests semantic continuations such as:

lasca  
damasca  
columns-draughts  

It may also suggest owner-bound identity candidates such as:

StackWorks — Lasca  
@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

StackWorks — Damasca  
@stackworks.games.strategy.abstract.capture.leaping.columns.damasca

If the user selects the plain semantic continuation:

lasca

then the expression becomes the unbound discovery path:

@games.strategy.abstract.capture.leaping.columns.lasca

If the user selects the owner-bound candidate:

StackWorks — Lasca

then the expression becomes the canonical owner-qualified identity:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

### Architectural Implication

This model preserves SIP’s anti-scarcity principle because broad roots such as:

@games

are not globally owned.

They remain semantic discovery spaces.

At the same time, SIP still supports deterministic identity resolution when a verified or trusted owner-qualified identity is selected, such as:

@stackworks.games.strategy.abstract.capture.leaping.columns.lasca

This allows SIP to support both:

- open semantic exploration
- specific owner-qualified identity resolution

without recreating DNS-style global namespace ownership at the root semantic level.


## Architectural Implications

Semantic IntelliSense reinforces that SIP is not merely a replacement for DNS naming.

Instead, SIP functions as:

- a semantic navigation architecture
- an AI-native semantic discovery layer
- a semantic knowledge routing system
- a contextual semantic memory system

This allows users and AI systems to collaboratively navigate semantic meaning rather than manually memorizing technical location identifiers.

## Relationship to Traditional URLs

Traditional URLs primarily require exact string knowledge and manual memorization.

Semantic IntelliSense instead supports:

- guided semantic discovery
- AI-assisted navigation
- contextual semantic exploration
- semantic graph traversal
- meaning-oriented interaction

This significantly improves usability, discoverability, and semantic clarity in large-scale AI-native information ecosystems.

---

# Semantic Path Search

SIP-aware interfaces may support a global semantic path search feature that allows users to search across the entire registered SIP identity space using one or more keywords.

Unlike Semantic IntelliSense, which guides users through the semantic hierarchy step by step, semantic path search allows users to query directly across all known SIP paths without knowing the starting category.

## Search-Based Navigation

In addition to guided hierarchical IntelliSense, users may wish to navigate directly to a known or partially remembered SIP identity using keyword recall rather than step-by-step category traversal.

Semantic path search allows users to type one or more keywords and immediately see a ranked list of matching SIP identities drawn from across:

- discovery paths in the semantic tree
- owner-bound canonical identities
- shortcut aliases and expansions
- personal shortcut bindings (within the user's trusted context)

Example:

User types:

lasca

Matching results may include:

@games.strategy.abstract.capture.leaping.columns.lasca  (discovery)  
@stackworks.games.strategy.abstract.capture.leaping.columns.lasca  (owner-bound)  
@stackworks.games.lasca  (shortcut)

The user may select any matching result to load it immediately as the active SIP expression.

## Boolean Keyword Expressions

Semantic path search should support boolean keyword expressions to allow precise multi-keyword filtering across large semantic identity spaces.

The query language is intentionally simple and familiar, using operators that do not conflict with SIP path syntax.

### OR Expressions

Multiple keywords separated by spaces, commas, or the `|` pipe operator return results matching any one of the keywords.

The following expressions are equivalent:

    chess | checkers
    chess, checkers
    chess checkers

All three return SIP identities whose path or label contains either chess or checkers.

### AND Expressions

Multiple keywords joined by `&` or `+` return only results matching all specified keywords.

The following expressions are equivalent:

    chess & columns
    chess + columns

Both return only SIP identities containing both chess and columns.

### NOT Expressions

A keyword prefixed with `!` excludes results that match that keyword.

Example:

    chess !checkers

Returns SIP identities containing chess but not checkers.

NOT may also be applied to grouped sub-expressions:

    chess !(checkers | draughts)

Returns SIP identities containing chess but not checkers and not draughts.

NOT binds to the immediately following term or group. A space before `!` is treated as an implicit AND, so `chess !checkers` is equivalent to `chess & !checkers`.

### Grouped Expressions

Parentheses allow combining OR and AND logic within the same query.

Example:

    (chess | checkers) & columns
    (chess | checkers) + columns

Both expressions return SIP identities that contain columns and at least one of chess or checkers.

### Operator Precedence

AND (`&`, `+`) binds more tightly than OR (`|`, `,`, space), following standard boolean algebra precedence.

Example:

    chess | checkers & columns

is interpreted as:

    chess | (checkers & columns)

Parentheses may be used to override default precedence explicitly.

## Synonym-Aware Matching

Semantic path search automatically expands query terms to their registered synonyms before matching.

If a keyword in the search query is a known synonym for a segment that appears in a SIP string, that SIP string will be returned as a match even though the literal keyword does not appear in it.

Example:

The segment `stacks` is registered as a synonym for `columns` within the displacement capture context.

A search for:

    chess + stacks

will therefore match:

    @games.strategy.abstract.capture.displacement.columns.chess

because `stacks` expands to its synonym `columns`, and `columns` is present in the SIP path.

Synonym expansion applies per query term. Each term in a boolean expression is independently expanded before the full expression is evaluated against the candidate SIP string.

Synonyms are context-defined. A synonym relationship established within one semantic branch does not automatically apply to unrelated branches where the same word carries a different meaning.

This allows search to behave naturally with the semantic vocabulary users already know, without requiring them to memorize which segment wording is canonical in a given part of the SIP hierarchy.

## Search Scope

Semantic path search may be applied across:

- **Discovery paths** — all registered semantic path segments in the SIP discovery tree, including intermediate nodes and leaf nodes
- **Owner-bound identities** — canonical owner-qualified SIP strings published by verified owners
- **Shortcut aliases** — compact semantic shortcut expressions and their expansion targets
- **Personal shortcuts** — user-saved shortcut bindings, included only within the user's trusted resolver context

Search matching may be applied to both the SIP path string and any associated human-readable label or description.

## Selecting Search Results

When a user selects a result from the search panel, the selected SIP string becomes the active expression in the semantic input field.

The interface then transitions to normal guided navigation mode with the selected SIP as the starting point.

This allows users to combine keyword-driven initial discovery with guided IntelliSense-based refinement.

For example:

1. User searches for: lasca
2. User selects: @games.strategy.abstract.capture.leaping.columns.lasca
3. Active SIP field is populated with the selected path
4. Semantic IntelliSense may then offer continuations or owner-bound candidates from that point

## Relationship to Semantic IntelliSense

Semantic path search and Semantic IntelliSense serve complementary navigation purposes.

Semantic IntelliSense is optimized for:

- step-by-step semantic exploration
- guided hierarchical navigation
- discovering semantic structure progressively
- navigating from a known starting category

Semantic path search is optimized for:

- finding a known or partially remembered SIP path by keyword
- querying across the entire semantic corpus at once
- combining multiple keyword constraints to narrow a large result set
- bypassing the semantic hierarchy when the user already has a keyword in mind

Together, these navigation modes allow SIP-aware interfaces to serve both exploratory and recall-driven user intent without requiring users to begin navigation from the root of the semantic tree.

## AI Integration

Semantic path search may also serve as an AI-mediated interface layer.

An AI assistant may translate natural language intent into a boolean search expression.

Example:

User says:

Find abstract board games that involve stacking or columns mechanics.

AI-generated search expression:

    (stacking | columns) & abstract

The search engine may return matching owner-bound identities, discovery paths, and shortcut aliases.

The AI may then rank, explain, and present these results contextually.

## Architectural Implications

Semantic path search further reinforces that SIP is:

- **queryable** — users and AI systems may retrieve SIP identities using structured keyword expressions
- **AI-navigable** — boolean queries may be automatically generated from natural language intent
- **context-aware** — personal shortcuts are included only within the user's trusted resolver context
- **federated** — search results may aggregate identity records across multiple Semantic Identity Providers
- **meaning-oriented** — search matches against semantic labels and human-readable descriptions as well as raw path strings

---