# S-meter on the high bands (Oct–Nov 2026)

How the "dead S-meter on 20, 15 and 10 m" was diagnosed and largely fixed. Short version: the cause was **IF unit T6 being off peak**, with VR1 (span) and VR2 (zero) compensating badly for it. The RF unit and the band-pass filters were cleared.

## Symptom

- 40 m: band noise floor at S6–7 (urban location).
- 20, 15 and 10 m: S0–1 even with resonant antennas. The needle only moved on very strong signals.
- Audio reception was good on all bands (AGC compensates).
- In the IF unit, the AGC test point sat at a fixed 11.5 V on the high bands (AGC at rest), and the base of Q12 measured 2.5 V on 40 m but 0 V on 10, 15 and 20 m.
- The S-meter had not read correctly since the technician undid the previous owner's **11 m (CB) modification** and realigned bands and filters. The technician "fixed" it by raising the zero, so the needle rested above 0. The owner later re-zeroed with VR2 and set the span with VR1 by ear, with VR1 ending up at maximum span.

## What the documentation says

Sources: service manual pp. 5–7, 33–40 and 42; WB4KDI RF unit and IF unit schematics; owner's manual schematic. Full transcriptions are in [reference/](reference/).

- **The RF unit BPF (L3–L17) and the VCO are shared by TX and RX.** RX path: ANT, IF trap (L1, L2), T1, D2, BPF, D4, Q1 (3SK74), Q2 (2SC1815), T2, RX mixer Q3/Q4. TX path: mixer Q5/Q6, D5, the same BPF in reverse, D3, Q7. Normal TX power rules out a gross BPF or VCO fault. It does not rule out a misalignment of a few dB, because ALC hides that on TX.
- **BPF coils per band:** 80 m L3–L5, 40 m L6–L8, 20 m L9–L11, 15 m L12–L14, 10 m L15–L17. The previous log had this table reversed.
- **RX level diagram** (14.25 MHz; signal generator level needed at each point for constant audio, 0 dB = 0.5 µV): ANT 0, BPF input 9, Q1 gate 11, Q2 base 27, T2 34, RIF 37 dB.
- **S-meter calibration per the manual** (at 14.175 MHz, generator at the antenna): IF **VR1** sets S9+60 with 100 dB (50 mV); IF **T6** sets S1 with 8 dB (1.25 µV); IF **VR2** sets S9 with 40 dB (50 µV). That is about **4 dB per S-unit** by design, not 6. WB4KDI considers the manual's procedure questionable and calibrates to 6 dB per S-unit.
- **IF unit T6** is the interstage IF transformer between the 2nd IF amp (Q2) and the 3rd IF amp (Q3), ahead of the AGC detector (Q7, D11/D12, Q6). It sets how much signal is needed before AGC voltage appears, i.e. where the needle starts. VR1 and VR2 only scale and offset that AGC voltage. Below the T6 threshold they have nothing to show.
- **RF ATT** (owner's manual schematic, Relay unit **X41-1300-00**): the same relay that protects the receiver on TX inserts R3 470 ohm in series plus R1 56 ohm to ground between ANT and the RF unit input, which is about **20 dB**. The service manual and WB4KDI show the earlier X41-1250-00 Relay unit, which has no ATT. The board label in this radio has not been checked yet.

## Tests and results

| Date | Test | Result | Conclusion |
|---|---|---|---|
| 2026-10-31 | RF ATT on 10 m | Seemed to kill reception | Misleading: the SDR display floor was set too high. With ATT on, strong signals are still heard on all bands |
| 2026-10-31 | Moved BPF L3–L14 (80–15 m) and returned them | No audible or S-meter change | BPF not the cause on those bands |
| 2026-10-31 | RF ATT on 40 m | Needle dropped about **9 S-units** | About 20 dB should be about 5 S-units at 4 dB per unit. That works out to about 2 dB per S-unit: **expanded scale**, needle working in a narrow window just above the AGC threshold |
| 2026-11-01 | **IF T6 peaked** for maximum S-meter reading on the internal CAL marker, on 10 m | **Needle came back to life on 10 m** | T6 was off peak, probably since the 11 m undo |
| 2026-11-01 | VR1 (span) reduced about 1/4 turn from maximum; VR2 (zero) unchanged | 40 m readings less exaggerated | Span no longer needs to be at its limit |
| by 2026-11-02 | Moved BPF L15–L17 (10 m) and returned them (approx.) | No detectable change | **BPF cleared on all bands** |

## Conclusion

- What looked like missing gain on the high bands was mostly an **S-meter indication problem**: T6 off peak, so little IF gain before the AGC detector. VR1 at maximum span tried to compensate, which expanded the scale. That made 40 m band noise (just above the AGC threshold) read S6–7 while the quieter high bands (just below it) read S0–1.
- **IF T6 was the key adjustment.**
- After the adjustment, the 10 m needle moves (from S0–1 upward) but still reads a little low in the owner's opinion. It is accepted as-is until proper test equipment is available.

## Pending (with test equipment)

1. Three-point calibration per the manual at 14.175 MHz: VR1 to S9+60 with 50 mV, T6 to S1 with 1.25 µV, VR2 to S9 with 50 µV. Or WB4KDI's 6 dB per S-unit.
2. Check the ATT step (about 20 dB) on the corrected scale, and compare the noise floor across bands.
3. Optional: per-band stage-by-stage injection (ANT, BPF input, Q1 gate, Q2 base, T2) reading the level at the IF, to rule out any residual gain loss on 10 m in Q1, Q2 or the RX mixer.
4. Check the Relay unit board label (X41-1250-00 or X41-1300-00), and R3 and R1 with an ohmmeter.
