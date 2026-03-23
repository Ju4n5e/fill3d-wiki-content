---
titulo: "Impresoras 3D"
slug: "impresoras-3d"
seccion: "lo-basico"
subseccion: ""
material: ""
tipo: "conceptual"
ultima_revision: "2026-03-23"
estado: "terminado"
version: "1.0"
---

# Impresoras 3D

> Entiende cómo funciona una impresora 3D por dentro para tomar mejores decisiones al imprimir.

---

## Para Principiantes

Una impresora 3D es, en esencia, una máquina que construye objetos capa por capa, como si apilaras hojas de papel muy delgadas hasta formar un bloque sólido. En lugar de papel, usa plástico fundido; en lugar de hojas, deposita líneas de material tan finas que a simple vista parecen una sola pieza.

El proceso empieza en tu computador: diseñas o descargas una figura en 3D, la procesas con un programa llamado [slicer](./slicers.md) <!-- ⚠️ página pendiente de crear --> —que la "rebana" en cientos de capas— y le envías las instrucciones a la impresora. Desde ese momento, la máquina trabaja sola: calienta el filamento hasta que fluye, lo empuja a través de una boquilla muy pequeña y lo deposita con precisión sobre una superficie plana llamada cama. Capa tras capa, el objeto va creciendo desde abajo hacia arriba.

Piénsalo como una pistola de silicona de altísima precisión montada sobre un brazo robótico: el mecanismo mueve la boquilla en el lugar exacto que el programa le indica, y el plástico se enfría rápido y se adhiere a la capa anterior. Al final del proceso tienes un objeto físico que horas antes solo existía en pantalla.

---

## Todo lo que Necesitas Saber

### Los tres tipos de arquitectura

No todas las impresoras 3D mueven sus piezas de la misma manera. Hay tres arquitecturas dominantes en el mercado, cada una con una lógica de movimiento distinta.

**Cartesiana** es la más común y la más fácil de entender: la boquilla se mueve en los ejes X e Y (horizontal), y la cama —o el cabezal, según el modelo— sube y baja en el eje Z. Es predecible, fácil de calibrar y la gran mayoría de impresoras de entrada y gama media usan este sistema. Ideal si estás empezando.

**Core XY** mantiene la cama fija en Z y mueve el cabezal en X e Y usando dos motores sincronizados mediante una correa en forma de H. Al no mover masa pesada en horizontal, puede imprimir más rápido sin perder precisión. Es el sistema preferido en impresoras de alta velocidad.

**Delta** usa tres brazos articulados que sostienen el cabezal desde arriba y lo posicionan mediante la coordinación de tres motores verticales. Su área de impresión es circular y su punto fuerte es la velocidad en movimientos verticales. Es menos común en uso doméstico pero muy usado en impresoras de gran formato o de nicho industrial.

### Componentes principales (comunes a las tres arquitecturas)

Independientemente de la arquitectura, todas las impresoras FFF comparten los mismos bloques funcionales:

| Componente | Función |
|---|---|
| **Extrusor** | Empuja el filamento desde el carrete hasta la boquilla. Puede ser directo (montado sobre el cabezal) o Bowden (separado, conectado por un tubo). Ver página dedicada: [Extrusores](./partes-impresora/extrusores.md) |
| **Hotend y boquilla** | Funden el filamento y lo depositan con precisión. El diámetro de la boquilla determina la resolución y la velocidad posibles. Ver página dedicada: [Boquillas](./partes-impresora/boquillas.md) |
| **Cama de impresión** | Superficie donde se construye la pieza. Puede ser fría o calentada, y de distintos materiales según el filamento. Ver página dedicada: [Camas de Impresión](./partes-impresora/camas-de-impresion.md) |
| **Estructura y ejes** | El chasis y los rieles o varillas que guían el movimiento. Su rigidez impacta directamente la calidad de impresión. |
| **Motores paso a paso** | Controlan el movimiento con precisión milimétrica en cada eje y en el extrusor. |
| **Placa controladora** | El "cerebro" de la impresora: interpreta el G-code y coordina todos los motores y sensores. |
| **Fuente de poder** | Alimenta la cama caliente, el hotend y la electrónica. Su potencia limita cuánto puede calentar la máquina. |
| **Pantalla / interfaz** | Permite controlar la impresora localmente. Algunos modelos se gestionan desde el computador o por Wi-Fi. |

### ¿Qué impacta en tu resultado final?

La calidad de una impresión no depende solo de la impresora: el filamento, el slicer y los parámetros que elijas son igual de importantes. Una impresora de gama media con un buen filamento y parámetros bien ajustados puede superar fácilmente a una impresora costosa mal calibrada con filamento de baja calidad.

Los tres factores que más afectan el resultado:

