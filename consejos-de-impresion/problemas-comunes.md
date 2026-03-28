---
titulo: "Problemas Comunes de Impresión 3D"
slug: "problemas-comunes"
seccion: "consejos-de-impresion"
subseccion: ""
material: ""
tipo: "problemas"
ultima_revision: "2026-03-22"
estado: "terminado"
version: "1.0"
---

# Problemas Comunes de Impresión 3D

> Diagnóstico y solución para los fallos más frecuentes — porque casi ningún problema de impresión 3D es irreversible.

La impresión 3D tiene una curva de aprendizaje real, y si tu pieza salió mal, no estás solo. La buena noticia es que la gran mayoría de los problemas obedecen a unas pocas variables —temperatura, velocidad, flujo y adhesión— y todos siguen una lógica que se puede depurar de forma sistemática. Este artículo cubre los nueve fallos más comunes, con sus síntomas, causas y una solución paso a paso. Úsalo como tu guía de diagnóstico: identifica el síntoma visual, sigue los pasos en orden y resuelve el problema antes de lanzar otra impresión.

---

## Warping y Mala Adhesión de Primera Capa

**Síntoma visible:** Las esquinas o bordes de la pieza se despegan de la cama durante o después de la impresión, curvándose hacia arriba. En casos severos, la pieza entera se despega a mitad del proceso. Una forma más temprana del mismo problema es la mala adhesión de primera capa: el filamento no se deposita correctamente desde el inicio — se enrolla alrededor de la boquilla, forma bolitas o se arrastra sin pegarse.

**Causas más frecuentes:**
- Superficie de impresión sucia o sin adherencia adecuada.

> 💡 **¿Por qué se ensucia la cama?** La superficie se contamina de forma natural con polvo ambiental —especialmente en impresoras abiertas— y con la grasa de las manos que se deposita al manipularla para retirar piezas o ajustar el nivel. Aunque no se vea sucia a simple vista, una capa invisible de grasa es suficiente para arruinar la adhesión.
- Temperatura de cama insuficiente para el material.
- Boquilla demasiado lejos de la cama (z-offset incorrecto).
- Enfriamiento brusco de las capas inferiores por corrientes de aire.
- Velocidad de primera capa demasiado alta.
- Piezas grandes con mucha área en contacto con la cama.
- Filamento húmedo que imprime de forma irregular.

**Solución paso a paso:**
1. Limpia la cama con jabón suave de loza y esponja suave bajo agua tibia. Seca bien antes de calentar. ⚠️ **No uses esponjas abrasivas** — pueden rayar o dañar permanentemente la superficie de impresión (PEI, vidrio o lámina flexible).
2. Ajusta el z-offset: el filamento de primera capa debe quedar ligeramente aplastado — visible pero sin ser tan delgado que se transparente.
3. Verifica que la temperatura de cama sea la adecuada para tu material (PLA: 50–60 °C, PETG: 70–85 °C, PA: 90–110 °C).
4. Reduce la velocidad de primera capa al 25–30% de tu velocidad normal en el slicer.
5. Activa el enclosure o elimina corrientes de aire del entorno de impresión.
6. En el slicer, agrega brim de al menos 5–8 mm alrededor de la pieza para aumentar el área de adhesión. El brim tiene variantes: el brim perimetral rodea toda la pieza, mientras que los **mouse ears** son pequeños discos de brim colocados únicamente en las esquinas críticas — una opción más limpia cuando no quieres brim en todo el contorno.
7. Si usas PEI, asegúrate de que esté limpio y sin rayaduras profundas.

**Cómo prevenirlo:**
- Para materiales que requieren temperaturas elevadas de cama (PETG, PPCF), precalienta la cama 5–10 minutos antes de iniciar la impresión para garantizar que la superficie alcance una temperatura suficiente y uniforme — no solo el sensor.
- Para materiales de alta contracción que requieren ambiente controlado, como PA (Nylon) y PP, precalienta tanto la cama como el enclosure durante 15–20 minutos antes de imprimir. Esto eleva y estabiliza la temperatura ambiente interior, reduciendo el gradiente térmico entre las capas que causa el warping en estos materiales.
- El nivel de cama es el factor más determinante. Revisa el tramado (mesh bed leveling) cada cierta cantidad de horas de impresión, no solo cuando algo falle.
- Asegúrate de que la cama esté nivelada y el z-offset sea óptimo antes de cada impresión — una primera capa bien aplastada es la base de todo lo demás.

