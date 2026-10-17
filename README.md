# Kenwood TS-120S: 2026 technical log

Repair and maintenance log for a Kenwood TS-120S transceiver (HF, 8.83 MHz IF). It covers the repair history, the sudden loss of TX in October 2026, the measurements, the conclusions, the fix and the open items.

## Current status (2026-10-17)

- TX and RX working on all bands.
- Latest repair: a **solder sliver was bridging the collector and emitter of Q7** (RF unit), leaving the Final unit with no drive (no TX in SSB or CW). The sliver was cleaned off and desoldered on 2026-10-17 and TX came back.
- Main open items: post-repair checks (Final unit idle current, AVB under normal drive), RIT, IC meter, S-meter on the high bands, VFO drift, RF GAIN pot, recap of the remaining units and calibration. Details in [docs/06-open-items.md](docs/06-open-items.md).

## Contents

| Document | What it contains |
|---|---|
| [docs/01-repair-history.md](docs/01-repair-history.md) | Chronology of repairs and maintenance, with tables per unit |
| [docs/02-tx-incident-oct-2026.md](docs/02-tx-incident-oct-2026.md) | The sudden loss of TX: symptom, step-by-step diagnosis, root cause and fix |
| [docs/03-measurements-and-levels.md](docs/03-measurements-and-levels.md) | All measurements (DC and SDR levels), nominal levels from the manual and a table for reference values |
| [docs/04-technical-reference.md](docs/04-technical-reference.md) | TX path, Q7, supply rails, idle currents, protections, service bulletins |
| [docs/05-methodology-and-probes.md](docs/05-methodology-and-probes.md) | How it was measured: probes, frequencies, SDR settings, test points and precautions |
| [docs/06-open-items.md](docs/06-open-items.md) | Prioritized open items |
| [img/](img/) | Schematics of the two probes (SVG) |

## How to read this log

- Many expected values come from **scanned images** of the WB4KDI schematic and the service manual. Confirm them on paper before drawing conclusions.
- Dates are approximate unless stated otherwise. The loss of TX happened about two days before 2026-10-17.
- RX/TX pairs in the tables are in that order. Voltages are DC unless marked "RMS" or "peak".
- SDR levels are **relative SNR**, not calibrated: they are only useful for comparing points measured with the same gain and the same bandwidth.

## Sources

- Kenwood TS-120S service manual (level diagram p. 36, troubleshooting chart p. 34, adjustments pp. 38 to 40).
- WB4KDI schematics (TS-120S/TS-120V). The actual board has a D8 in the RF unit that the schematic does not show.
- Service bulletins SB-816, SB-832 and SB-844.

## Credits

Put together with help from Claude (Anthropic) from a diagnostic session.
