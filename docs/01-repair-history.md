# Repair history

Chronological order, oldest first. The first two phases come from two accounts by the owner: the summary of the squeal repair (the older one) and the full logbook (more recent).

## Phase 1: TX squeal repair (the oldest)

**Symptom:** squeal or oscillation on TX on the high bands (20, 15 and 10 m), getting progressively worse. Absent on 40 and 80 m. Intermittent at first, then constant. 40 W output in SSB with no modulation. The external monitor shut off on PTT on 10 m.

**Causes found and fixed**

1. Cracked solder joint on the coax from the Relay unit (X41) to the RF unit. Reflowed and reinforced. Fixed most of the problem; the squeal remained only on 10 m.
2. Diode D8 (original 1S1585) with reverse leakage (600 mV forward and 1360 mV reverse, out of circuit). D2, D3 and D8 were temporarily replaced with 1N4148s, which fixed the squeal and the 40 W with no modulation. D8 was later changed to a 1N4448.
3. Cracked solder joint in the Filter unit, on the signal line. Fixed the reduced receive level after transmitting from cold.

**Service bulletins applied**

| Bulletin | Change |
|---|---|
| SB-844 | R47 from 33 to 10 ohm, R50 from 560 to 680 ohm, C61 removed, 0.01 uF bypass capacitor on the AVB line |
| SB-832 | Diodes D2, D3 and D8 replaced |
| SB-816 | R3, R5, R7, R9 and R11 from 1.5K to 470 ohm in the RF unit |

**Recap in this phase:** RF unit, IF unit, AF-GEN unit and PLL unit.

**Calibrations after the recap:** IF VR2 (S-meter zero and ALC readjusted, because the new capacitors shifted the offset) and IF VR1 (S-meter span partially adjusted by ear).

**Secondary problems identified in that phase:** see [open items](06-open-items.md).

## Phase 2: maintenance and later events (logbook, the most recent)

Three separate events:

1. Diode replacement in several units (due to degradation and as prevention).
2. Electrolytic replacement in the Relay, RF, IF, AF-GEN, PLL and Filter units.
3. Transistor replacement in the Filter unit due to the **AVB cable event**: the cable between the Filter unit and the Final unit was accidentally cut against a sheet-metal edge during a repair and shorted to ground, which burned out two transistors. The cable was repaired and the radio has worked fine since.

### RF unit (X44-1260-01)

| Ref. | Original | Replacement | Reason |
|---|---|---|---|
| D1, D3, D5 | 1S1587 | 1N4448 | Preventive |
| D2 | 1S2588 | BA389 | Preventive; previously a wrong part had been fitted (DO-35) |
| D4 | 1S2588 | BA389 | Degraded (870 mV out of circuit); previously a wrong part |
| D6 | 1S1555 | 1N4448 | Preventive |
| D7 | 1N60 | New 1N60 | A silicon diode had been fitted by mistake (measured 760 mV) |
| D8 | 1S1585 | 1N4448 | A 1N4148 had been fitted by mistake |

### IF unit (X48-1210-01)

| Ref. | Original | Replacement | Reason |
|---|---|---|---|
| D11 | 1N60 | New 1N60 | Degraded (high threshold) |
| D12 | 1N60 | New 1N60 | Degraded (measured 359 mV out of circuit) |
| D14, D15 | 1N60 | New 1N60 | Preventive |
| Relay | Original | New sealed Japanese relay | Preventive |

### Filter unit (X51-1200-00)

| Ref. | Original | Replacement | Reason |
|---|---|---|---|
| Q6 | 2SA562 (Y) | New 2SA562 | Damaged by the AVB line short |
| Q9 | 2SA473 (Y) | 2SA755 | Damaged by the AVB line short |
| C35 | 220 uF 16 V | 220 uF 25 V | Preventive recap |
| (other) | 10 uF 16 V | 10 uF 25 V | Preventive recap |
| (others) | 1 uF 50 V and 0.47 uF 50 V | Same values | Preventive recap |
| RL1 | Original relay | New sealed Japanese relay | Carbonized contacts |

### Relay unit (X41-1250-00)

| Ref. | Original | Replacement | Reason |
|---|---|---|---|
| D1, D2 | 1S1555 | 1N4448 | Preventive |

### Mechanical and electrical repairs

| Component | Work done | Reason |
|---|---|---|
| Connector J41 (Filter unit coaxial ANT/GND) | Resoldered and broken traces jumpered | Cracked cold joint; caused intermittent RX attenuation |
| AVB cable (Filter unit to Final unit) | Repaired | Accidentally cut by a sheet-metal edge during a repair |
| IF unit transformers T1 to T9 | Peaked by ear with a TP reference | Fine alignment pending with a calibrated generator |

## Phase 3: sudden loss of TX, October 2026

See [02-tx-incident-oct-2026.md](02-tx-incident-oct-2026.md). Fixed on 2026-10-17 by cleaning off and desoldering a solder sliver that was bridging the collector and emitter of Q7 in the RF unit.

## Known state of the RF unit diodes

According to the most recent logbook. The older summary said D2, D4 and D7 were kept original; the later logbook replaced them.

| Diode | Current state |
|---|---|
| D1, D3, D5 | 1N4448 |
| D2, D4 | BA389 (DO-35) |
| D6 | 1N4448 |
| D7 | New 1N60 (germanium) |
| D8 | 1N4448 (not shown on the WB4KDI schematic) |

## Recap: status

- Done: Relay, RF, IF, AF-GEN, PLL and Filter units (partially documented for the Filter unit).
- Not done: CAR unit, Counter unit and Final unit (the Final unit's bias and decoupling electrolytics are still original).

## Phase 3: S-meter on the high bands (Oct–Nov 2026)

- The radio had an 11 m (CB) modification from the previous owner, undone by a technician before the recap. The S-meter has read poorly since then.
- 2026-10-31: BPF coils L3–L14 moved and returned, no change.
- 2026-11-01: **IF unit T6 peaked** on the CAL marker on 10 m; VR1 (span) backed off about 1/4 turn; VR2 unchanged. The S-meter came back to life on 10 m and reads less high on 40 m.
- By 2026-11-02: L15–L17 (10 m) moved and returned, no change. BPF cleared on all bands.
- Full write-up in [07-s-meter-high-bands-2026.md](07-s-meter-high-bands-2026.md).

