# TS-120S service manual: raw OCR (all pages)

> Text obtained by automatic OCR (tesseract) from a 100 dpi scan. It has many errors, especially in tables, schematics and the parts list. Use it to **search** for references (part numbers, component names) and then confirm against the original PDF 'TS-120S Service Manual.pdf'. The reviewed transcription of the important sections is in [../service-manual.md](../service-manual.md).

---
## Page 1

```text
KENWOOD

SERVICE MANUAL

Model TS-120S
VFO-120 SP-120
PS-30 AT-120

TS—120VvV

ENCLUDES SCHEMATIC ONLY FOR
THIS VERSION OF THE TS-120S

HF SSB TRANSCEIVER

```

---
## Page 2

```text
CONTENTS

SPECIFICATIONS 88ers cere tas eeenanscersssesseeseeree a

SPECIAL COMPONENTS DATA 3

4

4

4

CIRCUIT DESCRIPTION Ss

FUNCTIONAL DESCRIFTION .. 6

OUTSIDE VIEWS..............-......08 we 10

BIDE VIEWS. cee cette te esses ttaaeeees er sindddcertesseserercree 11
PC BOARD/CIRCUIT OIAGRAME

RF UNIT (444-4260-01),....... cere scseereserseeseere be esaseserreessens 12

UF UNIT XAB-AZTOOD)srecscsesstecnpesesncneeseeneerssaneneeeesaces 12
SWITCH {A} UNIT {X41-1140-00) ........
SWITCH (8) UNIT (X41-1180-00) .
RELAY UNIT (X41-1250-00}
AF*GEN UNIT (048-1190-01} ..00..00..0.ccccceteeeeereeeerrererrrisene
PLL UNIT (X80-1490-00) ...........
COUNTER UNIT (X64-1360-00] .
VEO UNIT (X40-1130-O0) oon eee ccseeeeecceeeeeeeeerernee 18
CAR UNIT (X60-1600-00) .......
FILTER UNIT (X51-1200-00)
FINAL UNIT (X86-13B0-00) ....

PARTS LST........... deeeee ptances, °

PACKING/DISASSEMBLY...

EXPLODED VIEW/OISASSEMBLY ......... eceeceenate 90
TROUSLESHOOTING................. seemesvscisnetadosnigisssmacsssssesie BS
LEVEL DIAGRAM... : Ty

ADJUSTMENTS...
TEST AND ALIGNMENT SET-UP
PS-30 :

BLOCK DIAGRAM...

SCHEMATIC DIAGRAM... ccceccsseeersrrseeteererersseeneeceerens
AT-126...
M&-100..

```

---
## Page 3

```text
SPECIFICATIONS/SPECIAL COMPONENTS DATA

Frequency Range:
80 m band
40 m band
20 m band
15m band
10m band A
10 m band B
10 m band C
10 m band D
WW

Mode:

Power Requirements:
80m~
15 m band...

10m band

Antenna Impedance:
Carrier Suppression:

Sideband Suppression:

Mic. Impedance:
Audio Frequency
Response:
Harmonic Radiation:

Receiver Sensitivity:
Image Ratio:

3.5~4.0 MHz
7.0~7.3 MHz

. 140~ 14.35 MHz
. 21.0 ~ 21.45 MHz

28.0 ~ 28.5 MHz
28.5 ~ 29.0 MHz

. 29.0 ~ 29.5 MHz
. 29.5 ~ 29.7 MHz

15.0 MHz (receive only)
SSB (A3J), CW (AT)

200W PEP for SSB operation
160W DC for CW operation

160W PEP for SSB operation
140W PEP for CW operation

502

Carrier better than 40 dB down
from the output signal

Unwanted sideband is better
than 50 dB down from the output
signal

5002 ~ 50k2

400 ~ 2600 Hz (—6 dB) j
Better than 40 d8 down from
output signal.

O.25uV for S/N 10 GB or better
Image frequency better than 50
dB down from the output signal

@ Application

2SC2290 (HF power amplifier) (VO3-2290-06)

SPECIAL COMPONENTS DATA

IF Rejection:

Frequency Stability:

Selectivity:

AF Output:

AF Load Impedance:

Power Supply:

Power Consumption:

{at DC 13.8V):

IF frequency is.70 dB or more

down from the output signal.

Within 100 Hz during any 30

minute period after warm up.

Within =1 kHz during the first

hour after 1 minute of warm up.

SSB. CW 2.4 kHz {—6 dB)
4.2 kHz {—60 8)

More than 1.5W (82 load, 10%

distortion}

4 ~ 162 for both speaker and

headphone.

12 ~ 16V OC (13.8V)

Less than 18A in transmit (less

than 1:5 SWR ratio)

Less than 0.74 in receive

Semiconductors and Tube:

IC's
FET’s...,
Transistors
Diodes....
Display Tube
Dimensions:

Weight:
NOTE:

26
16
90

| 142

1
W 241(241) x H 94(108)
xD 235(281) mm
(With Projection)
Approx. 5.6 kg (12.3 Ibs)

The circuit and ratings may change without notice due to
Gevelopment in technology

@ Indicating tube 9-BT-12 (V40-7760-86)

NPN Epitaxial planar transistor Si
@ Absolute maximum ratings (.
item | Pe Ven Ves Ve80 «IG IE Tste A ;
_ 1 2
Value| 175 (Wh 45 1¥) 45 (Vv) 4.0(V¥) 20 (A) -20 1A) -65~175 (°C) como
(To=25t) Uh =)
‘l) if}
— 4
<—
oa Dh:
Op
@ Application =
2S5C2509 (HF power amplifier) (VO3-2509-06}
NPN Epitaxial planer transistor Si PIN NO t]2)3]4]s] 6] r[e| 9] solsspi2) pe
@ Absolute maximum ratings connection | F [Ne] Ge) ne |e] Ge) a | ¢ [er] | s |e] ne ne
§5:/06) 17/18) 99/20) 21/22/23) 24/25) 26/ 27| 28
G: a [00 | 2 {
Item | Pe Ves Vees Veeo Views 10 ie Tstg Salter |es|oo| ol « [> Ise] kerio vol F
Value] _20(w)  0(v) 40¢v) 18(v) a(v) (A) —S(A) —55~150(%)
(Tco=250)
```

---
## Page 4

```text
FEATURES/GENERAL INFORMATION/YK-88C

FEATURES

1, SINGLE CONVERSION SYSTEM USING PLL
CIRCUITRY

The single conversion system. with a unique PLL Phase Lock

ed Loop circuit, FET balanced mixers and MOS FET'S

assures excellent spurious and intermodulation

characteristics

2. BUILT-IN DIGITAL DISPLAY
The digital display affords easy reading of operating frequen-
cy to an accuracy of 100 Hz, on any band and any mode.

3. BUILT-IN SHIFT CIRCUIT (Passband Tuning)

An IF SHIFT system is built in to the transceiver to allow shif-
ting of the IF passband, thereby eliminating adjacent channel
interference,

4. 3.5~29.7 MHz AND WWV BANDS

The transceiver is designed to operate on LSB/USB/CW in
the 3.5~29,7 MHz bands. WWV (14.5~15 MHz) is also
built in to the transceiver to permit accurate frequency
calibration.

5. COMPACT, LIGHT-WEIGHT DESIGN

The TS-120 has many advanced features, yet it is compact
and light-weight and suitable for mobile and field operation
as well as fixed station operation

6. EASY OPERATION
All controls and switches are carefully arranged for ease of
operation, ensuring convenience and versatility.

7. ALL SOLID-STATE DESIGN
The all solid-state, compact unit features a wide band final
Stage, eliminating the need for peaking controls.

8. FOUR FIXED CHANNELS

Four FIX channels can be installed, one for each of the 7. 14.
21 and 28 MHz bands. The 3.5 MHz and 28 MHz fixed xtal
position can be exchanged by simply moving a connector on
ihe AF-GEN unit

9. FULL RANGE OF AUXILIARY FUNCTIONS
The TS-120 is equipped with VOX. balanced gate noise
blanker and a 25 kHz marker.

10. OPTIONAL CW FILTER YK-88C

The TS-120 permits use of the optional YK-88C CW filter.
CW semi-break-in operation is provided using the built-in
VOX and CW side tone circuits

11. WIDE VARIETY OF OPTIONAL ACCESSORIES
The following optional accessories are available:
Regulated Power Supply (PS-30), Mobile Mount (MB-100},
CW Filter (YK-88C), External VFO (VFO-120), External
Speaker (SP-120}. and antenna tuner AT-120

GENERAL INFORMATION

Page 49 shows a block diagram of the TS-120 HF Amateur
transceiver. It employs a single-conversion system with PLL
circuitry. The IF is 8.83 MHz,

The TS-120 features a number of unique circuits and overall
high performance. It is designed so the PLL lock frequency
of each band, the CAL marker signal, and the counter clock
circuit use @ single reference frequency crystal instead of in-
dividual crystals as found in the TS-820 series transceiver.
Circuits include IF SHIFT, VOX (with semi-break-in CW), side
tone. noise blanker (NB), and crystal calibrator (CAL) for con-
venient and versatile ansceive operation.

YK-88C SPECIFICATIONS

Center frequency: 8830.7 kKz

Center frequency
deviation:

Passband width:

Attenuation band width:

Ripple:

Minimum loss:

Guarranteed attenuation:

Less than +150 Hz (6 dB)
500 Hz —6 dB

1.5 kHz (—60 dB)

Less than 2 dB

6d822dB

Less than +2 kHz ~ +1 MHz
More than 80 d8

Terminal impedance: 6002 +5%, 15pF +5%

|
|
3—4—f
|

LOSS 5.848

) IMPEDANCE |
| 6002 15pF |

L
s z
——__|

1s “1 — oS ° +s -4 $15
8630. 7kHz
FREQUENCY(kHz)

YK-88C filter attenuation characteristic
```

---
## Page 5

```text
CIRCUIT DESCRIPTION

RECEIVING CIRCUIT

The signal from the antenna is fed to the 8.83 MHz IF trap
circuit. This signal is stepped up about 10 dB and im-
pedance-converted by a wide-band transformer before it is
applied to the bandpass filter (BPF). The BPF is common to
transmission and reception. eliminates the need for a
preselector, and makes the RF section compact in design
The signal from the BPF is fed to the dual-gate MOS FET
wideband RF amplifiers consisting of a 3SK74 (Q1) and a
2SC1815 (Q2). where the 2 MHz to 35 MHz signal is
amplified about 20 dB.

The RF amplifier output passes through a wide-band
transformer to the input balanced transformer of the
balanced mixer (two 3SK74s, Q3 and Q4). where it is mixed
with the VCO output from the PLL and converted to the 8.83
MHz IF. This signal is applied to the IF unit, through the
ceramic filters, NB gate circuit and the crystal filter. The NB
circuit is controlled by the NB switch on the front panel,
The signal, passing through the crystal filter. is amplified
about 90 dB by the three-stage 3SK74 MOS FET IF amplifier
(Q1, Q2. and Q3) and is demodulated into audio by the
four-diode ring detector

From the final IF stage, the signal also passes through a
buffer amplifier and is fed to the AGC circuit where it is
detected and amplified. Receiver gain is controlled by this
AGC voltage applied to the second gates of the RF and IF
amplifiers, with the time constant determined by R38
{2.2MQ) and C40 (1pF). Inout levels of 2 dB and 34 GB are
indicated as $1 and SQ on the S-meter. The AF signal is
amplified by Q1, a 2SC2240 (GR). gain controlled. and
further amplified by an HA1366W (Q7}, the power-amplifier
IC, to to drive the speaker. This signal, which is tran-
sistor-coupled with Q14, a 2SC1815(Y). and Q15, a
2SA1015(Y), is sampled for ANTI-VOX control, so the VOX
circuit is not ipped by the speaker output. This new system
is @ departure from the conventional transformer-coupled
sampling systems.

TRANSMITTING CIRCUIT

The microphone signal is amplified by transistors 018. a
2SC2240(GR), Q10. and Q11. each a 2SC18151Y), and is
fed to the four-diode balanced modulator (BM) circuit.
Microphone impedance is 5002 to 50k2.

The 8.83 MHz DSB signal! from the 8M is amplified about 10
dB by Q12, a 2SK19 FET. and is fed to the IF unit where the
unwanted sideband is removed by the crystal filter to
produce an SSB signal. The gate of 012 is also controlled by
the protection voltage which is developed when the
transmitter output looks into an incorrect load, continuously
reducing output power. The SSB signal from the crystal filter
is amplified about 30 GB by the 3SK74 IF amplifier (Q1), and
is fed to the transmit 3SK74 MOS FET balanced mixer (Q5
and Q6), where it is mixed with the VCO output and con-
verted to the final transmit frequency.

Unwanted spurious components are eliminated by the
transmit/receive BPF circuit, and the signal is
wideband-amplified by Q7, Q8 (2$C1815). and Q9
(2SC2086)

In the final unit. the signal is amplified by the 2SC2075
driver (Q1), and by the 2SC2509 push-pull power amplifiers
(Q2 and Q3). Then the signal is amplified by the 2$C2296
push-pull power amplifiers (Q4, 5). The signal then passes
through an RF filter and is fed to the antenna.

Antenna output is toroid-sampled to detect the forward and
reflected power. The forward power is used for ALC and the
reflected power for protection. Forward power is fed to the
second gate of the 3SK74 transmit/receive IF amplifier (Q1).
with a time constant determined by R4 (1.5 MQ) and C25
(0.47 pF). For CW operation, block bias keying controls the
base circuit of the 2541015 switching transistor (Q10) in the
RF circuit. Q10 controls the first and second gate voltages of
the transmit mixer (05 and Q6}) ane the base voltage of the
predriver (Q9}
```

---
## Page 6

```text
FUNCTIONAL DESCRIPTION

TS-120S FREQUENCY SYSTEM

The TS-120S employs single conversion with a unique PLL
circuit. as shown in Fig. 1.
The frequency system is basically that of the TS-820 with the
exception of the PLL circuit.

PLL CIRCUIT

VCO output is obtained by synthesizing the 10 MHz and 500
kHz reference, from the counter. and the VFO and CAR in-
stead of a separate HET crystal circuit for each band the TS-
120 uses the counter reference oscillator, and a program-
mable divider circuit contained in the PLL. This simplifies cir-
cuit design and eliminates changes in transmit/receive fre-
quency due to HET crystal frequency deffrences. Fig. 2
shows PLL circuit construction and Table 1 shows the fre-
Quency in each circuit

Referring to Fig. 1. MIX (3} combines CAR and VFO signals
and is operated straight through to mixer (1) on 3.5 and 7
MHz, MIX (2) operates at 14 MHz and above with the
output of MIX (3) to provide mixer (1) input. as shown in

Table 1. MIX (1) output is filtered, amplified, shaped and
divided by the programmable divider to obtain 500 kHz
output.

The programmable divider converts the information from the
band switch into a BCD signal in the counter. By presetting,
the signal is divided at the ratio shown in Table 1. The phase
comparator is a Motorola MC4044P. The loop filter
amplifier, component transistors, minimizes unwanted
Spurious signal. If output of the phase comparator unlocks
for any reason. VCO output is switched off to prevent out of
band emission and, simultaneously the digital display blanks

CAR OSCILLATOR

The CAR oscillator contains one oscillator and two crystals
for LSB, USB. and CW operation. The oscillator frequency in
each mode is listed in Fig. 1.

Oscillator frequency can be varied by the IF SHIFT control
during reception

FROM RF AMP fata.”
: XTAL fe
MIXtRx REO) XT AL if AMP DET A
PLL UNIT 2 PEE she cl
Pi i od 7 i
vco MIXd1) H |
1.00 i 1 |
I asumz}  ewin I | USB 6.8315 MHz
| or 20 MHz H | LSB 8.8285 MHz
(21.20 Cw (R} 8.8315 MHz
PI MIxX{2)
ice brid eal Fa CW (T) 8.8307 MHz
|
| S00KK: Paes 14.33~14.83 | xt
DIVIDER | Fi ‘ }—{D}— 12.8315)
| " ame | Ber mixta bet caR Osc
hid I | +O} t¢.szes)
| 1 4 i x2
ip cas reel DE eee a es | IF SHIFT
— "
1OMHz 7
S5-6.0MHz
SOOKHz COUNTER woth stav/agc | “°°
UNIT switch to SEND
1 wees gon
apr
MIXITX) iF ame Pron BM MIC AMP

‘— Common to Rix snd Tx. ——

Fig. 1 TS-120 Frequency configuration
```

---
## Page 7

```text
FUNCTIONAL DESCRIPTION

AX, TX MIX(1) MIXI1)
Frequency vco Input Output

ww 14.5 23.33 2433

Band Owider [DC BA

~150 | ~23.83 |~24a3 | '° Vz.. 10119
as | 12.33 | 14.33

35 | L409 |~1283|~1483| 2° v4 |1100
70 «| 15.83 | 14.33

Ul beer sal bern eere oe ear va |1101

14, [140 | 22.83. | 24.33 15 va ft 104

~145 | ~23.33 | ~24.83

210 | 2983 | 3433
21 | [215 |~3033|~3a83| 45

28 28.0 36.83 34.33

ve jo1ii

~28.5 | ~37.33|~3483| 7° Ue a
206 | ES) | 378 )| She, | '30 ve 11010
201] 280 eee (9532 | 3.6 v7 j1001
aos | 295 | 3833 | 3433 | yy we il 0 °0

~30.0 | ~38.83 | ~34.83

Table 1 The frequency chart

VFO OSCILLATOR

The TS-120 VFO oscillator has been developed on the basis
of the TS-820 and TS-520 VFO. It is physically smaller. and
its operating frequency has been raised to cover 5.5 to 6.0
Mkz, Is
During CW operation, transmit frequency is shifted approx.
800 Hz above the receive frequency. CW shift is also digital-
ly displayed

The main tuning dial covers 25 kHz per revolution and is
calibrated at 1 kHz intervals. A 10 kHz subscale is also
provided. The operating frequency can be read easily from
either the analog or digital display

DIGITAL COUNTER

The TS-120 digital counter employs a VFO frequency coun-
ting system as shown in Fig. 3.

The VFO frequency is mixed with a 5 MHz signal obtained
from the reference oscillator chain by a 3SK73 (Q7) and is
coverted to a 1 MHz signal. This signal passes through the
LPF. is amplified. buffered and shaped into a square wave.
passes through the 0.1 second gate Circuit and is applied to
the four-digit counter. The signal is counted from 10 Hz to
100 kHz and fed to the preset counter deriving the carrier
output.

The 100 kHz order digit presets “5” or “O” to display the
operating frequency

The 1 MHz and 10 MHz order digits are composed by diode
matrix operating on bandswitch information

The counter outputs are switched by the multiplexer and are
converted from 8CD to seven-segment information by the
decoder to light the fluorescent display tube

The 10 MHz signal from the time-base reference oscillator is
divided to produce gate, latch, and reset pulses which are fed
to the counter. The 10 MHz and 500 kHz signals are fed to
the PLL circuit

The marker circuit produces 2 100 kHz signal which syn-
chronizes the 25 kHz multivibrator to obtain a marker signal
as accurate as the reference frequency. The anelog dial can
be accurately calibrated to the marker signal

The 1/10 division at the first-stage count-down chain uses
low-power Schottky TTL. while the remaining divisions are
made by a CMOS IC for low power consumption and
minimum spurious emission.

Because of the IF SHIFT circuit, the CAR frequency is in-
dependent of the transmit/receive frequency. Once the VFO

(2243-2263) (2983~90.321 3683-38 84) 115.93-16 33) (12 33~12 43)
as veo

1a WN VED 21 veo 28 ¥CO ? veo

Bur utt
Os Q7 ft Approx. 10 MHz

autt Butt Ame Pee Mix

O14 Qr0 < On ae
1

Qisva Qs ve

a6 J
a T4LSI63 ————
Dy

1S
Loop filter L]

(Se va
oz OT) Qi | Lia oop 1 * p92!
Lille << Hife bow | SEO,

S00KH: fe27 i

[sees

Fram Counter
(BCD sgnall

Unlock dotectar
Phase detector

VCO output

eal 25,7
= Es 6 vro
Divider <G| 7 Tt pe SS5G0MNT
HL or fe

21,20 t can

- 343273483 aa SMe

VCO OFF signal

Tuning coil
ww, 14 SOMH:
sae, Fowl -
3 z& 21,28
3 Q24, Q25
FE J 20 Mz 2505 Ze0
3 aon Dose

Fig. 2 TS-120 PLL circuit configuration

```

