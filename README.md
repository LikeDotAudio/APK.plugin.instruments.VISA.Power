# INSTRUMENT.Power

**Wiki:** [Documentation/README.md](Documentation/README.md) — principles, architecture, delivery, and the [SDK](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK.md).

The **Power** instruments of the APK.audio bench, as one thing: 36 models, their command tables and the family's panel. DC power supplies: they source, and meter what they source.

| | |
|---|---|
| **Is** | **source** — puts something out — a stimulus, a supply or a load<br>**metering** — measures — its readings are numbers with units |
| **Inputs** | each model's BIM part: /api/bim/parts?full=1&id=<part> — ports where side is "input" and domain is not "power" |
| **Recipe** | none — data, not a container: read in place by the stacks that bake `INSTRUMENTS` |
| **Source** | this repository (https://github.com/LikeDotAudio/APK.plugin.instruments.VISA.Power.git), a submodule of [APK.plugin.instruments.VISA](https://github.com/LikeDotAudio/APK.plugin.instruments.VISA) at `INSTRUMENT.Power/` |
| **Family name** | `Power` — the device type, the topic segment and the `manifest.json` key; the `INSTRUMENT.` prefix belongs to the folder only |

## Models

| Model | Maker | What | Commands | Table | API |
|---|---|---|---:|:---:|---|
| [6032A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/6032A.md) | HP / Agilent / Keysight | 1000W Autoranging (60V/50A) | 188 |  | :15500 |
| [66000A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/66000A.md) | HP / Agilent / Keysight | Modular System Mainframe (8 Slots) | 188 |  | :15501 |
| [66101A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/66101A.md) | HP / Agilent / Keysight | Module 8V / 16A (128W) | 188 | ✅ | :15502 |
| [66102A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/66102A.md) | HP / Agilent / Keysight | Module 20V / 7.5A (150W) | 190 | ✅ | :15503 |
| [66103A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/66103A.md) | HP / Agilent / Keysight | Module 35V / 4.5A (150W) | 190 | ✅ | :15504 |
| [66104A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/66104A.md) | HP / Agilent / Keysight | Module 60V / 2.5A (150W) | 193 | ✅ | :15505 |
| [6632B](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/6632B.md) | HP / Agilent / Keysight | 100W System Supply (20V/5A) | 188 |  | :15506 |
| [DP711](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/DP711.md) | Rigol | Single Output 30V/5A | 188 |  | :15507 |
| [DP832](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/DP832.md) | Rigol | Triple Output (30V/3A x2, 5V/3A) | 188 |  | :15508 |
| [DP832A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/DP832A.md) | Rigol | Triple Output (High Accuracy Color) | 188 |  | :15509 |
| [E3610A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3610A.md) | HP / Agilent / Keysight | 30W Bench (8V/3A or 15V/2A) | 188 |  | :15510 |
| [E3615A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3615A.md) | HP / Agilent / Keysight | 60W Bench (20V/3A) | 188 |  | :15511 |
| [E3620A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3620A.md) | HP / Agilent / Keysight | Dual Output 50W (25V/1A x2) | 188 |  | :15512 |
| [E36300 Series](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E36300%20Series.md) | HP / Agilent / Keysight | Triple Output Low Noise (Modern E3631A) | 188 |  | :15513 |
| [E3630A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3630A.md) | HP / Agilent / Keysight | Triple Output 35W (6V, +20V, -20V) | 188 |  | :15514 |
| [E3631A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3631A.md) | HP / Agilent / Keysight | Triple Output 80W Programmable | 188 |  | :15515 |
| [E3632A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3632A.md) | HP / Agilent / Keysight | 120W Programmable (15V/7A or 30V/4A) | 188 |  | :15516 |
| [E3633A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3633A.md) | HP / Agilent / Keysight | 200W Programmable (8V/20A or 20V/10A) | 188 |  | :15517 |
| [E3634A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3634A.md) | HP / Agilent / Keysight | 200W Programmable (25V/7A or 50V/4A) | 188 |  | :15518 |
| [E3640A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3640A.md) | HP / Agilent / Keysight | 30W Programmable (8V/3A or 20V/1.5A) | 188 |  | :15519 |
| [E3641A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3641A.md) | HP / Agilent / Keysight | 30W Programmable (35V/0.8A or 60V/0.5A) | 188 |  | :15520 |
| [E3642A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3642A.md) | HP / Agilent / Keysight | 50W Programmable (8V/5A or 20V/2.5A) | 188 |  | :15521 |
| [E3643A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3643A.md) | HP / Agilent / Keysight | 50W Programmable (35V/1.4A or 60V/0.8A) | 188 |  | :15522 |
| [E3644A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3644A.md) | HP / Agilent / Keysight | 80W Programmable (8V/8A or 20V/4A) | 188 |  | :15523 |
| [E3645A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3645A.md) | HP / Agilent / Keysight | 80W Programmable (35V/2.2A or 60V/1.3A) | 188 |  | :15524 |
| [E3646A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3646A.md) | HP / Agilent / Keysight | Dual 60W Programmable | 188 |  | :15525 |
| [E3647A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3647A.md) | HP / Agilent / Keysight | Dual 60W Programmable | 188 |  | :15526 |
| [E3648A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3648A.md) | HP / Agilent / Keysight | Dual 100W Programmable (8V/5A or 20V/2.5A) | 188 |  | :15527 |
| [E3649A](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/E3649A.md) | HP / Agilent / Keysight | Dual 100W Programmable (35V/1.4A or 60V/0.8A) | 188 |  | :15528 |
| [HMP2020](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/HMP2020.md) | Rohde & Schwarz | Dual Output High Perf (188W) | 188 |  | :15529 |
| [HMP4040](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/HMP4040.md) | Rohde & Schwarz | Quad Output High Perf (384W) | 188 |  | :15530 |
| [N6700C](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/N6700C.md) | HP / Agilent / Keysight | Low-Profile Modular Mainframe (400W) | 188 |  | :15531 |
| [N6701C](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/N6701C.md) | HP / Agilent / Keysight | Low-Profile Modular Mainframe (600W) | 188 |  | :15532 |
| [N6702C](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/N6702C.md) | HP / Agilent / Keysight | Low-Profile Modular Mainframe (1200W) | 188 |  | :15533 |
| [NGL200](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/NGL200.md) | Rohde & Schwarz | Precision Power Supply (Linear) | 188 |  | :15534 |
| [NGM200](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SDK/NGM200.md) | Rohde & Schwarz | Precision Power Supply (High Speed) | 188 |  | :15535 |

## Layout

```
INSTRUMENT.Power/
  thing.json            what this thing is on the bench (authored)
  gui/                  the family panel, stamped once per discovered box
    Power.cad.json
    Power.dxf
    Power.json
    Power.probe.json
    Power_N.json
  <Model>/              <Model>.komand (the command table), <Model>.gui,
                        <Model>.api.json (generated), commands_tree.md, SOURCES.md
  Documentation/        the wiki; SDK/ is generated by _komand/family_sdk_docs.py
```

Generated by `_komand/family_sdk_docs.py` in the parent repository; edit `thing.json` or the
models, not this page.

<!-- wiki:smoke -->
**Smoke test** — ❌ FAIL 0/1 since 2026-11-04 20:50 EST — [results](Documentation/%F0%9F%A7%A9Manual%20and%20Artifacts/SMOKE.md)
<!-- /wiki:smoke -->
