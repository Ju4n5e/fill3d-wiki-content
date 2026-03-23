---
titulo: "Mantenimiento de la Impresora"
slug: "mantenimiento"
seccion: "lo-basico"
subseccion: "mantenimiento"
material: ""
tipo: "conceptual"
ultima_revision: "2026-03-22"
estado: "terminado"
version: "1.0"
---

# Mantenimiento de la Impresora

> Una impresora bien mantenida falla menos, imprime mejor y dura años más: este es el plan de cuidado que deberías seguir.

---

## Para Principiantes

Mantener una impresora 3D es parecido a mantener un carro: no necesitas ser mecánico experto, pero sí dedicarle atención periódica a unas pocas cosas clave. Si esperas a que algo falle para actuar, normalmente el problema ya es más grande de lo que habría sido con mantenimiento preventivo.

Las buenas noticias: la mayoría del mantenimiento básico toma menos de diez minutos y no requiere herramientas especiales. Limpiar la cama después de cada impresión, revisar que las correas no estén flojas, y lubricar los ejes cada cierto tiempo son los tres hábitos que más impacto tienen en la calidad de tus piezas y en la vida útil de tu equipo.

Lo más importante para empezar: **la limpieza**. El polvo, los restos de filamento y los aceites de los dedos son los enemigos silenciosos de una impresora. Una máquina limpia es una máquina que funciona. A partir de esa base, el resto del mantenimiento se vuelve más fácil de entender y de hacer.

---

## Todo lo que Necesitas Saber

### Calendario de mantenimiento recomendado

> **Nota:** Las impresoras modernas llevan registro de sus horas de trabajo y te darán recordatorios y recomendaciones de mantenimiento directamente desde su interfaz — úsalos como punto de partida, no como único criterio.

| Frecuencia | Tarea | Impacto si se omite |
|---|---|---|
| Antes de cada impresión | Limpiar cama con alcohol isopropílico, revisión visual rápida | Mala adhesión de primera capa |
| Cada semana | Retirar restos de filamento del extrusor y cama | Acumulación que causa atascos |
| Cada mes | Lubricar ejes y tornillo Z, revisar tensión de correas | Ruido, imprecisión dimensional, desfases de capa |
| Cada 1–3 meses | Cambiar boquilla de latón, revisar tubo PTFE | Subextrusión, stringing, atascos |
| Cada 6 meses | Revisar rodamientos, apretar tornillos del marco, limpiar electrónica | Vibración, capas irregulares |
| Según disponibilidad | Actualizar firmware del fabricante | Sin acceso a correcciones y mejoras |

### Limpieza

**Cama de impresión:** Limpia con alcohol isopropílico al 70–90% antes de cada impresión usando un paño que no suelte pelusa. Retira cualquier resto de filamento con una espátula plástica para no rayar la superficie. Si usas adhesivo, límpialo completamente antes de aplicar la siguiente capa.

**Extrusor y engranaje de arrastre:** Los restos de filamento molido se acumulan en los dientes del engranaje y reducen el agarre. Retíralos con un cepillo de cerdas rígidas (nylon o latón) con la impresora apagada. Si tienes impresora con AMS o alimentador multimaterial, revisa también los tubos de guía de filamento.

**Electrónica:** Cada seis meses, con la impresora apagada y desconectada, usa aire comprimido a baja presión para retirar el polvo de la placa madre, la fuente de poder y los ventiladores. El polvo acumulado genera calor y puede causar fallas eléctricas.

### Lubricación

La lubricación reduce la fricción en los ejes lineales y garantiza movimientos suaves y precisos.

- **Ejes de varilla (rods):** Aplica una gota pequeña de **grasa PTFE** o aceite de máquina liviano en cada eje y mueve el carro manualmente para distribuirla. No uses WD-40: desplaza la lubricación existente pero no lubrica de manera duradera.
- **Tornillo Z (lead screw):** Limpia la grasa vieja con un trapo, luego aplica grasa de litio blanca en toda la longitud y mueve el eje para distribuirla. El tornillo Z bien lubricado elimina el Z-wobble.
- **Rodamientos lineales:** La mayoría son sellados de fábrica y no requieren lubricación externa. Si escuchas chirridos, pueden estar desgastados —el reemplazo es preferible a lubricar por fuera.

### Tensión de correas

