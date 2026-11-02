# Kenwood TS-120S service manual (reviewed transcription)

> Source: "TS-120S Service Manual.pdf" (61 pages scanned at 100 dpi). The sections useful for diagnosis and alignment were reviewed and transcribed by hand. Page numbers are the PDF's. What is not here (parts list, board views, the PS-30, VFO-120 and AT-120 accessories) can be searched in [ocr/service-manual-raw-ocr.md](ocr/service-manual-raw-ocr.md) and confirmed in the PDF.
>
> Doubtful readings of the scan are marked **(?)**.
> Transcribed on 2026-10-31.

## PDF index

| Page | Content |
|---|---|
| 3 | Specifications |
| 4 | Features, general information, YK-88C filter |
| 5 | **Circuit description (RX and TX)** |
| 6–9 | **Frequency system, PLL, Table 1 (VCO per band)**, counter |
| 10–13 | Outside and inside views, board views (RF unit on p. 12) |
| 14–19 | PLL, counter, CAR, VFO, Final (diagrams and boards) |
| 20–28 | Parts list |
| 29–32 | Exploded view and disassembly (RF unit access on p. 32) |
| 33 | **RX troubleshooting** |
| 34 | TX troubleshooting |
| 35 | **Common-systems troubleshooting (S-meter, PLL)** |
| 36 | **RX and TX level diagram** |
| 37–40 | **Adjustments (items 1–19)** |
| 41–42 | Location of adjustment points on the boards |
| 43–54 | PS-30, VFO-120, AT-120 |
| 55–60 | Schematics (counter, RF unit, switch units, IF unit, Final and Filter) |

---

## 1. Specifications (p. 3)

| Item | Value |
|---|---|
| Bands | 80 m 3.5–4.0 · 40 m 7.0–7.3 · 20 m 14.0–14.35 · 15 m 21.0–21.45 · 10 m A 28.0–28.5 / B 28.5–29.0 / C 29.0–29.5 / D 29.5–29.7 MHz · WWV 15.0 MHz (RX only) |
| Modes | SSB (A3J), CW (A1) |
| Input power | 80–15 m: 200 W PEP SSB, 160 W DC CW · 10 m: 160 W PEP SSB, 140 W DC CW |
| Antenna impedance | 50 ohm |
| Carrier suppression | > 40 dB |
| Sideband suppression | > 50 dB |
| Mic impedance | 500 ohm to 50 kohm |
| TX audio response | 400–2600 Hz (−6 dB) |
| Harmonic radiation | > 40 dB down |
| **RX sensitivity** | **0.25 µV for 10 dB S/N or better** |
| Image rejection | > 50 dB |
| IF rejection | > 70 dB |
| Stability | ±100 Hz in any 30 min after warm-up; ±1 kHz during the first hour |
| Selectivity SSB/CW | 2.4 kHz (−6 dB) / 4.2 kHz (−60 dB) |
| AF output | > 1.5 W into 8 ohm (10 % THD), 4–16 ohm load |
| Supply | 12–16 V DC (13.8 V); < 18 A TX, < 0.7 A RX |
| Semiconductors | 26 ICs, 16 FETs, 90 transistors, 142 diodes, 1 display tube |
| Weight | about 5.6 kg |

---

## 2. Circuit description (p. 5)

### Receiver (original text)

> The signal from the antenna is fed to the 8.83 MHz IF trap circuit. This signal is stepped up about 10 dB and impedance-converted by a wide-band transformer before it is applied to the bandpass filter (BPF). **The BPF is common to transmission and reception**, eliminates the need for a preselector, and makes the RF section compact in design.
>
> The signal from the BPF is fed to the dual-gate MOS FET wideband RF amplifiers consisting of a 3SK74 (Q1) and a 2SC1815 (Q2), where the 2 MHz to 35 MHz signal is amplified about 20 dB.
>
> The RF amplifier output passes through a wide-band transformer to the input balanced transformer of the balanced mixer (two 3SK74s, Q3 and Q4), where it is mixed with the VCO output from the PLL and converted to the 8.83 MHz IF. This signal is applied to the IF unit, through the ceramic filters, NB gate circuit and the crystal filter. The NB circuit is controlled by the NB switch on the front panel. The signal, passing through the crystal filter, is amplified about 90 dB by the three-stage 3SK74 MOS FET IF amplifier (Q1, Q2 and Q3) and is demodulated into audio by the four-diode ring detector.
>
> From the final IF stage, the signal also passes through a buffer amplifier and is fed to the AGC circuit where it is detected and amplified. Receiver gain is controlled by this AGC voltage applied to the second gates of the RF and IF amplifiers, with the time constant determined by R38 (2.2 MΩ) and C40 (1 µF). Input levels of 2 dB and 34 dB are indicated as S1 and S9 on the S-meter. The AF signal is amplified by Q1, a 2SC2240 (GR), gain controlled, and further amplified by an HA1366W (Q7), the power-amplifier IC, to drive the speaker. […]

