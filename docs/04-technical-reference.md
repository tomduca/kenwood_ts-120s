# Technical reference

Data from the service manual and the WB4KDI schematic, read from scanned images: confirm on paper before using them to make decisions.

## 1. TX path

```
AF-GEN: microphone or carrier -> balanced modulator (D11 to D14, T2) -> Q12 (2SK19, about +10 dB)
  -> J30 (GEN) -> IF unit: SSB/CW switching diodes and crystal filter
  -> Q1 (3SK74, about +30 dB, gain controlled by the ALC)
  -> C23 (15 pF) + D9 + IF relay -> J32 (TIF) -> J35 (TIF) on the RF unit
  -> T4 -> mixer Q5/Q6 (3SK74; oscillator injection via J38 and T5)
  -> C52 -> band BPF (shared with RX) -> Q7 -> Q8 -> Q9 (2SC2086) + T6 -> DRV
  -> Final unit: Q1 (2SC2075) -> T1 -> Q2/Q3 (2SC2509) -> T2 -> Q4/Q5 (2SC2290) -> T3/T4 -> PO
  -> Filter unit: low-pass filters L1 to L11 (selector S4), L18 (forward and reflected power sampling), RL1-1 -> ANT
```

Notes:

- RX goes through the ceramic filters CF1/CF2, the NB gate (diode ring D1 to D4) and the crystal filter. In the IF unit, Q8 to Q13 is the **noise blanker (NB)**, not the TX chain.
- The BPF is the same for TX and RX: if RX passes fine through a section, that section's contacts and coils are healthy.

## 2. RF unit Q7 (2SC1815 Y)

| | |
|---|---|
| Stage | First TX amplifier after the BPF; the manual labels it "AMP" |
| Function | Wideband buffer: isolates the BPF from the following stages and delivers the signal to Q8 with low output impedance |
| Gain | Close to unity in voltage (0.16 V at its base and 0.15 V at Q8's, per the manual); provides current gain |
| Configuration | Emitter follower. Signal into the base (C54 and R62); collector on the TX supply; output from the emitter (C57 and R63 to Q8) |
| Supply | TX only (11 V on the collector; 0 V on RX) |
| Bias | R42 (82K, collector to base) and R40 (47K, base to ground), with DC feedback. Emitter to ground through R43 (100 ohm) and through R41 (100 ohm) in series with L30 (100 uH) |
| Values on TX | Base about 1.8 V, collector 11 V, emitter 1.1 V |
| 2SC1815 pinout | Emitter, collector, base, flat face towards you, left to right (verify against the circuit) |
| Incident fault | A solder sliver joined collector and emitter: the output was shunted to ground through the supply decoupling (about 40 dB down), on TX only |

## 3. Supply rails

| Rail | Source | Value |
|---|---|---|
| 14A | Power supply, unregulated | 14 V |
| AVB | Filter unit 11 V regulator (Q4, Q5, Q6 and pass transistor Q9, now a 2SA755), TX only | 0 V on RX, 11.3 to 11.4 V on TX |
| 9 V and 5 V | AF-GEN regulators | Nominal |
| -6 V | Negative bias for the mixer gates | About -5.9 V |

## 4. Idle current (manual, bias adjustment)

Conditions: LSB mode, mic at minimum, 14 MHz band, SEND position, ammeter in series.

| Stage | Control | Current | Where it is measured |
|---|---|---|---|
| Finals (Q4/Q5) | VR2 | 100 mA | Terminal F14 (3P) |
| Q2/Q3 | VR1 | 150 mA | Terminal D14 |

After adjusting, put the wires back in place. With the 15 mohm shunt, about 160 mA was measured on the finals, above specification.

## 5. Protections

- **Final unit thermal protection:** output transformer core (above 120 °C) and heatsink (above 90 °C). They force RX. The fan starts at about 45 °C.
- **SWR and ALC:** the L18 toroid in the Filter unit samples forward and reflected power. Q1 and Q2/Q3 in the Filter unit amplify that voltage and apply it to the ALC line, which controls the second gate of the 3SK74 Q1 in the IF and the 2SK19 Q12 in the AF-GEN.

## 6. Spares and replacements

- 2SC2290 finals: by hFE rank: R 30 to 65, O 55 to 95, Y 85 to 150. When replacing, use the same rank (matched pair).
- Filter unit Q9: now a 2SA755 (original 2SA473).
- RF unit diodes: see [repair history](01-repair-history.md).

## 7. Service bulletins applied

| Bulletin | Change | Effect to keep in mind |
|---|---|---|
| SB-816 | R3, R5, R7, R9 and R11 from 1.5K to 470 ohm (BPF damping) | Lowers the BPF's Q and raises its loss: may explain part of the -8 dB measured |
| SB-832 | Diodes D2, D3 and D8 | |
| SB-844 | R47 from 33 to 10 ohm, R50 from 560 to 680 ohm, C61 removed, 0.01 uF bypass on AVB | Changes the Q9 stage: the manual's nominal levels at Q9 and DRV may differ |

## 8. Schematic vs. actual board

- The WB4KDI schematic is headed "TS-120V" on its first sheet, but the unit sheets are for the TS-120S.
- The actual RF unit board has a D8; the schematic only shows D1 to D7. It may be a different board revision.
- Some voltage labels are ambiguous in the scan (for example the RX/TX pair for Q7's base).

## 9. Units and connectors

| Unit | Code |
|---|---|
| IF unit | X48-1210-01 |
| RF unit | X44-1260-01 |
| Filter unit | X51-1200-00 |
| Final unit | X56-1350-00 |
| AF-GEN unit | X49-1110-01 |
| CAR unit | X50-1500-00 |
| Counter unit | X54-1360-00 |
| PLL unit | X50-1490-00 |
| VFO unit | X40-1130-00 |
| Relay unit | X41-1250-00 |

| Connector | Pins |
|---|---|
| J30 (IF unit) | NBS, GND, GEN |
| J32 (IF unit) | GND, TIF (pin 2) |
| J35 (RF unit) | GND (pin 1), TIF (pin 2) |
| J33 (RF unit) | -6 V (1), KEY (2), AVB (3) |
| J36 (RF unit) | RLT, RLR, AGC, RB, 14V |
| J34 (RF unit) | MKR, ANT (each with its own GND) |
| J25 (IF unit) | ALC (pin 1), RLR, RLT, RL, RSC and others |
| J4 (AF-GEN) | pin 11 (RT1): RIT wiper |
