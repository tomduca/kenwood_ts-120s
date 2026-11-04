# Kenwood TS-120S: 2026 technical log

Repair and maintenance log for a Kenwood TS-120S transceiver (HF, 8.83 MHz IF). It covers the repair history, the sudden loss of TX in October 2026, the measurements, the conclusions, the fix and the open items.

## Current status (2026-11-02)

- TX and RX working on all bands.
- **S-meter on the high bands largely fixed (2026-11-01):** the key was peaking **IF unit T6**, then backing off VR1 (span) by about 1/4 turn. The RF unit band-pass filters (L3–L17) were tested on all bands and cleared. Fine calibration is waiting for test equipment. Details in [docs/07-s-meter-high-bands-2026.md](docs/07-s-meter-high-bands-2026.md).
- Earlier repair (2026-10-17): a **solder sliver was bridging the collector and emitter of Q7** (RF unit), leaving the Final unit with no drive. The sliver was removed and TX came back.
- **Improvement:** RTL-SDR Blog V4 used as a panadapter, fed from the 8.83 MHz IF through a 9 V buffer amplifier (no CAT). With the buffer the S-meter drops less than 1 S-unit on 40 m (about 2 S-units without it). Details in [docs/08-if-panadapter-output.md](docs/08-if-panadapter-output.md).
- Main open items: post-repair checks (Final unit idle current, AVB under normal drive), RIT, IC meter, S-meter fine calibration, VFO drift, RF GAIN pot, recap of the remaining units and calibration. Details in [docs/06-open-items.md](docs/06-open-items.md).

## Contents

| Document | What it contains |
|---|---|
| [docs/01-repair-history.md](docs/01-repair-history.md) | Chronology of repairs and maintenance, with tables per unit |
| [docs/02-tx-incident-oct-2026.md](docs/02-tx-incident-oct-2026.md) | The sudden loss of TX: symptom, step-by-step diagnosis, root cause and fix |
| [docs/03-measurements-and-levels.md](docs/03-measurements-and-levels.md) | All measurements (DC and SDR levels), nominal levels from the manual and a table for reference values |
| [docs/04-technical-reference.md](docs/04-technical-reference.md) | TX path, Q7, supply rails, idle currents, protections, service bulletins |
| [docs/05-methodology-and-probes.md](docs/05-methodology-and-probes.md) | How it was measured: probes, frequencies, SDR settings, test points and precautions |
| [docs/06-open-items.md](docs/06-open-items.md) | Prioritized open items |
| [docs/07-s-meter-high-bands-2026.md](docs/07-s-meter-high-bands-2026.md) | S-meter on 20/15/10 m: diagnosis, RF ATT analysis, IF T6 fix |
| [docs/08-if-panadapter-output.md](docs/08-if-panadapter-output.md) | Improvement: IF output with buffer amplifier for an RTL-SDR panadapter |
| [docs/reference/](docs/reference/) | Transcriptions of the service manual and RF unit schematic, plus raw OCR of both manuals |
| [img/](img/) | Schematics of the two probes (SVG); IF unit T6 location; IF buffer board photo |

## How to read this log

- Many expected values come from **scanned images** of the WB4KDI schematic and the service manual. Confirm them on paper before drawing conclusions.
- Dates are approximate unless stated otherwise. The loss of TX happened about two days before 2026-10-17.
- RX/TX pairs in the tables are in that order. Voltages are DC unless marked "RMS" or "peak".
- SDR levels are **relative SNR**, not calibrated: they are only useful for comparing points measured with the same gain and the same bandwidth.

## Sources

- Kenwood TS-120S service manual (level diagram p. 36, troubleshooting chart p. 34, adjustments pp. 38 to 40).
- WB4KDI schematics (TS-120S/TS-120V). The actual board has a D8 in the RF unit that the schematic does not show.
- Service bulletins SB-816, SB-832 and SB-844.
- Owner's manual schematic (Relay unit X41-1300-00 with RF ATT).

## Credits

Put together with help from Claude (Anthropic) from a diagnostic session.