RX chain summary:
`ANT → 8.83 MHz IF trap (L1, L2) → T1 (wideband transformer, +10 dB) → per-band BPF (shared TX/RX) → Q1 3SK74 + Q2 2SC1815 (about 20 dB, 2–35 MHz) → T2 → balanced mixer Q3/Q4 (3SK74) + VCO → 8.83 MHz IF → IF unit (ceramic filters, NB, XF, 3× 3SK74 about 90 dB, ring detector)`.
AGC acts on gate 2 of both the RF **and** IF amplifiers.

### Transmitter (summary)

Mic → Q18 2SC2240 + Q10/Q11 2SC1815 → four-diode balanced modulator → 8.83 MHz DSB → Q12 2SK19 (+10 dB, also receives the protection voltage) → crystal filter (SSB) → IF unit Q1 3SK74 (+30 dB, ALC on gate 2: R4 1.5 MΩ, C25 0.47 µF) → **TX mixer Q5/Q6 (3SK74) with the same VCO** → **the same TX/RX BPF** → Q7, Q8 (2SC1815), Q9 (2SC2086) → Final unit: Q1 2SC2075 driver → Q2/Q3 2SC2509 push-pull → Q4/Q5 2SC2290 push-pull → filter → antenna. In CW, block bias keying controls Q10 (2SA1015) in the RF unit, which drives the gates of the TX mixer (Q5/Q6) and the base of predriver Q9.

> **Practical consequence:** the BPF (L3–L17) and the VCO are shared by TX and RX. If TX gives normal power on a band, neither the BPF nor the VCO injection for that band can be grossly wrong. **RX-only** parts: IF trap (L1/L2), T1, RX switching diodes (D2, D4), Q1, Q2, T2 and the RX mixer Q3/Q4.

---

## 3. Frequency system and PLL (pp. 6–9)

- Single conversion, 8.83 MHz IF. The VCO is synthesized from the counter's 10 MHz and 500 kHz references plus the VFO (5.5–6.0 MHz) and the CAR. There are no per-band HET crystals.
- MIX(3) combines CAR and VFO; on 3.5 and 7 MHz it goes straight to MIX(1). On 14 MHz and up, MIX(2) mixes MIX(3)'s output with 10 MHz or 20 MHz (the latter comes from the Q24/Q25 2SC460 doubler on 21 and 28 MHz).
- Phase comparator MC4044P. If the PLL unlocks, **the VCO is switched off** (Q7, Q8, Q21) and the display blanks (the "two dots").
- CAR: LSB 8.8285 · USB 8.8315 · CW(R) 8.8315 · CW(T) 8.8307 MHz. IF SHIFT moves the CAR on receive.
- Separate VCOs: T1 (14 MHz and WWV), T2 (21), T3 (28), T4 (7), T5 (3.5).

### Table 1 / adjustment item 6: VCO frequency per band

VCO frequency = operating frequency + 8.83 MHz. In parentheses, the VCO control voltage specified at that point (measured at PLL TP1).

| Band | Dial "0" | Dial "250" | Dial "500" |
|---|---|---|---|
| WWV | 23.33 (3.5 V) | 23.58 | 23.83 |
| 3.5 | 12.33 | 12.58 (3.5 V) | 12.83 |
| 7.0 | 15.83 | 16.08 (5.5 V) | 16.33 |
| 14.0 | 22.83 | 23.08 | 23.33 (3.5 V) |
| 21.0 | 29.83 | 30.08 (3.5 V) | 30.33 |
| 28.0 | 36.83 | 37.08 | 37.33 |
| 28.5 | 37.33 | 37.58 | 37.83 (5.0 V) |
| 29.0 | 37.83 (5.0 V) | 38.08 | 38.33 |
| 29.5 | 38.33 | 38.58 | 38.83 |

**Oscillator (VCO) output level: 1 V ±2 dB** (item 6 specification).

---

## 4. Level diagram (p. 36)

### Receiver, 14.250 MHz