---
## Page 8

```text
FUNCTIONAL DESCRIPTION

nezme

Poe ps ee A

0s ee
= cnnenanen

Fig. 4 Timing chart

sovsenuca weuilles ¢— G98

seu wowtos

seen 24-90

pessiose
Wap

Anoay—

i
THD 9~S'S ANNI OFA

TnGT OOS

anorHAaT

woes SuySuey9
ge} 29220592 ABHGD1
38 a. $19) w01 By.
brrde z
4 38 zx
Govsaas 4) we (ronajag te ~ 4) ° 38 (a
Cunning Sunpamng vonup whi z. 108K
ABSIOFDL SB 0eD1 BIE DL PHIL :
anor ie —r oti 648
"mou
Bufueuy
OHNE -
69 ty
5 2 SF S/S vowewsoyy Cayueyg z
i 8 6 £ z 3 opp Zt
az 5 z
e* “in
eS Gur , ~~ yl rr
i; ae iteoten F La sreutys BuBom 2619 what
= ino¥¥o zg
(otuey> ab ~~ ~
Cangas 7
ayunoa
oubiarod NIL ABHOTDL
sor aor en
3 z- osine yey o6)nd jasoy BP ssina waoy
z| 133
Fs = our yaa)
e| |3¢
1 a =
5 3
| i mera ee gs (2.)3
ese] osx]s
3 |e v= 48
; 2 : nu
: Geass
xUnew opaig +
: en 4 ah | q 4a
ABH % Tonya sipemuds | a
SVTIS VII 3 Prt bo
Te Suu
ofa
ss209 1% SBGISrDL AONE AOROGDL NOES WINS 2
new ape yun yp woad wor THO re) oT) eo THS001 29 THE eT)
smpwup Z/L J3PMP OOL/L s0RIMP OOL/S sOpeIP OL/L PM OL/L

oS0

Fig. 3 TS-120 Counter circuit configuration
```

---
## Page 9

```text
FUNCTIONAL DESCRIPTION

frequency is counted. the operating frequency is indicated as
accurately as the 10 MHz reference oscillator frequency is
calibrated to WWV. Operating frequency is indicated ec-
curate to the 100 Hz order. regardless of the band or mode.
if the VFO output varies (beyond the band edge the 1 and 10
MHz digits disappear and a blanking signal is developed.

Operating band Blanking frequencies

3.5 MHz more than 4.000.0 MHz

7.0 MHz less than 7.000.0 MHz
14.0 MHZ oes less than 14.000.0 MHz
21.0 MHz.....0...... than 21.000.0 MHz
28.0 MHz........... ee than 28.000.0 MHz
28.5 MRzZ......... . more than 29.000.0 MHz
29.0 MH........... than 29,000.0 MHz
29.5 MHz than 30.000.0 MHz

PROTECTION CIRCUIT

Fig. & shows the TS-120 protection circuit. When the
transmit output load varies. the toroid in the final circuit
samples reflected power. It is then rectified and amplified,
producing @ protection voltage to control the 2SK19 (Q12)
on the AF-GEN unit, so transmitter output is continuously
reduced.

FILTER UNIT

1. ALC: Protection circuit (VSWR)

The protection voltage picked up by L18 in the filter unit is
amplified by Q1 {2SC1815). then applied to the ALC line to
control the output voltage

The ALC voltage is amplified by Q3 (2SC1815). For the 28
MHz bang. the output power is lowered to 50W by applying
BAND information to the B terminal so that Q2 controls the
emitter voltage of Q3. For mobile operation. the power out-
dul is lowered to SOW in all bands by grounding the PO ter-
minal of the filter unit so that the power down circuit for 28
MHz band is operated

2. Fan drive circuit

The output of the thermistor detecting the temperature of the
final unit is applied 10 O6 (2SA562) via Q7 and Q8, so that
Q6 is switched to operate the fan. The fan starts to rotate at
about 45°C although the operating range shown in specifica-
tion is 30~60°C. It stops when the temperature drops to a
level 5~15°C lower the start temperature, This circuit
operates regardless of ransmission or reception because it
detects the temperature of the heat sink.

3, AVR circuit

The 11¥ AVR consists of Q4. Q5 and Q6. The regulated
voltage is supplied to every unit except for the fan drive cir-
cuit during transmission, The fan arive circuit is always
supplied with the regulated voltage regardless of transmis:
sion or reception

4. Filter circuit
The filter is a 2-stage constant K filter (3-stage for 3.5 MHz
band).

FINAL UNIT

1. Temperature protection

1 Core temperature protection
operates when the output transformer temperature ex-
ceeds 120°C.

2 Operates when the heat sink temperature exceeds
90°C because of some defect
When either of the above protection systems operate,
the AL circuit in the AF GEN unit is turned OFF and the
unit is forcibly placed in the reception mode and
transmission is inhibited. The protection circuit
automatically recovers when the temperature drops to
the normal level (i.3., the temperature drops by about
40°C).

2. Temperature detection by the fan drive circuit
The heat sink temperature is detected by the thermistor TH3
to control fan operation

VAS SO« 1B)

VEL SORE)

c29.047]
ttt

```

---
## Page 10

```text
OUTSIDE VIEWS

Front glass {A} Dial scale (A) LED PR21120 Knob (Inside) x 3
{B10-0612-04) ] (B20-0810-04} (v11-7260-66) (K23-07 10-04)
Name plate 7
(B43-0621-04) (k)(Ww)——— Be neg caret 3
{B43-0620-04) (7)

Meter

(B31-0618-05)

Indicating tube 9-BT-12 = * oe -. . - __ Case (A)
{V40-7760-86) — (A01-0743-02)
Front glass (B) h

{810-0613-04) pe

Pe knob i} ‘ane

(23-07 1108) ) {(A20-2330-05}
(MODE SW}

Paddle switch

{STBY Sw) Case (8)
(S44-2402-05)

(401-0740-02)

4P Male socket {MIC}

Seesaw switch (POWER)
(E06-0451-05)

($36-2402-05)
5 Foot
Jack (PHONE:
ra 1"0034-26) = (JO2-0323-05)
Push knob (Square) x 6 ert Main knob Dial scale (B} _____. Pointer knob large BAND
{K29-0709-04) {K21-0722-04) {820-081 1-04) (K21-0723-04)

Heat sink VOX knobs x 3
{FO1-0735-03) (K23-0712-04)

__8P DIN Socket
(E06-0851-15) (EXT VFO

Panel ass'y
{A20-2349-03) US jack (EXT. SP}
(E11-0402-05)

M type receptacle {ANT}
{£04-0152-05) Cap

(J42-0038-04)

Wing nut

7P DIN
(N14-0509- 05)

Socket
{E06-0751-05)
{REMOTE}

Fan Cable {with DC cord),
(E30-1 4
‘30-1632-05) 6P square socket
{E06-067 1-05)
(POWER SUPPLY}

Fan motor
{740-0301-05)
Fan

(FO9-0405-05)

Motor housing Heat sink cover 3 pole phone jack (KEY)
(F29-0406-05) (FO7-0826-03) = (E11-0005-15)

10
```

---
## Page 11

```text
INSIDE VIEWS

TOP VIEW

AF GEN unit
(X49-1110-01)

Counter unit
(X54-1360-00}

Final unit
(X56-1350-00)

Filter unit
(X51-1200-00)
VEO ass'y unit

(X60-1070-00)

CAR unit
(X50-1500-00}

RF unit

Relay unit
(X44-1260-01)

(X41-1250-00)

BOTTOM VIEW

IF unit
(X48-1210-01)

‘Switch (A) unit
(X41-1140-00)

Switch |B} unit
{X41-1150-00)

PLL unit
{X50-1490-00

```

---
## Page 12

```text
PC BOARD VIEWS

Ene : F ae 7 ;
Q1,3~6. SSK74(L), Q2,7,8:2SC1815(Y), Q9: 25C2086, Q10:2SA1015(Y)
D1,3,5:181587, D2,4:1$2588, D6,7: 181555 is

ee
Kae l Ww
& xd pon
1s a, i :
a €° DS 36 5

2SC2086 2SA1015[Y) 2SC460(B) 2SKI9(Y) 2SK30A(0) 3SK74(L)

2S8C1815(Y) 2SK19 (GR) oe
2SC1815(GR)
Vv IF UNIT (X48-1210-01)
Daa 01~4,6,8
= 14181587
05,7
1181007
09,10,13,
17~32
2181555
Dit, 12,14,15
tiN60
DI6? MV13
$3 Ne sw
(SWITCH 4 UIT)
eat |
}
fe
Qin3s: SSK74(L), Q@4! 2SKi9(Y)
5 Q5:2SC1815(GR)
TTI Tish E23} S31 Q6,7,12, 13: 2SC1815(Y)
Seezeges ae fa] Tike = “© 98: 2SK19 (GR)
$1 ep $I pI foe Q911: 28C460(B), 014: 25K30A(0)

12
```

---
## Page 13

```text
vy SWITCH (B) UNIT

PC BOARD VIEWS

¥ SWITCH (A) UNIT

RELAY UNIT

(X41-1150-00) (X41-1140-00) (X41-1250-00)
= loey 7 | oul Pa: Le
4 | pal Sess Tee eS
| t PL2 co iT ener.
1 i = | ! ab afer 4
ed Bac lg ft ‘3 rol a, ib
H Ls 4,0 Jo (TH fhe
ri: L“¢) irae & bi si Stud
urwun by fe da 2 Prana
"na? g2x] es | pa
vy AF, GEN UNIT (X49-1110-00) Eek Q1:2SC1959(Y) 01,2:181555
O1 181585
tonten & oats - h
5] * eg ooh i —
Liviiti
a et: a Hod I
= an aetast Fe s pus ex
Sl ee ee ;
Hin suka L- Bs ot nc 3
epee) ef TE SRS 4 S00 25
FEE) | SI == = |

Q1,18: 2SC2240(GR)
Q2: yPCI4305H, Q3:2SA473(Y)

064 <7P Ces <7 com ot

> FSS 18K Bye
T 3. ae
Asiee st gel.

a a

cers
Ae
Ale tes 20P

8 cs +
ach
220 KW
im

50 22P

S

03

2 hte
Re

OST RI0 47K
cw
1
Bre

its
dk

eu?
2 Tet Zor
3
aye
nae
|

Q4~6, 10,11, 14,16,17,19,20,23,25 > 2SC1815(Y), Q7:HAIZ6E6W, 28,135 2SC4601B), Q9: 28C19591Y)

Q12. 2SKIS(GR), Q15,21: 2S5A1015 (y),

D1n4,11~14, 23, 24,26: 1N60,

”

2SA1015(Y) 25C1959(¥)
2SC1815(y) 2$C22401GR)
2SC1815(GR)

O05 ' wz-061,

2SK19(GR)

Q22° 2SC1815(GR),
06~9:1S2588,

2SA473(Y) 2SAS562(Y)

015°1S1587,

— Gx. ——
“SE : =e : 8

2SC460(B)

24° 2SA562(Y)

4
” I 144—4
= Z| eH
cm
| i “18
seg wo
c.0Mes7 sex
BO Bigs Pts,
T “>
zk
aay
B86,
a
w
Di?~ 22,25,27,28 | 1$1555

uPCIS305H

HAIZ66W

13
```

---
## Page 14

```text
CIRCUIT DIAGRAM

v PLL UNIT (X50-1490-00)

loyracase + 9'tD
‘BASZSE aia dPhOVON | 020 Oirase : £20
WESASE > EL'LE 6 's'50 NESS Tee | alo (ais224asz + ot BLO
&2 tt AOIS TET sto (algignase : 421260
4951S) “Lt bl “et B'90 sssist: Peed ACLGOLNS | 92210 (AIGGELISZ + ‘
»
824 Bo : lelogyasz * E
10] Lore Sh neh ad | RE ae ene poe q
I +
!
» ty r 9
if z Rs é h
bo.
7 .
|_| _| ree” E 4
1
3] : '
wags
cl P|
Iebtr iy
oe '
x i
wes
Lt mo
a 4
*)
1
ft |
1
1
!
‘
'
'
|
1
'
'
‘
1
1
'
|
1
1
1
1
i}
|
i
'
|
1
'
!
1
'
1
t
'
'
woe = wee ee a

14
```

---
## Page 15

```text
¥v PLL UNIT (X50-1490-00)

PC BOARD VIEWS

@

r

A6_OND O34 GND VD OND

tas Oyo ee aft ete
Oob ol 225 PE oo3 é tals NM” avdl” wv 71
= ie 3004 223 o1g§ of ef 4 PaO t + i Geep Fi LG
“i | ye ee Ly
~ o
4 Lan 3 aE geet Keo 2971 Feo.
= dS 969 d> 1D
ot GS ee a!
at a” _ WI
apap Elqep = iq
Seats
oS o _—— a
las) eatiE se sl Eoag
2 ae
-
°
c Fe20 ate Sean Spa!
; S 2095, OF
LY 104 ;efen wR 3 Sin tO oe more sin
sia {E85 Fi zg oe ee —V Co) |
rn re ee? SSG
| ITS coe Pe S eel
rons] F Ol, SasSeegT Pace a
10 Oped Boeke g Te Cea) + |
5 Bo a 3°88 -
LS feet} Sos ae) PN Sat 5
290) j
es YROL OO} a | WI faa) woos cou. sta le ¢|
3 7a g | a \¢ Ce 3}
290° 629 ee 1 py Hl |
7 7 i +e ee ee 3
ASH spe |: N &
caine | eae Lc| © | | hex |
ep CDS SF . ee ea.
= St $ | >|
o = 30 Hh =a tele|
» “Eg | L-a | AES-GOR™ | Meh [5|
NOS) Sey. oie ia = = i 89 ean | ia
N- Mie seul = as cae ols
S cea” ji | PSReRSPAl [ose Sal
ee © sGarepap se oy
| = StL SSTT Scott

25C46018)
“

Sa,

2sase6zty)
2sc7e84l0)

ee
6
a)
t c

3SK40(L)

(k So

G

2SC1775(E)
28c181i5(y)
25c1959(y)

HO74LS1G3N

SGtsra de OS

123465678

HOT4LS00P
MC4044P

wow eon

v234aser

SN16913P

ls
Tig

TOP VIEWS

15
```

---
## Page 16

```text
ABPEOSDL § Lor dBGCUFIL ¢ 6 Chay sza

Ziesars

d9ELOSL BLor aBLsusoL a1 O90 zx ora 0802M ¢ eta
dd9S0G9L 9891 Pn) ee a] (uoisiarosz = so
eae20594 + 198 euL2OrDE : $1 ve te loyaaeose © 90
ed6sOv94 ¢ plot ABSLGOL : reo : AAJGaG126E © zo
ed6.ovaa = et ZL "tio 4920591 : Ea) (wOlEeXse * is)
eDZpOv94 = ain ROSS TPLNS + 11 SS5USi ‘ea (AISRaIDSZ | EN'OL'G'S'b EE
“ eh a — a en Sa :
1
1
oa 1
1
i Tl Tip Tits
af ap Bh fd fE Ty Ole"
Peet Tete Ol
co ¥ i /3] 3
a ‘de he
sl | fled
Crm

ad

ewe

wed

CIRCUIT DIAGRAM

yY COUNTER UNIT (X54-1360-00)

ateesiestetesteietedeiedetetes

a i :
aan ae oo Goo 6} { 50 @ OW O}-------------------------

|
as Om DR DW eee LY WH MOS MF OMG On AD Zin

16
```

---
## Page 17

```text
PC BOARD VIEWS

vy COUNTER UNIT (X54-1360-00)

2SC78510) 2SC1815(GR)
2SC1815(Y) 2SC1959(Y)

Ly

r
ol Tcs019BP - TC5012BP
ol / Tc40278P = TC50228P
ol & TC4029BP TC5051BP
gi Tca0428P TcSo64BP
o Tc4049BP Tcso66BP
SL TC4518B8P

wha gus 22

TPs ese re

SN74LSSON TCSO268P

TC40118P
gp es 8
Tse 367
TOP VIEWS

eat et a a

oe

3000877
ao

ba

{Ras
¢ we

```

---
## Page 18

```text
PC BOARD VIEWS

¥v CARRIER UNIT (X50-1500-00)

Vv VFO UNIT (X40-1130-00)

(F swrt
WRI-2 sOKIE)

i jolene
PTL Sled aT of af hck

outed al

Q1,2: 2SC460(B), Q3: 2Sc1959(Y)
01,2,4~6: 1S1555, D3: 1SV53A

Ly 3
| aT 33 & | 5
7] =f oe 73 r ©
ants |S
giao E 7
a Aa) g 7 TF 3 gk ~
pees sO Ee & zo" 9
94 8 ond ge BY
Hite be
GO os St wall Re rT Ea o
wz Di oP godt Fe tes
3 8 po, Bie sme x
[Be Pca wea) &
Bt he a Was bd OO tees beg nN
fis. rn =
oo. TT n
a
T Ieee) Ty * rs red
Sore ped J =
z | u
ir oe x
Fe ®
a Or 5

ISV53A

182588, D5:

04°

Q4° 2SC19591Y),

Vv FILTER UNIT

a = se

weieeress .

seis = Reale eae

Qt~5,7,8 : 2501815 (Y)

Q6! 2SA5621Y), Q9: 25A4731Y)
D1,2:41N60, D3 :Wz-044

7181555
05,10: WZ-061, 08,11,13:wZ-090

04,6,7,9,12

3SK22(Y)

2SKI9S(Y) 2SA473(Y) 2SA562(y)

2SC460(B)

2SC1i B15 ly)

2SC1959(y)

18
```

---
## Page 19

