# Mediciones y niveles

Todas las mediciones se tomaron **con la falla presente**, salvo la última sección (valores de referencia con el equipo funcionando, a completar). Pares RX / TX salvo indicación. CW, carga fantasma, 3 a 5 segundos por medición de TX.

## 1. Fuente y consumo

| Medición | Valor |
|---|---|
| Tensión de la fuente | 14 V estable, sin caída en TX |
| Consumo RX | 0,73 A |
| Consumo TX (CW) | 1,87 A, sin variar con el carrier |
| AVB en la entrada de la Final | 0 V / 11,3 V |
| AVB en J33 (RF unit) | 0 V / 11,4 V |
| J33 KEY (CW) | 0 V / 0,34 V, fijo |
| J33 pin -6 V | -5,94 V / -5,89 V |

## 2. Final unit: continua

| Punto | RX | TX |
|---|---|---|
| Q1 base | 0 | 1,65 a 1,84 V |
| Q1 colector | 0 | 11,0 a 11,2 V |
| Q1 emisor | n/d | 0,9 V |
| Q6 base / emisor | n/d | 1,35 V / 0,76 V |
| Q7 (Final) base / emisor | 0 / 0 | 1,39 V / 0,79 V |
| Q7 (Final) colector | 13,97 V | 13,79 V |
| Q2/Q3 base | 0 | 0,72 V |
| Q2/Q3 emisor | 0 | 0 |
| Q2/Q3 colector | 13,97 V | 13,79 V |
| Q4/Q5 base | 0 | 0,65 V |
| Q4/Q5 colector | 13,89 V | 13,84 V |

**Resistencia de 15 mohm (alimentación F14 de los finales):** ambos extremos a 14 V incluso con el equipo apagado. Entre extremos: 0 mV en RX y 2,4 mV en TX (unos 160 mA), sin variar con el carrier en CW. El manual da 100 mA de reposo para los finales.

**Ohmetro con el equipo apagado** (artefactos de medir en circuito, no indican falla): colector de Q4/Q5 en OL en ambos sentidos y luego 0,08 V con pitido (rojo a masa, negro a colector); Q1 158 y 170; Q2/Q3 "cerrado" en las tres patas. Los colectores de Q4 y Q5 son el mismo nodo (primario de T4).

## 3. RF unit: mezclador Q5/Q6 (RX / TX)

| Pin | Q5 | Q6 |
|---|---|---|
| Compuerta | -3,1 / 0,68 V | -3,0 / 0,67 V |
| Compuerta | -3,34 / 0,77 V | -3,34 / 0,77 V |
| Fuente | 0 / 1,0 V | 0 / 1,0 V |
| Drenador | 13,6 / 12,68 V | 13,6 / 12,7 V |

Esquema: compuertas -3,9 / +0,6 V, fuente 0 / 0,7 V, drenador 13,5 / 12,6 V. El mezclador conduce en TX.

## 4. RF unit: Q7 con la falla

| | Base | Colector | Emisor |
|---|---|---|---|
| RX | 0 | 0 | 0 |
| TX medido | 2,0 V | 5,68 V | 5,68 V |
| TX esperado (esquema) | unos 1,8 V | 11 V | 1,1 V |

La base coincide con el divisor R42 (82K) y R40 (47K) con el colector a 5,68 V: 5,68 x 47 / 129 = 2,07 V.

## 5. Sondas por proximidad y de diodo

- **Lazo SDR:** señal que varía con el carrier en T1, Q2/Q3, T2, bases de Q4/Q5, T4 y PO. Detecta por proximidad: no prueba potencia.
- **Sonda de diodo (tester, 1N4148):** 0 en PO, base y colector de Q1, T1 y colectores de Q2/Q3 (colector de Q1 con 30 a 60 mV en RX y TX, ruido). Reacciona con un handy, así que la sonda funciona. El silicio no rectifica por debajo de unos 0,5 V de pico.

## 6. Niveles con SDR++ (SNR, sonda de contacto 33 pF + 4,6 kohm)

Los números de SNR no son lineales ni calibrados. Comparar solo series con la misma ganancia.