Conditions: 0 dB input (0.5 µV) at the antenna → 0.63 V audio into 8 ohm (50 mW). The numbers are the **signal generator level needed at each point to get the same audio output** (fixed AF GAIN; measured at the IF unit ring detector). The generator is injected through a 0.01 µF capacitor. A higher number at a later point means there is gain before that point.

| Injection point | Required level (dB) | Implied gain/loss |
|---|---|---|
| Antenna (ANT) | **0** | reference |
| T1 output / BPF input | **9** | T1 about +9 dB |
| BPF output / Q1 gate | **11** | BPF about −2 dB |
| Q1 drain / Q2 base (C33) | **27** | Q1 about +16 dB |
| Q2 output / T2 input to mixer | **34** | Q2 about +7 dB |
| Mixer output (RIF, to the IF unit) | **37** | mixer about +3 dB |
| IF unit: C56 / ceramic filter / T2 / T3 / NB / T4 / XF | 31 / 35 / 30 / 38 / 25 / 20 **(?)** | (doubtful transcription: arrow order) |
| IF Q1 (1st IF) G1 / output | 52 / 51 **(?)** | |
| IF Q2 (2nd IF) | 79 / 72 **(?)** | |
| IF Q3 (3rd IF) output | 102 | |

> The RF section (ANT → mixer) reads clearly. That is the part useful for comparing bands: inject the same level at each point on 7 / 14 / 21 / 28 MHz and measure the level at the IF. The stage whose gain drops on the high bands is the culprit.

### Transmitter, 14.25 MHz, ALC in the full-scale zone

RF voltages (VTVM): CW 0.072 V / SSB 1 kHz 0.1 V at the BM · CAR 0.71 V · BM output 0.038 V · Q12 0.054 V · IF unit input 0.112 V · XF 0.033 V · IF Q1 input 0.011 V, output 0.28 V · TX mixer input (T4/T5) 0.004 V · **after the BPF 0.165 V** · Q7 0.16 V · Q8 0.15 V · Q9 0.11 V · RF unit DRV output 0.3 V · Final Q1 1.75 V.

---

## 5. Troubleshooting (pp. 33 and 35)

### Receiver (p. 33): "No receiver output"

1. Noise output NG → Speaker (NG: speaker) → AF-GEN output (NG: Q7 HA1366W) → phones jack (NG: loose contact).
2. Noise output OK → AF GAIN VR (NG: pot, wiring or contact).
3. **VCO circuit** NG → voltage regulator / see PLL troubleshooting.
4. **IF circuit** NG → **Bias circuit**: no RLR/RLT voltage, −6 V supply trouble (may be low), defective Q6/Q7 (AGC) → **IFT**: IF unit T1–T7 need adjustment → **Filter**: CF1/CF2, XF (SSB or CW; check a customer-installed CW filter) → **Transistors**: IF unit Q1–Q3.
5. **RF ANT circuit** NG → **defective RF unit Q1–Q3 · band switch malfunction · RF BPF coils need adjustment or are defective · loose contact of RL1-1 in the Filter unit**.
6. Marker inoperative → counter: Q4/Q5 (multivibrator), Q6 (buffer).

### Common systems (p. 35)

**S-meter malfunction:**
- S-meter NG → IF unit NG: **VR1 10 kΩ zero set needs adjustment · VR2 470 kΩ meter sensitivity needs adjustment** · Q6/Q7 (AGC) · L4 150 µH · relay RL.
- IF unit OK → AF-GEN: carrier balance TC1.
- ALC meter NG → Filter unit: Q2 (ALC amp), lead from the S-meter circuit → IF unit: relay, Q5/Q6 (S-meter circuit).
- RF meter NG → Filter unit: D2 1N60, RL1-3 contact → Switch B unit: ALC/RF switch.

**Power supply:** fuse → B line shorted, Q7 HA1366W, Q3 2SA473(Y) (9 V), Q2 µPC14305H (5 V) in the AF-GEN; power switch; cord.

**PLL, no RX and no TX:** VFO stopped · VCO cut-off circuit Q7/Q8/Q21 active (Q8 collector about 5.7 V DC nominal) · CAR not oscillating or not reaching the PLL · programmable divider signal.

---

## 6. Adjustments (pp. 37–40)

### Test equipment (p. 37)

VTVM/DVM (> 1 MΩ) · RF VTVM (1 MΩ, < 3 pF, 10 mV–300 V, ≥ 50 MHz) · AF VTVM · AF generator · AF dummy load 8 ohm 3 W · RF dummy load 50 ohm 100 W · oscilloscope · sweep generator 8.83 MHz ±5 kHz · **SSG 1.8–30 MHz, −6 to 120 dB (0.25 µV – 0.5 V)** · frequency counter ≥ 40 MHz · noise generator · detector for the TX BPF (2× 1N60).

