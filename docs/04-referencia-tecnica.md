# Referencia técnica

Datos del manual de servicio y del esquema de WB4KDI, leídos de imágenes escaneadas: confirmar en papel antes de usarlos para decidir.

## 1. Camino de TX

```
AF-GEN: micrófono o carrier -> modulador balanceado (D11 a D14, T2) -> Q12 (2SK19, unos +10 dB)
  -> J30 (GEN) -> IF unit: diodos de conmutación SSB/CW y filtro de cristal
  -> Q1 (3SK74, unos +30 dB, ganancia controlada por el ALC)
  -> C23 (15 pF) + D9 + relay de la IF -> J32 (TIF) -> J35 (TIF) en la RF unit
  -> T4 -> mezclador Q5/Q6 (3SK74; inyección del oscilador por J38 y T5)
  -> C52 -> BPF de banda (compartido con RX) -> Q7 -> Q8 -> Q9 (2SC2086) + T6 -> DRV
  -> Final unit: Q1 (2SC2075) -> T1 -> Q2/Q3 (2SC2509) -> T2 -> Q4/Q5 (2SC2290) -> T3/T4 -> PO
  -> Filter unit: filtros pasa-bajos L1 a L11 (selector S4), L18 (muestreo de potencia directa y reflejada), RL1-1 -> ANT
```

Notas:

- El RX pasa por los filtros cerámicos CF1/CF2, el NB gate (aro de diodos D1 a D4) y el filtro de cristal. En la IF unit, Q8 a Q13 es el **limitador de ruido (NB)**, no la cadena de TX.
- El BPF es el mismo para TX y RX: si el RX pasa bien por un sector, el contacto y las bobinas de ese sector están sanos.

## 2. Q7 de la RF unit (2SC1815 Y)

| | |
|---|---|
| Etapa | Primera amplificadora de TX después del BPF; el manual la marca como "AMP" |
| Función | Buffer de banda ancha: separa el BPF de las etapas siguientes y entrega la señal a Q8 con baja impedancia de salida |
| Ganancia | Casi unitaria en tensión (0,16 V en su base y 0,15 V en la de Q8, según el manual); aporta ganancia de corriente |
| Configuración | Seguidor por emisor. Señal por la base (C54 y R62); colector a la alimentación de TX; salida por el emisor (C57 y R63 hacia Q8) |
| Alimentación | Solo en TX (11 V en el colector; 0 V en RX) |
| Polarización | R42 (82K, colector a base) y R40 (47K, base a masa), con realimentación de continua. Emisor a masa por R43 (100 ohm) y por R41 (100 ohm) en serie con L30 (100 uH) |
| Valores en TX | Base unos 1,8 V, colector 11 V, emisor 1,1 V |
| Pines del 2SC1815 | Emisor, colector, base, vistos con la cara plana de frente y de izquierda a derecha (verificar con el circuito) |
| Falla del incidente | Una viruta de estaño unía colector y emisor: la salida iba a masa por el desacople de la alimentación (unos 40 dB menos), solo en TX |

## 3. Alimentaciones

| Riel | Origen | Valor |
|---|---|---|
| 14A | Fuente, sin regular | 14 V |
| AVB | Regulador de 11 V de la Filter unit (Q4, Q5, Q6 y el transistor de paso Q9, hoy un 2SA755), solo en TX | 0 V en RX, 11,3 a 11,4 V en TX |
| 9 V y 5 V | Reguladores de la AF-GEN | Nominales |
| -6 V | Polarización negativa de las compuertas del mezclador | Unos -5,9 V |

## 4. Corriente de reposo (manual, ajuste de bias)

Condiciones: modo LSB, mic al mínimo, banda de 14 MHz, posición SEND, amperímetro en serie.

| Etapa | Control | Corriente | Dónde se mide |
|---|---|---|---|
| Finales (Q4/Q5) | VR2 | 100 mA | Terminal F14 (3P) |
| Q2/Q3 | VR1 | 150 mA | Terminal D14 |

Después de ajustar hay que devolver los cables a su lugar. Con el shunt de 15 mohm se midieron unos 160 mA en los finales, por encima de lo especificado.

## 5. Protecciones

- **Térmicas de la Final:** núcleo del transformador de salida (más de 120 °C) y disipador (más de 90 °C). Fuerzan RX. El ventilador arranca a unos 45 °C.
- **ROE y ALC:** el toroide L18 de la Filter unit muestrea potencia directa y reflejada. Q1 y Q2/Q3 de la Filter unit amplifican esa tensión y la aplican a la línea ALC, que controla la segunda compuerta del 3SK74 Q1 de la IF y el 2SK19 Q12 de la AF-GEN.

## 6. Repuestos y reemplazos

- Finales 2SC2290: por rangos de hfe: R 30 a 65, O 55 a 95, Y 85 a 150. Al reemplazar, usar el mismo rango (par apareado).
- Q9 de la Filter unit: hoy 2SA755 (original 2SA473).
- Diodos de la RF unit: ver [historial](01-historial-de-intervenciones.md).

## 7. Boletines de servicio aplicados

| Boletín | Cambio | Efecto a tener en cuenta |
|---|---|---|
| SB-816 | R3, R5, R7, R9 y R11 de 1,5K a 470 ohm (amortiguación del BPF) | Baja el Q del BPF y sube su pérdida: puede explicar parte de los -8 dB medidos |
| SB-832 | Diodos D2, D3 y D8 | |
| SB-844 | R47 de 33 a 10 ohm, R50 de 560 a 680 ohm, C61 retirado, bypass de 0,01 uF en AVB | Cambia la etapa de Q9: los niveles nominales del manual en Q9 y DRV pueden diferir |

## 8. Esquema contra placa real

- El esquema de WB4KDI está encabezado "TS-120V" en su primera hoja, pero las hojas de unidad son del TS-120S.
- La placa real de la RF unit tiene D8; el esquema solo muestra D1 a D7. Puede ser otra revisión de la placa.
- Algunas etiquetas de tensión se leen con ambigüedad en el escaneo (por ejemplo el par RX/TX de la base de Q7).

## 9. Unidades y conectores

| Unidad | Código |
|---|---|
| IF unit | X48-1210-01 |
| RF unit | X44-1260-01 |
| Filter unit | X51-1200-00 |
| Final unit | X56-1350-00 |
| AF-GEN unit | X49-1110-01 |
| CAR unit | X50-1500-00 |
| Counter unit | X54-1360-00 |
| PLL unit | X50-1490-00 |
| VFO unit | X40-1130-00 |
| Relay unit | X41-1250-00 |

| Conector | Pines |
|---|---|
| J30 (IF unit) | NBS, GND, GEN |
| J32 (IF unit) | GND, TIF (pin 2) |
| J35 (RF unit) | GND (pin 1), TIF (pin 2) |
| J33 (RF unit) | -6 V (1), KEY (2), AVB (3) |
| J36 (RF unit) | RLT, RLR, AGC, RB, 14V |
| J34 (RF unit) | MKR, ANT (cada una con su GND) |
| J25 (IF unit) | ALC (pin 1), RLR, RLT, RL, RSC y otros |
| J4 (AF-GEN) | pin 11 (RT1): wiper del RIT |