| Serie | Ganancia | Frecuencia | Puntos |
|---|---|---|---|
| A | 43,4 | Operación | DRV de la RF unit 18 a 20 |
| B | 37,2 | Operación | DRV ~15, base de Q1 ~15, colector de Q1 ~24, T1 sec. ~10, colectores de Q2/Q3 ~40 (posible saturación) |
| B' | 8,7 | Operación | Colector de Q1 5, colectores de Q2/Q3 22, bases de Q4/Q5 9 |
| C | 0 | 8828,5 kHz | J30 GEN 37, J32 TIF 20, J35 TIF 20 (carrier 50 %) |
| D | 25,4 | 8825,5 kHz | J30 GEN 68, J32 TIF 48, J35 TIF 48 |
| D' | 25,4 | 7074,5 kHz | C52 58, DRV 12, colector de Q1 20, colectores de Q2/Q3 35, bases de Q4/Q5 25, PO 54 |
| E | 25,4 | 8828,5 kHz | J35 TIF 48, C11 lado L8 21 |
| E' | 25,4 | 7074 kHz | C11 lado L8 32, C11 lado L7 75 (C11 une L8 con L7), C10 lado L6 52, otra pata de C10 35, C54 lado Q7 50, J34 ANT 5, J34 MKR 2, DRV 12 |

## 7. Niveles nominales del manual (página 36)

A 14,25 MHz, con voltímetro de RF y el ALC a fondo de escala. Tensiones eficaces.

| Punto | Nominal |
|---|---|
| Entrada de carrier al modulador (CAR) | 0,71 V |
| Salida de la AF-GEN a la IF (GEN, Q12) | 0,112 V |
| Salida del filtro de cristal | 0,033 V |
| Salida de Q1 de la IF (IF amp) | 0,28 V |
| Entrada del mezclador de TX (TIF) | 0,004 V |
| Salida del mezclador (C52) | 0,165 V |
| Q7 / Q8 / Q9 (entradas) | 0,16 / 0,15 / 0,11 V |
| DRV (entrada de la Final) | 0,3 V |
| Colector de Q1 de la Final | 1,75 V |

Ganancias nominales en tensión: GEN a TIF unos -29 dB; TIF a C52 unos +32 dB; C52 a DRV unos +5 dB; DRV a colector de Q1 unos +15 dB.

## 8. Medido contra nominal (serie de ganancia 25,4)

| Tramo | Medido | Nominal | Lectura |
|---|---|---|---|
| GEN a TIF | -20 | -29 | Bien, sin pérdida |
| TIF a C52 (mezclador) | +10 | +32 | Algo bajo, incierto (la referencia de TIF está antes de T4) |
| C52 a C54 (BPF) | -8 | casi 0 | El BPF pasa la señal; SB-816 (470 ohm) puede explicar parte de la pérdida |
| **C54 a DRV** | **-38** | **+5** | **Faltan unos 43 dB: el puente de estaño en Q7** |
| DRV a colector de Q1 | +8 | +15 | Leve |
| DRV a PO | +42 | unos 47 | Cercano al nominal |

Con los boletines SB-816 y SB-844 aplicados, los niveles nominales del manual en el BPF, Q9 y DRV pueden diferir.

## 9. Valores de referencia con el equipo funcionando (a completar)

| Medición | Esperado | Medido |
|---|---|---|
| Q7 RF unit, TX: base / colector / emisor | unos 1,8 / 11 / 1,1 V | |
| Q8 RF unit, TX: base / emisor / colector | unos 2,8 / 2,1 / 9,9 V | |
| Q9 RF unit, TX: base / emisor / colector | unos 1,1 / 0,5 / 12 V | |
| DRV con SDR (ganancia 25,4, 7074 kHz, CW 50 %) | mucho más que 12 | |
| PO con SDR | mucho más que 54 | |
| Potencia de salida con vatímetro | | |
| ALC e IC con carrier moderado | reaccionan | |
| AVB en TX con excitación normal | unos 11 V | |
| Corriente de reposo de los finales (F14) | 100 mA | |
| Corriente de reposo de Q2/Q3 (D14) | 150 mA | |
| Consumo TX con excitación normal | | |