> 💡 **Boquilla limpia antes de imprimir:** Verifica que la boquilla esté libre de material adherido o carbonizado antes de comenzar. Los restos de filamento en la punta interfieren con los sensores de nivelación automática (ABL), impidiendo que la impresora calibre correctamente la altura de la primera capa y comprometiendo la adhesión desde el inicio.
- El FiLL-3D PLA

**Síntoma visible:** Hilos finos de plástico que quedan entre zonas separadas de la pieza, como telarañas. Frecuente en modelos con partes aisladas o torres.

**Causas más frecuentes:**
- Filamento con humedad absorbida que reduce la viscosidad del fundido. Además, la humedad atrapada en el filamento se evapora al alcanzar temperaturas superiores a 200 °C dentro del extrusor, generando burbujas de vapor que empujan plástico fuera de la boquilla incluso cuando no se está extrudiendo — ese goteo involuntario es el origen directo de los hilos de stringing.
- Temperatura de impresión demasiado alta (el plástico fluye con más facilidad al hacer movimientos en el aire).
- Retracción insuficiente o mal configurada.
- Velocidad de desplazamiento (travel speed) baja.

**Solución paso a paso:**
1. Seca el filamento 6–8 horas a 45–50 °C (PLA) o según el rango del material antes de reimprimir — si hay humedad, ningún ajuste de slicer resolverá el problema de raíz.
2. Reduce la temperatura de boquilla en 5 °C e imprime una torre de temperatura para encontrar el rango óptimo.
3. Aumenta la retracción: en extrusores directos, empieza con 0.5–1 mm; en Bowden, 4–6 mm.
4. Aumenta la velocidad de desplazamiento a 150–200 mm/s si tu impresora lo soporta.
5. Activa "combing" o "avoid crossing perimeters" en tu slicer para que la boquilla no cruce espacios vacíos.

**Cómo prevenirlo:**
- Guarda siempre el filamento en bolsas herméticas con desecante entre usos.
- El FiLL-3D PLA.
3. Reduce la velocidad de impresión un 20%.
4. Si usas ventilación activa al 100%, redúcela al 50–70% para materiales como PLA que igual necesitan algo de enfriamiento, pero no excesivo.
5. Para materiales técnicos (PA, PETG, PP), desactiva completamente la ventilación en las primeras capas.

**Cómo prevenirlo:**
- Consulta siempre el rango de temperatura recomendado para cada filamento. Los materiales FiLL-3D tienen rangos probados y documentados en sus páginas de material.

---

## Subextrusión

**Síntoma visible:** Las paredes de la pieza tienen huecos o líneas incompletas; el relleno (infill) tiene espacios vacíos; la superficie superior se ve porosa o con agujeros.

**Causas más frecuentes:**
- Flujo (flow ratio o multiplicador de extrusión) configurado por debajo del valor real necesario.
- Temperatura de boquilla insuficiente para fundir el filamento a la velocidad de impresión usada.
- Diámetro de boquilla configurado en el slicer mayor al real — el slicer calcula que la boquilla deposita más material del que realmente deposita, resultando en subextrusión.
- Engranaje del extrusor desgastado o con restos de plástico que reducen el agarre.
- Parcialmente obstruida la boquilla (clog parcial).
- Filamento con diámetro inconsistente que genera variaciones de flujo.

**Solución paso a paso:**
1. Corre el test de multiplicador de extrusión de Orca Slicer — método YOLO recomendado para ajustar el valor de flow ratio de forma precisa y rápida.
2. Verifica que el diámetro de boquilla configurado en el slicer coincida con el diámetro real de tu boquilla. Mídela o consulta la documentación de tu impresora y corrige el valor si es necesario.
3. Sube la temperatura 5 °C si imprimes a alta velocidad y vuelve a correr el test de multiplicador de extrusión para confirmar el nuevo valor óptimo.
4. Si sospechas de clog parcial, haz un cold pull a 90 °C (PLA) para limpiar la boquilla.
5. Limpia el engranaje del extrusor con un cepillo de dientes seco.

