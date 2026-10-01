# Null_nx

Standalone, offline HTML tools for fullerene geometry, Millennium-problem demonstrations, and a sharded compute engine built around the NullNX byte-stream format. No installs, no libraries, no network.

Created by Joseph La Follette.

## Files

| File | What it is |
|---|---|
| `null_nx.html` | Six-tab dashboard: C60 cage, Riemann critical line, other Millennium problems, Torsus, Remainders, Benchmark |
| `nullnx_engine.html` | NullNX stream decoder and Hamming-wrap demo, built from the Capability Deck's opcodes |
| `nullnx_shards.html` | 60-shard compute engine (one shard per C60 vertex) on Web Workers, plus a scientific calculator with wave plots, a recordable tape, and `nx()` / `unnx()` commands |
| `run.sh` | Linux launcher: opens `null_nx.html` in your browser, or serves it with Python 3 if none is found |

## Run it

Open any `.html` file in a modern browser. On Linux (including a ChromeOS Linux partition):

```sh
sh run.sh
```

## What each part really computes

- **C60 cage:** exact truncated-icosahedron geometry (60 vertices, 90 edges, 32 faces).
- **Riemann critical line:** Hardy Z function, with zeros checked against published values.
- **Other Millennium problems:** small demonstrations (random 3-SAT, 1D Burgers, 2D U(1) lattice gauge theory, curve-shortening flow). They illustrate ideas. They do not solve or attack the actual problems.
- **Remainders:** the Chinese remainder theorem on 252 = 4 × 9 × 7.
- **Shard engine:** counts primes and zeta zeros in 60 parallel shards. Results are checked against known values (for example 5,761,455 primes below 10^8 and 138,069 zeros up to t = 10^5).
- **NullNX engine:** follows the deck's opcodes; where the deck is silent, the rules used are listed on the page.

## Limits

- All compute runs locally on your CPU cores. A standalone page cannot reach outside machines, remote clusters, or observatory time sources.
- Browser timers are deliberately coarse (tens of microseconds or worse).
- Speed depends on your device and browser.

## License

Copyright (C) 2024 Joseph La Follette

This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License along with this program. If not, see <https://www.gnu.org/licenses/>.

If you run a modified version of this software as a network service, AGPL section 13 requires you to offer its source to the users of that service.

SPDX-License-Identifier: AGPL-3.0-or-later
