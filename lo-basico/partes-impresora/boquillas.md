---
titulo: "Boquillas"
slug: "boquillas"
seccion: "lo-basico"
subseccion: "partes-impresora"
material: ""
tipo: "conceptual"
ultima_revision: "2026-03-22"
estado: "terminado"
version: "1.0"
---

# Boquillas

> La boquilla define cuánto detalle tiene tu pieza, qué tan rápido puedes imprimir y qué materiales puedes usar.

---

## Para Principiantes

La boquilla es la punta por donde sale el filamento fundido. Es una pieza pequeña —normalmente del tamaño de una punta de bolígrafo— pero tiene un impacto enorme en el resultado final. El **diámetro** del orificio determina el grosor de cada línea de material depositado: una boquilla de 0.4 mm es el estándar universal y sirve bien para la mayoría de proyectos.

Piénsalo como los pinceles de un pintor: el pincel fino permite detalles pequeños pero tarda más en cubrir una superficie grande; el pincel grueso es más rápido pero menos preciso. Con las boquillas pasa exactamente lo mismo. Si imprimes miniaturas o piezas con texto en relieve pequeño, querrás 0.2 o 0.3 mm. Si imprimes piezas estructurales grandes donde el detalle no importa tanto, una boquilla de 0.6 o 0.8 mm te ahorra horas.

El **material** de la boquilla también importa: las de latón son baratas y funcionan perfectamente para PLA y PETG, pero se desgastan rápido con filamentos que contienen fibras o partículas duras. Para esos casos existen boquillas de acero endurecido o de carburo de tungsteno.

---

## Todo lo que Necesitas Saber

### ¿Cómo funciona?

El hotend calienta el bloque calefactor hasta la temperatura de fusión del filamento. La boquilla, atornillada a ese bloque, recibe el material ya fundido y lo fuerza a salir por su orificio calibrado. La precisión del diámetro del orificio —usualmente con tolerancia de ±0.01 mm en boquillas de calidad— determina el ancho real de cada línea extrudida.

La **altura de capa máxima recomendada** es el 75–80% del diámetro de la boquilla. Con una boquilla de 0.4 mm no deberías superar 0.32 mm de altura de capa; con 0.6 mm puedes llegar a 0.48 mm.

### Tipos por diámetro

| Diámetro | Altura de capa máx. | Mejor para | Limitaciones |
|---|---|---|---|
| 0.2 mm | 0.16 mm | Miniaturas, detalles finos | Lento; se tapa fácil con fibras |
| 0.3 mm | 0.24 mm | Joyería, modelos decorativos | Velocidad limitada |
| 0.4 mm | 0.32 mm | Uso general — el estándar | Ninguna notable |
| 0.6 mm | 0.48 mm | Piezas funcionales, prototipos | Menos resolución superficial |
| 0.8 mm | 0.64 mm | Piezas grandes, relleno estructural | Detalle mínimo |
| 1.0 mm | 0.80 mm | Impresión industrial rápida | Solo para piezas grandes y robustas |

### Tipos por material

Dos propiedades del material de la boquilla determinan todo lo demás: la **dureza** (resistencia a la abrasión) define cuánto tiempo sobrevive la boquilla con filamentos que contienen partículas duras como fibra de carbono o metal-fill; la **conductividad térmica** define qué tan eficientemente transfiere el calor del bloque calefactor al filamento, lo que afecta directamente la viscosidad del fundido y el caudal volumétrico máximo alcanzable.

| Material | Conductividad térmica | Resistencia al desgaste | Temperatura máx. | Ideal para |
|---|---|---|---|---|
| **Latón** | Alta | Baja | ~300 °C | PLA, PETG, PA — filamentos no abrasivos |
| **Acero inoxidable** | Media | Media | ~500 °C | Aplicaciones alimentarias; filamentos no abrasivos |
| **Acero endurecido** | Media | Muy alta | ~500 °C | Compuestos: PPCF, fibra de vidrio, metal-fill |
| **Níquel/cromo (coated)** | Alta | Alta | ~500 °C | Abrasivos moderados con buena conductividad |
| **Rubí (punta)** | Alta | Extrema | ~500 °C | Abrasivos duros; frágil ante golpes |
| **Diamante policristalino** | Alta | Extrema | ~600 °C | Uso intensivo industrial; el más duradero |

### Guía de selección rápida