**Cómo prevenirlo:**
- El diámetro de filamento es crítico: una variación de ±0.1 mm puede traducirse en una diferencia de volumen extruido de hasta 5%. El FiLL-3D PLA mantiene tolerancias de ±0.02 mm, lo que hace que el flow calibrado se mantenga estable a lo largo de toda la impresión.

---

## Sobreextrusión

**Síntoma visible:** Superficie superior irregular con montículos o bultos; paredes más gruesas de lo esperado; exceso de material visible en las esquinas; blobs frecuentes.

**Causas más frecuentes:**
- Flujo (flow ratio o multiplicador de extrusión) configurado por encima del valor real necesario.
- Diámetro de boquilla configurado en el slicer menor al real — el slicer subestima el volumen depositado por capa, compensando con más material del necesario.
- Temperatura de boquilla demasiado alta que reduce la viscosidad del material.
- Velocidad de impresión muy lenta que acumula material.
- Diámetro de filamento incorrecto en la configuración del slicer.

**Solución paso a paso:**
1. Corre el test de multiplicador de extrusión de Orca Slicer — método YOLO recomendado para ajustar el valor de flow ratio hacia abajo de forma precisa.
2. Verifica que el diámetro de boquilla configurado en el slicer coincida con el diámetro real de tu boquilla y corrige si es necesario.
3. Baja la temperatura 5 °C si está en el límite superior del rango recomendado y vuelve a correr el test de multiplicador de extrusión para confirmar el nuevo valor óptimo.
4. Asegúrate de que la velocidad de impresión no sea innecesariamente lenta para geometrías de paredes delgadas.

**Cómo prevenirlo:**
- Calibra el flow una vez por marca de filamento. Con filamentos de tolerancia consistente como FiLL-3D, el valor calibrado se mantiene de rollo en rollo — no tienes que recalibrar cada vez que abres un paquete nuevo.

---

## Clogging (Tapado de Boquilla)

**Síntoma visible:** El extrusor hace clic repetitivos (skipping); el filamento deja de salir parcial o completamente; la impresión tiene zonas sin material o para abruptamente.

**Causas más frecuentes:**
- Cambio de material sin hacer purga adecuada (ej.: pasar de ABS a PLA sin limpiar).
- Temperatura demasiado baja que solidifica el material antes de que pase por la boquilla.
- Flujo demasiado alto que demanda más material del que la boquilla puede fundir y evacuar a tiempo.
- Restos de filamentos anteriores carbonizados dentro de la boquilla por impresión a alta temperatura sin purga.
- Polvo o partículas abrasivas acumuladas en boquillas de latón.
- Retracción excesiva que jala material fundido al interior frío del hotend (heat creep).

**Solución paso a paso:**
1. **Clog parcial:** Sube la temperatura 10–15 °C sobre tu temperatura normal y extrude manualmente 30–50 mm para intentar empujar el obstruyente.
2. **Cold pull:** Calienta a temperatura de impresión, introduce filamento limpio, luego enfría a 90 °C (PLA) o 120 °C (PETG) y jala el filamento con un movimiento firme y constante. Repite 3–5 veces.
3. **Limpieza con aguja:** Con la boquilla caliente, introduce una aguja de 0.35 mm por la punta para desalojar residuos.
4. **Reemplazo:** Si ninguno de los anteriores funciona, reemplaza la boquilla — son componentes de desgaste.
5. Si luego de cambiar la boquilla el taponamiento persiste, revisa los engranajes del extrusor — es probable que haya pedazos de filamento triturado atrapados que bloquean el avance del material.
6. Después de limpiar, purga 100–150 mm de filamento antes de retomar la impresión.

