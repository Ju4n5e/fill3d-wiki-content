---
titulo: "Extrusores"
slug: "extrusores"
seccion: "lo-basico"
subseccion: "partes-impresora"
material: ""
tipo: "conceptual"
ultima_revision: "2026-03-22"
estado: "terminado"
version: "1.0"
---

# Extrusores

> El extrusor es el corazón mecánico de tu impresora: entiende cómo funciona y la mitad de los problemas se explican solos.

---

## Para Principiantes

Si le preguntas a alguien cuál es la parte más importante de una impresora 3D FDM, muchos señalarán la boquilla o la pantalla. Pero el verdadero protagonista es el **extrusor**: el mecanismo que agarra el filamento y lo empuja hacia el hotend para que se derrita y salga formando tu pieza.

Piénsalo como el émbolo de una jeringa gigante. Un motor con engranajes aprieta el filamento y lo mueve a una velocidad precisa y constante. Demasiado lento y la pieza queda con huecos; demasiado rápido y el material se apila y deforma.

Hay dos filosofías principales de diseño: el **extrusor Bowden**, donde el motor está fijo en el marco y el filamento viaja por un tubo hasta el cabezal, y el **direct drive**, donde el motor va montado justo encima de la boquilla. Cada uno tiene sus ventajas según el material que quieras imprimir. Lo importante para empezar: saber qué tipo tiene tu impresora te ayuda a configurar correctamente la retracción en el slicer y a entender por qué algunos materiales son más difíciles de imprimir que otros.

---

## Todo lo que Necesitas Saber

### ¿Cómo funciona?

El filamento entra por la parte superior del extrusor, donde un **engranaje de arrastre** (drive gear) lo agarra con dentado preciso mientras un rodillo idler aplica presión desde el lado opuesto. El motor paso a paso (stepper) gira ese engranaje y avanza el filamento milímetro a milímetro hacia el hotend. La calibración de los **E-steps** (pasos por milímetro de extrusión) garantiza que cuando el slicer pida 10 mm de filamento, el motor entregue exactamente eso.

Cuando el slicer ordena retracción —para evitar el stringing entre partes— el motor invierte su giro y jala el filamento hacia atrás unos milímetros. La distancia óptima depende directamente del tipo de extrusor.

### Tipos de extrusor

| Característica | Bowden | Accionamiento directo |
|---|---|---|
| Ubicación del motor | Marco de la impresora | Cabezal de impresión |
| Peso del cabezal | Ligero | Mayor |
| Velocidad posible | Alta (menos inercia) | Moderada–alta |
| Retracción necesaria | 4–7 mm | 0.5–2 mm |
| Filamentos flexibles (TPU) | Difícil | Excelente |
| Precisión de flujo | Buena | Muy buena |
Las impresoras **CoreXY** modernas de alta velocidad suelen usar accionamiento directo con cabezales livianos de diseño compacto, combinando lo mejor de ambos mundos.

### Variantes avanzadas

- **Doble engranaje (dual-gear):** Dos engranajes dentados atrapan el filamento desde ambos lados, reduciendo el deslizamiento y mejorando el control del flujo. Ideal para materiales que requieren precisión como el PPCF.
- **Reductores orbitales:** Incorporan una caja reductora compacta para generar alto torque en un paquete liviano.
- **Alta temperatura con refrigeración líquida:** Permiten temperaturas de boquilla superiores a 400 °C para materiales de ingeniería como PEEK o PEI.

### ¿Qué impacto tiene en tu impresión?

El extrusor afecta directamente tres aspectos:

1. **Stringing:** Un extrusor Bowden requiere más retracción; pasarte del valor óptimo puede causar atascos. Un extrusor directo perdona mejor las variaciones.
2. **Compatibilidad de materiales:** Los filamentos flexibles como TPU prácticamente exigen accionamiento directo; en un Bowden el tubo PTFE genera fricción que deforma y atasca el material blando.
3. **Velocidad:** Con Bowden, el cabezal más liviano puede moverse más rápido sin vibración; con directo, la masa extra del motor limita la aceleración, aunque los diseños modernos han reducido mucho esta diferencia.

### Problemas frecuentes y causas

| Síntoma | Causa probable |
|---|---|
| Subextrusión intermitente | E-steps descalibrados, engranaje desgastado |
| Trituración del filamento | Presión del idler excesiva, temperatura baja |
| Stringing severo | Retracción mal ajustada para el tipo de extrusor |
| Atasco con flexible | Bowden con TPU (considerar extrusor directo) |

---

## Para Expertos

### Calibración de E-steps: cuándo y cómo

Los E-steps solo necesitan recalibrarse en impresoras antiguas o de construcción propia. En impresoras modernas calibradas de fábrica, el parámetro relevante es el **factor de flujo (flow ratio)** dentro del slicer, que compensa la variación real del diámetro del filamento. Marca 100 mm en el filamento entrante, extruye 100 mm desde el slicer o terminal, y mide el error. Un 5% de desviación ya justifica ajuste.

### Retracción: valores de partida según extrusor

El punto de partida más seguro es 0.5–1.5 mm para accionamiento directo y 4–6 mm para Bowden, ambos a 35–45 mm/s. Pero el valor final depende del material: el PLA Turbo con Pressure Advance activo puede operar con retracciones de apenas 0.1 mm en directo, mientras que PA en Bowden puede necesitar hasta 7 mm. Nunca copies valores de otro usuario sin conocer su tipo de extrusor primero.

### Desgaste de engranajes con materiales abrasivos

El Fill3D PPCF (PP con fibra de carbono) no solo desgasta la boquilla: las partículas abrasivas también erosionan el engranaje de arrastre a lo largo del tiempo, especialmente si es de acero inoxidable estándar. Para impresión frecuente con composites, considera engranajes de acero endurecido o nitruro (DLC-coated). Inspeccionalos visualmente cada 100–200 horas de impresión con abrasivos.

> 💡 **Nota técnica:** El Adaptive Pressure Advance (disponible en Orca Slicer / Bambu Studio) modela la respuesta dinámica del extrusor en función de la velocidad de cambio, reduciendo el error de flujo en aceleraciones bruscas sin necesidad de afinar la retracción para cada velocidad manualmente.

---

## También te puede interesar
- [Boquillas](./boquillas.md)
- [Mantenimiento de la Impresora](../mantenimiento/mantenimiento.md)
- [Consejos por Tipo de Material](../../consejos-de-impresion/por-tipo-de-material.md)