```text
PC BOARD VIEWS/CIRCUIT DIAGRAM

Y FINAL UNIT (X56-1350-00)

ave
o1@

pry
onl
GND

R2 100 V2W

13.8v

R23 56 1/20)

c49 jpoozs R20, 58 vaw

ca5y,o022] [R2i se) is.ev

Teze p22} ] 2.5

1 car foceal

Te) 3.9 |

w

a
Fo
g

2

[- 2:

C40, )220P

648  ja70r

CAT | | 330F

I

TLS

Hs
2 3
6

Et

RR

C20 100 25%

tH
C23. 008

R2z

356 |
v2w

21.047 - at ]
ar :28C2075 4,5: 2$C2290 04,3: SV-03
Q2,3: 28C2509 Q6,7: 2S0235(Y) D2 :(SV-4A
04,5 : 1N6O
oO at oR a> a B344 — vRe 4708 a7 Th2_25uee ) BS or a
Ee Ae TS
© 3 hr 029 fas. woes a0 7%, 01 E Tra 31026. 5] > 738 ile
See - oe a ens SEES RIS) 3p Te ee 6 6
a 330, | 1 Ss Seas, Seen pt Ps | oa poe 4
er BQ SES eye) sey ——— fox 1 ©
SHI og \ gap | 3538 ‘al |
=DE peal 02 3 ( 2 Ronn i 1
y sis * : Peta =H
5a) SHEy Fae rill i
Pad > “3 qr | & 3 38 [4 |
Li 4h at son o en enone — Tt
2 we BhegBt2100,vam ay, 2 i
¥ Me er LA | aii. !
« 2 SEs |
ob ch chaste # q a iy
% ht us H 6
ar Serbs 28 F
a oe re ite Ag Q3 ‘| a es
By OR f £ Sic cs Fl
ys REN |e @)s ar
Gro, O0F if Ee =} 3 55 a 3 Fa
bikin EY BOT i oe
T
© 21300
ce
‘ ‘ ale
Ce, SS  &g fy
Se SSSATS X i
6 . ‘ 2
2sc2075 2S0235(Y) 2scC2509 2SC2290 .

19
```

---
## Page 20

```text
PARTS LIST

Note 1:

Only special type of resistors (example: cement. metal film. etc.) and capacitors (example: electrolytic, tantalum. mylar. temp
coeff. capacitors) are detailed in the PARTS LIST. Forthe to value of all common type components refer to the schematic
diagram or the PC board illustration. Resistors not otherwise detailed are carbon type (1/4 of 1/8W}

Order carbon resistors and capacitors according to the following example:

A carbon resistors part number is RD14BY 2E222J.

A ceramic capacitor’s number is CK45F1H103Z, CC45TH1H220J.

1. Type of the carbon resistor 3. Resistance value
—— a 2
22 @-— means 22 x 10? = 22000 (2.2kn}
RD14BY
RD14CY Significant figure Multiplier
mi ae ‘ Example: 221+ 2202 224 + 220K0
1/8W + 28 222 + 2.2k2 225 = 2.2m
223 + 22kn
4. Tolerance
J = +5% (Gold)
K = £10% (Silver)
Note 2:
K: USA. W: Europe T: Britain
CAPACITORS 1= Type ..... Ceramic, Electrolytic etc.
2= Shape Round. Square etc.
af !
Pe Type 3= Temp range
SK 45 FH 103 2 = cc 45 TH. JH. 220 J = 3'=Temp coeff
ee poe cee eee pmeY eae Novem tem eae 4= Voltage rating
5= Value
6= Tolerance
6. Tolerance
Type Cc D G J K M x z P No Type

+40 | +80 |+100] More than 10uF —10~+50
+
(%) {+0.26] +05 | +2 +5 +10 | +20 —20 | —20 |—o Less than 4.7uF —10~ 475

/
Cord B c D F G (Value less than 10 pF}

(pF) | +0.1 [40.25] +0.5 | +1 +2

CK45F 5. Capacitor value
Ceramic capacitor (type |) 3 Example: 010 — 1pF
3 100 — 10pF
Cord B dD E F 101 + 100pF
Operating temperature | —30 | ~30 | —30 | —10 102 > 1000pF = 0.001uF
°c +85 | +85 | +85 | +70 103 + 0.014F
CC45 ....
CC4500..., Color CK45..
Peat capacitor (type !!) temperature coeff. capacitor 1° 3° ‘.

CH LH PH RH SL TH UH
(Black) | (Red) [Orange)|{Yellow) |{Green) | (Blue) | (Violet) I

Ippm/°C} 0 —80 | —150 | —220 | —330 | —470 | —750
20

Color

Type II Type |
```

---
## Page 21

```text
PARTS LIST

vw New parts
Re-
Ref. No. Parts No. Description marks
GENERAL
CAPACITOR
c1 | ¢90-0806-05 Electrolytic 2200uF 16WV
c3~39 | CK45F1H103Z Ceramic O.01nF +80%— 20%
RESISTOR
Ri~3 RDI4ZBB2ECOOI Carbon resistor COOL +5% 1/4W
R56 RCOSGF2H101J Solid resistor 1008 +5% 1/2W
RT R92-0620.00 Cementresistor 15 mit
SEMICONDUCTOR
01 V11-2163-05 Diode $31C
b2 V11-7260-66 LED PA212D
D3 V11-0240-05 Zenerdiode W2Z-090
POTENTIOMETER
VRI RO6-9402-05 TOKE (A) AF
10k (B) RF
VR2 ROG-9402-05 10Ki2 (A) MIC
10ki? (B) CAR
VR3 RO6-9403-05 Ski? (B) RIT
1Oki2 (F) IF SHIFT
MISCELLANEOUS
$1 $36-2402-05 See saw switch POWER
$2 $44-2402-05 Paddle switch STBY
$3 $01-2417-05 Rotary switch MODE
s4 S$01-2417-15 Rotary switch BAND
l2~5 L40-1511-03 Ferti-inductor 150uH
- AO1-0743-02 Case {A} upper w
A01-0744-02 Case (B) Lower &
- A20-2349-03 Panel ass'y *
- 805-0701-04 Speaker grill cloth
- B10-0613-04 Front glass [B)
- 820-0811-04 Dial scale (8)
PL1,2 830-0808-05 | Pilotlamp x 2
ad 831-0618-05 | Meter
a 839-0407-04 Spacer x 2 forleg
842-1644-00 Indicating plate (VOX)
_ 842-1659-14 Indicating plate (ADJUSTMENT)
- 843-0620-04 Name plate |T) *
oe 843-0621-04 Name plate (WIIK) ®
850-2643-00 Operating manual (WI{K) 2
~ 850-2644-00 Operating manual (T) *
- 851-0877-00 Service manual |K)(W){T) *
021-0807-05 Band shaft
- 922-0404-05 Universal joint
- 040.0603.04 Gear Assy
£04-0152-05 M type receptacle ANT
- | £06-0252-05 2P metal socket (Power supply) |
€06-0451-05 4P metal socket MIC
c £06-0751-05 7P DIN socket REMOTE [ACSY)
= | €£06-0851-05 8P DIN socket EXT. VFO SW
E07-0751-05 7? DIN plug REMOTE
- £11-0005-15 3 pole phone jack KEY
- £11-0034-25 PHONES jack
ra £11-0402-05 EXT.SP jack
= £12-0001-05 Phone plug EXT.SP (ACSY)
= £22-0207-05 Lug plate 1018
= £22-0405-05 Lug plate x 3 2028
- £29-0407-05 Bridge connector

Re-
Ref. No. Parts No Description rink
- £30-1632-05 Fan Cable (with BC cord)
= €30-1638-05 PC Cord Ass"y (ACSY) cd
- FO5-2034-05 Fuse 204
= FO?7-0626-05 Heat sink cover tt
FO9-0405-05 Fan
- GO2-0505-05 Knob D spring x 3
- HO1-2619-04 Carton [inside] (WICK)
- HO1-2620-04 Carton inside) (T} *
~ HO3-1706-04 Carton {outside} (K)
HO3-1707-04 Carton loutsice) (WI *
- HO3-1 708-04 Carton (outside) IT) a
- HO1-2574-04 Case cover
- H10-2509-02 Front packing fixture *
- H10-2510-02 Rear packing fixture
- H12-0441.04 Accessory box
- H20-1405-03 Protective cover
= #21-0701-04 Protection sheet for VOX CONTROLS,
~ J02-0323-05 Footx 4
- J02-0407-04 | Tilt bracket
_ J21-2504.04 Mounting stopper (SP} rd
- J31-0141-04 | Spacer ring for mic
- J42-0038-04 Hole plug
- J42-0407-04 Knob bush x 2
- J61-0019-05 Vinyle tie x 10.
- J61-0210-05 Vinyle tie
- J61-0401-05 Nylon cable tie x 4
~ K21-0722-04 Main knob VFO
- K21-0723-04 Pointer knob large
K21-0724-04 Knob (outside) x 3
- K23-0710-04 Knob (inside) x 3
- K23-0711-04 Pointer knab (small)
- K23-0712-04 VOX knob x 3
= K29-0709-04 Push knob (square) x 6
- N14-0508-04 Spanner Nut
- N14-0509-05 Wing nut
- N18-0607-04 Nylon panel washer
e N99-0303-05 Hex. head screw (VFO)
- TO3-0027-15 Speaker
= 710-0301-05 Fan motor a
846-0058-00 Warranty Card (K)
SWITCH (A) UNIT (X41-1140-00)
: Ae-
Ref. No. Parts No. Description eins
Si~3 $40-2404-05 Push switch SPJ222H
SWITCH (B) UNIT (X41-1150-00)
Ref No Parts No. Description fe:
marks
Ri RD14CB2E681) Carbon resistor 68012 =5% 1/4W
ot V11-0076-05 | Diode 181555
Si~3 $40-2405-05 | Push switch SPJ222E
C1 CK45FIN103Z —| Ceramic 0.01uF +80%—20%

21
```

---
## Page 22

```text
PARTS LIST

RELAY UNIT (X41-1250-00) ae PaaNG Daas ipaice Re
Rei..No, Parts No. Description sl C66 C91-0456.05 Ceramic 0.0474F 25WV
cés CEO4WIH4SR? Electrolytic 4.?uF 50Wwy
CAPACITOR C74 | CC45RH1H120J | Ceramic 12pF 40.25 pF
C1 CK45F1H103Z Ceramic O.01uF +80%—20% C76 | CC4SRHIHIOIN | Ceramic 100pF — +5%
C2 CEO4WIHR47 Electrolytic 0.47uF SOWV c78 CC45SLiHOS5OC | Ceramic — SpF +0.25pF
RESISTOR RESISTOR
R12 RO14BB2ECOOJ | Carbon resistor OCON 45% 1/4W RI~66 | RDI4CBZ2EQCOY | Carbon Resistor OOO +5% 1/4W
R22.32 | NOT USED
SEMICONDUCTOR/RELAY -
SEMICONDUCTOR
3-1959-06 Transistor 2SC1959 {Y,
a “i 0076-05 Diode 181688 = YO9-1 002-56, fey sonra)
§51-2406.08 Relay G2v2 Q2 VO3-1815-06 Transistor — 2SC1815(Y)
Q3~6 | VO9-1002.56 FET 3SK74(L)
Q7.8 V03-1815-06 Transistor  2SC18151Y)
DC CABLE ASS’Y (E30-1638-05) as V03-2086-06 Transistor 2SC2086
Q10 | V01-1015-06 Transistor — 2S41015(Y)
Ref. No Parts No. Description Re- o1 | ¥11-0370-05 Diode 181587
marks}! 92 | y11-0414.05 Diode 182588
D3 V11-0370-05 Diode 181587
R Bees /508 Cable D4 V11.0414-05 | Diode 182588
F05-2034-05 Fuse (204) |
a J13-0404°05 paper DS V11-0370-05 Diode 181587
a 481-0201-08 Vinvla tex 10 06 V11-0076-05 Diode 181555
07 V11-0061-05 Diode 1N6O
08 V11-3172-76 Diode 181585
RF UNIT (X-1260-01)
COIL/INDUCTOR/TRANSFORMER
Ref. No. Parts No Description fe u 1.34-0559-05 Trap coil 8.83 MHz
2 L34.0558-05 Trap coil 8.83 MHz
L3 L34-0698-05 BPF coil 3.5 MHz
CAPACITOR \4 L34.0699-05 BPF coil 3.5 MHz
C1 CC45RH1H101) | Ceramic 100pF +5% us L34-0698-05 BPF coil 3.5 MHz
3 ca0gs1H102 Styrene  1000pF_ +5% 6 134-0700.05 | 8PF coil 7 MHz
cs CC45RH1H221J | Ceramic = 220pF_ = +5% u7 £34.0701-05 PF coil 7 Miz
C6 CC45RHIH151J =| Ceramic 150pF +5% Ls | L34-0700-05 BPF coil 7 MHz
c? CC45RH1H221J | Ceramic =220pF 40+ 5% is | L34-0702-05 BPF coil 14 MHz, WW
C10 CC45RHIHB20J | Ceramic 82pF = +5% L10 | _L34-0703-05 BPF coil 14 MHz. WW
ci CC45RH1H390J | Ceramic 39pF +5% un | L34-0702-05 BPF coil 14 MHz. WWV
C12 CC4SRHIHIO1J | Ceramic 100pF +5% u12 134-0704-05 BPF coil 21 MHz
C15 CC4SRH1H100D | Ceramic 1 0pF +0.5pF u3 134-0705-15 BPF coil 21 MHz
ci6 CC45RH1H270J =| Ceramic 27pF = + 5% L146 134.0706-05 BPF coil 21 MHz
C17 CC45RH1H330J | Ceramic 33pF 45% Ls 134-0707-05 BPF coil 28 MHz
c20 CC45RH1H330J | Ceramic 33pF = + 5% L16 34-0737-05 | BPF coil 28 MHz
c2t CC45RH1H100D Ceramic 10pF +0.5pF Li7 L34-0738-05 BPF coil 28 MHz
c22 CC45RH1HOSOC =| Ceramic 5p F +0.25pF L18,19 | L40-1021-03 Ferri inductor 1mH
c25 CC45RH1HO3OC | Ceramic = 3p F +0.25pF 120 140-101 1-03 Ferti inductor 100uH
C26 CC45RH1HO70C Ceramic 7oF +0.25pF 21 L40-1592-02 Ferri inductor 1.5uH
C27 CC45RH1H2705 Ceramic 27pF 25% 122.23 | L40-4711-03 Ferriinductor 470 wH
€31,32 | C90-0262-05 Ceramic 0.047uF 25WVv 24 L40-4782-02 Ferri inductor 0.474H
c33 CC45SL1HO70C Ceramic 7pF 20.25pF L25~27 L40-4711.03 Ferriinductor 470uH
C35 C90-0262-05 Ceramic 0.047uF 25wV 128.29 | L40-1021-03 Ferri inductor 1 mH
C37 ~33| C90-0262-05 Ceramic 0.047uF 25wv 130,31 L40-1011-03 Ferri inductor 100 uH
cao CC45SL1H220) | Ceramic 22pF  +0.5pF 132 40-4791-02 Ferriinductor 4.7uH
cat C90-0262-05 Ceramic §=0.047uF 25WVv 33 33-0032-05 Choke coil 3 «H
ca3 CC45SL1H150J Ceramic 15pF = +5% L34 L40-1011.03 Ferri inductor 100 wH
C44 CC45SLIH220J Ceramic 22pF = 5% L35 34-0553-05 Trap coil 8.83 MHz
cas CC45SL1H270) Cerarme 27pF +5% 11 L34-0696-35 Input coil ANT
C46.47 | C91-0455-05 Ceramic = =O0.01uF T2 | L19-0303-05 Wide range transformer
C48,50 | C90-0262-05 Ceramic 0.047nF 25WV 13.4 L34.0697-05 Output coil
C56 €90-0262-05 Ceramic = 0.047uF 25WV 1S L19-0303-05 Wide band transformer
cee €90-0262-05 Ceramic = 0.0474F 25WV Té L19-0302.05 Wide band transformer P.DRV
C61 CC45SL1H2215 Ceramic 220pF =5% MISCELLANEOUS
ce3 CEO4W1C100 Electrolytic 10xF  16\WV
cB4 CEO4Wi1C100 Ceramic 10uF 16ewy — $29-3404-15 Rotary wafer assy

22

```

---
## Page 23