**Cómo prevenirlo:**
- Siempre purga al cambiar de material o color.
- Usa boquillas de acero endurecido si imprimes materiales con fibra (PPCF) que desgastan las boquillas de latón.
- Un filamento con baja humedad y tolerancias precisas reduce la probabilidad de clog: el material húmedo genera vapor que puede crear burbujas y residuos dentro del hotend.

---

## Blobs y Zits

**Síntoma visible:** Pequeñas protuberancias o puntos en la superficie exterior de la pieza, especialmente en el punto donde la boquilla inicia o termina cada perímetro. Arruinan la estética de superficies que deben verse lisas.

**Causas más frecuentes:**
- Presión residual en el hotend que libera un pequeño exceso de material al inicio del perímetro.
- Configuración de retracción insuficiente al finalizar un perímetro.
- Punto de inicio/fin de perímetro siempre en el mismo lugar (crea una línea vertical de blobs).
- Extra restart distance mal calibrada después de la retracción.

**Solución paso a paso:**
1. Activa "randomize seam position" o "align seam to back" en tu slicer para distribuir o esconder el punto de inicio.
2. Ajusta la retracción: aumenta ligeramente (0.1–0.2 mm) y observa si los blobs en el punto de inicio desaparecen.
3. Activa "wipe before retract" en el slicer — mueve la boquilla sobre el perímetro impreso antes de retraer para reducir la presión.
4. Ajusta el "extra restart distance" a un valor ligeramente negativo (−0.05 a −0.1 mm) para compensar el ooze al reiniciar.
5. Calibra el pressure advance (o linear advance) con el test de línea de Orca Slicer — el proceso dura menos de 10 minutos y mejora notablemente los resultados, especialmente a altas velocidades de impresión.

**Cómo prevenirlo:**
- Los blobs son en gran medida un problema de calibración de slicer, no de filamento. Dicho esto, un filamento con diámetro uniforme hace que la presión interna del hotend sea más predecible, facilitando la calibración de pressure advance.

---

## Mal Desempeño en Voladizos

**Síntoma visible:** Las zonas de la pieza que se imprimen en el aire (sin superficie debajo) se curvan hacia abajo, muestran capas irregulares o tienen una apariencia deshilachada. Ángulos mayores a 45–50° suelen verse afectados.

**Causas más frecuentes:**
- Enfriamiento insuficiente: el material no solidifica lo suficientemente rápido antes de que la capa siguiente lo aplaste.
- Temperatura de impresión demasiado alta que mantiene el material blando por más tiempo.
- Velocidad de impresión muy alta en zonas de voladizo — menos tiempo para que cada segmento se enfríe.
- Altura de capa demasiado grande que exige más material "en el aire" por capa.
- Geometría del modelo no orientada para minimizar los voladizos.

**Solución paso a paso:**
1. Aumenta la velocidad del ventilador al 100% para las zonas de voladizo (en el slicer puedes configurar esto por ángulo de overhang).
2. Reduce la temperatura de boquilla 5–10 °C para voladizos extremos.
3. Reduce la velocidad de impresión al 50% en zonas de overhang — la mayoría de slicers tienen esta opción automáticamente.
4. Reduce la altura de capa si el modelo tiene geometrías críticas: pasar de 0.2 mm a 0.16 mm mejora notablemente los voladizos.
5. Si el modelo lo permite, reoriéntalo en el slicer para que los voladizos críticos apunten hacia arriba o usa soportes estratégicamente.
6. Para voladizos extremos (>70°) en materiales técnicos, los soportes son la solución más confiable.

**Cómo prevenirlo:**
- Al diseñar o preparar modelos, la regla de los 45° es tu aliada: ángulos menores a 45° desde la vertical casi siempre imprimen bien sin soporte.
- Los voladizos son especialmente exigentes con PA (Nylon) y PP por su mayor temperatura de impresión — planifica los soportes desde el inicio para estas piezas técnicas.

---

## También te puede interesar
- [Post-Procesado](./post-procesado.md)
- [Referencia Técnica](../referencia-tecnica/index.md)
- [Materiales de Impresión 3D](../lo-basico/materiales-impresion-3d.md)