**SSG dB reference (0 dB = 0.5 µV):**

| dB | −6 | 0 | 6 | 12 | 24 | 30 | **40** | 50 | 60 | 70 | 80 | 90 | **100** | 120 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| voltage | 0.25 µV | 0.5 µV | 1 µV | 2 µV | 8 µV | 15.8 µV | **50 µV** | 158 µV | 500 µV | 1.58 mV | 5 mV | 15.8 mV | **50 mV** | 0.5 V |

> Into 50 ohm: 50 µV ≈ −73 dBm (S9). 0 dB = 0.5 µV ≈ −113 dBm.

### Preparation (p. 38)

AF GAIN minimum (CCW) · **RF GAIN maximum (CW)** · MIC GAIN and CAR LEVEL centered · RIT and IF SHIFT centered · MODE LSB · REC · NB OFF · CAL OFF · RIT OFF · VFO · meter on RF · VOX on MAN.

### Adjustment table

| # | Item | Condition | Measure at | Adjust | Specification |
|---|---|---|---|---|---|
| 1.1 | 9 V | — | AF-GEN J4 pin 4 (DC VTVM) | AF-GEN VR3 | 9 V |
| 1.2 | 2.8 V | — | AF-GEN J4 pin 10 | AF-GEN VR2 | 2.8 V |
| 1.3 | AVB 11 V | STBY → SEND | FILTER, AVB | FILTER VR4 (WB4KDI: actually **VR5**) | 11.0 V |
| 2.1 | CAR output | — | AF-GEN J3 pin 2 (RF VTVM) | CAR T1 | 0.3 Vrms ±1 dB |
| 2.2 | CAR frequency | IF SHIFT centered; LSB / USB | AF-GEN J3 pin 2 (counter) | CAR TC2 (LSB) / TC1 (USB) | 8.82850 / 8.83150 MHz |
| 2.3 | CAR CW | CW mode | same | CAR VR2 | 8.83070 MHz |
| 3 | IF SHIFT | alternate SEND/REC | same | CAR VR1 | no frequency change |
| 4 | VFO | output across 0–500 | AF-GEN J1 pin 6 (RF voltmeter) | VFO TC2 | 0.2 Vrms ±1 dB at 250; ±2 dB in FIX |
| 5 | RIT | VFO at 5.5 MHz, RIT centered | AF-GEN J1 pin 6 (counter) | AF-GEN VR1 | no change RIT ON/OFF; range > ±1.5 kHz |
| 6 | **VCO** | — | **PLL TP1 (DC VTVM)** | PLL **T1**: WWV → 3.5 V (VFO 00) and 14 MHz → 3.5 V (VFO 500) · **T2**: 21 MHz → 3.5 V (VFO 250) · **T3**: 28.0 → 5.0 V (VFO 500) or 29.0 → 5.0 V (VFO 0) · **T4**: 7 MHz → 5.5 V (VFO 250) · **T5**: 3.5 MHz → 3.5 V (VFO 250) | **Oscillator level 1 V ±2 dB** (see VCO table) |
| 7 | **TX BPF** | order 3.5 → 7 → 14 → 21 → 28 MHz | sweep generator + oscilloscope + detector; RF DRV / PLL VCO | **RF L3–L17** | waveform per Fig. 15. Ripple: 3.5 MHz < 6 dB; 7 MHz < 2 dB; 14 < 2 dB; 21 < 1 dB; 28 < 2 dB |
| 8 | **RX BPF** | needs a spectrum analyzer + tracking generator; otherwise adjust as in item 7 | tracking generator at ANT (rear panel); analyzer at **RF Q2 emitter** | RF L3–L17 | same as item 7 (Fig. 16) |
| 9 | IF AMP | VFO 250, 14 MHz band, USB | SSG, oscilloscope, AF VTVM, 8 ohm load (SP) | **RF T3**, **IF T1–T7** | 1) maximum output; 2) SSG at 0.25 µV (−6 dB) at the antenna → S/N about 15 dB |
| 10 | IF trap | 1) 7 MHz band: RF L1, L2 · 2) 14 MHz band: L35 | SSG, AF VTVM (SP) | RF L1, L2 / L35 | minimum S-meter and audio with 8.83 MHz; repeat 2–3 times; ≥ 80 dB attenuation of 8.83 MHz |
| 11 | NB | noise generator at ANT, S-meter S5–7 | IF D14 (cathode), oscilloscope | RF T3 · IF T1 | waveform as shown; repeat 2–3 times |
| 12 | Counter standard oscillator | WWV band, VFO 500 (15.000 MHz), CAL ON, antenna connected | — | counter TC1 | zero beat between WWV and CAL |
| 13 | Idle (base) current | LSB, MIC minimum, 14 MHz, SEND | ammeter: ① D14 terminal (+) and L7 150 µH side (−) · ② F14-3P | FINAL ① VR1 / ② VR2 | **150 mA / 100 mA**. Then move the wire from D14 back to the L7 150 µH side and resolder the red wire to terminal 3P |
| 14 | Carrier suppression | 14 MHz, full CW power; switch to SSB with no modulation | wattmeter, oscilloscope, directional coupler at ANT | AF-GEN VR5, TC2 (min.) | > 40 dB; repeat 2–3 times |
| 15 | Carrier point | AG at MIC, 1500 Hz at 7 mV; MIC GAIN for 5 W | wattmeter, oscilloscope, AF VTVM | CAR TC1 (USB) / TC2 (LSB) | sweep 300–2700 Hz: 400 and 2600 Hz −6 dB, 1500 Hz centered; equal output in USB and LSB; recheck carrier suppression |
| 16 | Side tone | AF GAIN at 12 o'clock, CW, key down | AF VTVM | AF-GEN VR4 | 0.63 V / 8 ohm |
| 17 | Ic meter | CW, SEND, same as item 13 | wattmeter, DC ammeter | FILTER VR4 | with the item 13-② current, set CAR level for 11 A on the IC meter |
| 18 | ALC | 14 MHz, VFO 200, CW; FILTER VR2 minimum (CCW); SEND | wattmeter, AG, AF VTVM | FILTER **VR3: 95 W** (14 MHz) · **VR2: 75 W (28.5 MHz)** | check that SSB with 7 mV / 1500 Hz at MIC gives the same power |
| 19 | Protection | FILTER VR1 fully CW; 50 ohm then 150 ohm load with a Bird wattmeter | FILTER TP1/TP2 (DC) | FILTER TC1 → minimum (about 0.2–0.4 V); then ② VR1 for 39 W into the 150 ohm load | (WB4KDI: it is actually **VR1**, not VR2) |
| 20 | **S-meter** | 14.175 MHz on receive, SSG at the antenna | — | 1) **IF VR1**: 100 dB (50 mV) → **S9+60 dB** · 2) **IF T6**: 8 dB → **S1** (tolerance "less than 8 dB ±4 dB") · 3) **IF VR2**: 40 dB (50 µV) → **S9** (tolerance "less than 40 dB ±6 dB") | |

