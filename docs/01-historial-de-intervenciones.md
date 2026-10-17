# Historial de intervenciones

Orden cronológico, de lo más antiguo a lo más reciente. Las dos primeras fases salen de dos relatos del propietario: el resumen de la reparación del pitido (el más antiguo) y la bitácora completa (más reciente).

## Fase 1: reparación del pitido en TX (la más antigua)

**Síntoma:** pitido u oscilación en TX en bandas altas (20, 15 y 10 m), progresivo. Ausente en 40 y 80 m. Intermitente al principio y luego constante. 40 W de salida en SSB sin modular. El monitor externo se apagaba al PTT en 10 m.

**Causas encontradas y resueltas**

1. Soldadura partida en el coaxil de la Relay unit (X41) hacia la RF unit. Refluida y reforzada. Resolvió la mayor parte del problema; el pitido quedó solo en 10 m.
2. Diodo D8 (original 1S1585) con fuga inversa (600 mV directa y 1360 mV inversa fuera de placa). D2, D3 y D8 se reemplazaron provisoriamente por 1N4148, lo que resolvió el pitido y los 40 W sin modular. Después D8 pasó a 1N4448.
3. Soldadura partida en la Filter unit, en la línea de señal. Resolvió la atenuación de recepción posterior al TX en frío.

**Boletines de servicio aplicados**

| Boletín | Cambio |
|---|---|
| SB-844 | R47 de 33 a 10 ohm, R50 de 560 a 680 ohm, C61 retirado, capacitor de 0,01 uF de bypass en la línea AVB |
| SB-832 | Diodos D2, D3 y D8 reemplazados |
| SB-816 | R3, R5, R7, R9 y R11 de 1,5K a 470 ohm en la RF unit |

**Recap en esta fase:** RF unit, IF unit, AF-GEN unit y PLL unit.

**Calibraciones posteriores al recap:** VR2 de la IF (cero del S-meter y ALC reajustado, porque los capacitores nuevos corrieron el offset) y VR1 de la IF (span del S-meter ajustado parcialmente a oído).

**Problemas secundarios identificados en esa fase:** ver [pendientes](06-pendientes.md).

## Fase 2: mantenimiento y eventos posteriores (bitácora, la más reciente)

Tres eventos separados:

1. Recambio de diodos en varias unidades (por degradación y como prevención).
2. Recambio de electrolíticos en las unidades Relay, RF, IF, AF-GEN, PLL y Filter.
3. Cambio de transistores en la Filter unit por el **evento del cable AVB**: el cable entre la Filter unit y la Final se cortó accidentalmente contra una chapa durante una intervención y produjo un corto a masa, que quemó dos transistores. El cable se reparó y el equipo funcionó bien desde entonces.

### RF unit (X44-1260-01)

| Pos. | Original | Reemplazo | Motivo |
|---|---|---|---|
| D1, D3, D5 | 1S1587 | 1N4448 | Preventivo |
| D2 | 1S2588 | BA389 | Preventivo; antes había un componente incorrecto (DO-35) |
| D4 | 1S2588 | BA389 | Degradado (870 mV fuera de placa); antes componente incorrecto |
| D6 | 1S1555 | 1N4448 | Preventivo |
| D7 | 1N60 | 1N60 nuevo | Se había puesto uno de silicio por error (medía 760 mV) |
| D8 | 1S1585 | 1N4448 | Se había puesto un 1N4148 por error |

### IF unit (X48-1210-01)

| Pos. | Original | Reemplazo | Motivo |
|---|---|---|---|
| D11 | 1N60 | 1N60 nuevo | Degradado (umbral elevado) |
| D12 | 1N60 | 1N60 nuevo | Degradado (medía 359 mV fuera de placa) |
| D14, D15 | 1N60 | 1N60 nuevo | Preventivo |
| Relay | Original | Relay sellado japonés nuevo | Preventivo |

### Filter unit (X51-1200-00)

| Pos. | Original | Reemplazo | Motivo |
|---|---|---|---|
| Q6 | 2SA562 (Y) | 2SA562 nuevo | Dañado por el corto de la línea AVB |
| Q9 | 2SA473 (Y) | 2SA755 | Dañado por el corto de la línea AVB |
| C35 | 220 uF 16 V | 220 uF 25 V | Recap preventivo |
| (otro) | 10 uF 16 V | 10 uF 25 V | Recap preventivo |
| (otros) | 1 uF 50 V y 0,47 uF 50 V | Iguales | Recap preventivo |
| RL1 | Relay original | Relay sellado japonés nuevo | Contactos carbonizados |

### Relay unit (X41-1250-00)

| Pos. | Original | Reemplazo | Motivo |
|---|---|---|---|
| D1, D2 | 1S1555 | 1N4448 | Preventivo |

### Reparaciones mecánicas y eléctricas

| Componente | Intervención | Motivo |
|---|---|---|
| Conector J41 (ANT/GND coaxial de la Filter unit) | Re-soldado y pistas rotas puenteadas | Soldadura fría partida; causaba atenuación intermitente en RX |
| Cable AVB (Filter unit a Final unit) | Reparado | Cortado accidentalmente por una chapa durante una intervención |
| Transformadores T1 a T9 de la IF unit | Optimizados a oído con referencia en TP | Ajuste fino pendiente con generador calibrado |

## Fase 3: pérdida repentina de TX, octubre de 2026

Ver [02-incidente-tx-oct-2026.md](02-incidente-tx-oct-2026.md). Resuelto el 17/10/2026 al limpiar y desoldar una viruta de estaño que hacía puente entre colector y emisor de Q7 de la RF unit.

## Estado conocido de los diodos de la RF unit

Según la bitácora más reciente. El resumen más antiguo decía que D2, D4 y D7 se conservaban originales; la bitácora posterior los reemplazó.

| Diodo | Estado actual |
|---|---|
| D1, D3, D5 | 1N4448 |
| D2, D4 | BA389 (DO-35) |
| D6 | 1N4448 |
| D7 | 1N60 nuevo (germanio) |
| D8 | 1N4448 (no figura en el esquema de WB4KDI) |

## Recap: estado

- Hecho: Relay, RF, IF, AF-GEN, PLL y Filter units (parcialmente documentado en la Filter unit).
- Sin hacer: CAR unit, Counter unit y Final unit (los electrolíticos de bias y desacople de la Final siguen originales).