```text
PARTS LIST

IF UNIT (X48-1210-01)

AF-GEN UNIT (X49-1110-00)

Ref. No. Parts No. Description Biers Ref. No. Parts No Description anes
CAPACITOR CAPACITOR
ci CC45SL1HO50C Ceramic 5SpF +0.25pF teal CC45CH1H1000 Ceramic 10pF +0.5pF
34 CC45SLIH470J | Ceramic 47pF 2 = 5% c3 CQ92M1H333K — | Mylar 0.033uF +10%
ce ceoaw1c100 Electrolytic 10uF = 16WV c4 CEO4W1HR47 Electrolytic O47uF —SOWV
€22 CC45SLIH470J) | Ceramic 47pF —-$5% cs CEO4Ww1A221 Electrolytic 220nF — 10WV
c23 CC45SLIH150) Ceramic 15pF 25% c7.8 CEO4W1C100 Electrolytic 10pF 16WwV
c28 CC45SLIHO70D | Ceramic 7pF +0.5pF c3 CO92MTH104K — | Mylar OtuF  +10%
c34 CC45SH1H1000 | Ceramic 10pF = +0.5pF €10,11 |ceoawic102za =| Electrolytic 10004F ~16WV
c35 CC45SH1H470) Ceramic 47pF +5% c12 CQ92M1H104K Mylar O.1uF +10%
c338 CC4SSLIH470J | Ceramic 47pF = 45% 13 cEO4w1C470 Electrolytic 474F = 16WV
cao CEO4W1HO10 Electrolytic tu 50wv c14 CO92MIH1O4K | Mylar O1uF  +£10%
ca? CEO4W1HO10 Electrolytic tuF sowy c16 cEO4W1C470 Electrolytic 47uF = 16WV
cag CC4ssLiHos0c§ | Ceramic = 3pF +0.25pF C17 CEO4W1HOTO Electrolytic 1uF sowy
C56 CC34SL1H470K | Ceramic 4 70pF + 10% cig CQ92M1H223K — | Mylar 0.022uF +10%
c19 CEO4wiC100 Electrolytic 10uF = 16WV
RESISTORS phe VAchNT
R1~67 | ADI4CB2ECOOI Carbon resistor OOO +5% 1/4w €21.22 |CeEO4wic4a7o0 Electrolytic 47 uF 16WY
SEMICONDUCTOR €23 CQ92M1H104K — | Mylar O1uF = £10%
c24 CEO4W1C221 Electrolytic 220uF 16WV
Qi~3 | VO9-1002-56 Fer 3SK74(L) €30~33 |CC45CHIH220) | Ceramic 22pF  +5%
a4 Vos-0012-05 Fer 2SK19(GR} 37 CC4SSL1H1S1J | Ceramic 150pF + 5%
as VO1-1015-06 Transistor 2SA1015(Y) cae CC45CH1H1000 Ceramic 10pF +0.5pF
06.7 V03-1815-06 Transistor © 2SC1815{¥} ¢39 CC45SL1H180) | Ceramic 18pF —-£5%
ae VO9-0012-05 FeT 2SK19(GR) €41,42 |CC45SLIHIO1N | Ceramic 100pF = +5%
a9~11 | ¥O3-0079-05 Transistor  2SC46018) C43 cEO4w1H010 Electrolytic uF SOW
012,13 | VO3-1815.06 Transistor 2SC18151Y) 4a CEOSWI1A221 Electrolytic 220.F  10WV
DIi~4 | V11-0370-05 Diode 181687 cas CEOSW1E4R7 Electrolytic 4.74F = 25WV
os V11-4160-66 Diode 181007 C46 CEO4W1HO10 Electrolytic taf soWwy
06 V11-0370-05 Diode 181887 ca? CQ92M1H473K | Mylar 0.047uF +10%
o7 V11-4160-66 Diode 181007 C48.49 |CEO4WIEGR7 — Electrolytic 4.7uF — 25WV
08 V11-0370-08 Diode 181587 cso CEOSWIHOIO — Electrolytic tuF SOWY
09.10 | ¥11-0076-05 Diode 181555 51 CEO4W1H3R3 Electrolytic 33uF SOW
011.12 | V11-0051-05 Diode 1N6O 52 CEO4W1H010 Electrolytic 1aF sOWY
B13 V11-0076-05 Diode 151555 C55 CC45UJ1H220J | Ceramic = 22pF_ «= +5%
NIB: | ev 1 OGe 1-08 Diode 1néO C56 CC4SSLIH1015 | Ceramic 100pF 45%
016 V21-0004-05 Varistor mvi3 cs CC45CHIHOSOC | Ceramic SpF +0.25pF
017~32) V11-0076-05 Diode 181555 64 CC4SSL1HA70N |Ceramic 47pF —-+8%
POTENTIOMETER c66 CC45SLIH470J | Ceramic 47pF 2 £5%
c67 CEO4W1C100 Electrolytic 10u# = 16WY
wae nigetoroe naonie céB CEO4W1HO10 Electrolytic 1aF sowy
69.70 |ca92M1H123K | Mylar O.012uF +10%
INDUCTOR/COIL c71 ca921H104K Mylar O1uF = £10%
Tree relicannsiicos Feri-nductor 1SOuF ze | ]972-73 [cas2miHi23k | Mylar = 0.012uF_ + 10%
aa (34.0708-05 Tuning coil c74 CEO4W1HO10 Electrolytic 1uF sowy
3 134-0837-08 Tuning coil c7s CEO4W1A221 Electrolytic 220uF — 10WV
mi 134-0838-05 Tuning coil ©7677 |CEO4W1A470 Electrolytic 474F = 10WV
15.6 L34.0535-05 Tuning coil c78 Cag2m1H223k =| Myler, = O.022uF + 10%
7 134-0536-05 Tuning coil c73 CEO4W1H3R3 Electrolytic 3.3uf  SOWV
13 134-0835.08 Tuning coil cso CEO4W1HO10 Electrolytic 1uF sowy
13 L34.0536-05 Tuning coil de COS2MIH473K = | Mylar, (0.047uF, £10%
a3 CO92M1H102K —| Mylar 1O00pF-+10%
MISCELLANEOUS ca4 (CQ92M1H473K | Mylar 0.047uF +£10%
XFL L71-0208-05 Cristal filter 4 element, monolitic tt C85.86 CEO4WIE4RT Electrolytic 4.74F 25WV
cF1,2 | L72.0310.05 Ceramic filter for NB « | |cee CEOaw1E3R3 Electrolytic 3.34F § 25WV
a E23-0046-04 Terminal (Square) css CC4S5SLIHION Ceramic 100pF 75%
- $51-4401-05 Relay LZN-4 cso CEO4W1C220 Electrolytic 22uF = 16WV
RESISTOR
R1~113 |RD14CB2ECCOJ =| Carbon COCR +5% 1/4W
RDI4BB2ECOON
R14 AS14GB308R2J | Metalfilm 822 45% 2w
36,80.93NOT USED

23
```

---
## Page 24

```text
PARTS LIST

pe. | PLL UNIT (X50-1490-00)
Ref No Parts No. Description i
i marks
Ref, No, Parts No. Description on
SEMICONDUCTOR
ai VO3-2240-06 Transistor 2SC2240 (GR)
a2 V30-1028-36 1c uPC14305H CAPACITOR
a3 V01-0473-06 Transistor 254473 lY) | C1 CC45TH1H2205 Ceramic = 22pF £5%
Q4~6 | VO3-1815-06 Transistor 28C1815(Y) | c2 CC45TH1HO30C Ceramic 3pF +0.25pF
a? V30-1045-06 Ic HAIZ66W c3 CC45TH1H220) | Ceramic 22pF = +5%
as V03-0079-05 Transistor  2SC460 (B) ca | CEow1A470 Electrolytic 474F = 10WV
ag V03-1959-06 Transistor 2SC1959 (Y) cs | CC45UJ1HS5605 Ceramic 56pF $5%
10,11 | vo3-1815-06 Transistor 281615 (¥) ce | CC45UJ1H270J | Ceramic 27pF = £5%
ai2z V09-0012-05 FET 2SK19 (GR) co CC45THIHI50J | Ceramic 1SpF  +5%
a3 V03-0079-05 Transistor 2SC460 (B} c10 CC45TH1HO30C Ceramic = 3pF +0.25pF
a4 VO3-1815-06 Transistor 2SC 1815 [Y) cu CC45THIH2205 | Ceramic 22pF +5%
a5 V01-1015-06 Transistor  2SA1015(Y) 12 CEO4W1A470 Electrolytic 47uF = 10WV
Q16.17 | VO3-1815-06 Transistor 28C1815(Y) c13 CC45THIH3305 Ceramic = 33pF +5%
as V03-2240-06 Transistor 2S$C2240 (GR) C14 CC45THIH4705 Ceramic = 47pF £5%
Q19.20 | Vo3-1815.06 Transistor  2SC1815{Y) c17 CC45THIH270J) | Ceramic 27pF = +5 %
a21 V01-1015-06 Transistor © 2SA1015(Y) ce CC45UJ1H220J | Ceramic 22pF = ++5%
022 VO1-1815-16 Transistor  2SC1815 (GR) cig CEO4W1A470 Electrolytic 474F = 10WV
022,23 | vo3-1815-06 Transistor 2$C1815{Y) c20 CC45UJIH1014 = | Ceramic = 100pF_ 45%
a24 V01-0032-05 Transistor  2SA562 (¥) c21 CCASUJTH220J =| Ceremic — 22pF ----£5%
Q25 V03-1815-06 Transistor 2SC1815(Y) C24 CEO4W1C100 Electrolytic’ 10nF _ 16WV
p~4 | v11-0051-05 Dioge 1N6O c25 CC45TH1IH270J | Ceramic = 27pF ss $5%
DS V11-0243-05 Zener diode W2z-061 C26 CC4STH1H150J | Ceramic 15pF +5%
pé~9 | v11-0414-05 Diode 182588 c27 CC45TH1H220J | Ceramic ©. 22pF_ + 5%
D10 NOT USED | c28 CEO4W14470 Electrolytic 47uF = 10WV
b11~14] v11-0051-05 Diode 1N60 €29,30 |CC45UJ1HS60J | Ceramic S6pF +5%
DIS ¥11-0370-05 Diode 1$1587 C33 CC45TH1H270J Ceramic = 27 pF 15%
p16 VACANT c3¢ CC4STH1H100D | Ceramic 10pF —- +0, 5p F
D17~22) v11-0076-08 Diode 181555 C35 CC45TH1H220J =| Ceramic «= 22pF_ 45%
023.24 | v11-0051-05 Diode 1N6O C36 CEO4W1A470 Electrolytic 47uF = 10WV
p25 V'11-0076-05 Diode 11555 C37 CC45RH1H390J Ceramic 9 39pF 42 + 5%
p26 V11-0051-05 Diode 1N60 c3B CC4SSHIH560J) | Ceramic = 56pF = + 5%
027.28 | V11-0076.05 Diode 781555 c40 ©C45CH1H100D Ceramic = 10pF +0.5pF
c41 CC45CHIHOZ0C | Ceramic §=—-2pF +0.25pF
POTENTIOMETER 43.44 | C90-0262-05 | Ceramic 0.047uF 25WV
VRI R12-3025-05 10k2 (B} RIT c45 CC4SSLIHI515 Ceramic = 150uF 9 + 5%
VR2 R12-4016-05 50kf RF C47 CC4SSLIH271J Ceramic 270pF +5%
VA R12-0042.05 502 (8) ov C48 CC45SLIH1215 Ceramic 120pF 445%
VAG R12-4016-05 5Oke SIDE TONE C50.51 | CC45SLIH390) | Ceramic 39pF 5%
VAS R12-0401.05 1002 8M C53 CEO4W1C100 Electrolytic 10uF = 16WV
VR6 R12-0405-05 3302 (8) ANTI VOX C54.55 | C90-0262-05 Ceramic § 0.047uF 25WV
VR? R12-3408-05 47k2 VOX GAIN €57.58 | CC45SL1H221N Ceramic 220pF +5%
VRB R12-5402-05 220k DELAY cs9 CQ92M1H122K Mylar 1200pF +10%
C60 CC45SL1H390) Ceramic 39pF +5%
TREE RACOIINDUGTOR €61,62 | CC45SL1H820J Ceramic 82pF + 5%
TC1~6 | CO5.0030-15 Ceramic trimmer 20pF C63 CC45SL1H390J Ceramic  39pF +5%
ui L40-1021-03 Ferri-inductor 1 mH> C65 C90-0262-05 Ceramic 0.047xF 25wv
L2.3 L40-1511-03 Ferri-inductor 150 4H c70 CC45SL1H1200 Ceramic 12pF +5%
U4 L40-4771.03 Fern-inductor 470 gH cn VACANT
6 L40-3392-03 Ferri-inductor 3.3 aH C73 CC45CHIHOIOC =| Ceramic =I pF +0.25pF
6.7 L40-1511.03 Ferri-inductor 150 uH cra CC45CHIHOSOC =| Ceramic SpF +0,25pF
us 440-1021-03 Ferri-inductor 1mH c76 CC45SLIH2715 Ceramic 270pF +5%
" L15-0016-05 ‘Filter choke C77 €90-0262-05 Ceramic 0.0474F 25WV
T2 34-0567-05 Tuning coil c7e CEO4W1A101 Electrolytic 100uF  10WV
MISCELLANEOUS c79 C90-0262-05 Ceramic 0,0474F 25WV
a Biloasicoe Ceiuiicotaer ap cao CQ92M1H104K Mylar O1uF =+10%
x Rootes sic ane cat CQ92M1H102K Mylar 1000pF +10%
5 cage os sort €82.83 | C90-0262-05 Ceramic 0.047uF 25wv
Ld Shoulder washer cas CEOswoy101 Electrolytic 1004F — 6.3WV
cag CEO4W1A470 Electrolytic 47uF = 1OWV
cso VACANT
c95 CC45RH1H330J | Ceramic 33pF +5%

24

```

---
## Page 25

```text
PARTS LIST

Ref No Parts No. Description aie | Ref. No Parts No Description ales
ca6 CC45RH1H150D Ceramic 15pF £0.SpF 13 L40-1292-02 Ferri-inductor 1.24H
cs? CC45RH1H330J Ceramic 33pF 15% ie 40-2701-03 Ferri-inductor 27yH
c100 CC4S5RH1H150D Ceramic 15pF +0.5% Lis (40-4711-03 Ferri-inductor 470uH
c10t CC45RH1HO40C Ceramic 4pF +0.25pF Li6 L40-1511-03 Ferri-inductor 150uH
102 CC45AH1H150D Ceramic 15pF 20.5pF ui7 140-1011-03 Ferri-inductor 100ur
C106 CC45CH1H1000 Ceramic 10pF =0.5pF Lis L40-1511-03 Ferri-inductor 150uH
c109 CC45AH1H4S70) Ceramic 47pF +5% L19~21) L40-2701-03 Fern-inductor 27aH
c110 CC45AH1H220J Ceramic 22pF 25% L22~24) L40-1511-03 Ferni-inductor 1504
C112 | CC45RH1HSE60U Ceramic S6pF 25% | 125 L40-1001-03 Ferri-inductor 10uH
c113 CC45SL1HO70D Ceramic 7pF +0. 5pF L26 L40-4711.03 Ferri-inductor 4704H
Cie CC45RH1H390)5 Ceramic 39pF +5% 127 L40-1511-03 Ferri-inductor 150uH
C117 CC45SL1IH470J Ceramic 47pF +5% L28 L40-1001-03 Ferrinductor 10uH
C118 CC45CH1H100D Ceramic 1OpF +0.5pF 129.30 L40-1511-03 Ferri-inductor 150uH
c119 CC45RH1H470N Ceramic 47pF +5% T1 L32-0199-05 OSC coil 14.MHz
C127 CC4SRH1HOTOD Ceramic TpF +0.5% T2 L32-0197.05 OSC coil 21 MHz
RI~92 RO14CB2E MJ T3 L32-0198-05 OSC coil 28 MHz
RD14BB2e 4 L32-0195-05 OSC coil 7 MHz
RI? NOT USED TS 132-0193-05 OSC coil 3.5 MHz
SEMICONDUCTOR 6 134-0529-05 Trap coil 8.83 MHz
7 134-0714-05 Tuning coil
Q12 V03-0079-05 Transistor 2SC460 (B) Ts 134-0715-05 Tuning coil
Q3 VO3-0368-05 Transistor 280784 (QO) T9 L34-0716-05 Tuning coi
a4 V03-0079-05 Transistor  2SC460 (8) Tio 34-0717-05 Tuning coil
6 V03-0368-05 Transistor 25C784 (0) Ti L34-0718-05 Tuning coil
are VO3-1959-06 Transistor — 2SC1959(Y) T12 L34-0757-05 Tuning coil
as VO3-1815-06 Transistor — 2SC1815[¥) 113 34-0711-05 Tuning coil
Q10.11 | ¥O3-0079-05 Transistor 25C460 |B) 14 L34-0709-05 Tuning coil 10 MHz
ai2 V30-1048.06 ic SN16913P Tis L34-0710-05 | Tuning coil 20 MHz
13.14 | V03-0079-05 Transistor 2SC460 (B) Tl? L34-0712.05 | Tuning coil
ais V30-1046.06 | ic HO74LSO0P T18 L34-0713-05 | Tuning coil
a6 V30-1037-06 ) ic HO74LS163N
Q17~ 19] vo3-1775-06 | Transistor ~— 2SC1775{E! MISCELLANEOUS
a20 ¥30-0173-05, | ic MC4044P - E23-0046-04 | Terminal (square}
a21 VO3-1815-06 | Transistor 2SC1815(¥} -
Q22 VO3-0079-05 | Transistor 2SC460 (B)
a23 ¥O9-0079.05 | FET 38K40(L) CAR UNIT (X50-1500-00)
024.25 | V03-0079-05 | Transistor 2SC460 (B)
Q26 V30-1048-06 Fic SN16913P , Re-
027 | vo3-1815-06 Transistor 2SC1815 (¥) spec ie sircachier Description marks
Bi~4 V11-0076-05 Diode 181555 |
05 V11-4161-36 Diode 1SVS3A | CAPACITOR
eo bi : Gilvae vee ; Stee, c2 CC45UJ1H220) | Ceramic 22pF + 5%
Ds V11-0370-05 Diode 181587 | c3 CC45US1H2705 Ceramic 27pF 5%
pe V11-4161-36 Varicap 1S¥53A | ba CCAEUITH220J | Ceramic © 22nF = 5%
D190 | ¥11.0414.05 Diode 12588 olead Mile bec all
Dit V11-4161-36 Varicap 1SV53A cs CS1SE1VR22M Tantalum O0.22yF 35WwV
D12 V11-0370-05 Diode 181587 ci3 CC45SLIH1015 Cerarmec 100pF +5%
p13 V11-4161-36 Varicap 1SV53A cl4 CC45CH1HO20C Ceramic 2pF +0.2SpF
pia V11-0370-05 Diode 181587 cis CC45CH1H3305 Ceramic 33pF +5%
DIS ¥v11-0370-05 Diode 191587 C16 C90-0262-05 Ceramic 0.0474uF 25wy
O16 NOT USED RESISTOR
ha ip ma ioe oieee Ht JA1~21 | ROIACB2ECCOJ | Carbon resistor OOOR +5% 1/4W
024~23| V11-0370-05 Diode 181587 SEMICONDUCTOR
POTENTIOMETER a12 | vo3-0079.05 Transistor 28460 {B) |
az VQ3-1959-06 Transistor 2801959 (Y}
VAL A12-5014.05 100k2 Spuricus D1,2 ¥11-0076-05 Diode 181555
INDUCTOR/COIL 3 V11-4161-36 Varicup 1SV53A
Li~s | L40.1511-03 Ferri-inductor 150cH DEB is] V11-0076-05 Diode 1S1656
Lo L40-4701-03 Ferri-inductor 47 4H POTENTIOMETER
L10 L40-1§92-02 Ferri-inductor 1.S5uH VRI2 R12-1012-05 +82 (B)
111,12 | L40-1092-02 Ferri-inductor 1H

25
```

---
## Page 26

