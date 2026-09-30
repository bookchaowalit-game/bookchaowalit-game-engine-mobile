# bookchaowalit-game-engine-mobile

Planned small, shared game-runtime layer for the `bookchaowalit-game` mobile
games: game loop, input, randomness and scene state, so each game only has
to implement its rules and drawing.

## Status

**Empty / planning.** This repository has no code yet. It is not a
general-purpose engine and is not intended to compete with Unity, Godot or
similar; it only covers what the arcade's short 2D games need.

## Intended scope

- Fixed-timestep game loop that pauses when the app is backgrounded.
- Input mapping from touch gestures (tap, swipe, drag) to game actions.
- Seeded random number generator so runs are reproducible in tests.
- Minimal scene/state machine (title, playing, paused, won, lost).
- Pure logic with no UI framework dependency, so it is unit-testable.

Out of scope: physics engines, 3D, networking, asset pipelines, ads or
analytics.

## Related repositories

| Repository | Role |
|---|---|
| `bookchaowalit-arcade-games-mobile` | Planned first consumer of this layer |
| `bookchaowalit-game-collection-frontend` | Web arcade; its per-game rule modules show the shape this layer must support |

## Next step

See [`docs/UPGRADE-PLAN.md`](docs/UPGRADE-PLAN.md).
