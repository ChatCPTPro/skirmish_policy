# skirmish_policy

Privacy policy for the Skirmish iPhone/iPad app, served by GitHub Pages at
**https://chatcptpro.github.io/skirmish_policy/**.

That URL is set as the app's privacy policy URL in TestFlight's test
information (`skirmish-ios/scripts/beta-external.mjs` → `PRIVACY_URL`).
Apple requires one for external testing.

This repo is public on purpose, because Pages needs a publicly reachable
page. The Skirmish game hosts sit behind the Cloudflare IP allowlist, so the
policy can't live there. Edit `index.html`, bump the "Last updated" date,
and push. Pages redeploys within a minute or two.

What the policy claims is based on the code as of 2026-09-25:
- Chat: last 10 messages per room, 100 characters each (`skirmish/src/index.js`).
- AI-game archive: moves only, no chat, no identity (`skirmish/skirmish-ai/game-archive-plan.md` §2).
- The AI agent never reads player chat (`skirmish/skirmish-ai/agent/agent.mjs`).
- On the device: room code + seat token in the Keychain (`skirmish-ios/Skirmish/Session/SessionStore.swift`).

If any of those change, update the policy.
