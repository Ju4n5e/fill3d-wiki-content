---
titulo: "Slicers (Laminadores)"
slug: "slicers"
seccion: "lo-basico"
subseccion: ""
material: ""
tipo: "conceptual"
ultima_revision: "2026-03-23"
estado: "terminado"
version: "1.0"
---

# Slicers (Laminadores)

> El software que traduce tu modelo 3D en instrucciones reales de impresión — sin él, tu impresora no sabe qué hacer.

---

## Para Principiantes

Imagina que quieres hornear un pastel con una forma muy específica: primero necesitas la receta con cada paso detallado antes de encender el horno. En impresión 3D, el slicer es exactamente esa receta. Tomas un modelo digital —un archivo 3D que descargaste o diseñaste— y el slicer lo convierte en instrucciones que tu impresora entiende.

¿Cómo lo hace? Básicamente "rebana" tu modelo en capas horizontales, como si cortaras un pan en tajadas muy delgadas. Luego calcula la ruta exacta que debe seguir la boquilla para depositar el plástico capa por capa hasta construir el objeto. Ese conjunto de instrucciones se llama **G-code**, y es el archivo que finalmente envías a tu impresora.

Lo mejor es que la mayoría de los slicers son gratuitos y tienen interfaces visuales muy intuitivas. Puedes ver en pantalla cómo va a quedar tu impresión antes de comenzar, ajustar la velocidad, la altura de capa, los soportes y mucho más. No necesitas saber programar ni entender el G-code para usarlos bien.

---

## Todo lo que Necesitas Saber

### ¿Cómo funciona un slicer?

El proceso ocurre en cuatro etapas principales:

1. **Importación del modelo**: el slicer acepta archivos 3D en formatos como STL, OBJ o 3MF.
2. **Segmentación en capas**: divide el modelo en capas horizontales según la altura de capa que elijas (típicamente entre 0.1 mm y 0.3 mm).
3. **Generación de trayectorias**: calcula el recorrido exacto del extrusor, incluyendo los patrones de relleno interno (infill), las paredes externas y las estructuras de soporte.
4. **Exportación del G-code**: genera el archivo de instrucciones listo para enviar a la impresora.

### Parámetros clave que configuras en el slicer

| Parámetro | Qué controla | Impacto principal |
|---|---|---|
| **Altura de capa** | Grosor de cada capa (mm) | Resolución visual y tiempo de impresión |
| **Temperatura de boquilla** | °C de extrusión | Adhesión entre capas, fluidez del material |
| **Temperatura de cama** | °C de la superficie | Adherencia de la primera capa, warping |
| **Velocidad de impresión** | mm/s de movimiento | Tiempo total y calidad superficial |
| **Infill (relleno)** | % de densidad interna | Resistencia mecánica y peso de la pieza |
| **Retracción** | mm hacia atrás al viajar | Stringing entre partes separadas |
| **Enfriamiento** | % de ventilador activo | Solidificación, overhangs, bridging |

### Slicers más usados en la comunidad maker

| Slicer | Precio | Ideal para | Notas |
|---|---|---|---|
| **Orca Slicer** | Gratis / open-source | Usuarios intermedios y avanzados | Herramientas de calibración avanzadas; compatible con gran variedad de impresoras |
| **Bambu Studio** | Gratis | Impresoras Bambu Lab | Soporte multi-color y detección de fallos por IA |
| **Cura** | Gratis / open-source | Principiantes y hobbyistas | Interfaz amigable; amplia base de perfiles |
| **PrusaSlicer** | Gratis / open-source | Flujos multi-material | Soportes de árbol robustos; optimizado para Prusa |
| **Simplify3D** | Pago (~USD 199) | Control granular | Perdió relevancia por falta de actualizaciones recientes |

> **¿Cuál slicer usar?** Lo más sencillo es utilizar el slicer oficial de la marca de tu impresora — en la mayoría de los casos será una variante de Orca Slicer o Cura, y usarlo te garantiza mayor compatibilidad con las funciones específicas de tu equipo. Si necesitas realizar una calibración puntual de parámetros, te recomendamos **Orca Slicer** por sus herramientas de calibración integradas.

