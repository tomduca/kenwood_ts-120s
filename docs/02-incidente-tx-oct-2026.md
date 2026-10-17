# Pérdida repentina de TX, octubre de 2026

## Resumen

| | |
|---|---|
| Síntoma | Sin TX en SSB ni en CW. RX perfecto. Medidores ALC e IC en 0 |
| Causa raíz | Una **viruta de estaño hacía puente entre colector y emisor de Q7 (2SC1815)** en la RF unit |
| Resolución | Se limpió y se desoldó la viruta el 17/10/2026; el TX volvió a funcionar. No se reportó reemplazo del transistor |
| Origen de la viruta | No investigado |

## Síntoma

- RX correcto en todas las bandas.
- Los relays conmutan y el PTT funciona (por MIC y por VOX).
- Sin TX en SSB ni en CW. ALC e IC siempre en 0, con ganancia de mic y carrier al máximo.
- Con carga fantasma, un handy sintonizado en la frecuencia, junto a la radio, no oye nada.

## Contexto

- El equipo transmitía normalmente, en todas las bandas y modos, hasta unos dos días antes. La pérdida de TX fue repentina.
- Todas las intervenciones del [historial](01-historial-de-intervenciones.md) eran anteriores.
- El diagnóstico se hizo con tester y SDR, usando el diagrama de niveles del manual como referencia (ver [metodología](05-metodologia-y-sondas.md)).

## Causa raíz y por qué producía ese síntoma

Q7 es la primera etapa amplificadora de TX después del BPF: un seguidor por emisor con el colector a la alimentación de TX y la salida por el emisor hacia Q8 (ver [referencia técnica](04-referencia-tecnica.md)). Con el colector y el emisor unidos por la viruta, el emisor quedaba a la tensión de la alimentación y la señal de salida se iba a masa por el desacople de esa alimentación. Solo pasaba lo que se acopla por capacidades parásitas, unos 40 dB menos. Como Q7 está alimentada únicamente en TX, el RX no se enteraba.

Sin excitación, la Final conduce su corriente de reposo pero no recibe señal: la corriente no varía con el carrier, los medidores ALC e IC quedan en 0 y no hay potencia de salida.

## Cómo se llegó a la causa (cronología del diagnóstico)

| # | Paso | Resultado |
|---|---|---|
| 1 | Alimentación | 14 V estables; consumo RX 0,73 A y TX 1,87 A, sin variar con el carrier en CW. AVB: 0 V en RX y 11,3 a 11,4 V en TX (regulador de 11 V, normal) |
| 2 | Continua en la Final | Bias de Q1, Q6, Q7, Q2/Q3 y Q4/Q5 coherente con el esquema; colectores con 13,8 V. La corriente de reposo medida (unos 160 mA) está algo por encima de los 100 mA del manual |
| 3 | Señal en la IF | Portadora y modulación visibles en el SDR. De GEN a TIF no hay pérdida respecto del nominal (GEN 68 y TIF 48, ganancia 25,4): la IF unit, su ALC, D9 y el relay están bien |
| 4 | Mezclador Q5/Q6 | Compuertas de -3,0/-3,34 V (RX) a +0,67/+0,77 V (TX), fuente de 0 a 1,0 V, drenador de 13,6 a 12,7 V: conduce, y la conmutación de bias (Q10) funciona |
| 5 | Niveles con SDR a 7074 kHz | C52 58; salida del BPF (C54 lado Q7) 50; J34 ANT 5 y MKR 2; DRV 12. El BPF pasa la señal (unos -8 dB), no hay fuga hacia la antena, y de C54 a DRV faltan unos 43 dB respecto del nominal |
| 6 | Continua de Q7 en TX | Base 2,0 V, colector 5,68 V, emisor 5,68 V (esperado: unos 1,8 / 11 / 1,1 V). Colector y emisor a la misma tensión: están unidos. La base coincide con el divisor R42/R40 con el colector a 5,68 V (unos 2,07 V) |
| 7 | Reparación | Se limpió y se desoldó la viruta de estaño que unía colector y emisor; el TX funciona de nuevo |

## Descartado y con qué evidencia

| Hipótesis | Evidencia en contra |
|---|---|
| Fuente, fusible, alimentación general | 14 V estables, RX normal |
| Línea AVB y su conmutación; cable remendado | AVB 11,3 a 11,4 V en TX en la Final y en la RF unit |
| Polarización de la Final | Valores cercanos al esquema |
| Final en corto C-E | RX normal con la fuente estable |
| Finales abiertos | Conducen en reposo (unos 160 mA); de DRV a PO hay unos +42 dB (nominal unos 47) |
| IF unit (modulador, filtro, ALC, D9, relay) | GEN a TIF sin pérdida |
| Bias de TX de la RF unit (Q10, KEY, D6/D7) | Compuertas de Q5/Q6 conmutan como en el esquema |
| BPF y diodos D2/D3 | C52 a C54 pierde unos 8 dB; J34 ANT y MKR sin señal |
| Cable DRV | DRV en la RF unit y en la Final coinciden |
| Relays (IF, Filter) | La señal pasa por el relay de la IF y D9 con nivel nominal; RL1 está después de PO |
| Protecciones térmicas | AVB presente en TX |
| Reguladores fuera de rango | AVB 11,4 V, -6 V correcto, bias del mezclador y de la Final en rango |

## Lecciones del diagnóstico

- El ohmetro en circuito engaña (finales, Q2/Q3, colectores): el transformador y las resistencias vecinas dan lecturas bajas o abiertas aunque el transistor esté bien.
- Una señal por proximidad (lazo o sonda) no prueba potencia ni que el camino conduzca. Un corte deja pasar unos 40 a 60 dB por acople parásito.
- El SNR del SDR no es lineal. Comparar solo puntos medidos con la misma ganancia y el mismo ancho de banda, y cada punto a su frecuencia correcta (FI a 8,83 MHz; RF a la frecuencia de operación).
- El diagrama de niveles del manual (p. 36) fue decisivo: comparar las diferencias entre puntos consecutivos con las nominales ubica el tramo cortado.
- La tensión de continua en cada pin de la etapa sospechosa confirmó la causa de una forma que la señal no podía.
- Antes de cambiar piezas, una inspección visual con lupa de los pads de la etapa sospechosa: una viruta de estaño suelta explicaba todo.
- AVB mide 11 V (no 14 V): sale de un regulador de 11 V.

## Correcciones del propio proceso (para no repetirlas)

- Se trató a Q8 a Q13 de la IF unit como cadena de TX; es el limitador de ruido (NB). El camino de TX pasa por Q1 de la IF, y CF1/CF2 son del camino de RX.
- Se pensó que D6/D7 daban el bias de Q7; el bias sale de R42/R40.
- Se supuso que los finales estaban abiertos por pruebas de ohmetro en circuito.
- Se midió la resistencia de 15 mohm con el jack de Amp: cortocircuito directo, chispa y cable fundido (el equipo no sufrió daños).
- Se tomaron lecturas a una frecuencia equivocada en J30/J32/J35 (se midió a la de operación en lugar de 8,83 MHz); se repitieron.
