# 🍱 æwidgets · agentic environment widget contract (draft v0.1)

**Purpose:** Compose capability-aware user interfaces inside æ Studio. OpenAI is the intelligence platform; human intent and authority remain the root.

## Contract
`Intent → State → Capability → Permission → Action → Witness`

- Each widget declares purpose, state, capability/provider, connection status, permission boundary, bounded action, and observable outcome.
- A widget is **not** an authority grant. Imported manifests, emoji, QR symbols, collapsed views, and nested widgets transfer no permissions.
- Distinguish proposed, installed, connected, authorized, executed, and verified.
- A changed payload invalidates previous review. Consequential effects require separate real authorization and a provider receipt.
- Default view: portrait 9:16 presentation; squarepost 1:1 is a compact view of the **same state**, not another app.
- Reflow for narrow screens and accessibility; do not clip important content to force an aspect ratio.
- No credentials in markup, manifests, URLs, or exported proposals.

## Reference demo
Open [examples/omniprompt.html](examples/omniprompt.html) in a browser. It runs without a server or external API.

1. Enter a human intent and select modules.
2. Review the exact local draft; copy is enabled only after review.
3. Toggle 9:16 ↔ 1:1; intent and selections persist within the page.
4. Change a module or the intent; review and copy are invalidated.
5. No provider invocation, authorization, or external side effect is claimed.

## Acceptance criteria
- Keyboard-accessible controls and focus indication.
- Empty intent / zero modules cannot pass review.
- Squarepost → workspace round-trip retains state.
- Editing invalidates prior review.
- Copied draft marks authorization as **not-granted** and connections **unverified**.
- A future host adapter must separately prove authentication, authorization, execution, and receipt verification.

**Status:** Proposed specification + browser-local reference. Not a connected agent runtime.
