# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/IlhamEl777/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/IlhamEl777/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine squeezed into 4 KB of Python: negamax alpha-beta search with
iterative deepening under a fixed node budget, quiescence over captures,
promotions and check evasions, a transposition table, null-move pruning,
late-move reductions, and a tapered piece-square evaluation. No clock and no
randomness: the same position always gets the same move.

## Run it

```sh
MAKEFUN_ENV_URL=<env url> python3 main.py
```

It plays every game the env serves, one after another, until the env answers
`{"status": "done"}`.

## Verification

The move generator is perft-validated against the standard test suites
(start position, Kiwipete, and the en-passant-pin and promotion positions)
with exact node counts to depth 4. `main.py` ships the engine as an
lzma-compressed, base85-encoded payload with its unpacker (the readable
source does not fit the 4 KB cap on its own); decompressing the payload
reproduces the developed source byte for byte. In local practice against
the kit's gauntlet the engine plays at a fixed 40,000 nodes per move
(about 20,000–28,000 nodes/second in this environment, roughly
1.5–2 seconds per move, far under the 10-second limit).

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
