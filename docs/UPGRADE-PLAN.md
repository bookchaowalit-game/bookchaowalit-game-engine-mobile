# Upgrade plan

## Current state

**Score: 1/10.** Initial commit: README, `.gitignore`, this plan. No code,
no CI (there is nothing to check yet).

## Proposed scaffold (decision needed)

A framework-free **TypeScript** package, so it works with the Expo/React
Native app proposed in `bookchaowalit-arcade-games-mobile` and with the web
arcade. If the mobile games end up in Flutter instead, this becomes a Dart
package with the same API.

```
src/loop.ts        # fixed-timestep loop: update(dt) / render(alpha)
src/input.ts       # gesture -> action mapping
src/random.ts      # seeded PRNG (e.g. mulberry32)
src/scene.ts       # small state machine for game phases
tests/             # Vitest unit tests, one file per module
.github/workflows/ci.yml  # npm ci, lint, typecheck, test, build
```

## Backlog

### P0
- Confirm TypeScript vs Dart together with the arcade app decision.
- Extract only what the first game (Signal Shift in the arcade app) needs;
  do not build modules ahead of a consumer.
- Add CI and tests from the first commit that contains code.

### P1
- Seeded RNG and loop with deterministic tests (same seed, same run).
- Background/foreground pause handling documented per platform.

### P2
- Publish as a private package or consume via workspace/monorepo, decided
  once there are two consumers.

## Done in this pass (2026-09-30)
- Initial commit with an honest README (planning only), `.gitignore`, and
  this plan.
