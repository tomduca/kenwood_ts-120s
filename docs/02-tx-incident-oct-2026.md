# Sudden loss of TX, October 2026

## Summary

| | |
|---|---|
| Symptom | No TX in SSB or CW. RX perfect. ALC and IC meters at 0 |
| Root cause | A **solder sliver was bridging the collector and emitter of Q7 (2SC1815)** in the RF unit |
| Fix | The sliver was cleaned off and desoldered on 2026-10-17; TX came back. No transistor replacement was reported |
| Origin of the sliver | Not investigated |

## Symptom

- RX correct on all bands.
- The relays switch and PTT works (via MIC and via VOX).
- No TX in SSB or CW. ALC and IC always at 0, with mic gain and carrier at maximum.
- Into a dummy load, a handheld tuned to the frequency, right next to the radio, hears nothing.

## Context

- The radio had been transmitting normally, on all bands and modes, until about two days earlier. The loss of TX was sudden.
- All the work in the [repair history](01-repair-history.md) predates it.
- The diagnosis was done with a multimeter and an SDR, using the manual's level diagram as the reference (see [methodology](05-methodology-and-probes.md)).

## Root cause and why it produced that symptom

Q7 is the first TX amplifier stage after the BPF: an emitter follower with its collector on the TX supply and its output taken from the emitter towards Q8 (see [technical reference](04-technical-reference.md)). With the collector and emitter joined by the sliver, the emitter sat at the supply voltage and the output signal was shunted to ground through that supply's decoupling. Only what couples through stray capacitance got through, about 40 dB down. Since Q7 is powered only on TX, RX was unaffected.

With no drive, the Final unit draws its idle current but receives no signal: the current does not change with the carrier, the ALC and IC meters stay at 0 and there is no output power.

## How the cause was found (diagnosis timeline)

| # | Step | Result |
|---|---|---|
| 1 | Power supply | 14 V stable; current draw RX 0.73 A and TX 1.87 A, not changing with the carrier in CW. AVB: 0 V on RX and 11.3 to 11.4 V on TX (11 V regulator, normal) |
| 2 | DC in the Final unit | Bias of Q1, Q6, Q7, Q2/Q3 and Q4/Q5 consistent with the schematic; collectors at 13.8 V. The measured idle current (about 160 mA) is somewhat above the manual's 100 mA |
| 3 | Signal in the IF | Carrier and modulation visible on the SDR. From GEN to TIF there is no loss relative to nominal (GEN 68 and TIF 48, gain 25.4): the IF unit, its ALC, D9 and the relay are fine |
| 4 | Mixer Q5/Q6 | Gates from -3.0/-3.34 V (RX) to +0.67/+0.77 V (TX), source from 0 to 1.0 V, drain from 13.6 to 12.7 V: it conducts, and the bias switching (Q10) works |
| 5 | SDR levels at 7074 kHz | C52 58; BPF output (C54, Q7 side) 50; J34 ANT 5 and MKR 2; DRV 12. The BPF passes the signal (about -8 dB), there is no leakage towards the antenna, and from C54 to DRV about 43 dB are missing relative to nominal |
| 6 | Q7 DC on TX | Base 2.0 V, collector 5.68 V, emitter 5.68 V (expected: about 1.8 / 11 / 1.1 V). Collector and emitter at the same voltage: they are shorted together. The base matches the R42/R40 divider with the collector at 5.68 V (about 2.07 V) |
| 7 | Repair | The solder sliver joining collector and emitter was cleaned off and desoldered; TX works again |

## Ruled out, and on what evidence

| Hypothesis | Evidence against |
|---|---|
| Power supply, fuse, main supply | 14 V stable, RX normal |
| AVB line and its switching; patched cable | AVB 11.3 to 11.4 V on TX at the Final unit and at the RF unit |
| Final unit bias | Values close to the schematic |
| Final shorted C-E | RX normal with a stable supply |
| Open finals | They conduct at idle (about 160 mA); from DRV to PO there is about +42 dB (nominal about 47) |
| IF unit (modulator, filter, ALC, D9, relay) | GEN to TIF with no loss |
| RF unit TX bias (Q10, KEY, D6/D7) | Q5/Q6 gates switch as per the schematic |
| BPF and diodes D2/D3 | C52 to C54 loses about 8 dB; no signal on J34 ANT and MKR |
| DRV cable | DRV at the RF unit and at the Final unit match |
| Relays (IF, Filter) | The signal passes through the IF relay and D9 at nominal level; RL1 is after PO |
| Thermal protections | AVB present on TX |
| Regulators out of range | AVB 11.4 V, -6 V correct, mixer and Final bias in range |

## Lessons from the diagnosis

- The ohmmeter in circuit is misleading (finals, Q2/Q3, collectors): the transformer and neighboring resistors give low or open readings even when the transistor is fine.
- A signal picked up by proximity (loop or probe) does not prove power or that the path conducts. A break still lets about 40 to 60 dB through by stray coupling.
- SDR SNR is not linear. Only compare points measured with the same gain and the same bandwidth, and each point at its correct frequency (IF at 8.83 MHz; RF at the operating frequency).
- The manual's level diagram (p. 36) was decisive: comparing the differences between consecutive points with the nominal ones locates the broken section.
- The DC voltage on each pin of the suspect stage confirmed the cause in a way the signal could not.
- Before swapping parts, inspect the pads of the suspect stage with a magnifier: a loose solder sliver explained everything.
- AVB measures 11 V (not 14 V): it comes from an 11 V regulator.

## Mistakes made during the process (so as not to repeat them)

- Q8 to Q13 in the IF unit were treated as the TX chain; they are the noise blanker (NB). The TX path goes through Q1 of the IF, and CF1/CF2 belong to the RX path.
- D6/D7 were thought to provide Q7's bias; the bias comes from R42/R40.
- The finals were assumed to be open based on in-circuit ohmmeter tests.
- The 15 mohm resistor was measured with the lead in the Amp jack: a dead short, a spark and a melted lead (the radio was not damaged).
- Readings at J30/J32/J35 were taken at the wrong frequency (the operating frequency instead of 8.83 MHz); they were repeated.
