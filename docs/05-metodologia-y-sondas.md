# Metodología y sondas

Cómo se midió durante el incidente, para poder repetir o comparar.

## Sondas

### Sonda de diodo para tester (tensión de pico, con bloqueo de continua)

![Sonda de diodo](../img/sonda-diodo-tester.svg)

| Componente | Valor |
|---|---|
| C1 | 1 nF (102), cerámico de 50 V o más |
| D1 | 1N4148 (silicio) o 1N60 (germanio); la banda (cátodo) hacia el nodo A |
| R | 220 kohm |
| C2 | 10 nF (103) |

- Uso: punta en el punto a medir, clip de masa cerca, tester en continua en el jack V (nunca en Amp), escala de 20 V o de 2 V.
- Limitación: el silicio no rectifica por debajo de unos 0,5 V de pico y el germanio por debajo de unos 0,2 V. Una lectura de 0 no prueba que no haya señal.
- Con el 1N60, no pasar de unos 15 a 20 V de pico (menor tensión inversa que el silicio).

### Sonda de contacto para SDR (divisor capacitivo)

![Sonda SDR](../img/sonda-sdr-contacto.svg)

| Versión | C | R | Atenuación aprox. | Uso |
|---|---|---|---|---|
| Principal | 33 pF | 4,6 kohm | unos 40 dB | Colectores, PO, T1 y T2 |
| Bajo nivel | 820 pF | 460 ohm | unos 20 dB | Solo puntos sin continua (DRV, base de Q1) |

La atenuación supone la entrada del SDR en 50 ohm. No lleva diodo: el SDR necesita la RF tal cual. El capacitor bloquea la continua y debe ir del lado de la punta.

## Ajustes del SDR (SDR++)

- **Misma ganancia, mismo zoom, ancho de banda y tamaño de FFT** en toda una serie. Se usó ganancia 25,4 (la mitad aproximadamente).
- CW, carrier al 50 %, carga fantasma, manipulador cerrado 3 o 4 segundos por punto.
- Anotar el SNR de la línea que **aparece solo en TX**. En CW esa línea puede quedar a unos cientos de Hz del RX.
- El SNR no es lineal: tomar diferencias como orientación (más o menos 5 a 10 dB). Si un punto satura, anotarlo como "saturado".

## Frecuencia del SDR según el punto

| Grupo | Frecuencia |
|---|---|
| IF unit, J30, J32 y J35 (TIF) | 8,83 MHz (portadora de TX en torno a 8825 a 8831 kHz) |
| C52, BPF, Q7 a Q9, DRV, Final y PO | Frecuencia de operación (por ejemplo 7074 kHz) |

Comparar niveles entre ambos grupos con la misma sonda y ganancia es válido con una diferencia de pocos dB por frecuencia.

## Recorrido de TX con puntos de prueba

| # | Unidad | Punto | Frecuencia |
|---|---|---|---|
| 1 | IF unit | J30, pin GEN | 8,83 MHz |
| 2 | IF unit | J32, pin TIF | 8,83 MHz |
| 3 | RF unit | J35, pin 2 (TIF) | 8,83 MHz |
| 4 | RF unit | C52, pad del lado de R36 (debajo de Q6) | Operación |
| 5 | RF unit | C11 (pata del lado de L8 y del lado de L7) y C10 (pata del lado de L6): sector de 7 MHz, la fila con C12 100P, C11 39P y C10 82P | Operación |
| 6 | RF unit | C54, pata del lado de Q7 (salida del BPF) | Operación |
| 7 | RF unit | J34, pines ANT y MKR (fuga hacia la antena) | Operación |
| 8 | RF unit | DRV (salida) | Operación |
| 9 | Final | DRV (entrada), colector de Q1 (pata de C6), colectores de Q2/Q3 (patas de C15), bases de Q4/Q5 | Operación |
| 10 | Final | PO (solo con el carrier al mínimo) | Operación |

Criterio: el nivel debería subir o mantenerse entre puntos consecutivos según las ganancias nominales (ver [mediciones](03-mediciones-y-niveles.md)). Una caída de 20 dB o más entre dos puntos marca el tramo cortado.

## Precauciones

- Cable rojo del tester **siempre en el jack V** para tensión. En el jack de Amp es un cortocircuito directo.
- No apoyar la sonda en el primario de T4 ni en los colectores de Q4/Q5 (RF fuerte y 13,8 V muy cerca de masa).
- No sondear con puntas los pines de los 3SK74 (cuatro pines juntos); medir en componentes vecinos o por tensión.
- En los bipolares de potencia la estática no es crítica; en los 3SK74 de la RF unit sí: tocar masa seguido.
- Con el equipo apagado y el cable de DC afuera para ohmetro y para tocar placas. En TX, mediciones de 3 a 5 segundos.
- No tocar VR1 ni VR2 mientras no se resuelva una falla.