```text
PARTS LIST

Ref. No. Parts No Description ines Ref. No, Parts No. Description pie!
MISCELLANEOUS Dt ¥11-0240-05 Zener diode WZ-090
D12 ¥11-0076-05 Diode 181555
TC1,2 C05-0056-05 Ceramic trimmer 30pF 013 V11-0240-05 Zener Diode WZ-090
x1 L77-0485-05 Quartz crystal 8831.5 kHz D4 V11-0076-05 Diode 181585
x2 L77-0486.05 Quarw crystal 8828.5 kHz
Li~3 140-1511-03 Ferri-inductor 150uH VR R12-4016-05 Potentiometer 50ks! (B)
4 133-0266-05 Choke coil = 28H VR2 R12-3025-05 Potentiometer 10k! (B)
t5~7 | L40.1511-03 Ferri-inductor 150 VR3 R12-4016-05 Potentiometer 50k%? (B)
Lal (32-0201-05 OSC coil VR4 R12-0042-05 Potentiometer 5000 (B)
VRS R12-1020-05 Potentiometer 1ki! (8)
FILTER UNIT (X51-1200-00) Te1 C05-0043.05 Ceramic trimmer 20pF
Ref. No. Parts No, Description Fei Be $31-4402-06 Relay
i. LI~3 | L34-0826-05 Filter coil (A) *
1 CM93D2H821J Mice 820pF + 5% 14.5 L34-0827-05 Filter Coil (B) *
C2.3 CM9302H122) Mica 1200pF +5% 6.7 134.0828-05 Filter coil (C) &
c4 CM93D2H561) Mica 560pF +5% Lag 34-0829-05 Filter coil (D} te
cs CM93D2H331J Mica 330pF = + 5% L10.11 | L34.0830-05 Filter coil (E) ®
cé CM9302H621J Mica 620pF _+5% L12 140-102 1-03 Ferri-inductor  1mH
c7 ©MS302H331J Mica - 330pF = +5% L13
ce CM9302H271) Mica 160pF ==5% L14.15 | L40-1021-03 Ferri-inductor imH
co CM93D2H331J Mico 330pF + 5% 16.17 | L40-1511-03 Ferri-inductor  150«H
C10 CM93D2H161J Mica 160pF «+ 5% us 139-0406-05 Detector coil *
cu CM9302H121) Mica 120pF + 5% ug L40-1511-03 Ferri-inductor 150uH
ci2 CM93D2H221) Mica 220pF «$ 5%
c13 CM93D2H121J | Mica 120pF = +5% ‘ £23.0046-04 Terminal (square) x 4
C4 CMS3D2H820) Mica 82pF +5% = E23-0401.05 Terminal (circle) x 24
c1s M93D2H 161) Mica 160pF = +5%
c16 CM93D2H 1310 Mica 130pF = +5% - F20-0078-05 Insulating mica
17,18 | NOTUSED es F29-0014.05 Shoulder washer
20 CC45SL2H221J | Ceramic 220pF +5%
c21 CC4SCH2HO30J =| Ceramic 3p F £0.25 pF _ J31-0502-04 Board stand (color) x 6
22 CC4SCHIHEBOS | Ceramic 68pF = + 5% - J62-0404-05 Board stand (bush) x 6
C24 C91-0456-05 Ceramic 0.047uF 25 WV
C25 CEO4W1HRA? Electrolytic O.47uF SOWV
c27 CEO4W1HO10 Electrolytic 1uF 50WV COUNTER UNIT (X54-1360-00)
c28 ceEO4w1C100 Electrolytic 10uF = 16WV
we ree Ceramic —0.047uF 25WV err pare e. Desorists wie:
C35 CEO8W1C221 Electrolytic 220uf 1 6WV
C36 €91-0456-05 Ceramic 0.047 uF 25WV CAPACITOR
c38 NOT USEO
cai €91.0456-05 Ceramic 0.087 4F 25WV C1 CCASCH1H330J =| Ceramic 33pF 5% |
C42 CM9302H1010 Mica 100pF = +5% c2 CC4SSLIH391N Ceramic 390pF +5% |
c3 CC4SCHIH470J | Ceramic 47pF = 45%
R~33 | RDI4CBZ2ECCOJ | Carbon resistor COC = +5% 1/6W ad €90-0262-05 Ceramic §=0.047uF 25Wv
R67 NOT USED cs CC45SL1H150J | Ceramic 15pF  +5%
R23 RCOSGF2H151J | Solid resistor 1502 +5% 1/2W = CCASSLIHOZOC | Ceramic 2pF = £0.25pF
R33 RD14BB2E820) | Carbonresistor 820 +5% 1/4W cy CC45SLIH100D | Ceramic 10pF_ + 0.5pF
c10 €90-0262-05 Ceramic 0.0474F 25WV
ai~s | vo3-1815-06 Transistor 2SC1815{¥) c1y — |SEOSWOITOIA | Electroytic 100uF  6.3WV
as V01-0032.05 Transistor 2SA562 (Y) Ci2_—|ECASSLIHIO1J | Ceramic 100pF_—-$5%
97.89 | vo3-1815-06 Transistor, 2SC1815 {YI CUS He] C00;0282,05 Goremic. | {0.06725 25WV.
a10 | vo1-0473-06 Transistor 28473 (Y) C14 [ECASSLIH390J | Ceramic 39pF £5 %
cis CC45SL1H330J | Ceramic 33pF = +5%
01.2 | V11-0051-05 Dioce 1N6O C16 | CCASSLIHI01N | Ceramic 100pF 5%
D3 V11-4161-06 Zener diode W2-044 ¢17 CC4SSLIH221J | Ceramic 220pF = +5%
Da v11-0076-05 Diéde 181585 cs CC45SL1H220J | Ceramic 22pF = + 5%
DS V11-0243-05 Zone? ide!“ Wz-084 cig CC45SLIHOSOC =| Ceramic SpF +0.25pF
06,7 ¥11-0076-05 Diode 181555 c20 €90-0262-05 Ceramic 0.047uF 25WV
pe v11-0240.085 Zene¢ diode. Wz-090 c21 CC45SL1H101J | Ceramic 100pF +5%
D9 V11-0076-05 Diode 1$1555 C22 CC45SL1H270J | Ceramic 27pF 45%
D10 V11-0243-05 Zener diode WZ-061 23 CC4SSLIH56Q) | Ceramic S6pF = 5%

26

```

---
## Page 27

```text
PARTS LIST

Ret. No. Parts No. Description Res Ref No Parts No Descrption mai
C24 CC45SLIH270J Ceramic = 27pF +5% 110.11 | L40-4711-03 Ferri-inductor 470uH
c25 CC4SSL1H470) | Ceramic 47pF = +5% 12,13 | L40-1511-03 Fetri-inductor 150uH
C26 NOT USED v1 L19-0305-05 Oscillator transformer *
C27.28 | CC4SSLIH470N Ceramic = 47 pF t5% x2 L77-0482-05 Quartz crystal 10 MHz
c29 €90-0262-05 Ceramic 0.047 4F 25WV = £31-0430-15 Ribbon conductor
c31 €90-0262-05 Ceramic 0.047uF 25WV
C32 CC4SSL1H121J | Ceramic 120pF = +5%
C33 CC4SSLIH271J | Ceramic 270pF +5% FINAL UNIT (X56-1350-00)
c34 CC4SSL1H121J | Ceramic = 120pF = 45%
C36 C90-0262-05 Ceramic 0.0474F -25WV Ref. No eae Dasciption Re-
C38 ~40 | C90-0262-05 Ceramic 0.047 uF 25WVv marks
cai CEO4wos1010 Electrolytic 10QuF 6. 3WV 7a
ean cap2miHis2k> “| Myler 1500pF +10% C1 €91-0455-05 Ceramic = 0.01uF = 25WV
45.56 | C90-0262-05 Ceramic 0.0474 25WV c3 C91-0450-05 Coramic® | 0.04747 -25WV
c47.48 | ceo4woj2210 Electrolytic 220uF 63WV C4 €91-0456-05 Ceramic §—0.047F 25WV
cag CEO4W1V¥1000 | Electrolytic 10.F — 35WV ce CK45B1H10ZK | Ceramic = O.001uF +10%
C51~53|CEO4WIVI000 =| Electrolytic 10uF = 35WV ce C91-0455-05 Ceramic = O.01mF = 25
C55 ~58 | C90-0262-05 Ceramic 0.0474F 25WV C7 NOT USED
cio CK45B1H102K Ceramic 0.0014F =10%
RESISTOR eu €91-0456-05 Ceramic 0.047uF 25WV
R1~57 | ADI4CB2ECOO) | Carbon resistor COOM +5% 1/4W ci2 CEO4W1E100 Electrolytic 10yF 25Wv
R13 NOT USED 13.14 | c91-0456-05 Ceramic 0.047uF 25Wv
RBI R90-0506-05 (47RD + 47K x 6 cis CM93AD2H151J | Mica 1S0pF = 5%
R823 | A90-0521-05 47K2 x 7 16.17 | CK45B1H102K > Ceramic «0.00 1uF + 10%
RB45 A90-0522-05 a7k2 x6 €18.19 | C91-0456-05 | Ceramic 0.047.F 25WV
Bee c20 ceoawie101 | Electrolytic 100uF  25WV
21 €91-0456-05 | Ceramic 0.047uF 25WV
Qt~5 |Vv03-1815-06 Transistor — 2SC1815lY) 22 NOT USED |
a6 V03-0473.05 Transistor  2SC785 {0) c23 CK45B1H102K =| Ceramic «= 0.001uF_ +10%
a? VO9-1002-46 FET 3$K73 (GR} C24 €91-0456.05 | Ceramic 0.047 ~F 25Wv
ag~ 10 | vo3-1815-06 Transistor 2SC 1815 (¥! 2s CEO4W1E100 == Electrolytic 10uF — 25WV
11.12 | vo3-1959-06 Transistor 281959 Y) C26~29| CK45B1H222KMU | Ceramic —0.0022F + 10%
ar3 V03-1815-06 Transistor  2SC1815(Y) C30~32) NOT USED
ica V30- 1005-26 ic SN74LS90N €33.34 | C91-0448-05 Ceramic 0.68uF
Ic2 V30-1040.06 Ic TCs0268P c3s €91-0456.05 Ceramic 0.047 uF 25Wv
1¢3.4 | ¥30-1039-06 Ic TC4518B8P C36 CK4581H102K Ceramic — O.001uF + 10%
Ics V30- 1050-06 ic Tc40278P c37 cEOaW1H1010 Electrolytic 100uF  SOWV
1C6.7 V30-1030-06 ic TC40118P c38 91-0456-05 Ceramic O.067.F 25Wwv
ics V30-1088-06 ic TC50S18P c39 CM93AD2H271J | Mica 270pF + 5%
Ico V30-1051-06 ic Toso298P c40 CM93AD2H331J | Mica 330pF 0 -+5%
Ic10 V30-1052-06 Ic Teaoa2aP C41~ 43] €91-0455-05 Ceramic §=O.01uF 25WV
IC11~ 13] ¥30-1049-06 ic TCao1g—P cae CM93AD2H271J | Mica 270pF ++ 5%
Ic14 V30-1009-26 Ic Tcs049aP C45.46 | CK4581H222KNU | Ceramic —0.00224F +10%
Ic15 V30- 1054-06 Ic Tes0228P ca7 ©M93402H331J | Mica 330pF = +5%
Ic16 V30-1057-06 ic TCS50668P C48.49 | CK4581H222KMU | Ceramic 0.00224F +10%
118 V30-1053-06 Ic TC50128P c50 CC45SLIH220J | Ceramic 22pF = +5%
Ic19 V30-1056-06 ic TCs0648P 51,52 | C90-0455-05 Ceramic = 0.01uF  25WV
DI V11-0240.05 Zener diode WZ-090 53 CM93A02H471T | Mica 470pF = + 5%
b2 VACANT = _— ae
03~18 | v11.0076.05 Diode 181555 ibaa aa acaseaae Corhon, resistor CORED SU
p19 V11-4160-86 Zener diode = WZ-O71
020 V11-4162-66 Zener diode XZ.060 Ag ACSGF2H4A7N Solid resistor 4.74 +5% 1/2W
021~24| v11-0076-05 Diode 181555 R12,13 | RCOSGF2H101J | Solid resistor 1002 45% 1/2W
025 V21.0004.05 Varistor MV-13 R14~77)/ASI4AB3A3R9J — Metalfilm 3.90 +5% 1W
iSCELTANEOUS R18B~23) RCOSCFZHS5RGJ — Solid resistor 5.68 45% 1/2W
pte V40-7760-08 Indicating tube9-BT-12 al V03-2075-06 Transistor 28C2075
11 605-0035-05 Caramie titeamer BODE 02.3 V03-2509-06 Transistor 2S€2509
u2 40-4711-03 Feri-inductor 470aH Q4.5 | VO3-2290-16 Transistor: 28C2290J co
\3.4 L40-4701-03 Ferri-inductor 47uH 06.7 VO4-0046-05 Transistor 250235 (Y)
“6 L40-4711-03 Ferri-inductor 470gH DI v22-0031-05 Varistor SV-03
6.7 L40-2711-03 Ferri-inductor 270uH D2 V11-4363-36 Vanstor SV.4A
8 (40-4711-03 Ferrisinductor 470uH 03 V22-0031-05 Varistor SV-03
iz) (33.0616-05 Choke coil = 43uH « |] oes V11-0051-05 Diode 1N6O

27
```

---
## Page 28

```text
PARTS LIST

Ref No Parts No Description aus Ref. No. Parts No Description te
Th1.2 V11-3360-16 Thermustor 25029 . 3 ce CC45CH1tHO20C Ceramic 2pF +0.25pF
Th3 V11-7762-16 Thermistor 31026 C10. | C90-0262-05 Ceramic §=—0.0674F 25WV
c1i2 | CC4SSG1HOSOC Ceramic SpF +0.25pF
VRIV2 R12-0058-05 Potentometer 4706! (B) C13 | CC45LG1H470J Ceramic 47pF +5%
ci | CCA45LG1H2205 Ceramic 22pF +5%
TM $59-1404.05 x C15.16 | CC45LG1H1514 Ceramic 150pF +5%
TM2 $59-1403-05 ci7 CC4SSG1H150J Ceramic 15pF +5%
cis CC4SRG1H120J Ceramic 12pF 25%
ui 140-4701-03 Ferri-inductor 47uH cig CC45LGIH1510 Ceramic 150pF 25%
L2 L33-0025-05 RFC c20 CC45CG1H121J Cerame 120pF t5%
13,4 L33-0032-05 RFC RESISTOR
L5.6 NOT USED
u 133-0617-05 RFC -R~14_ | AO14cB2E0005 | Carbon resistor COOM =5% 1/4W
Ls 133-0025-05 RFC SEMICONDUCTOR
ug | L33-0625.05 RFC
L10~ 12) L40-1011-08 Ferri-inductor = 100uH = eatin de ou sitio MM
113.14 | L60-1021-04 Ferri-inductor = 1mH oS Veecoreos bine seraneis)
| “ - ransistor
11 | L19-0317-05 ‘Wide band transformer a4 VO03-1959-06 Transistor 28C1959 {Y)
T2 | L19-0311-05 input transformer D4 ¥11-0414.05 Diode 182588
3 L19-0313-05 NF Transformer oS V1104161-36 Diode 1SV53A
T4 | L19-0312-05 Output transformer TRIMMER/VC
= £04-0152-05 | M type receptacle ANT Te1 CO5-0305-05 Ceramic trimmer 12pF
a £08-0271-05 DC socket Tce2 CO5-0013-15, Ceramic trimmer 20pF
Ln £23.0043-04 a C02-0010-05 Variable capacitor
x E23-0046-04 Terminal (square) = 4 INDUCTOR/COIL
ben £23-0401- T ici «8
eee ee Sane * L1.2 L40-4711-03 Ferrwinductor 470uH
a FO1-0735-05 L3 | L40-1501-03 Ferri-inductor 15yuH
= F20-0078-05 Insulating mica x 3 L$~7 | L40-4711-03 Ferri-inductor 470u#
F23-0014-08 Shoulder washer x 3 is | L33-0025-05 Choke coil leH
Lg | L32-0609-05 Oscillator coil B
J31-0503-05 Beads x 4 L10 | b32-0608-05 Oscillator coil A
J32-0730-04 Hex: boss MISCELLANEOUS
- N14-0503-05 Wing nut B42-1645-04 Indication tape
- 0D22-0405.0¢ | Coupling
a D40-0604-05 | Dial hi
VFO ASS'Y UNIT (X60-1070-00) a £13-0163-05 | ‘pena
= £23-0046-04 | Terminal (square) x 4
Ref No Parts No. Description oe |
GENERAL j
- 801.0615-05 Dial escurcheon |
= 810-0612-04 Front glass (A}
= 820-0810-04 Dial scale |A}
GO1-0804-04 Coil spring
coe K21-0722-04 Main knob |
- N19-0608.04 Washer x 2 |
a X40-1130-00 VFO unit
VFO UNIT (X40-1130-00)
Ref No. Parts No. Description ere
CAPACITOR
c2 CC45SL1H390) Ceramic  39pF +5%
c3 CC4SCH1#1000 Ceramic 10pF +0. SpF
c4 CC45SL1H390J Ceramic = 39pF +5%
C7 C90-0262-05 Ceramic =0.047«4F 25Wv

28

```

---
## Page 29

```text
EXPLODED VIEW/DISASSEMBLY

Front glass (B)
Panel ass'y (810-0613-04)
{A20-2349-03)

Spanner ut

Dial scale (B)
(B20-0811-04)
Main knob
{K21-0722-04)
DD pean
+e
VFO unit assy a
(K60-1070-00) 9" ;
SS 2c Knob D spring
a” (G-02-0505-05}
AF gain knob . * Remove the VFO ass’ 4 Hex. head 3
= 'y by ex. hea mm screws.
6) {K23-0710-04) Symbol * . N99-0303-05.
Fig. 7 Front panel exploded view/removing the VFO ass'y

No} Description Parts No. Romarks

11] Subpanet 422.0714-13)

2| GND screw Woo -0266-08|

3] Rotary switch $01-1410-05) MODE

4| Phone Jack €11.0024-05| PHONE

6| 4P Mic socket | €06-0451-05] mic

6| Paccte swnen | $44-2402.05] STBY

7| Switch unit ig) | X41-1150-00

8| Motor 831.0618-05

8| Meterhouring | £29-0404-05

10] Potansiomerer | A06-9402-05] MIC CAR

11| Potontiomater | A06-9402-05] RF, AF

12| Potentiometer | 06-9403-05] RIT IF SHIFT

13) Gene ass’y 040.0603.05]

14| Seosaw switch | $36-2402-05| POWER

15) Switeh unit (A) | X41-1140-00)

16] Screw N30-2604-48)

17| Screw N34.3004.45)

(oy,

30

```

---
## Page 30

```text
PACKING /DISASSEMBLY

___. Warranty card
B46-0058-00 (K)

EXT SPKA 7P DIN plug

Phone plug (£07-075 1-05}

(E12-0001-05)

Operating manual
~~ B50-2643-00 (K}(W}
B50-2644-00 (T)
Protective cover
~~” 1H20-1410-03}

Fuse Plastic bag

(FOS-2434-05) oy H25-0116-04)
DC cable assy Se
sess,

&
Plastic bag

(H25-07 12-04) —~ \ y

|

|

Rear packing fixture
{H10-2520-02)

Accessory box _--——~
(H12-0441-04)
HO3-1708-04 (T)
Carton inside
HO1-2619-04 (K)(W)
HO1-2620-04 {T)

Carton outside
HO3-1706-04 (K}
Ae HO3-1707-04 (W)

Front packing fixturee-———
{H10-2509-02}

Short Jumper Lead

Cable with terminal

Green

Frant panel view Short jumper lead Rear panel view

ee aaa

Fig.6 BAND rotary switch (SO1-2417-05) wiring.

29
```

---
## Page 31

```text
DISASSEMBLY

8P DIN Socket (EXT VFO) ma
(E06-0851-05)

oo (€11-0005-15)

Self tapping screw
(N89-3006-45} x 4

{E06-0751-05)

Heat sink cover
(FO?7-0826-03}

3 * 6.8 pes.
yn

(N88-3006-46)

* Shaft coupling

< Rear panel removal >

< Filter unit removal >
1. Remove 6 screws *

Fig. 10 Rear panel/filter unit removal

1E31-0487-05)

1. Remove screws (6 self tapping screws.).

US jack (E11-00402-05) {EXT SP)

3 pole phone jack (KEY}

——7P DIN socket (REMOTE)

Self tapping flat head screw

31
```

---
## Page 32

```text
DISASSEMBLY

<To gain access to the RF unit> 7 %* Self tapping screw
1. Remove the six screws from the IF unit (as shown at right). (NB9-3005-46)

2. Remove the four shield screws.
3. Remove the shield.

*

|
| RF unit Bottom side
Self tapping round head screw

3x 63 pes.
(N87-3006-46}

IF unit
————— Self tapping round head screw

—s
(X48-1210-00) i
; 3x 143 pes
: IN87-3014-46)

Fig. 11 Repairing the RF unit

< Removing the counter unit >

1. Remove the six screws from the AF*GEN unit REMOVING THE FINAL UNIT
{X49-1110-00) (as shown at bottom)
2. Remove screws (*) from the counter unit, Remove Nine screws (®)
Q1: 2SC2075 Q4: 2SC2290 * J M type receptacle

(VO3-2075-06) (VO3-2290-16) (E04-0152-05)
Q2: 2SC2509 | Q5: 2SC2290 * J
(VO3-2509-06)) {VO3-2280-16)

Q6-: 2$0235 [Y)
(V04-0046-05)

9 AF+GEN unit
__ (X49-1110-00)
ae ~ Q3:; 28¢2509

(VO3-2500-06)

TM1: Thermostat
(S59-1404-05}

Counter unit
(X54-1360-00}

Wing nut

Heat sink s
leat sin 3 1N14-0509-05)

({FO1-0735-05)

Q7: 2SD235 (Y} = Nut
{V04-0046-05) (N14-0508-04}

@ Shoulder washer @ Insulating mica Self tapping round head screw
{F29-0014-05) (F20-0078-05) (N87-3014-46)

Fig. 12 Removing the counter unit Fig. 13 Final unit disassembly
32
```

