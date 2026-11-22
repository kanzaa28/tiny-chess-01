# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/kanzaa28/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/kanzaa28/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A deterministic chess engine in a single 4 KB Python file (stdlib only). 0x88 board, negamax alpha-beta search with a transposition table (Zobrist hashing), principal-variation search with late-move reductions, check extensions and iterative deepening under a fixed node budget (160k/130k/100k nodes by game phase — never the clock). Quiescence search covers captures, promotion pushes and check evasions. Evaluation is incremental piece-square tables plus bishop-pair and passed-pawn terms. Local practice gauntlet (6 games vs anchored house engines from Elo 855 to 1596): this exact build scored Elo 1364 (2 wins, 3 draws, 1 loss), above the 1154 qualification mark; slowest move 4.4 s of the 10 s limit.

## Run it

```sh
# with the make.fun trial environment serving games on a local port:
MAKEFUN_ENV_URL=http://127.0.0.1:PORT python3 main.py
```

`main.py` is the packed entry (LZMA-compressed source + unpacker, produced by the kit's `makefun compress`); it unpacks itself in memory and plays every game the environment offers.

---
<sub>Entered on [make.fun](https://make.fun/?ref=bcc5x9p5&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
