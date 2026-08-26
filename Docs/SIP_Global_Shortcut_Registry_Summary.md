## Global SIP Shortcut Registry

A **global SIP shortcut** is a short, public, owner-neutral alias — such as `@games/lasca` or `@games/chess`
— that resolves to a semantic discovery path rather than to any private owner's destination. These shortcuts
are governed by a **Global SIP Shortcut Registry** managed by namespace stewards (e.g. the *SIP Games
Namespace Registry* for `@games`). Acceptance requires a formal process: proposal, public review, conflict
check, semantic path assignment, and cryptographic signing. First-come, first-served registration does **not**
apply — no individual or company can claim ownership over a public semantic concept simply by registering
first. Each accepted entry is a signed JSON record identifying the shortcut, the discovery path it expands to,
the steward, and a version stamp.

Global shortcuts sit in the second of three shortcut tiers. `@games/lasca` is a **global semantic shortcut**
that expands to `@games.strategy.abstract.capture.leaping.columns.lasca` and returns ranked owner candidates
— any publisher can appear there. `@stackworks/lasca` is an **owner-brand shortcut** controlled by StackWorks
that resolves deterministically to their specific record. `@my/lasca` is a **local personal shortcut** stored
in the user's trusted context only. This layering ensures that short, memorable paths remain a shared public
vocabulary while owner identity and user preferences each have their own distinct, non-competing layer.

Global shortcuts and JSON-LD-based SIP identity assertions are complementary adoption paths. See the [JSON-LD Integration Architecture annex](SIP_JSON-LD_Integration_Architecture.md).