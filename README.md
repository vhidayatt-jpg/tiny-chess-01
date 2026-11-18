# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/vhidayatt-jpg/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/vhidayatt-jpg/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine for the make.fun tiny-chess-01 competition: an
adapted fork of sunfish, rebuilt here with its own board, search and
packing. `main.py` is the whole engine: at most 4,096 bytes as committed,
Python 3.13, standard library only. It reads, imports or execs no other
file in the repository. A `main.py` that unpacks and execs a compressed
payload (`lzma`) is fine; the payload and the unpacker are both part of its
4,096 bytes. Search runs to a fixed node budget, never a clock.

## Credit

This entry is a fork of [sunfish](https://github.com/thomasahle/sunfish)
by Thomas Ahle and contributors, licensed GPL-3.0-only — specifically its
4 KB entry (`nnue_4k/pst_entry.py`, commit e396948). The piece-square
tables and the MTD(f) search design come from sunfish; the board
representation, move generation, transposition table, quiescence and
packing in this repository were rewritten here for this competition. See
`LICENSE` (SPDX-License-Identifier: GPL-3.0-only).

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:18100 python3 -P -s main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
