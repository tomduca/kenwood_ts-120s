# Kenwood TS-120S: diario técnico 2026

Diario de reparación y mantenimiento de un transceptor Kenwood TS-120S (HF, FI de 8,83 MHz). Reúne el historial de intervenciones, la pérdida repentina de TX de octubre de 2026, las mediciones, las conclusiones, la resolución y los pendientes.

## Estado actual (17/10/2026)

- TX y RX funcionando en todas las bandas.
- Última reparación: una **viruta de estaño hacía puente entre colector y emisor de Q7** (RF unit) y dejaba sin excitación a la Final (sin TX en SSB ni en CW). Se limpió y se desoldó la viruta el 17/10/2026 y el TX volvió a funcionar.
- Pendientes principales: controles de cierre tras la reparación (corriente de reposo de la Final, AVB con excitación normal), RIT, medidor IC, S-meter en bandas altas, deriva del VFO, pot RF GAIN, recap de las unidades restantes y calibración. Detalle en [docs/06-pendientes.md](docs/06-pendientes.md).

## Contenido

| Documento | Qué contiene |
|---|---|
| [docs/01-historial-de-intervenciones.md](docs/01-historial-de-intervenciones.md) | Cronología de reparaciones y mantenimiento, con tablas por unidad |
| [docs/02-incidente-tx-oct-2026.md](docs/02-incidente-tx-oct-2026.md) | La pérdida repentina de TX: síntoma, diagnóstico paso a paso, causa raíz y resolución |
| [docs/03-mediciones-y-niveles.md](docs/03-mediciones-y-niveles.md) | Todas las mediciones (DC y niveles con SDR), niveles nominales del manual y tabla para valores de referencia |
| [docs/04-referencia-tecnica.md](docs/04-referencia-tecnica.md) | Camino de TX, Q7, alimentaciones, corrientes de reposo, protecciones, boletines de servicio |
| [docs/05-metodologia-y-sondas.md](docs/05-metodologia-y-sondas.md) | Cómo se midió: sondas, frecuencias, ajustes del SDR, puntos de prueba y precauciones |
| [docs/06-pendientes.md](docs/06-pendientes.md) | Pendientes priorizados |
| [img/](img/) | Esquemas de las dos sondas (SVG) |

## Cómo leer este diario

- Muchos valores esperados salen de **imágenes escaneadas** del esquema de WB4KDI y del manual de servicio. Confirmarlos en papel antes de concluir.
- Las fechas son aproximadas salvo indicación. La pérdida de TX ocurrió unos dos días antes del 17/10/2026.
- Los pares RX/TX de las tablas van en ese orden. Las tensiones son en continua salvo que se indique "eficaz" o "pico".
- Los niveles del SDR son **SNR relativos**, no calibrados: sirven para comparar puntos con la misma ganancia y el mismo ancho de banda.

## Fuentes

- Manual de servicio Kenwood TS-120S (diagrama de niveles p. 36, diagrama de fallas p. 34, ajustes pp. 38 a 40).
- Esquemas de WB4KDI (TS-120S/TS-120V). La placa real tiene un D8 en la RF unit que el esquema no muestra.
- Boletines de servicio SB-816, SB-832 y SB-844.

## Créditos

Armado con ayuda de Claude (Anthropic) a partir de una sesión de diagnóstico.