---
## Page 33

```text
RECEIVER SYSTEM

TROUBLE SHOOTING

No receiver
Noise output
output

NG

Speaker

OK

NG

1 + Defective speaker |

NG

| + Defective O7: HA1368W (AF power amp]

- F

AF GAIN VR

1 Loose phanes jack contact |

+ Defective AF GAIN VR

NG

vco

+ Defective AF GAIN VA wiring
+ Loose contact

+ Defective voltage regulator

circuit

IF circuit

RF ANT NG

Defective
IFT

Defective
filter

* Refer to PLL troubleshooting

+ No RLA, RLT voltage
+ —6V supply trouble (May be low!
+ Defective Q6. 7 (AGC circuitl

+ T1~T? in IF unit requires adjustment

+ Defective CF1, 2
+ Defective XF (SSB or CW

* Check customer installed CW
filter.

+ Defective Q1~Q3 in the IF unit |

* Defective Q1~Q3 in the RF unit
+ Malfunction of band switch
+ RF BPF coil requires adjustment

circuit

Marker
inoperative

or is defective
+ Loose contact of RL1-1 in the
filter unit

unit

Soo NG
NOT

+ Defective Q4, 5 (Multivibrator)
+ Defective Q6 (Buffer amp!
* COUNTER circuit

33
```

---
## Page 34

```text
TROUBLE SHOOTING

TRANSMITTER SYSTEM

+ Protection ON

+ Fiker L1~11 malfunction

+ Relay AL1 inoperative

* Defective Q1~Q5 in the Final unit

+ Defective Q6, 7 (AVB} in the Final unit

Transmitter
output

inoperative

Low level

lf power transistors are

changed, they must be
of the same hfe rank. + Defective FET 5. 6.TR 7.8.9
Defective BPF in the RF unit

+ Defective BPF switch

2SC2290

R (hfe 30~ 65)
O (hfe 55~95)

Y (hfe 85~150)

+ ALC circuit inoperative
1) Defective Q2 in the filter unit

Defective Q1 in the IF unit
Defective relay in the IF unit

Confirm “No Power Output”

OK

NG

Defective Q10~Q12 in the AF+GEN unit
+ Check CAR input
+ Check MIC input

STBY switch
inoperative

+ Check VS. SS leadwire and this line
Defective Q24 [relay control)

+ Loose switch contact

COUNTER SYSTEM

Defective counter
operation

(Main operation
also abnormal)

No readout + PLL is UNLOCKED

YES a
terminal

+ Check VFO input |

\ YES
Readout rolls

VFO oscillator level insufficient

Defective counter Defective BL signal line

operation No readout YES + Defective IC15, 16 signal line
(Main operation i J + Defective indicating tube
is normal}
NO
\ YES + Counter input insufficient

Readout rolls 1) Q? (VFO MIX) circuit faulty
2) ICS, 11 (MIX) level faulty
+ Defective IC6 (Gate reset, latch
circuit)

34

```

---
## Page 35

```text
COMMON SYSTEMS

TROUBLE SHOOTING

No power from
power supply

S-meter
malfunction

PLLSYSTEM

No receive
and transmitt

+ B line shorted to ground

+ Defective Q7: HA1366W in the
AF*GEN unit

+ Defective Q3: 254473[Y)

{9V power supply} in the AF*GEN unit
+ Defective G2: uPC14305H

(5V power supply! in the AF*GEN unit
+ Replace fuse

Fuse NG
Power NG
switch

NG

+ Defective switch
+ Defective switch wiring

S-meter

OK

ALC
meter

OK

VFO NG

-| + Defective plug and wire

+ VR1 10k zero set requires
adjustment

+ VR2 470k? meter sensitivity
requires adjustment

+ Defective Q6, 7 (AGC circuit)

+ Defective L4: 150uH

* Defective relay RL

+ Carrer balance TC! requires adjustment]

NG

+ Defective Q2 |ALC amp}
+ Lead wire trouble from S-meter circuit

NG

+ Defective relay
+ Defective QS. 6 (S-meter circuit!

+ Defective 02: 1N6O
+ Relay RL1-3 loose contact

* Defective ALC-RF changing switch |

signal

CAR NG

+ VFO oscillator stopped

+ VCO output stop circuit Q7, 8. 21,
in the PLL is ON. Q8 voltage
collector is 5.7¥ DC, Nominal

signal
flove

NG

+ No CAR oscillation of signal not
reaching the PLL circuit

a
+

+ Defective preset dividing signal

35
```

---
## Page 36

```text
Ag Ae AGE Ag

ze)! I 2s
noo \#9" ! hes
| ihe Ce)
1 v 20
el e1
Aud any
Ag
|
Bulpeas ajeos ny 10} YA [243] DTy Isnlpy 2g
100-0021-1SX) (00-0€1-95x) | ee
LIND HSL LINQ WWNId auoz aje9s |INJ UL “OVW
LNO INV ZHW SZ HL
ALLO" AED" Apso’ AlZ’ uw? t t
3 1 rarer se £ if
= 4 M/s H > ceed L0'M>
rs)
= St mov ut vl | eso wa Av ZH ASS
cc
S
i 7 : AgZ AZ AgstO"
—
i=) | (LO-OLLL-6X) LIN, NAD
| (LO-O9ZI-PPX) LINN Ju (LOOLZI-8#xX) LINN 3!
Lud
> NOILOAS HALLIWSNV YL
ar {10
oll
-OLZL-@bX} WU 4] 94) UO 1O;98)ap Bu B41 18 INGiNO sy ay) duNseaWy [Zz
ZHW OSZ'PL te Indu
yuiod yoyo By pug 20)es9U0b yeubrs ay, wBBMIaq JODRdeo 201810408 jeubis gp Q 18 }Nd}No OIpNE (AAW OS) 118/AE9'O 404 JoUOD 818 AEIO “LNdLNO 4¥
AM 00G 47 100 & WaUUOD Indino so}e1aUOb jeubis eunseaw OY |p ule5 yy ay) 18g “Bunas jonU09 web yy JUeISUOD 2 YBIVA INdINO OIpNe “
WALA JY UP WO pea sae juduUNseaW abeyos yy ([E 1UeISUOS EB 40) PauINDSs Indo JoOpe29Ue5 jeUBIs ae UsoYs saan ML (At S) aP O -1NdNI
‘S3LON ZHIN OS¢@'PL -AONANDSYS
9 zal ze 6£ 6 29 oz sz as of se ve “a “ 6 eo
' £
7
= leach 4a Bg? &/} SEH 4k
ax vi BvD BN EL zg. w34Nd
£0 gz 20 ake 1O onnva32 20 10
AWY SOIR WY SI Uz diy J IE anvuine diy #8
{LO-O1Z 18x) LINO JI (00-002 1-1$x) LIN ¥aLtd

(LO-O9ZI-PPX) LINN 4

NOILO3S H3RAIFOaY &
```

---
## Page 37

```text
ADJUSTMENTS

GENERAL

Adjustment procedures for this transceiver are classified into
formal adjustments requiring @ full service bench and
simplified adjustment using a VTVM. AF and RF VITVM. AG.
and AF and RF dummy load

Complete adjustment also requires a frequency counter.
SSG. sweep generator, etc

(TX BPF, RX BPF, IF trap)

TEST EQUIPMENT REQUIRED

1. VTVM or DVM
1) Input resistance: More than 1 MQ
2) Voltage range: 1.5 to 1000V AC/DC
NOTE:
A high-precision voltmeter may be used. However, accurate
readings can not be obtained for high-impedance circuits.

2. RF VTVM
1) Input impedance: 1 MQ and less than 3 oF. min.
2) Voltage range: 10 mV to 300 V
3) Frequency range: 50 MHz or greater

NOTE:

6. RF DUMMY LOAD

1) Impedance: 50 to 752, 1502

2) Dissipation: 100W continuous or greater

3) Frequency limits. 1.8 to 30 MHz
The above-mentioned instruments may be used for simplified
adjustment. For complete, precise adjustment, the following
instruments are also necessary

7, OSCILLOSCOPE
Requires high sensitivity
capability

and external synchronization

8. SWEEP GENERATOR
1) Center frequency: 8.83 MHz
2) Frequency deviation. Maximum +5 kHz
3) Output voltage: More than 0.1V
4) Sweep rate: At least 0.5 sec/cm

9. Standard Signal Generator

1} Frequency range: 1.8 to 30 MHz

2) Output -6 dB~120 4B (025 pV~0O.5V)
NOTE:
Generator must be frequency stable

During adjustment special accuracy is not required (such as
input level or PLL circuit carrier oscillator output). a VTVM or
VOM may substitute for an RF VTVM by measuring through
the output of a detector as shown in item 12.

3. AF VTVM
1) Frequency range: 50 Hz to 10 kHz
2) Input resistance: 1 M@ or greater
3) Voltage range: 10 mV to 30 V

4, AF GENERATOR (AG)

10. FREQUENCY COUNTER
1} Minimum input voltage: 50 mV
2} Frequency range: Greater than 40 MHz

11. NOISE GENERATOR
Must generate ignition noise containing harmonics beyond
30 MHz

12. DETECTOR (TX B.P.F.)

1} Frequency range: 200 Hz to 5 kHz input O- ' Output
2} Output: 2 m¥~1 V. low distortion (To RF unit} 40P 4N6O (To oscilloscope}
330 1N60 400P
5. AF DUMMY LOAD I
1) Impedance: 82 GNDO © GND
2) Dissipation: 3 W or greater
REFERENCE
Japanese “SSG” American “SG”
BIB WR acho iesccevsannsts sennensssennedhsysensoesssvanves soe 0.25 uv
ods 0.5 uv
648 TuVv
D2 AG wrensveauseivbudeth cunana.ocatennsince-s Abs soSsnnsceevexvaly’ 2uVv
24 dB Bu
30 dB 158 "Vv
AQ B. cl ec RE h cecccecceecusternser essssressetbenseene 50 py
IB ieee tee leet dan SenecRA rs acunrves) osnnass’s dodbeoen canteens, 158 wv
600B 500 uv
70 dB 1.58 mv
80 dB 5mv
$0 dB 15.8 mV
100 dB 50 mV
120 dB

O5V 37
```

---
## Page 38

```text
ADJUSTMENTS

PREPARATORY WORK 2. Unless otherwise specified, set the controls as follows.
FS AF GAIN COUNTER i
1. Remove the upper and lower cases as shown in figure 7 COU CLOCKWISE
14. below RF GAIN FULL CLOCKWISE
: MIC GAIN CENTERED
CAR LEVEL CENTERED
RIT CENTERED
IF SHIFT CENTERED
MODE LSB
SEND/REC REC
NB OFF
CAL OFF
RIT OFF
FIX /VFO VFO
ALC/RF RF
VOX/MAN MAN
POWER ON
Fig. 14 Case disassembly
Measuring point Adjust
Item Condition T Specifications/Remarks
equinnien | Unit |Terminal) Unit | Part Reference
1. Power Supply
Voltage DC VTVM AF+GEN| J4.4P | AF+GEN| VA-3 ov
1) SV set
2} 2.8V J4.10P | AF+GEN| VA-2 2.8V
3) AVB T1V STBYSW — SEND FILTER | AVB FILTER | VR-4 11.0V
2. CAR 7 +
1) CAR output RF VTVM AF-GEN | J3,2P | CAR 1 0.3Vrms 0.3V=1dB6
2) Freq. RX 1) IF SHIFT
centered
2) LSB MODE Frequency | AF-GEN|J3,2P | CAR Tc2 8.82850 MHz
3) USB MODE counter CAR TC1 8.83150 MHz
3) Freq. RX CW MODE Frequency | AF*-GEN/J3.2P | CAR VR2 8.83070 MHz
counter |
| RX and TX SB: 8.82850 MHz
3. IF SHIFT Alternate Frequency . 7
SEND/REC counter AF-GEN | J3,2P | CAR VRe1 prhenad no
1
4. VFO }
Check output across > 0.2V=1 dB rms at VFO scale 250
0~500 range | RF voltmeter | AF-GEN/J1,6P | VFO Tc2 0,.2Vrms 0.2V£2 4B rms in FIX CH output
5. RIT v eee to 1) No frequency change between
Frequency 7 j Altenate RIT RIT ON and OFF
5.5 MHz | counter AF*GEN | J1.6P | AF-GEN | vat ON and OFF | 2) More than +1.5 kHz variable
2) RIT control | RIT range
centered ! |
6. VCO ] Oscillator level 1V +2 dB
“o" =250" “600~
" ww —3.5v | I]
(VFO: 00} | | NY Toa 33 ans [29.58 MMe 129 63 Mi
14 MHz — 3.5V |
POT EO SV | | asm [12.33 une 12 getdate | 12:83 Mi
= | is. 5¥)
T2 Fle | | 70m Jrseamns | look, | 16.33 MHz
PLL 13 28.0--5.0V | |14.0m |22.83 nz [23.08 MME | 0035 haus
(vFO: 500} | | (a5v1
OC VTVM | PLL TPA or 29.0 129.63 MHZ 139 08 anne | 20-39 MME
29.0+5.0V
(VFO: 0} 260M | 36.63 MHz |37.08 Moz | 37.33 MHz
74 7? MHz + 5.5V 265M [37.93 MHz [37.58 Miz | 4.(5.9¥)
(VFO: 250) : oe
TS 3.5 MHz 3.5V| |290m | 4,30¥1 |se.o8.mm: | 38.23 mHz
(VFO: 250)
286M |38,33 MHz 138.58 MHe 138.63 MHz
Note (| control voltage

38
```

---
## Page 39

```text
ADJUSTMENTS

Meesuring point Adjust
Item Condition Specifications/Aemarks
Instruments Unit | Terminal) Unit Parts Referance
7. TX BPF Maintain adjustment 35 MHP L345 7 MH: U6, 7.8
order 3.5 MHz, 12.58
ie mine. 28 mie Sweep Adjust coils tees, 833
if generator RF DAV RF i3~17 for waveform 1008
Oscilloscope | PLL vco as shown at 12.33 12.83]
Detector right (Fig, 15)
ae E Aippiw catio less than 6 dB Ripple ratio less than 2 al
8. AX BPF This adjustment Tracking Rear ANT RF L3~17 | Same as above
requires a spectrum | generator panel IFig. 161
analyzer and track: 29937352 | og pees a058
ing generator,
Otherwise adjust 22.83
as in item 7.
Spectrum RF Q2,E iw
analyzer | \
|
+ Ripple rate less than 2 dB Rigple cabo less than 1 dB
3. IF AMP 1) VFO: 250 ssc SP RF 3 1) Adjust for a
BAND: 14MHz | Oscilloscope IF Tint? maximum
MODE: USB AF VTVM output
82 dummy or | 2) Apply SSG
speaker output at( 25
i “Vl —6 6B to
the antenna
| terminal signa)
| to noise ratio
| approx. 15 dB| Airis ravo tess then 2 dB
10. IF trap 1) BAND: 7 MHz | SSG | sP RF L1.2 Adjust for mini- | Check for 80 dB attenuation :
AF VTVM mum S-meter | of 8.83 MHz signal. (Fig. 17)
reading and AF
output level
repeat the pro-
2) BAND: 14 MHz L3s cedure two
of throe times.
11. NB Connect the noise | Noise IF DI4IK| | AF 13 Adjust for a
generator to ANT | generator (cathode) wave form as > }
terminal Oscilloscope IF 1 shown at right.
S-meter reading repeat the pro- by L
S5~7. cedure two or + — Eo
three umes Aetore adjustment “ Afrer adjustment
12. Counter BAND: WWV U ANT Freq. TCci Set the BAND | Set for zero beat between WWV
standard VFO: 500 count. switch to WWV | and CAL
Oscillator | (15.000 MHz) dial scale: 500)
CAL ON connect an,
antenna to the
set.
While receiving
WWY Signal at
16 MHz. adjust
trimmer TC1 at
the side of
counter unit
for zero beat
between this
signal and 15
MHz
13, Base MODE: LS8 | ® 1) After adjustment, move the wire
current MIC: Counter- RE power | NAL Pte) FINAL |@ var | 150 ma fram D14 to L7 15QuH side.
clockwise 7 150pH| @ VR2 | 100 mA 2) After adjustment. resolder
BAND: 14 MHz Current meter, side 109 red wire to 3P terminal.
SEND position 2 ap
14. Carrier | Adjust at 14 MHz | Power meter ANT | AF-GEN VAS Carrier better * Repeat the procedure two or three
suppression | for RF full CW Oscilloscope TCc2 than 40 dB down| times
power. Switch Direction (Min.) | from output
to SSB position, coopler s signal
No input

3¢

```

---
## Page 40

```text
ADJUSTMENTS/TEST SET UP

|
| Measuring point Adjusting paint
ftem | Condition Specifications/Remarks
| instruments Unit | Terminal) Unit Pants Reference
15. Carrier point | 1) Connect AG RF power ANT CAR USB-+ | Shift the AF sig- | 400 Hz, 2600 Hz(—6 dB down!
to MIC terminal |meter Oscillo- Tc1 nal between 1500 Hz: Centered
and apply scope AG LSB— | 300 Hz and Check carrier suppression if carrier
an input of AF VTVM Tc2 2700 Hz sain: point is adjusted.
1500 Hz at 7 mV TC1 {in USB)
2) Adjust MIC and TC2 (in LSB}| Adjust TCI lin USB) and TC2
GAIN until so AF. output {in LSB) so RF reading is
output becomes reading is equal | the same.
Sw high and low
| level
16. Side tone AF GAIN: |
12 o'clock
MODE: CW KEY AF*GEN | VA4 0.63V/82
Install KEY and AF VTVM |
KEY down |
17. Ic meter MODE SW: CW Power meter, | When same es item 13-2)
STBY SW: SEND | DC current FILTER | VR4 } 491A | Adjust CAR level,
Same as item 13 meter | | IC meter reading to 114.
18, ALC BAND: 14 MHz | Check that RF output power is the
VFO: 200 j | same level input, SSB position at
MODE: CW RF power vee | ssw | 7 mV (1500 Hz) input
VR2 in the filter meter. AG FILTER | yr2 | 75W (28.5 MHz}
Unit: counter- AF VTVM |
clockwise |
STBY: SEND |
19. Protection | VR1 in the filter RF VIVM | FILTER TP! and @FILTER TCI MIN. —
DC vol: 501? TP2 as (Approx.
Unit: Full clock- meter. coaxial | shown O2~0.4V)
wise cable (50:2), dummy 4; right
Same as above Aad ieee 7 = pr = ” Fear Teo
Refer to 42 page OOW dummy | a tm _— Te umes
| (QVRLSSW 15020 wan meer (50%) peo saw Filter unit
19. Semeter | Adjust 14, 175 $s¢ | | BD
1) Starting | MHz in receive }1)1F 14) v1 | 10048 to the
level position | antenne fram
2).$1 2) IF 2) 76 $SG—S9 2) Less than 8 6B 2448
+60 dB. |
| 2)
3) $9 | 3) IF 13) VR2 | 8dBtothean- | 3) Less than 40 d8 +648
tenna from |
SSG-—S1 |
3)
| 40 dB (50
| #VI to the
| antenna from |
| | | SSG + s9 |
TEST AND ALIGNMENT SET-UP
Sweep generator Oscilloscope Spectrum analyzer Tracking generator

f -——~ 4} . 9
| °

Fig. 15 Test equipment connection/Item 7 TX BPE

40

oe

Refer to page 37

| |
+PLL unit} | RF unit |

i; L_ |

TS-120S : :

a

fig

NOTE:
Remove J18 and connect the sweep
generator to J18 connector (pin 1).

,O00

bd

|
| RF unit

f |
O2te) | de |

|
ss}

eS |

TS-120S vo

Fig. 16 Test equipment connection/Item 8 RX BPF

```