### Perfiles de material: el atajo que deberías usar

Un **perfil de material** es un conjunto de parámetros preconfigurados para un filamento específico. En lugar de ajustar temperatura, velocidad y retracción desde cero, cargas el perfil del material que vas a usar y el slicer aplica automáticamente una configuración de punto de partida probada.

Cuando usas [Fill3D PLA](https://www.fill-3d.com/tienda/) o [PLA Turbo](https://www.fill-3d.com/tienda/), el perfil de material te da los valores base correctos. A partir de ahí puedes hacer ajustes finos según tu impresora particular.

### Soportes y adhesión a la cama

Los slicers modernos generan automáticamente **estructuras de soporte** para geometrías con overhangs pronunciados (generalmente más de 45–50°). También añaden elementos de adhesión a la primera capa:

- **Skirt**: un contorno que no toca la pieza; purga el filamento antes de empezar.
- **Brim**: extensión plana alrededor de la base; aumenta la adhesión.
- **Raft**: plataforma completa debajo de la pieza; útil para materiales con tendencia al warping como PA o PP.

---

## Para Expertos

### Calibración con modelos de prueba dentro del slicer

Antes de imprimir cualquier pieza funcional, vale la pena ejecutar secuencias de calibración desde el slicer: torres de temperatura (temp towers), pruebas de retracción por rango de velocidades, y cubos de calibración dimensional. Orca Slicer integra estas herramientas nativamente — en Cura debes importarlos como modelos STL por separado. El proceso de calibración debería ser obligatorio cada vez que cambias de lote de filamento, incluso dentro del mismo material, ya que variaciones en el diámetro real (±0.02 mm) afectan el flow rate efectivo.

### Ajuste de flow rate por zona

El flow rate global en el slicer es un multiplicador sobre el diámetro de filamento configurado. Para piezas con requisitos dimensionales estrictos (tolerancias ≤0.1 mm), lo más preciso es ajustar el flow por zona: paredes externas ligeramente por debajo del 100% (97–99%) para mejorar el acabado superficial, e infill a 100–103% para garantizar densidad sin afectar la geometría visible. Orca Slicer y PrusaSlicer exponen estos controles por separado; en Cura se maneja via "outer wall flow" y "inner wall flow" como parámetros independientes.

### Estrategias de infill para propiedades mecánicas específicas

El patrón de infill no es solo estético: **gyroid** distribuye carga isotrópicamente en los tres ejes, ideal para piezas sometidas a fuerzas multidireccionales; **honeycomb** y **cubic** son más eficientes para cargas de compresión axial. Para piezas impresas con Fill3D PPCF o PA donde la orientación de las fibras cortas importa, el patrón de infill interactúa con la dirección de las paredes y puede aumentar o reducir la resistencia en puntos críticos.

### Gestión de G-code post-procesado

Los slicers avanzados permiten insertar scripts de post-procesado en el G-code: cambios de filamento en capas específicas (M600), pausas programadas para insertar insertos metálicos, o ajustes dinámicos de temperatura por sección. PrusaSlicer y Orca Slicer tienen editores de scripts integrados; en Cura se accede vía el plugin "Post Processing". Esta funcionalidad es especialmente útil al imprimir piezas con zonas de tolerancias diferentes donde conviene bajar la velocidad solo en las capas críticas.

> 💡 **Nota técnica:** El G-code generado por distintos slicers para el mismo modelo puede variar en longitud de filamento calculado hasta un 8–12% dependiendo del algoritmo de generación de trayectorias. Si tu impresora usa sensor de filamento por peso o longitud, recalibra el offset con el slicer específico que uses en producción.

---

## También te puede interesar
- [Introducción a la Impresión 3D](./introduccion-impresion-3d.md)
- [Calibración de Filamento con Orca Slicer](calibracion/metodologia-orca.md)
- [Consejos por Tipo de Material](../consejos-de-impresion/por-tipo-de-material.md)
- [Problemas Comunes de Impresión](../consejos-de-impresion/problemas-comunes.md)