- **Calibración de la primera capa:** Si la boquilla está demasiado lejos o demasiado cerca de la cama, todo lo que viene después falla.
- **Temperatura y flujo del filamento:** Cada material tiene una ventana óptima. Salirse de ella produce stringing, warping o capas mal adheridas.
- **Velocidad vs. calidad:** Más velocidad exige más presión en el hotend. Con materiales de alto flow como el PLA Turbo esa exigencia disminuye, pero la física no desaparece.

### Impresión multicolor

Imprimir con más de un color o material requiere que la impresora pueda cambiar el filamento activo durante el proceso. Hay dos enfoques principales, con lógicas de funcionamiento y costos muy distintos.

**Multiplexor (una sola boquilla, varios filamentos)**
Un sistema de selección alimenta múltiples rollos hacia un único hotend: solo uno de los filamentos está activo en cada momento, y el cambio implica retirar el anterior y cargar el siguiente. Es el enfoque más accesible económicamente y compatible con impresoras existentes. Su principal desventaja es el desperdicio de material: cada cambio de color requiere purgar el filamento residual de la boquilla, lo que genera una cantidad significativa de material descartado por transición —especialmente problemático en impresiones con muchos cambios frecuentes.

**Multiherramienta (varias boquillas, un material por cabezal)**
Cada filamento tiene su propio hotend dedicado y la impresora activa el cabezal correspondiente según lo necesite. No hay purga entre colores porque no hay contaminación cruzada, lo que elimina casi por completo el desperdicio de material. A cambio, el costo de entrada es considerablemente más alto —tanto en hardware como en la complejidad de calibración— y el volumen de impresión efectivo se reduce, ya que los cabezales inactivos deben mantenerse fuera del área de trabajo.

| | Multiplexor | Multiherramienta |
|---|---|---|
| **Costo de adquisición** | Bajo — compatible con muchas impresoras existentes | Alto — requiere hardware especializado |
| **Desperdicio de material** | Alto — purga necesaria en cada cambio | Mínimo — sin contaminación cruzada |
| **Complejidad de calibración** | Moderada | Alta |
| **Ideal para** | Impresiones con pocos cambios de color por capa | Impresiones con colores simultáneos o materiales de soporte solubles |

---

## Para Expertos

### Cinemática y compensación de resonancia

En arquitecturas Core XY el perfil de aceleración es determinante: la masa del toolhead define la frecuencia de resonancia del sistema. Herramientas como Input Shaping (Klipper con ADXL345) permiten medir y compensar la resonancia por eje independientemente, desbloqueando velocidades de 300–500 mm/s sin ghosting. En cartesianas con cama móvil en Y, la frecuencia de resonancia cambia con el peso de la pieza en curso —factor que Input Shaping estático no compensa dinámicamente.

### Extrusores de alta velocidad y presión avanzada

Con filamentos de alta velocidad el cuello de botella se desplaza del motor al hotend: la viscosidad del fundido y el volumen de fusión por unidad de tiempo (flow rate volumétrico, en mm³/s) limitan la velocidad real antes que la cinemática. Hotends de alto volumen (Revo Voron, Dragon Ace, Bambu hardened) combinados con Pressure Advance / Linear Advance bien sintonizados permiten mantener la presión en el nozzle constante en aceleraciones y desaceleraciones bruscas, eliminando blobs en esquinas y under-extrusion en líneas largas a alta velocidad.

### Multi-material y purge towers

Los sistemas multi-material (AMS, ERCF, Palette) introducen variables de purga que impactan directamente en el consumo de filamento: una purge tower mal dimensionada genera contaminación de color; sobredimensionada, desperdicia entre 5–15% del material por cambio. El volumen de purga óptimo depende del par de materiales, del orden de cambio (claro-sobre-oscuro vs. oscuro-sobre-claro) y del caudal volumétrico del hotend. En impresiones largas vale calcular el consumo total de purga antes de lanzar el trabajo.

### Tolerancias dimensionales y shrinkage por material

Las tolerancias reales de una pieza impresa no dependen solo de la resolución del eje: el shrinkage del material al enfriar introduce errores sistemáticos que el slicer puede compensar con un factor de escala. PA y PP tienen shrinkage anisótropo significativo (hasta 2–3% en XY vs. Z); PLA y PETG son más estables (<0,5%). Para piezas de ensamble con tolerancias < 0,2 mm es indispensable imprimir una pieza de calibración dimensional antes de producir el lote.

> 💡 **Nota técnica:** El coeficiente de expansión térmica lineal (CTE) del PLA ronda los 68 µm/m·°C, frente a los ~90 µm/m·°C del PETG y los ~100–150 µm/m·°C del PP. En piezas que operan en ambientes con variación de temperatura, esta diferencia determina si el ensamble mantiene o pierde tolerancia en servicio.

---

## También te puede interesar
- [Extrusores](./partes-impresora/extrusores.md)
- [Boquillas](./partes-impresora/boquillas.md)
- [Camas de Impresión](./partes-impresora/camas-de-impresion.md)