Las correas deben estar tensas pero no excesivamente rígidas. La prueba práctica: pínchala como una cuerda de guitarra; debe sonar un tono claro sin estar tan rígida que no se mueva. Una correa floja causa **desfases de capa** (layer shifts) y fantasmas (ghosting/ringing) en las paredes. Usa los tensores del marco si tu impresora los tiene, o busca piezas tensoras imprimibles compatibles con tu modelo.

### Extrusor y boquilla

- **Cold pull periódico:** Cada vez que cambies de un material de alta temperatura a uno de baja (por ejemplo, de PA a PLA), realiza un cold pull con nylon para limpiar residuos. Ver detalles en [Boquillas](../partes-impresora/boquillas.md).
- **Reemplazo de boquilla de latón:** Cada 1–3 meses de uso regular, o antes si notas subextrusión persistente tras limpiar. Las boquillas de acero endurecido duran significativamente más.
- **Tubo PTFE:** Inspecciónalo por decoloración (amarillamiento) o kinks. El PTFE degradado puede liberar vapores a temperaturas superiores a 260 °C. Cámbialo si presenta desgaste visible, especialmente en la zona del hotend.

### Revisión del marco y hardware

Vibración y movimiento continuo aflojan los tornillos del marco con el tiempo. Aprieta todos los tornillos del marco con llave Allen cada seis meses. Presta especial atención a los tornillos de los perfiles de extrusión en impresoras tipo Cartesiana con carros sobre ruedas: las ruedas/rollers deben estar ajustadas al punto de no girar libremente pero sin exceso de presión que deforme la ranura.

### Firmware

Revisa periódicamente el sitio del fabricante por actualizaciones. Las actualizaciones de firmware corrigen bugs, mejoran algoritmos de nivelación automática y en algunos casos añaden soporte para nuevos materiales o mejoras de Pressure Advance.

---

## Para Expertos

### Diagnóstico por artefactos visuales

Las fallas de mantenimiento dejan firmas específicas en las piezas:
- **Ghosting / ringing (ondas en las paredes):** Correas flojas o rodamientos desgastados. Mide la frecuencia del patrón de ondas y compárala con la frecuencia de resonancia de los ejes.
- **Z-wobble (ondulación periódica en el eje Z):** Tornillo Z desalineado, acoplamiento flexible desgastado o tuerca de avance con juego.
- **Layer shifts (desfase súbito):** Correa que patina, motor paso a paso sin corriente suficiente, o colisión del cabezal con material desbordado.
- **Stringing progresivo sin cambio de parámetros:** Tubo PTFE degradado que aumenta la fricción de retracción, o boquilla desgastada con orificio agrandado.

### Selección correcta de lubricantes

No todos los lubricantes son iguales en una impresora 3D:
- **Grasa PTFE (Superlube, Molykote):** Ideal para varillas lisas. No atrae polvo, temperatura de servicio amplia.
- **Grasa de litio blanca:** Mejor opción para tornillos Z y engranajes. Más viscosa, aguanta mejor la carga mecánica.
- **Aceite de máquina liviano (ISO 32):** Para varillas en entornos limpios donde la grasa podría atraer partículas abrasivas.
- **Evitar:** WD-40 (desplazante, no lubricante duradero), aceite de cocina (se oxida y emplana), grasa de carro (demasiado viscosa para movimientos lineales finos).

### Mantenimiento específico por cinemática

- **Cartesiana (Ender, Prusa i3):** Prioriza varillas y rodamientos lineales. Las varillas tienden a desarrollar líneas de desgaste localizadas; rótalas 90° cuando notes huellas visibles.
- **CoreXY (Bambu Lab, Voron, RatRig):** El sistema de correas es más complejo (dos correas en H-bot o correa cruzada). Asegúrate de que **ambas correas tengan la misma tensión** o la geometría de movimiento se descompensa y aparecen errores dimensionales en los ejes diagonales.
- **Delta:** Los brazos articulados necesitan revisión de juego en las rótulas. Incluso un milímetro de juego en un brazo se traduce en error de posicionamiento en el plano XY.

> 💡 **Nota técnica:** En impresoras CoreXY, la tensión desigual entre las dos correas del eje XY es una causa frecuente de imprecisión dimensional en piezas con geometría diagonal (rombos, ángulos de 45°). Usa la función de vibration compensation / input shaping del firmware para detectar resonancias asimétricas que indican tensión desbalanceada.

---

## También te puede interesar
- [Accesorios y Repuestos](./accesorios-y-repuestos.md)
- [Boquillas](../partes-impresora/boquillas.md)
- [Problemas Comunes de Impresión](../../consejos-de-impresion/problemas-comunes.md)