---
## Page 41

```text
TEST AND ALIGNMENT SET-UP

PC BOARD ALIGNMENT ar Oscilloscope _AF VTVM s8¢
lummy
a ° ° s as —
¥ COUNTER UNIT (X54-1360-00) Poli ce [> j< Bs) =]
ex) 9A ES #2 HLA _AJ@ | |= — a an 6
23 22 32 ooOdg00 SS © ° ®
bal ee zo 2° —
rs |

ie To SP OUT oO To antenna
fav tA

3

&

7) GND
6/ GND
5

a

3

2

Sv
sv
BL
-6
Mz

TS-120S

13] 4
12| 7
1} 3s
20} Mn
a}2r

ve?
. LJ
a * Caution:

8
?

6

5] ce NEVER TRANSMIT with SSG at antenna terminal.
¢/ Mo
3

2

LJ

- Fig. 17 Test equipment connection/Item

co 9 IF AMP, Item 10 IF TRAP

CAR UNIT »
(X50-1500-00) | S@=2=====) E
B2S2ae22 fewsae
DISPLAY SECTION Tt FA
pa ;
Te2
O
¥ AF-GEN UNIT (X49-1110-01) ro 2s
e38
RF UNIT >
(X44-1260-01) size
woo
== 2
ee ae
Y VFO UNIT (x40-1130-00) (Ol, fl (el,
lExqs gi co |] lo le Ss AHA le eX Ie
ae is Gt GEORGE GE
8 SE oo oo oO

ms 439 eX ta vss

sen: co ps Sone
06 6 om SO

=
a
ff
ov
aie
33
7
4
au
28
28

op]
oe

41
```

---
## Page 42

```text
PC BOARD ALIGNMENT

vy IF UNIT (X48-1210-01)

Jaz
1
“6 J2
6 |3
4
s
Zeeorpprpee

no

=Nwheanum©
°
z
°

CSyeeeUN =

cw

r4 ssp

[OQ]

ssa
J2s

42

FILTER UNIT >
(X51-1200-00)

FINAL UNIT >
(X56-1350-00)

PLL UNIT (X50-1490-00)

23

GND
SO0K

TPs
°

Of} [OF

OF

Pala

3s

2

OF |OF

‘
a

meoomr
recoan
Cees

+
a

fei(e)
(OllO)

@
dl

Oo

Tie

Ti,

4
©
PY
a

[Ok

fe z {Geen ¢
£ 3! 5
go O poces e
z
3s eeSESS 685
i” was
17x) VRS Din De. Do Oi inne Oe Op OreO.
oo
] < 2
oo i a
ek
=
é =
(]e GND - — x
Oond am 2 7 ch aummy
Ft ad pa \vR2° TSw 4a) 26 SMH?
orse - |¥VRZ. S5wAa) 16. 2Mrr
o 2 VR 154 fa}
TP TR2 Po H
ry OD o S]aur
jel
7) CMA e< eo ge eve ¢
2ie2 g2 2222
Hehes Grompreera cs 200) 202-55
vee vR2 VR2 vRe er 2 9° oo o 0° o°
°°
oO °
GNO
°
oRV
TM2
a 148
PO SND °
°° =a) TH Ave
25. oo °o
™ cr EEE vR2 VR
oo bs] a

```

---
## Page 43

```text
SPECIFICATION

(Power Supply Section)
Input voltage:

Output voltage:

Output current:
Continuous load current:
Output voltage fluctuation:

Ripple voltage:
Power consumption:

[General]
Dimensions:
Weight:

LED
GD4-203S-RD
(V11-7260-56)

Front panel
A20-2363-05 (T) Ee
A20-2364-05 (KW)

PS-30

Leg
(J02-0033-15)

Heat sink
(F01-0738-03)

5/16}D mm inch)

__ Case {Upper}
(A01-0746-12)

Case {Lower}

} {A01-0755-02)

Power switch

{S36-2402-05)

: . Rear panel

(A23-1432-02)

Fuse holder
{J13-0033-15)

Slide switch
($31-2027-05)

_AC cord with plug
{E30-0545-05)

2? Terminal plate
(E20-0282-05}

Cord bush

(J42-0403-05)

Power cord with plug

(E31-0500-05)

43
```

---
## Page 44

```text
<PS-30 PARTS LIST >

PS-30

Ref. No Parts No. Description Ris Ref. No Parts No. Description a
GENERAL AVR UNIT (X43-1330-00)
C1 €90.0813-05 Electrolytic G8O0uF 25WV w C12 CK45F1H103Z Ceramic = =O0.0lyF +80%—20%
Cc2~5 CK4SE2H103P Ceramic = OOtyF +100, -O% c3~s C90-08 14-05 Electrolytic 4700.F 25WV &
Cé.7 C90-0300-05 Ceramuc 470pF = ACI 50WV cé CK45F1H473Z Ceramic O.047uF +80%—20%
cs €91-0412-05 Ceramic 470pF ACSOOWV Cc? CK45F1H103Z Cerarmc O0mwFe +80%—20%
cg CK4SFIH473Z Ceramic § 0.047uF + 80%—20%
c10 CEO4WItE4SR7 Electrolyte 4.7uF 25Wwv R2~10 | RD148B2EO00) Carbon resistor OCOn +5% 1/4w
Q12 V08-1012-06 Transistor 2N5885 * RI RS14GB302A25 Resistor (Metal film) 2.20) +5% 2W
o1 V11-1365-06 Diode $25vB810 e a3 A92-0622-05 Resistor (cement) 5622 SW
- V11-7260-56 LED GD4-203S-RD w R78 R92-0619-05 Resistor (cement) SOmi? 5Ww
Ro RS14GB3F221J Resistor (metal film] 22002 =5% 3W
ALI $51-1406-05 Relay t |
ar VO1-0139-05 | Transistor  2SA671TDB
- A01-0746-12 Case lupper) « a2 V03-0183-05 Transistor 28C€733 [Y)
- A01-0755-02 Case [Lower| « |
- A20-2363-03 Frant panel (T} e 01,2 V11-0270-05 Oiede yosa
= A20-2364-03 Front panel (K.W) O03 V11-4167-06 |Zener diode XZ-090
- A23-1432-02 Rear panel {K) bs Da V11-0076-05, Diode 181555
- A23-1433-02 Rear panel (W.T)
VAI Rt2-0042-05 Potentiometer 500!) (B)
- B46-0058-00 Warranty card
- 650-2652-00 Operating manual (K.WI « |
> B50-2656-00 Operating manual (T)
- £20-0282-05 2P Terminal plate
- £22-0207-08 Lug plate x 3
= £30-0545-05 AC cord with plug
- €31-0500-05 Power cord with plug r
- FO1-0738-03 Heat sink 2
oe FOS-2035-05 Fuse |24) tt
- FO5-602 1-05 Fuse (6A) x 2 (K}
- FO5-4022-05 Fuse (44) {WT}
a HO1-2623-04 Carton case (inside) *
a H10-2523-02 Styren foam cushion IF} ®
- H10-2524.02 Styren foam cushion (R} x
-_ H12-0455-04 Cushion cd
~ H20-1413-03 Protection cover 2
- H25-0029-04 Protection bag [60 x 110mmi
- J02-0049.14 legx6
- J13-0033-15 Fuse holder
al }419-0509-04 LED holder
- | J32-1030.14 C000 « 2
= J41-0006--5 Core bush (K}
- (J41-0024-15 Cord bush (W.T)
- | J42-0403.05 Cord bush
aul J61.0019-05 Vinyle tie x 7
oad LO1-8066-15 Power transformer &
= X43-1330-00 AVR Unit t
$31-2027-05 Slide switch
$36-2402-05 Power switch ®

44

```

---
## Page 45

```text
PS-30

My HNOE-Sd VSXVN ASEIO

[e+ —9]ono
Amse/ley
belie) Ea Cie, >
Ww arg [is
v 2 NOISYSA AOZzZ-AOZI NOISUSA AObZ-AOZZ
2 ee ‘aa
'
!
H
\
H
[SoSisi 0 O60ZX: £0 ason: 210 =F
| AgeELISZz:z0 aWgvsz: +O * |) 2»
| c q
| |_ 49, 92
i Ae i
NmS2/tooLe $2
| ee O22 GY
! BUO0OS INA
|
| nee ee
= Le ie
8 3 B 8
|
| 3
| ee AS'9190 1 yoz AS91900
| ° ° ,
| Ane OLY | Ie T
o
| © 3h? : ] JE be-seoz-raszo
| amse/noory |g ime: A Ol@AGZS:10
| ft;  «|bO
| v2 [ a
| O6E O18 H <
es se ee
(O0-O£€E1- fbx)

45

```

---
## Page 46

```text
VFO-120 FEATURES/BLOCK DIAGRAM/SPECIFIGATIONS/ EXTERNAL
VIEW/ INTERNAL VIEW

FEATURES SPECIFICATIONS

1. The model VFO-120 is 8 remote VFO designed for use Oscillator frequency 5.50~600 MHz

with the 1208S (V) SSB transceiver. permitting cross- Oscillator circuit Clapp

channel transceive operation Output voltage O2V +1 GB (across 4702 load}
2. The VFO-120 matches the TS-120S (V) in design and Frequency stability hin 100 Hz per 30 minutes

appearance. its mounting angle is also adjustable
3. The FET oscillator circu assures high
distortion-i

4. The combi

after 3 minutes warm-up (at
bility and room temps

ature}

ULDUT Solid-state complement FET 2
on of precision antu-backlash gearing ar
ate

Te Transistor: 2

a lingar variable capacitor allows sccur frequency Diode: 6

reading. Calibration is at 1 kHz imtervals from 0 to 25 Power source From TS-120V

kHz Dimensions 123 (4-7/8) Wx 96 (3-13

The indented main knob is convenient for rapid tuning H 235 (9-1/4) D mm finch}
5. The RIT circuit allows independent receive frequency Weight 2.5 kg (3.5 Ibs)

adjustment without disturbing the main tuning * Spec SUBJECT 2 for improvement

fe)

Transmit frequency can be preset (spotted) by simply without 9
pressing the T-F switch without using FUNCTION

switch. The VFO is placed in transmit mode during BLOCK DIAGRAM

O and RIT indicators for error-

VFO unit X40-1130-00

receives p from its companion | os Butter amp Butter Amp Butter amet

is installed by simply connect e . |

supplied VFO and ground cab The VFO cable «
the output. power. and control lines

RAT Zemiret

f=~4

av IN
+[ Taansctive
Songrel 9v OUT
ian al Masitt WFO
ad p-—-t---,
Qe 1 om boo |
oe) Pee?) Oz.
EXTERNAL/INTERNAL VIEW Ne ae et me eer

INDICATOR unit
X54-1450-00

Front glass {A}(B10-0620-04) sy unit (X60-1070-00)

Dial scale {A} (B20-0810-04)

|
|
|
i

Push knob {square}
1K29-0709-04)

LEO PR2112D
(V11-7260-66}
Knob (K23-0721-04}

Pointer knob
(K29-07 15-04)

Panel
(A20-2342-04)

U—___teg 1J02-0323-05)
Main knob Hex. socket screw
{K21-0722-04) {N99-0303-05)

Switch unit 8P DIN socket
{X41-1240-00} (£06-0852-05}

46
```

---
## Page 47

```text
~> Mark denotes New Part

VFO-120 PARTS LIST

GENERAL

u Re-
Ref. No. Parts No. Description slice Ref. No, Parts No. Description marks
General - X40-1130-00 VEO unit
Sod AO1-0739-03 \ Case (Al upper - X54-1460-00 Incicator unit
al AQ1-0740-03 Case (8) lower
- A20-2341-04 Panel VFO UNIT (X40-1130-00)

- A23-1430-04 Rear panel = CAPACITOR
pe 839-0407-04 Spacer x 2 for leg cl CKASFIH103Z Cerame = O0.01uF = =+80.—20%
~ 846-0058-00 Warranty card (kK) c2 CC45SL1H380) | Ceramic 39pF = +5%
- 850-2633-00 Operating manual (Kw) 3. CC4SCHIHI00D | Ceramic = 10pF_ £0. SF
| 8S0-2634-00 Operating manual mm ca CC45SLIH390J | Ceramic = 39 F +5%
cs CK4561H 102K Ceramic 1O000pF +10%
= £02-0107-05 Diode socket c6 CK45F1H223Z Ceramic 0.022uF +80,~20%
a £06-0852-05 8P DIN socket . c7 €90-0262-05 Ceramic § 0.047uF 25WV
ie £30.1628-05 VFO cable i“ cs CC4SCH1HO2OC | Ceramic 2pF +0.25pF
ca CK45F1H223Z Ceramic 0.022uF +80.—20%
ia H01-2609-04 carn 1K). Ww) 10,11 | €90-0262-05 Ceramic 0.0474F 25WV
= HO1-2610-02 Carton (Tt) C12 | CC45SG1HOSOC Ceramic = 5pF 20.250F
= H10-2513-02 Front packing fixture C13 | CC4SLG1H470) =| Ceramic © 47pF 0 48%
a H10-2514-02 Reser packing fixture ca CC45LG1H220) | Ceramic 22pF = $5 %
= H12.0845.04 Cushion €15.16 | CC45LGIH1S1J | Ceramic 150pF +5%
- H20-1407-03 Protective cover ci7 CC4SSG1H150J Ceramic 15pF 25%
= H25-0117-04 Polyethylene bag 80 x 250 cis CC45RG1H120) Ceramic 12pF +5%
cig CC45LGIHI5IJ Ceramic 150pF =5%
a J02-0323-05 legx4 c20 CC45CGIHI21N Ceramic 120pF +5%
a J02-0409-04 Assistance teg c21 CK45F1H103Z Ceramic §0.01uF +80.—20%
- | J42-0412.04 Knob bush RESISTOR
ie qa 2018-26 Vinyle tie <5 Ri~1a | RD1ACB2ECCO. | Carbon resistorOCO2 +5% 1/4W
- K23-0721-04 Knob {RIT} SEMICONOUCTOR
- K29-0715.04 | Pointer knob {FUNCTION} at | voa-0020-05 FET 38K22 (Y)
- K29-0709-04 | Push knob [square) a2 | vO9-0011-05 FET 2$K19 (Y)
} Q3 V03-0079-05 Transistor 250460 (8)
- N99-0303-05 Hex. socket screw x 4 (VFO M4 x 10} a4 v03-1959-06 Transistor 2SC1959(¥)
oO. V11-7260-66 LED PR21120 D4 ¥11.0414.05 Diede 182588
os 17-4161-36 Varicap diode 1SV53A
- X41-1240-00 Switch unit od z
a X60-1070.01 VEO ass'y unit | TRIMMER/VC/INDUCTOR/COIL
TC) C05-0305-05 Ceramic timmer 12pF
SWITCH UNIT (X41-1240-00) TC2 C05-0013-15 Ceramic trimmer 20pF
oe = C02-0010-05 Variable capacitor J
cl CH45F1H103Z | ceramic | | }
POTENTIOMETER/SWITCH 1.2 | 40-4711.03 Ferri inductor 470uH
u3 L40-1501-03 Fert inductor 1SuF
vR1 RO1-2404-05 Ski? (B) (RIT) \5~7 | L40-4711-03 Ferri inductor 4704H
va2 12-3025-05 10k (8) us 33-0025-05 Choke col = txH
ie: L32-0609-05 Oscillator coil B |
si $29-1470-05 Slide rotary switch SAG-A4 ft L10 L32-0608-05 | Oscillator coil A |
$2 $40-2409.15 Push switch T.F SET SW MISC EOUS
$3 $40-2404.05 Push switch RIT SW tt tat cheb
RELAY) SEMICONDUCTOR 842-1645-04 indication tape
Rul $51-2408-05 Relay G2V-2 - 022-0405-04 Coupling
_ 040-0604-05 Dial mechanism 7
o1 | ¥11-0219-05 Diode VO6E
| - £13-0163-05 1P Pin jack
VFO ASS'Y UNIT (X60-1070-00) - | £23-0046-08 | Terminal (squarel x 4

- 801-0621-05
- 810-0620-04
- B20-0810-04
- 820-0811-04
- 830-0808-05
- K21-0722-04

bed N19-0608-04

Dial escutcheon
Front glass (A)
Dial scale (A)
Dial scale (B)
Pilot lamp

Main knab

Washer x 2

INDICATOR UNIT (X54-1450-00)

SEMICONDUCTOR
01 V11-3163-16 LEO TLY-205
02 V11-3162-86 LED TLG-205

47

```

---
## Page 48

```text
SCHEMATIC DIAGRAM/SPECIFICATIONS/PARTS LIST

NOTE: The circuit and ratings may change without notice due to developments in technology.

VFO-120 SCHEMATIC DIAGRAM
X60 -1070-O1

pe

|

|

|

|

|

|

|

|

|

|

|

|

|

|

|

|

!

|

1 Ou: 3sk2aiv), Q2:2SKI9(Y), 03:28C460(8) Oa 25c195907)

| D4:1s2 588, OS)isvs3a

|

|

|

| am

i aay)

|

1

b-——-—-————---— —---------—-
ono

VFO-120 SPECIFICATIONS

Speaker size: x is

Rated input: 1.0 wats

Impedance: 8 ohms

Frequency response: 300 Hz to § kHz

Dimensions: 4-7/8" wide x
3-3/4" high x
9-1/3" deep
lexcluding feet)

Weight: 3.1 Ibs.

48

MAIN RMT
ae? Soca sal
“9,
ea: ba X41-1240-00
ee ee eisaae me!
r TF SET RIT |
| s2¥ Usa if
orrQ; Baca
| ait e ‘|
2 eFedoogte ono m3 \
|
de Ms H
5
\ 4 mT | [|
| |
| an Hh H
|
| al lg ao |
| | fie [7 =e A ls |
ages SP (sits I 2 H
1 1 |] : I
! | ph z cra!
| t va a
l
I
|
| | Orcprati2o
|
|
T
ree
Orty-205 |
Ce:tec-205 |
SP-120 PARTS LIST
i] Ri
Ref. No. Parts No. Descnption Paris
— A01-0739-03 Case lA) e
— AQ1-0740-03 Case (8) e
= A20-2343-03 Panel cd
- A23-1431-04 Rear panel te
= BO4-.0401-04 SP orill s
= 807-0613.04 SP ring rad
- 639-0407-04 Spacer x 2
_ BS50-2636-00 Operating manual (K).(W) | ov
- B50-2637-00 Operating manual {T) | =
E20-0208-04 Terminal plate
- G53-0507-04 Packing x 4
HO1-2611-04 Carton +
- H10-2513-02 Front packing fixture
= H10-2514-02 Rear packing fixture
- H12-0445.04 Cushion
- H20-1407-03 Protective cover
H25-0077-03 Polyethylene bag i.
- J02-0323-05 Legx4
is J02-0409-04 Assistance leg
- J21-1144.14 Speaker mounting hardware x 2
a J61-0019-05 Vinyle te
=a T07-0204-05 Speaker z

```

