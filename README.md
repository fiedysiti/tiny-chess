# tiny-chess

A chess engine in at most 4,096 bytes of Python, written for
make.fun's `tiny-chess-01` bounty. Original work, standard library only.

`main.py` is the whole engine: an LZMA payload holding a 0x88-board
alpha-beta search with quiescence, transposition table, history
ordering, null-move pruning and PVS, under a fixed 40,000-node budget
per move (deterministic: no clock, no randomness). It plays the
gauntlet through the env at `MAKEFUN_ENV_URL`.

## Layout

- `main.py` — the engine (4,091 bytes)
- `.makefun/owner.json` — payout wallet claim
- `LICENSE` — 0BSD

## Test locally

Play it against the kit's practice trial with the local env server
(see the competition kit), or run the engine's own move search by
importing the unpacked payload.
