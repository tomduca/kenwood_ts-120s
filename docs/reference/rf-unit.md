# Kenwood TS-120S RF unit X44-1260-01 (schematic as text)

> Sources: WB4KDI annotated schematic ("TS-120S_sch_WB4KDI.pdf", p. 16; the red voltages are WB4KDI's) and the service manual (pp. 5, 12, 36–40). Transcribed on 2026-10-31.
> In WB4KDI's voltage pairs, the **upper value is RX** and the **lower is TX**. This is confirmed by Q1 G2 (2.5 V / 0 V) and by Q9, which only works on TX (collector 0 V / 12 V).
> Doubtful readings are marked **(?)**.

## Semiconductors (schematic list)

| Ref. | Type | Function |
|---|---|---|
| Q1 | 3SK74(L) | RX RF amplifier (dual gate; AGC on G2) |
| Q2 | 2SC1815(Y) | RX RF buffer |
| Q3, Q4 | 3SK74(L) | RX balanced mixer |
| Q5, Q6 | 3SK74(L) | TX balanced mixer (balance with VR1 500 ohm (B)) |
| Q7, Q8 | 2SC1815(Y) | TX amplifiers |
| Q9 | 2SC2086 | TX predriver (DRV output through T6) |
| Q10 | 2SA1015(Y) | keying/bias switch (TX mixer and Q9) |
| D1, D3, D5 | 1S1587 | D1: marker input (MKR) · D3, D5: TX switching |
| D2, D4 | 1S2588 | **RX switching** at the BPF input (D2) and output (D4) |
| D6, D7 | 1S1555 | Q10 keying circuit |

> State of this radio (see the repair history): D2/D4 → BA389, D7 → new 1N60, the rest → 1N4448. D8 (added by SB-844) → 1N4448.

## Connectors

| Connector | Pins |
|---|---|
| J34 | 1 MKR (marker), 2 GND · 1 ANT, 2 GND |
| J40 | RIF (RX IF output to the IF unit), GND |
| J35 | TIF (TX IF input from the IF unit), GND |
| J36 | 1 RLT, 2 RLR, 3 AGC, 4 RB, 5 14 V |
| J38 | VCO (from the PLL), GND |
| J33 | −6 V, KEY, AVB |
| J37 | band lines from the switch: 29.5, 29 · 28.5, 28, 21, 14, 7, 3.5, JJY, 9 V |
| DRV | TX output to the Final unit |

## Receive path

```
ANT (J34)
 ├─ L2 ∥ C3 (0.001 µF) in series ─┐   8.83 MHz IF trap (adjust L1, L2)
 └─ L1 + C1 100 pF to ground ─────┘
 → T1 (wideband, about +10 dB; R1 2.2 kohm)  ← SB-040/831: T1 is damaged by static
 → C4 0.01 µF ─ node with C20 33 pF to ground (SB-832) ─ D2 (RX) ─┐
                                        D3 (TX, from Q7) ─────────┤→ band switch → BPF
 Per-band BPF (3 coupled tuned circuits, adjustable cores):
   80 m L3-L4-L5 (C5 220P, C8, R3 1.5 kohm, R4 4.7 kohm)
   40 m L6-L7-L8 (C10 82P, R5 1.5 kohm, R6 4.7 kohm)
   20 m L9-L10-L11 (C15 10P, R7 1.5 kohm, R8 4.7 kohm)
   15 m L12-L13-L14 (R9 1.5 kohm, R10 4.7 kohm)
   10 m L15-L16-L17 (R11 1.5 kohm, R12 4.7 kohm)
   (R3/5/7/9/11 = input termination → SB-816 proposes 470 ohm)
 → band switch → D4 (RX) ─ C30 0.01 µF ─ R58 56 ohm → Q1 G1   (D5 = TX, to the TX mixer)
   (R61 47 kohm to ground at the D4 node; R13 100 kohm switching bias feed (?))
 → Q1 3SK74: drain load R16 470 ohm + L20 100 µH + L21 1.5 µH ∥ C74 5 pF (high-frequency compensation network)
   G2 = AGC (R14 470 kohm, C31); source R15 560 ohm ∥ C32
 → C33 0.01 µF → Q2 2SC1815: base R17 27 kohm / R18 8.2 kohm; R19 56 ohm
   emitter: R20 100 ohm, C35 0.047 µF, L35 + C76 100 pF (L35 is also used in adjustment item 10, the 14 MHz trap)
 → T2 (wideband) → R24/R25 56 ohm → balanced mixer Q3/Q4 (3SK74)
   R26/R27 56 ohm, R28/R29 220 ohm, C38/C39 0.047 µF, R22 150 kohm / R30 100 kohm (G1 bias), C37
   VCO: J38 → C44 22P / L24 0.47 µH / C43 15P / R56 100 ohm → C40 10 pF → RX mixer
 → T3 (8.83 MHz IF, adjusted in items 9 and 11) → J40 RIF → IF unit
```

## Transmit path (summary)

`J35 TIF → T4 / C45 27P / R66 100 ohm / T5 → mixer Q5/Q6 (VCO through C45/T5; balance VR1 500 ohm) → L28/L29 → D5 → BPF (the same coils, in reverse) → D3 → Q7 (C54, R62) → Q8 (C57, R63) → Q9 2SC2086 (R47, C59, R48, R60, C61 220P, R50 560 ohm, L32) → T6 → C67 → DRV`.
SB-844: R47 33 → 10 ohm, R50 560 → 680 ohm, remove C61, D8 (2× 1S1587) at C4/D8, 0.01 µF bypass on the AVB line.

## Reference DC voltages (WB4KDI, RX / TX)

| Point | RX | TX |
|---|---|---|
| Q1 drain | 13.0 V | 13.3 V |
| Q1 G2 (AGC at rest) | **2.5 V** | 0 V |
| Q1 G1 / R58 node **(?)** | 2.2 V | −2.9 V |
| Q1 source | 2.2 V | 2.2 V |
| Q2 collector | 12.0 V | 11.8 V |
| Q2 base | 2.2 V | 2.2 V |
| Q2 emitter | 1.5 V | 1.5 V |
| Q3/Q4 drain (T3) | 11.7 V | 13.3 V |
| Q3/Q4 G2 | 2 V | 0 V |
| Q3/Q4 G1 / C40 node **(?)** | 2.2 V | −2.9 V (or −2.3 V) |
| Q5/Q6 gates | −3.9 V | 0.6 V |
| Q5/Q6 source | 0 V | 0.7 V |
| Q7 collector | 0 V | 11 V |
| Q8 base / emitter **(?)** | 0 V | 1.1 V / 2.8 V |
| Q9 collector / base / emitter | 0 / −0.2 / 0 V | 12 / 1.1 / 0.5 V |
| 13.5 V line (J33/J36) | 13.5 V | 12.6 V |
| Q10 (keying) **(?)** | −1.2 / 1.7 / −1.9 V | 8.9 / 8.2 / 9 V |

## RX RF levels (manual p. 36, at 14.25 MHz)

Generator level needed at each point for the same audio output (0 dB = 0.5 µV at ANT):

`ANT 0 dB → T1 output 9 dB → BPF output / Q1 G1 11 dB → Q1 drain / Q2 base 27 dB → Q2 output / T2 34 dB → RIF 37 dB`

Implied: T1 about +9 dB · BPF about −2 dB · Q1 about +16 dB · Q2 about +7 dB · mixer about +3 dB.

## Relevant service notes

- **The BPF and the VCO are shared by TX and RX.** If TX gives normal power on a band, that band's BPF and VCO injection are not grossly wrong.
- Adjustment item 7 (TX BPF): sweep generator into J18 (VCO line, PLL), detector at DRV, coils L3–L17 in the order 3.5 → 7 → 14 → 21 → 28 MHz.
- Item 8 (RX BPF): tracking generator at ANT and spectrum analyzer at the Q2 emitter.
- WB4KDI: "Readjustment of band pass circuits only necessary if modified for CB/11 meters."
- SB-060: "Receiver Sensitivity Down → T1 (L34-0696-35) on the RF unit shorted (see SB-831)". "15 Meters NG → broken wafer on the band switch or connectors on the PLL/RF units".
- SB-844: check D2, D3 and D8 for reverse leakage; loose screws on the RF unit and the Relay unit.