| Aplicación | Boquilla recomendada |
|---|---|
| PLA, PETG, PA (impresión general) | Latón 0.4 mm |
| Miniaturas y modelos de detalle | Acero endurecido 0.2–0.3 mm |
| Fill3D PPCF o fibra de vidrio | Acero endurecido 0.4–0.6 mm |
| Prototipos rápidos de gran volumen | Latón o acero endurecido 0.6–0.8 mm |
| Uso con materiales de temperatura alta (>300 °C) | Acero inoxidable o coated |

> **¿Por qué acero endurecido para miniaturas?** El latón se desgasta con el uso y el orificio pierde su diámetro calibrado con el tiempo, lo que se traduce en líneas irregulares que arruinan el detalle fino. El acero endurecido mantiene la geometría del orificio por mucho más tiempo, garantizando consistencia en impresiones de alta precisión a largo plazo.

### Mantenimiento básico

- **Cold pull (tirón en frío):** Calienta la boquilla a temperatura de impresión, inserta filamento de nylon, deja enfriar a 90–100 °C y jálalo de golpe. Los residuos quedan atrapados en el nylon. Repite hasta que salga limpio.
- **Aguja de limpieza:** Para atascos parciales, una aguja de 0.35–0.40 mm introducida con la boquilla caliente libera bloqueos menores.
- **Señales de reemplazo:** La primera señal —y la más importante— es una degradación visible en la calidad: detalles pequeños que pierden definición, superficies superiores (top layers) con acabado irregular o rugoso que antes salían bien. Si notas esto, la boquilla probablemente ya se desgastó aunque no haya atascos. La segunda señal son atascos repetidos que vuelven tras el cold pull o la aguja de limpieza. Por último, un orificio visualmente agrandado o rayas en la punta confirman desgaste avanzado, pero para entonces ya deberías haber reemplazado la boquilla.

---

## Para Expertos

### Regla del 75–80% y su excepción

La regla de altura de capa ≤ 80% del diámetro existe porque extrudir una línea más alta que ancha genera presión excesiva en el hotend y adhesión deficiente entre capas. Sin embargo, con boquillas de alto flujo (geometría CHT o Volcano) que aumentan la zona de fusión, es posible aproximarse al 90% de altura relativa manteniendo buena adhesión, siempre que el caudal volumétrico esté dentro del rango del hotend.

### El problema del PPCF con boquillas de latón

El Fill3D PPCF puede destruir una boquilla de latón en una sola sesión de impresión de 3–4 horas. Las partículas de fibra de carbono actúan como papel de lija a 300 °C. La única opción viable es acero endurecido (o superior). Después de cambiar a endurecido, recalibra el flujo: la menor conductividad térmica del acero puede requerir subir 5–10 °C respecto al perfil de latón para mantener la misma viscosidad de fundido.

### Boquillas de alto flujo para impresión a velocidad

Las boquillas con geometría CHT (Core Heating Technology) o cámaras de fusión extendidas (Volcano, Super Volcano) permiten caudales volumétricos de 30–60 mm³/s frente a los 15–20 mm³/s de una boquilla estándar. Son indispensables para aprovechar impresoras CoreXY rápidas imprimiendo PLA Turbo a velocidades superiores a 200 mm/s. El trade-off: el tiempo de purga al cambiar de material es mayor porque hay más volumen de material en la zona de fusión.

> **Advertencia con materiales compuestos:** No usar geometría CHT con filamentos que contengan fibras (PPCF, fibra de vidrio, metal-fill). El diseño de núcleo dividido de la CHT reduce el área de flujo efectiva, lo que aumenta la probabilidad de que las fibras generen taponamientos. Para compuestos, usar siempre boquilla de orificio abierto estándar en acero endurecido.

> 💡 **Nota técnica:** La conductividad térmica del latón (~109 W/m·K) frente al acero endurecido (~25 W/m·K) es real pero su impacto práctico a 0.4 mm es mínimo a velocidades normales. La diferencia se vuelve relevante por encima de 25 mm³/s de caudal volumétrico, donde la menor conductividad del acero puede provocar bajo-fusión si no subes la temperatura.

---

## También te puede interesar
- [Extrusores](./extrusores.md)
- [Camas de Impresión](./camas-de-impresion.md)
- [Consejos por Tipo de Material](../../consejos-de-impresion/por-tipo-de-material.md)