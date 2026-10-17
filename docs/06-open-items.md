# Open items

Prioritized. The secondary problems come from the older summary; the close-out items come from the October 2026 loss of TX.

## High priority: closing out the Q7 repair

1. **Check the parts around Q7:** R41 and R43 (100 ohm, each dissipated about 0.3 W while the sliver was in place), L30 and C57; measure Q8 on TX (base about 2.8 V, emitter 2.1 V, collector 9.9 V).
2. **Check into a dummy load** the power, ALC and IC with moderate carrier, and fill in the reference values table in [03](03-measurements-and-levels.md).
3. **Measure AVB under normal drive.** The pass transistor (Filter unit Q9) is a 2SA755, not the original.
4. **Set the idle current per the manual** (100 mA for the finals with VR2, 150 mA for Q2/Q3 with VR1). About 160 mA was measured on the finals; more idle current means more heat in the Final unit.

## Medium priority: maintenance

5. **Systematic inspection of solder joints and coax,** and of loose solder debris, in the RF unit, the Filter unit and the Relay unit. The radio has a history of cracked joints (Relay unit coax, Filter unit, J41) and now a solder sliver on Q7.
6. **Thermal paste on Q2 to Q5 and the temperature sensors:** agreed to clean and renew without desoldering anything, with the sensors in place, using non-conductive paste in a thin film. Not done yet.
7. **Possible cold joint on the base lead of one of the 2SC2290s** (visible line, no play): reflow only if the surface is dull or has a ring crack; do it with a temperature-controlled 40 to 60 W iron, flux and a heatsink on the lead. Record the base voltage (0.65 V on TX) and the shunt mV (2.4 mV) before and after.
8. **Pending recap:** CAR unit, Counter unit and Final unit. In the Final unit, the bias (C12 and C25) and decoupling (C20 and C37) electrolytics.

## Secondary problems (from the older summary)

9. **RIT unusable** after the recap. Probably a broken wiper wire (RT1) between the front-panel pot and pin 11 of J4 on the AF-GEN. Check continuity with the radio off and J4 disconnected.
10. **Front-panel dual concentric pots (VR1, VR2 and VR3):** replacement. 50K can be used instead of the original 10K/5K with little impact, except VR3 (the RIT section, 5K). The VR2 switch is the critical point for mechanical compatibility.
11. **IC meter** cannot be calibrated with Filter unit VR1: possibly a worn carbon track.
12. **S-meter insensitive on 20, 15 and 10 m:** possible misalignment of L16/L17; re-measure D4 and D5.
13. **VFO micro-drift:** variable capacitor shaft with dirty lubrication.
14. **RF GAIN pot** mechanically jammed: needs replacement.
15. **Full calibration** of IF, RF and S-meter with a generator; BPF alignment on 20, 15 and 10 m; fine alignment of IF T1 to T9 (currently done by ear).
