# Measurements and levels

All measurements were taken **with the fault present**, except the last section (reference values with the radio working, to be filled in). RX / TX pairs unless stated otherwise. CW, dummy load, 3 to 5 seconds per TX measurement.

## 1. Power supply and current draw

| Measurement | Value |
|---|---|
| Supply voltage | 14 V stable, no sag on TX |
| RX current draw | 0.73 A |
| TX current draw (CW) | 1.87 A, not changing with the carrier |
| AVB at the Final unit input | 0 V / 11.3 V |
| AVB at J33 (RF unit) | 0 V / 11.4 V |
| J33 KEY (CW) | 0 V / 0.34 V, fixed |
| J33 -6 V pin | -5.94 V / -5.89 V |

## 2. Final unit: DC

| Point | RX | TX |
|---|---|---|
| Q1 base | 0 | 1.65 to 1.84 V |
| Q1 collector | 0 | 11.0 to 11.2 V |
| Q1 emitter | n/a | 0.9 V |
| Q6 base / emitter | n/a | 1.35 V / 0.76 V |
| Q7 (Final) base / emitter | 0 / 0 | 1.39 V / 0.79 V |
| Q7 (Final) collector | 13.97 V | 13.79 V |
| Q2/Q3 base | 0 | 0.72 V |
| Q2/Q3 emitter | 0 | 0 |
| Q2/Q3 collector | 13.97 V | 13.79 V |
| Q4/Q5 base | 0 | 0.65 V |
| Q4/Q5 collector | 13.89 V | 13.84 V |

**15 mohm resistor (F14 supply to the finals):** both ends at 14 V even with the radio switched off. Across it: 0 mV on RX and 2.4 mV on TX (about 160 mA), not changing with the carrier in CW. The manual specifies 100 mA idle for the finals.

**Ohmmeter with the radio off** (artifacts of measuring in circuit, not a sign of a fault): Q4/Q5 collector OL in both directions and then 0.08 V with a beep (red to ground, black to collector); Q1 158 and 170; Q2/Q3 "shorted" on all three legs. The Q4 and Q5 collectors are the same node (T4 primary).

## 3. RF unit: mixer Q5/Q6 (RX / TX)

| Pin | Q5 | Q6 |
|---|---|---|
| Gate | -3.1 / 0.68 V | -3.0 / 0.67 V |
| Gate | -3.34 / 0.77 V | -3.34 / 0.77 V |
| Source | 0 / 1.0 V | 0 / 1.0 V |
| Drain | 13.6 / 12.68 V | 13.6 / 12.7 V |

Schematic: gates -3.9 / +0.6 V, source 0 / 0.7 V, drain 13.5 / 12.6 V. The mixer conducts on TX.

## 4. RF unit: Q7 with the fault

| | Base | Collector | Emitter |
|---|---|---|---|
| RX | 0 | 0 | 0 |
| TX measured | 2.0 V | 5.68 V | 5.68 V |
| TX expected (schematic) | about 1.8 V | 11 V | 1.1 V |

The base matches the R42 (82K) and R40 (47K) divider with the collector at 5.68 V: 5.68 x 47 / 129 = 2.07 V.

## 5. Proximity and diode probes

- **SDR loop:** signal that varies with the carrier at T1, Q2/Q3, T2, Q4/Q5 bases, T4 and PO. It detects by proximity: it does not prove power.
- **Diode probe (multimeter, 1N4148):** 0 at PO, Q1 base and collector, T1 and Q2/Q3 collectors (Q1 collector with 30 to 60 mV on both RX and TX, noise). It responds to a handheld, so the probe works. Silicon does not rectify below about 0.5 V peak.

## 6. SDR++ levels (SNR, 33 pF + 4.6 kohm contact probe)

SNR numbers are neither linear nor calibrated. Only compare series with the same gain.

| Series | Gain | Frequency | Points |
|---|---|---|---|
| A | 43.4 | Operating | RF unit DRV 18 to 20 |
| B | 37.2 | Operating | DRV ~15, Q1 base ~15, Q1 collector ~24, T1 sec. ~10, Q2/Q3 collectors ~40 (possible saturation) |
| B' | 8.7 | Operating | Q1 collector 5, Q2/Q3 collectors 22, Q4/Q5 bases 9 |
| C | 0 | 8828.5 kHz | J30 GEN 37, J32 TIF 20, J35 TIF 20 (carrier 50 %) |
| D | 25.4 | 8825.5 kHz | J30 GEN 68, J32 TIF 48, J35 TIF 48 |
| D' | 25.4 | 7074.5 kHz | C52 58, DRV 12, Q1 collector 20, Q2/Q3 collectors 35, Q4/Q5 bases 25, PO 54 |
| E | 25.4 | 8828.5 kHz | J35 TIF 48, C11 L8 side 21 |
| E' | 25.4 | 7074 kHz | C11 L8 side 32, C11 L7 side 75 (C11 joins L8 to L7), C10 L6 side 52, other leg of C10 35, C54 Q7 side 50, J34 ANT 5, J34 MKR 2, DRV 12 |

## 7. Nominal levels from the manual (page 36)

At 14.25 MHz, with an RF voltmeter and ALC at full scale. RMS voltages.

| Point | Nominal |
|---|---|
| Carrier input to the modulator (CAR) | 0.71 V |
| AF-GEN output to the IF (GEN, Q12) | 0.112 V |
| Crystal filter output | 0.033 V |
| IF Q1 output (IF amp) | 0.28 V |
| TX mixer input (TIF) | 0.004 V |
| Mixer output (C52) | 0.165 V |
| Q7 / Q8 / Q9 (inputs) | 0.16 / 0.15 / 0.11 V |
| DRV (Final unit input) | 0.3 V |
| Final unit Q1 collector | 1.75 V |

Nominal voltage gains: GEN to TIF about -29 dB; TIF to C52 about +32 dB; C52 to DRV about +5 dB; DRV to Q1 collector about +15 dB.

## 8. Measured vs. nominal (gain 25.4 series)

| Section | Measured | Nominal | Reading |
|---|---|---|---|
| GEN to TIF | -20 | -29 | Fine, no loss |
| TIF to C52 (mixer) | +10 | +32 | Somewhat low, uncertain (the TIF reference is before T4) |
| C52 to C54 (BPF) | -8 | almost 0 | The BPF passes the signal; SB-816 (470 ohm) may explain part of the loss |
| **C54 to DRV** | **-38** | **+5** | **About 43 dB missing: the solder bridge on Q7** |
| DRV to Q1 collector | +8 | +15 | Slight |
| DRV to PO | +42 | about 47 | Close to nominal |

With bulletins SB-816 and SB-844 applied, the manual's nominal levels at the BPF, Q9 and DRV may differ.

## 9. Reference values with the radio working (to be filled in)

| Measurement | Expected | Measured |
|---|---|---|
| RF unit Q7, TX: base / collector / emitter | about 1.8 / 11 / 1.1 V | |
| RF unit Q8, TX: base / emitter / collector | about 2.8 / 2.1 / 9.9 V | |
| RF unit Q9, TX: base / emitter / collector | about 1.1 / 0.5 / 12 V | |
| DRV on the SDR (gain 25.4, 7074 kHz, CW 50 %) | much more than 12 | |
| PO on the SDR | much more than 54 | |
| Output power on a wattmeter | | |
| ALC and IC with moderate carrier | they respond | |
| AVB on TX with normal drive | about 11 V | |
| Finals idle current (F14) | 100 mA | |
| Q2/Q3 idle current (D14) | 150 mA | |
| TX current draw with normal drive | | |
