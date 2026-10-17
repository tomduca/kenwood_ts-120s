# Pendientes

Priorizados. Los problemas secundarios vienen del resumen más antiguo; los de cierre, de la pérdida de TX de octubre de 2026.

## Prioridad alta: cierre de la reparación de Q7

1. **Revisar el entorno de Q7:** R41 y R43 (100 ohm, con la viruta soportaron unos 0,3 W cada una), L30 y C57; medir Q8 en TX (base unos 2,8 V, emisor 2,1 V, colector 9,9 V).
2. **Comprobar con carga fantasma** la potencia, el ALC y el IC con carrier moderado, y completar la tabla de valores de referencia de [03](03-mediciones-y-niveles.md).
3. **Medir AVB con excitación normal.** El transistor de paso (Q9 de la Filter unit) es un 2SA755, no el original.
4. **Ajustar la corriente de reposo según el manual** (100 mA los finales con VR2, 150 mA Q2/Q3 con VR1). Se midieron unos 160 mA en los finales; más corriente de reposo es más calor en la Final.

## Prioridad media: mantenimiento

5. **Inspección sistemática de soldaduras y coaxiles,** y de restos de estaño suelto, en la RF unit, la Filter unit y la Relay unit. El equipo tiene un historial de soldaduras partidas (coaxil de la Relay unit, Filter unit, J41) y ahora una viruta de estaño en Q7.
6. **Pasta térmica de Q2 a Q5 y sensores de temperatura:** acordado limpiar y renovar sin desoldar nada, con los sensores en su lugar, con pasta no conductora en película fina. No se hizo todavía.
7. **Posible soldadura fría en el terminal de base de uno de los 2SC2290** (línea visible, sin juego): refluir solo si la superficie es opaca o tiene una grieta en anillo; hacerlo con soldador de temperatura controlada y 40 a 60 W, fundente y un disipador en el terminal. Anotar antes y después la tensión de base (0,65 V en TX) y los mV del shunt (2,4 mV).
8. **Recap pendiente:** CAR unit, Counter unit y Final unit. En la Final, los electrolíticos de bias (C12 y C25) y de desacople (C20 y C37).

## Problemas secundarios (del resumen más antiguo)

9. **RIT inutilizable** tras el recap. Probable cable del wiper (RT1) cortado entre el pot frontal y el pin 11 de J4 en la AF-GEN. Verificar continuidad con la radio apagada y J4 desconectado.
10. **Potenciómetros dobles concéntricos del panel (VR1, VR2 y VR3):** reemplazo. Se pueden usar 50K en lugar de los 10K/5K originales con poco impacto, salvo VR3 (la sección RIT, de 5K). El switch de VR2 es el punto crítico de compatibilidad mecánica.
11. **Medidor IC** no calibrable con VR1 de la Filter unit: posible pista de carbón gastada.
12. **S-meter duro en 20, 15 y 10 m:** posible desalineación de L16/L17; re-medir D4 y D5.
13. **Micro-deriva del VFO:** eje del capacitor variable con lubricación sucia.
14. **Pot RF GAIN** trabado mecánicamente: requiere reemplazo.
15. **Calibración** completa de IF, RF y S-meter con generador; ajuste del BPF en 20, 15 y 10 m; ajuste fino de T1 a T9 de la IF (hoy a oído).
