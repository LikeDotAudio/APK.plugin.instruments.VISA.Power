# SDK — INSTRUMENT.Power

Every Power model this library drives, and how to drive it. Each model answers the same five verbs over HTTP (its own port), WebSocket, a Unix socket and the bus; one page per model below lists its routes and every command.

← [Manual and Artifacts](INDEX.md)

| Verb | What it does |
|---|---|
| `get` | reads one value |
| `set` | writes one value |
| `nab` | reads more than one thing (observation, telemetry) |
| `rig` | configures several arguments at once |
| `do` | executes an action; takes no value |

| Model | Maker | get | set | nab | rig | do | Port |
|---|---|---:|---:|---:|---:|---:|---:|
| [6032A](SDK/6032A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15500 |
| [66000A](SDK/66000A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15501 |
| [66101A](SDK/66101A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15502 |
| [66102A](SDK/66102A.md) | HP / Agilent / Keysight | 64 | 148 | 67 | 4 | 61 | 15503 |
| [66103A](SDK/66103A.md) | HP / Agilent / Keysight | 64 | 148 | 67 | 4 | 61 | 15504 |
| [66104A](SDK/66104A.md) | HP / Agilent / Keysight | 64 | 149 | 67 | 4 | 62 | 15505 |
| [6632B](SDK/6632B.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15506 |
| [DP711](SDK/DP711.md) | Rigol | 64 | 149 | 66 | 2 | 61 | 15507 |
| [DP832](SDK/DP832.md) | Rigol | 64 | 149 | 66 | 2 | 61 | 15508 |
| [DP832A](SDK/DP832A.md) | Rigol | 64 | 149 | 66 | 2 | 61 | 15509 |
| [E3610A](SDK/E3610A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15510 |
| [E3615A](SDK/E3615A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15511 |
| [E3620A](SDK/E3620A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15512 |
| [E36300 Series](SDK/E36300%20Series.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15513 |
| [E3630A](SDK/E3630A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15514 |
| [E3631A](SDK/E3631A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15515 |
| [E3632A](SDK/E3632A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15516 |
| [E3633A](SDK/E3633A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15517 |
| [E3634A](SDK/E3634A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15518 |
| [E3640A](SDK/E3640A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15519 |
| [E3641A](SDK/E3641A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15520 |
| [E3642A](SDK/E3642A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15521 |
| [E3643A](SDK/E3643A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15522 |
| [E3644A](SDK/E3644A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15523 |
| [E3645A](SDK/E3645A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15524 |
| [E3646A](SDK/E3646A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15525 |
| [E3647A](SDK/E3647A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15526 |
| [E3648A](SDK/E3648A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15527 |
| [E3649A](SDK/E3649A.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15528 |
| [HMP2020](SDK/HMP2020.md) | Rohde & Schwarz | 64 | 149 | 66 | 2 | 61 | 15529 |
| [HMP4040](SDK/HMP4040.md) | Rohde & Schwarz | 64 | 149 | 66 | 2 | 61 | 15530 |
| [N6700C](SDK/N6700C.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15531 |
| [N6701C](SDK/N6701C.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15532 |
| [N6702C](SDK/N6702C.md) | HP / Agilent / Keysight | 64 | 149 | 66 | 2 | 61 | 15533 |
| [NGL200](SDK/NGL200.md) | Rohde & Schwarz | 64 | 149 | 66 | 2 | 61 | 15534 |
| [NGM200](SDK/NGM200.md) | Rohde & Schwarz | 64 | 149 | 66 | 2 | 61 | 15535 |
