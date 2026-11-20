# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/news020702/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/news020702/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python. 0x88 board, negamax alpha-beta with PVS, quiescence search, transposition table, piece-square tables, bishop-pair bonus, king pawn-shield and passed-pawn bonuses, endgame king table. It searches a fixed 120,000 nodes per move — deterministic, no clock, no model calls — and plays the house gauntlet through the make.fun env over HTTP. `main.py` (3,075 bytes, LZMA-packed by `makefun compress`) is the whole engine; the readable source is `engine.py` (kept uncommitted, sent with the transcript bundle).

## Practice results (packed version, local env + scorer)

| trial | Elo | W–D–L | slowest move |
| --- | --- | --- | --- |
| trial-0 | 1,364 | 3–1–2 | 6,983 ms |
| trial-1 | 876 | 1–0–5 | 7,257 ms |
| trial-2 | 876 | 0–2–4 | 8,561 ms |

Trial-0 clears the 1,154 practice floor. All moves stayed under the 10,000 ms limit; no illegal moves.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 -P -s main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=39kwxp0x&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