> **Notes on the S-meter:**
> - The manual numbers this item "19" (the table repeats the number).
> - The p. 35 troubleshooting calls VR1 "zero set" and VR2 "meter sensitivity". The adjustment table instead uses VR1 for the top end (S9+60) and VR2 for S9.
> - **The S1 point is set with IF unit T6**, an IF transformer. If the IF unit transformers are retouched by ear, the start of the S-meter scale moves too.
> - WB4KDI considers the manual's procedure "seems to be wrong" and proposes calibrating to the standard (S9 = 50 µV, 6 dB per S-unit), achievable roughly from S3 to S9+40 (see *Help! I Just Got a TS-120*).

### RF unit BPF coils per band (Fig. 15/16 and schematic)

| Band | Coils | Input termination resistor (SB-816: 1.5 kohm → 470 ohm) |
|---|---|---|
| 80 m | **L3, L4, L5** | R3 |
| 40 m | **L6, L7, L8** | R5 |
| 20 m | **L9, L10, L11** | R7 |
| 15 m | **L12, L13, L14** | R9 |
| 10 m | **L15, L16, L17** | R11 |

> Fig. 15 labels the sweeps with each band's VCO frequencies (e.g. 12.33 / 12.58 / 12.83 for 3.5 MHz): they are the band-edge and center markers as they appear on the sweep.
> Item 7 setup (Fig. 15): J18 is removed and the sweep generator is connected to the PLL's J18 connector (pin 1), i.e. the sweep enters on the VCO line. It is measured at the RF unit DRV with the detector.
> Item 8 setup (Fig. 16): tracking generator at ANT; spectrum analyzer at the RF unit Q2 emitter.
