# tiny-chess-engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Dimzy14/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Dimzy14/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A complete chess engine in 4,019 bytes of Python: 0x88 board, iterative-deepening alpha-beta (PVS) with quiescence, a transposition table, check extensions, and a tapered material + piece-square evaluation. Deterministic — a fixed node budget (45k/30k/18k by game ply), never a clock. On the kit's three practice instances it scored Elo 1654 / 1279 / 1279 (mean 1404) against the house ladder, above the 1,154 qualification floor.

## Run it

The harness runs the engine against the game environment; it reads `MAKEFUN_ENV_URL` and plays over HTTP:

```sh
MAKEFUN_ENV_URL=http://localhost:PORT python3 -P -s main.py
```
