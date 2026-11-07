# Sources — 66104A.komand

Every change to this table that a vendor manual confirms, with where the manual says it (AUDIO.komand `check-tables --strict` research, 2026-10-31). A finding no manual confirmed is listed under *Not confirmed* with what was searched, and the table is left as it was.

## Programming Guide for HP Series 66lxxA MPS Power Modules (HP Part No. 5959-3362)

September 1997 — Chapter 3, Language Dictionary; it states the commands work the same in every 6610xA module — <https://xdevs.com/doc/HP_Agilent_Keysight/661xxA_programming.pdf>

| Command | Change | Manual |
|---|---|---|
| `set/Set_Output_Dfi_Source` | arg = `{"kind": "enum", "values": ["LINK"], "default": "LINK"}` | OUTP:DFI:SOUR, p. 40 — Parameters LINK — "The only available source is LINK" |
| `set/Set_Output_Relay_Polarity` | arg = `{"kind": "enum", "values": ["NORM", "REV"], "default": "NORM"}` | OUTP:REL:POL, p. 41 — Parameters NORMal | REVerse, *RST NORM |
| `set/Set_Output_Ttltrg_Source` | arg = `{"kind": "enum", "values": ["BUS", "EXT", "LINK", "HOLD"], "default": "BUS"}` | OUTP:TTLT:SOUR, p. 42 — Parameters BUS | EXTernal | LINK | HOLD, *RST BUS |
| `set/Set_Source_Current_Mode` | arg = `{"kind": "enum", "values": ["FIX", "LIST"], "default": "FIX"}` | CURR:MODE, p. 35 — Parameters FIXed | LIST, *RST FIX |
| `set/Set_Source_Voltage_Mode` | arg = `{"kind": "enum", "values": ["FIX", "LIST"], "default": "FIX"}` | VOLT:MODE, p. 48 — Parameters FIXed | LIST, *RST FIX |
| `set/Set_Trigger_Source` | arg = `{"kind": "enum", "values": ["BUS", "EXT", "HOLD", "LINK", "TTLT"], "default": "BUS"}` | TRIG:SOUR, p. 47 — TRIGger[:STARt]:SOURce Parameters BUS | EXT | HOLD | LINK | TTLT, *RST BUS |
| `set/Set_Trigger_Start_Source` | arg = `{"kind": "enum", "values": ["BUS", "EXT", "HOLD", "LINK", "TTLT"], "default": "BUS"}` | TRIG:SOUR, p. 47 — the same node, TRIGger[:STARt]:SOURce |

### Not confirmed (left as is)

- `set/Set_Status_Operation` — searched: 5959-3362 Status subsystem pp. 43–44: STATus:OPERation[:EVENt]? is query-only and the settable registers are STAT:OPER:ENAB/NTR/PTR <NRf> (0–32727); no `STAT:OPER <value>` set command exists, so there is no choice list to give it. Removing or re-pointing the entry is the owner's call (the commands floor)
- `set/Set_Voltage_Alc_Source` — searched: 5959-3362 VOLT:SENS:SOUR?, p. 49: the remote-sense switch is READ ("This command reads the state…"), query-only, returns EXTernal | INTernal; VOLT:ALC:SOUR is its SCPI alias. No set form, so no settable choice list
- `set/Set_Voltage_Sense_Source` — searched: as Set_Voltage_Alc_Source: query-only [SOURce]:VOLTage:SENSe:SOURce?, p. 49

## Retired (owner decision, 2026-10-31)

The manual shows these commands do not exist. Each entry stays in the table with `"retired": true` and its citation in `retired_because`; KOMAND never sends it, check-tables skips it, and it still counts toward the commands floor.

- `set/Set_Status_Operation` — HP 66lxxA MPS Programming Guide 5959-3362 (https://xdevs.com/doc/HP_Agilent_Keysight/661xxA_programming.pdf) pp. 43-44: STATus:OPERation[:EVENt]? is query-only; only :ENABle/:NTR/:PTR take a value — there is no settable STAT:OPER
- `set/Set_Voltage_Alc_Source` — HP 66lxxA MPS Programming Guide 5959-3362 (https://xdevs.com/doc/HP_Agilent_Keysight/661xxA_programming.pdf) p. 49: VOLT:SENS:SOUR? (alias VOLT:ALC:SOUR?) reads the rear sense switch; query-only, no set form
- `set/Set_Voltage_Sense_Source` — HP 66lxxA MPS Programming Guide 5959-3362 (https://xdevs.com/doc/HP_Agilent_Keysight/661xxA_programming.pdf) p. 49: [SOURce]:VOLTage:SENSe:SOURce? is query-only, no set form

## Link, DFI and relay rows — GUI certificate on the 66102A Dev730-1 (2026-11-06)

The certificate failed `Get_Output_Ttltrg_Link` ("SDK says BOOL, the unit answered "OFF"") and `Get_Output_Dfi_Link` ("SDK says NR3, the unit answered "SUM3""). The same manual (5959-3362) and the unit at gpib7,30,1 agree on these rows:

| Command | Change | Manual · unit |
|---|---|---|
| `nab/Get_Output_Ttltrg_Link` | returns `STR` (was BOOL) | OUTP:TTLT:LINK, p. 42, Table 3-1 · answers `"OFF"` |
| `nab/Get_Output_Dfi_Link` | returns `STR` (was NR3) | OUTP:DFI:LINK, p. 40, Table 3-1 · answers `"SUM3"` |
| `nab/Get_Trigger_Link`, `nab/Get_Trigger_Start_Link` | returns `STR` (was BOOL / CRD) | TRIG[:STAR]:LINK, p. 47 · answers `"OFF"` |
| `nab/Get_Output_Dfi_Source` | returns `CRD` (was NR3) | OUTP:DFI:SOUR, p. 40 · answers `LINK` |
| `nab/Get_Output_Dfi_Status` | returns `BOOL` (was NR3) | OUTP:DFI[:STAT], p. 39 · answers `0` |
| `nab/Get_Output_Relay` | returns `BOOL` (was NR1) | OUTP:REL[:STAT]?, p. 41 · `-241 "Hardware missing"` (no relay option) |
| `nab/Get_Output_Relay_Polarity` | returns `CRD` (was NR1) | OUTP:REL:POL?, p. 41 — NORM \| REV |
| `set/Set_Output_Ttltrg_Link`, `set/Set_Trigger_Link`, `set/Set_Trigger_Start_Link` | `… "<value>"`, enum of Table 3-1's 15 (was bool OFF/ON), default OFF | string data: `OUTP:TTLT:LINK OFF` is `-148 "Character data not allowed"`, `"OFF"` is taken |
| `set/Set_Output_Dfi_Link` | `OUTP:DFI:LINK "<value>"`, enum of the 10 marked valid for DFI, default SUM3 | p. 40, Table 3-1, *RST SUM3 |
| `set/Set_Output_Relay` | arg `bool` OFF/ON (was unknown) | OUTP:REL[:STAT] <bool>, p. 41 |

The relay rows are valid only with the optional relay connector; a module without it answers `-241 "Hardware missing"` — the unit's fact, not the table's (noted on each row).

### Retired (2026-11-06)

- `do/Do_Ttltrg_Link` — `TTLT:LINK`: there is no TTLT root node; the link is OUTPut:TTLTrg:LINK (Set_Output_Ttltrg_Link)
- `do/Do_Output_Dfi` — bare `OUTP:DFI`: OUTPut:DFI[:STATe] takes a <bool> (p. 39); it is Set_Output_Dfi_Status
