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

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