---
## Page 49

```text
BLOCK DIAGRAM

om te ° sre
rs) ~ @ wo 3 G22
a 8 = eos
: nN 7
g i Sth 858
a a 5 Baa
nN “ ” NNN
by og anne
© F O55 olys Eset
=o = noo
@ Lenn Seeker
9° non g OPR@
a = ent
oO MxM x tO000
7) wu w 1 nanan
nu un m | AUN

2sc2290
eXe

wer

2sc2509

& &S e
pPC14305H

“2SA4731Y)
25¢2075
250238(Y)

Sy
2SA562(Y)
2SC784(0)

3SK73(GR)

AQ

Tl
s

SNi6913P

—<—S
3SK7S (lL)
j

oS
Walia HI

oO
o

HAI366W

HD74LSOOP MCAO44P

were (Lo
send quM,
sna 657
ne Bsn

te ete ee vee

“One eee it

we cece sae
Te C9 “
cOee tH Se "
ects cn ee "
an
ae

os 1
Lard) st
wt cote

acon

(ny 0385

cay Os

D3us YVO

(O9A)Oaus 13H

aacoad
$ Hoo ow ws
0 Veys2zo
a NOOO- —
is) 99000 wr.
84k S8ssset &
nt fe .
Fr o f RERFRFR sf pe
= . a 7
=, i” bf _
ons ~ a2o%00q }
HOH ~$ HGHOND| Zi fv
aon” HEDAUD gy *
ar =v TS
+O 900000
st teroeto
zo OUOO00H
OF FREREEE
r

ae

~ nee 55

Cra.) ~7 | arn |
I —— Le
| |_seovs | u
{ [peer |

(AW7dsI0) LINN 43LNNOD | I UND Wd |
fr -——— — — — J Le

we wx
Ww meme

ees |

ov woirnone [TO

LINA WAL Wa

AINA TWNId

aS eee ee

=
|
I
|
I
!
I
1
|
|
!
|
|
|
|
|
|

&

i a

LIND: N39-3¥

49
```

---
## Page 50

```text
ase

MANOAIG AQ

Ther WE FA

pore

+

Se a

4 {

oi wht hate
Seve i Rene ar mag a leelee a rd “t
Das) Me tan i : Tees 08 i
a be ad bon.
| 2 eane a2 *
aa recent: pe
ee a
i
{

now toe a Danae: com aby

*
1

mre ~ At hg Wide | int 2 OF be tee te te te be
wees ts 6 8 Deed Son eon”
ce Le zx amo 400 / $& 4 aos ee
eine psig Aen 22h Meooes
So tS Sten ge +550 iene tS
ne \ 3 ere bes Seay. SEP ASE yy.
ef = Wot By eSac EM geo 4 i RE Be
= he ia fs » ea
& o% ee Se 7 : ee
Ot aS aN 3 o— Pee aa 85 ‘ M hit mise 7 4
. ‘ 7 % fi RFit Eee
3 os b 4 t' bie BeR . & r “43 gues E
, b Cee gist.
ae a EF 3 re tld
~ . ae. on oO
2 = a ; ac: Sue ae
7 ba ed ad Serees
7 «

PaCOOSs

=a
2
baa
*
ie

ae

```

---
## Page 51

```text
VFO-120 FEATURES/BLOCK DIAGRAM/EXTERNAL VIEW/INTERNAL

VIEW/CIRCUIT DESCRIPTION

FEATURES

1. The AT-120 is a high performance HF antenna tuner and
is a modification of the popular AT-200 antenna tuner.
The AT-120 is small and light. and is suitable not only for
operation in your HAM shack but also for mobile of field
operation

2. The AT-120 is designed to be used on all Amaeur bands
meter, and an antenna switch

3. The AT-120 is designed to be used on the Amateur bands
between 3.5 MHz and 30 MHz

4 Antenna MATCHING or THROUGH operation is
BANOD-switch selected

5. The SWR meter operates in both THROUGH and
MATCHING modes

6. A mounting bracket is included for mobile operation

7. The panel meter can be illuminated by an external power
source.

8. The antenna matching circuit is effective in reducing TVI
since it acts as a band-pass filter

CIRCUIT DESCRIPTION

Directional Coupler

The directional coupler samples forward and reflected power
from the transceiver to the load.

Meter Circuit

The forward and reflected power sampled by the directional
coupler is used for SWR measurement. Forward power is

calibrated with the CAL control so the meter reads reflecte
poweer as SWR

EXTERNAL VIEW/INTERNAL VIEW

Case [A) {A01-0752-03)

Dicest panel
(A20-2362-03)
Meter :
(B31-0620-08)—

Panel

A20-2361-08 Case (B}

(KNW) E (A01-0753-08)

i Main knob
——r SS (K21-0744-08)

CAL knob

(K21-0746-04) BAND knob
(K21-0745-08)

Knob |push)

(K27-0406-04)

Band Selector Switch

This selects the band to which the matching circuit is tuned

In the “THROUGH” position, the antenna is connected di-
rectly to the transceiver, by passing the coupler, while still al-
lowing SWR measurement.

Antenna Coupler

The universal matching circuit is capable of matching 20 to
3002 loads to the 502 input impedance

BLOCK DIAGRAM

INPUT | DIREC-
4 SAND ANTENNA

@—S4TIONAL Lot secec-L44
courter| | son COUPLER

| |

METER
CIRCUIT
METER, ANT GND :

UHF receptacle

Detector unit
1X41-1208-00) =. —— L3 coil (5)
{L34-0841-08)
L4 coil (4)
(L34-0840-08)

7 —~vex2
(C02 .0014-08}

§1
```

---
## Page 52

```text
Mark: New Parts

AT-120 PARTS LIST/MB-100

Fi DETECTOR UNIT (X41-1208-00)
taf. No. Parts No. Description marke
GENERAL Ret No Parts No Description eee
2 A01-0752-08 Case (A) *
a A01-0753-08 Case (3) re C12 CM93B2H150J Mica 15pF +5%
- A20-2360-08 Panel (7) & C34 | CKaSFIH104z Ceramic = O.1uF = + 80% — 20%
- A20-2361-08 Panel (K} (W) &
A20-2362-03 Dicasting panel & R12 PD148B62E510) Carbon resistor 512 +5% 1/aw
z 831.0620-08 Meter te L1,2 L39-0403-08 Detector coil w
- 831-0058-00 Warranty card (K)
- 850-2667-08 Operating manual (K} (W) (T) 4
- 851-0875-00 Service manual (K} (W) (7) t
- 023-0061-04 Bearing
- EO4-0102-05 UHF receptacie x 2
- £€08-0203-25 2P socket
- £09-0203-25 2P plug
- E23-0015-04 Earth lug x 3 Support arm
J02-0089-05 Foot Stay attaching holes
7 J29-0402-08 Moble maunt &
- J42-0401-04 Knob bush
Guide stopper
: K21-0744-08 Knob x 2 R, X TUNE 2
- K21-0745-08 Knob BAND *
- K21-0746-04 Knob CALL
- K27-0406-04 Knob PUSH
coll
3 134-0841-08 Coil (5) t
4 L34-0840-08 Coil (4) 2
| 7 i M hol
5 L34-0849-08 Coil (6) Guide slot lounting holes
SWITCH
- $01-3404-08 Rotary switch *
; B40-2103:05 pum See Fig. 21 MB-100 Installation location
VC/POTENTIOMETER
C1,2 C02-0014-08 Variable capacitor 2 250pF 1KV|
- AO5-3406-08 Variable resistor 20 ki? (B) *
CAPACITOR
4 Not used Ref. No. Parts No. Description/Specification | Re:
5 CK45F1H 1042 Ceramic 0. 1)0F + 80% — 20%
6 CM93B2H2505 Mica 25pFo 0 + 5% aj J51-0008-15 pepe
7 CM93B2H171J Mica 170pF 5% 5 J84-0401-14 Stay x 2 te
8 M9382H101J Mica 100pF = +5% = J21-2633-04 Guide Bopper e
9 CM93B2H201J Mica 200pF = £5% J21-0401-04 Guide stopper (V)
10 CM93B2H341d Mica 340pF $5% = NOS-0008-04 6mm Hex. Screw x 6
an) CM9382H951tJ Mica Q950pF = =5% a N14-C009-04 6mm Nutx6
12,13 | CK45F1H104Z Ceramic = 0. 1) + 80% —20% = N15-1060-46 Flat washer
MISCELLANEOUS oa N16.0040-46 Lock washer x 2
: N0S:0007-08 Wingvot'x4 M5x8 - N16-0060-46 Lock washer x 6
E N14-0609-05 Wing nut - N13.0609-04 Nylon washer cd
- N30-4008-46 Screw
- N32-3006-46 Flat head screw
X41-1208- ie] wt ~
wad hago pln - NB7-3006-46 Round hedu phillips self tapping
- 401-2633-08 Carton {T) s Se ashlee
H01-2634.08 Carton (Kk) (WI sa eee Flat tap light tight screw x 2
v H12-0461-08 Cushion a N99-0304-04 Hex. nead screw x 6
ce WO1-0401-04 Hex. wrench

52

onsets «
```

---
## Page 53

```text
AT-120 SCHEMATIC DIAGRAM/SPECIFICATIONS

NOTE: The circuit and ratings may change without notice due to developments in technology.
SCHAMATIC DIAGRAM

SPECIFICATIONS

1. Antenna Coupler
Frequency range:

Input impedance:
Output impedance:
Through power:

Insertion loss:

2, SWR Meter
Frequency range:
Max. power:
Measurable range:

Min. power required:

(OE RuN

OUT PUT BANO S.w

1. THROUGH
3.5 MHz
7
14 oni =
21 | a
28 LAMP
12v

5 amateur bands from
3.5 to 29.7 MHz
502

20 to 3002, unbalanced.

150 W max. (3.5 MHz
band, 120 W)

Less than 0.5 dB at
optimum .match,

3.5 to 28.7 MHz
150 W

1.0:1 to 10:1
2W

C6 25P

. General
INPUT Connector:
ANT Connector:
GNO:
Dimensions:

Weight:

ee eee dk
BAND S.W

UHF type (509)

UHF type (50)

Wing nut and STUD.

162 (6) W x 60 (20-3/8) H
* 159 (6-1/4) DB mm.
{inch}

1.6 kg (3.5 Ibs) approx.
```

---
## Page 54

```text
| QWOITADFHOSVA\MARDAIG SITAMIHO2 OSt-TA
; P hey tanita yar apne) Ons Romip ect -BTGH

MEHORI SITAMANDE

“pélenAgat mi gyramolave cf sub eaioo my

be
ae 4
=f i
ra |
7 i
jo"
bo Be

comeretl ae bs be
® oy Fain Fact te
‘ ; BUNT ADISI9S 42
levered selqueD annaae fF

: ioe} gee) HY

cee aan -AOO8Y eet ARG

yohaas fed! B18) gt Ot

- UTS wae rot pnivy.

ond. TUSK
smatpoanag> THA
QuD

aro

ragne? yorsupert

sSonshertral suget

©) SW BNeOSiian Wi ierser eepienemid igbsari spas
J pie Oh ERAT SG) €ST. x Neendg guar
: 7 fm)

egal neingent

wel, AWS
‘wofd) yousbow
“wt xabt
ung obtamwReaht
‘Decne? sewoq ih

LET ARTO EIR: HA i mE, ae

```

---
## Page 55

```text
SC!

—~ Tire

Bccoscorcel

Fer
yserec
PEKI9CF)
PSciersccR)
2.9 BSCIBISEYT
25K) 96GR)
25C 46008)
25K30a(0)

isiter
151007

23.

COUNTER UNIT (X34°1360-00)

ab sth GS EEE

oe

PLE UNIT (X50-1490-001

—

; : i : =
| ——
Lf
|
—— : T
aie J} | =
hae i -
L {| | | cs
F 7 it | a ee ew i : =
1! | i] | if
mal | bp pe bb
T
HT |
} Li ||

ro

—=—3 Ho

af GEN UNIT
(X49-1110-01)

Et

ecovol

1
naiseew

. Bce60(8)
21999001
PSK19(GR) :
25ar013¢7) -
ESCI#IS(GAD O24: 28ane2tT)

```

---
## Page 56

```text
SCHEMATIC DIAGRAM

RF UNIT (X44-1260-01)

sKreiey
2 Psciarscy)
oT) 25c2086

210 Sarees cv)

iT | t :
———— — | Le
_ ,
= ~ | ; =
vent remeae ee ace, | f = - =
a SE || =
TT + -
7g
Sa _ tanieen i | |
al eras me, | = =
| !

peciazosK
- Os 2saa7 sy)

oo” asciesety)
Qa | a5KHOLGRI
Qes.ay | aSAIONS TY?

WFO UNIT (X4071130-00)

> 3sa2207) Qe BSE mSOLTD isvane
Q2 rKiecy) Oa 1SEROe
Os zcesois «oe SERA

Qzz | 25C1MES TGR

```

---
## Page 57

```text
MATIC DIAGRAM

SWITCH & UNIT
[X4h140-00}

1% 44-1269-01)

SWITCH @ UNIT
(x41e150-00)
c——

Brau: S5K76IGI Oo.9,0 5 1s1987
Qzi7,8 | Esciaiscy) Cae 152300 i
a Pree Oey Ysi9s3 itt }
10 Arar (v9 Ge i isi303

— ee ee ee EE Thi r oo

- LT | Tih Ty Ta te
—— = = = That ToT T ie? V2.4 a
i} — — — —o

| SS = | ge ee, mow

(4,23,24,26 | 1M6O
7-081
132380
wstse7
s.27,20 . sStBOS

4

|
|
|
|
|
|

fae RELAY UNIT
(X41-1250°00)

CAR UNIT [X50-1500-90)

Gr.2 : 2scesoce)
G3 | 2scrss9tr

VFO UNIT (x40-1120-a0) O12 886 as | a to Treg (ESTISSE-OS!
Ons Sseazeyy Oe We wOwIT! o3 isvssa os a
Oz: 25Kr90y) Oa” $2588 FILTER UNIT (X5I-1200-001 Se4. no: sieinscr Sree pana

: io sss ie wh
3 | 2scaso) Ds) 1Sva3e Ge daaarsyy 35.10 wrcer Ts-120$

Serer 2 wz-090

```

---
## Page 58

```text
TS-12C

(X48 -1210-01)

iF UNIT

TEL | | |e |)
t ohat tS tet
Heber | [SM
sail a S

vg P HBWHE EHH
pis ete

s2scaze

3 -
| it pes
| te
of “4
| lpate
= toe
. i - + "hr
a — —— : *
’ a4
ar : “
1 so
3 =
oT) bye!
Ee —— EE
t
+
|
ol
air
=i = =
, == t
j are : : 1
T
- dl ho =| al ils sce] sf
Babs ites pe te 1

{00 -09€}-#6X) LIND H3LNNOD

pan Woy i |

Jk

Lae His dopa BY

{00-O6p!-OSX) LINN Tid J

```

---
## Page 59

```text
TS-120V SCHEMATIC DIAGRAM

>] Finay PHIL _{x$6-15300-90) pre
3 car CT
gees | |
2
al { is Ox: $¥-03
aa a tee ae = = rors == Q2 be
ofth ce 4 2st2hi i ‘
et 82°23 &
IF UNIT (X48 -1210-01) E aeleer Hy
S7(x44-1260-017 if
ail Vig gaat it
4 & ° TI oa =
Seales nie
= | er
| try ae] | er
ox | oe 2sc2o75 Qe 25C496(¥) T i
| Q2,3:2862809 06 25023517) “UW |
-——
33 a3) PY
on
=e
-—— a
a
~ at
Bnei — = —
sSiais= on a] EL 71 ro ;
i + = :
— —— ee Fhe
cp
Ls + — °

£
a |

if

co

<
3

OF

mB an4,
nom.
7e,1@ 15185
20.8,22,23.27,70
Cares 152500
ow 10387
cy wr-08t

Ore 12SC224000R) or MAIMGgw Qy2 -2sxrsigAD
PCI43O5H Gens 2904008) Ss Baoisirh
Qs 2SA473Ir) Qe 2scisseiy) = See raasge ry)
‘ ee SENET 2S eg CES
— a — nn

|

|

je |
Ibe
—

```

---
## Page 60

```text
OV SCHEMATIC DIAGRAM

|
J

md
iz

z

4

Nr —1s88- 1200-00) _ —_—

FILTER

UNIT _xs1-1179-91)

1a] [ ane ©
HE : | 2k.
fg teas iq tS :
ate MSE Sh
4H Tae | | _
i Uff a4 ae Ta
=f | iS i £ rs " 7
| 2° ates, SE Beash ‘UJ oSHsRN,
| ac: ine, =
| —— sto eS
H aft 7 = 2
| =
=e
= = .
= == =F Ne! Don -toqy
=o = ipa a eye |
= =f + Ae a bar
ee i Wo 13 ster ©
= i r ye pel
AE CEA_UNIT 49-1110-O1) 4. a
4 “| neat ts t Se
| cy Gs Fat
4 rs Pare |-*t FJ |
| “ | Franti ial ade ads |
Bl ln Sly | ~ 3 bal i} a
i! iy § BE I" | - | { { { |
az a i ses jt
| i ia ages a
; | $ ar & oT
ies (| lfaweoy 8
oat on oy pret "i
2) ee Pata | dadidddg = 4
Ll ti TT Lit a 5 seis
2 eee fe a ell TE
=. ee or ba (no tae [~ CAR UNIT | if, Gs D
Hae ote | JI ixS0-1500-00) |
Hh 7 he iF. eye eA One en l | | i | |
i rs t Sion B LM y cf | | | dap
al ~ Mas | || | or mercies
a ar massege en recigion | | II | na oo 7
Pees pull 1 Saar es Mp | A lees soriearacon|
```

---
## Page 61

```text
A product of
TRIO-KENWOOD CORPORATION
6-17. 3-chome. Aobadai. Meguro-ku. Tokyo 153, Japan
san ERR eniaiinemmmemmeenemmmmsemmeememmemmmmmmmmmmmsiemmmmmtammesemmesds
TRIO-KENWOOD COMMUNICATIONS, INC.
119. West Wainut i. Compton. Califormia, 90220. U.S.A

TRIO-KENWOCO COMMUNICATIONS, GmbH

0-6374 Stempach TS. Indusinestrasse BA, Weat Garmacry
TRIO-KENWOOO( AUSTRALIA PTY. LTD.

30 Whiting Street. Artarmon, Sydney NSW. Austrana 2060

© 1979.4 PRINTED IN JAPAN 851-0877-10 &
```

