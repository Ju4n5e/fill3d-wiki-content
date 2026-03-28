---
titulo: "Post-Procesado de Impresiones 3D"
slug: "post-procesado"
seccion: "consejos-de-impresion"
subseccion: ""
material: ""
tipo: "problemas"
ultima_revision: "2026-03-25"
estado: "terminado"
---

# Post-Procesado de Impresiones 3D

> Porque una pieza recién salida de la impresora casi nunca es el producto final.

La impresión FDM deja marcas de capa visibles, estructuras de soporte que hay que retirar y superficies que no siempre están listas para usarse directamente. El post-procesado es el conjunto de técnicas que transforma esa pieza cruda en algo terminado: funcional, resistente o con la apariencia que necesitas. No todas las piezas lo requieren en la misma medida — a veces basta con retirar los soportes; otras veces quieres un acabado pintado y sellado. En esta guía encontrarás las técnicas más comunes, los materiales que necesitas y los pasos para ejecutarlas bien desde la primera vez.

---

## Remoción de Soportes

**Qué logra:** Elimina las estructuras de soporte generadas por el slicer para imprimir geometrías con voladizos o puentes, dejando la pieza lista para las etapas siguientes.

**Materiales/herramientas necesarios:**
- Alicates de punta fina o alicates de corte
- Bisturí o cúter de precisión
- Lija de grano grueso (80–120) para limpiar la zona de contacto
- Guantes si los soportes son de material técnico con bordes filosos

**Proceso paso a paso:**
1. Espera a que la pieza esté completamente fría antes de retirarla de la cama.
2. Identifica todos los puntos de contacto soporte–pieza antes de empezar.
3. Dobla el soporte en dirección contraria al punto de contacto para romperlo limpiamente.
4. Usa el bisturí para raspar o cortar los restos de soporte pegados a la superficie.
5. Lija suavemente la zona de contacto para eliminar imperfecciones.

**Consejos y errores comunes:**
- Con FiLL-3D PLA los soportes se desprenden con facilidad si usas un separador de soportes en el slicer — actívalo siempre.
- El FiLL-3D PETG tiende a soldar el soporte a la pieza con más fuerza; reduce la densidad del soporte o aumenta la distancia Z de soporte en el slicer.
- El FiLL-3D PA y el FiLL-3D PP son más flexibles — los soportes se pelan mejor que en PLA pero pueden dejar marcas más notorias; ten paciencia y usa el bisturí.
- Error frecuente: retirar los soportes en caliente. La pieza todavía blanda se deforma o se arranca material donde no debe.

---

## Lijado y Acabado de Superficie

**Qué logra:** Reduce o elimina las líneas de capa visibles, suaviza irregularidades y prepara la superficie para pintar o pegar.

**Materiales/herramientas necesarios:**
- Lijas de agua en progresión: 120 → 220 → 400 → 800 → 1200 (según el nivel de acabado deseado)
- Agua o lubricante para lijado en húmedo
- Bloque de lijado o respaldo rígido para lijar plano
- Masilla de relleno (filler) en spray para rellenar imperfecciones entre pasadas

**Proceso paso a paso:**
1. Empieza con grano 120–220 para eliminar las líneas de capa más gruesas. Usa movimientos circulares y uniformes.
2. Lija en húmedo a partir de grano 400 — el agua evita que el plástico se caliente y se atasque la lija.
3. Aplica una capa de masilla de relleno en spray si hay huecos o imperfecciones profundas. Deja secar el tiempo indicado y lija de nuevo con 400.
4. Avanza progresivamente hasta 800–1200 si quieres una superficie casi espejada.
5. Limpia bien con agua y paño seco antes del siguiente paso.

**Consejos y errores comunes:**
- El FiLL-3D PLA lija bien pero genera calor con fricción — trabaja en sesiones cortas o en húmedo para evitar que el plástico ablande.
- PETG y PA tienen mayor resistencia al lijado; necesitan más pasadas con granos intermedios antes de avanzar.
- El FiLL-3D PPCF (PP con fibra de carbono) libera partículas de fibra al lijar — usa mascarilla y trabaja en un espacio ventilado.
- Imprime con al menos 3 paredes cuando planees lijar la pieza — así tendrás suficiente material para remover y mejorar el acabado sin comprometer la resistencia estructural.
- Error frecuente: saltarse granos. Ir de 120 a 800 directamente solo profundiza los rayones en lugar de eliminarlos.

---

## Pegado de Partes

**Qué logra:** Une piezas impresas por separado para ensamblar modelos grandes, piezas multicomponente o reparaciones.

**Materiales/herramientas necesarios:**
- Cianoacrilato (pegante instantáneo) para PLA y PETG
- Epoxy de dos partes para uniones estructurales o materiales técnicos
- Activador de cianoacrilato (spray) para acelerar el fraguado
- Cinta de enmascarar para fijar las partes mientras fragua
- Lija de grano 120 para preparar las superficies

**Proceso paso a paso:**
1. Lija ligeramente ambas superficies de contacto con grano 120 para crear rugosidad mecánica — mejora la adhesión notablemente.
2. Limpia el polvo con un paño seco o aire comprimido.
3. Aplica el adhesivo en una de las superficies (capa fina y uniforme).
4. Une las partes y presiona firmemente durante 30–60 segundos.
5. Retira exceso de adhesivo con alcohol isopropílico antes de que cure.
6. Para uniones estructurales, aplica un cordón de epoxy en el perímetro de la unión como refuerzo.

**Consejos y errores comunes:**
- El cianoacrilato funciona muy bien con PLA y PETG; para PA y PP el epoxy de dos partes da mejores resultados porque estas superficies son menos receptivas al cianoacrilato.
- El [FiLL-3D PP](https://www.fill-3d.com/tienda/) es uno de los materiales más difíciles de pegar — su baja energía superficial repele casi todos los adhesivos. Usa un imprimante adhesivo específico para polipropileno o considera diseñar uniones mecánicas (encastres, tornillos).
- Si necesitas rellenar un hueco o imperfección en la unión, mezcla cianoacrilato con bicarbonato de sodio — el bicarbonato actúa como relleno y la mezcla cura casi al instante formando una masa dura que se puede lijar.
- Error frecuente: aplicar demasiado adhesivo. El exceso no mejora la unión, llena las líneas de capa y mancha la superficie.

---

## Pintura y Acabados Estéticos

**Qué logra:** Agrega color, textura o protección superficial a la pieza terminada, ya sea para estética o para identificación visual de partes.

**Materiales/herramientas necesarios:**
- Pintura acrílica en spray (base + color + barniz)
- Imprimante (primer) en spray — idealmente formulado para plásticos
- Lija fina (400–800) para preparar entre capas
- Mascarilla y espacio ventilado

**Proceso paso a paso:**
1. Asegúrate de que la pieza esté limpia, seca y lijada al nivel de acabado deseado.
2. Aplica una capa de imprimante para plásticos a 30–40 cm de distancia, con pasadas uniformes. Deja secar 20–30 minutos.
3. Lija suavemente con 400 para eliminar rugosidad del imprimante. Limpia el polvo.
4. Aplica la pintura de color en capas finas (2–3 manos). Espera entre cada capa.
5. Finaliza con una capa de barniz (mate, satinado o brillante) para sellar y proteger.

**Consejos y errores comunes:**
- El imprimante es obligatorio — sin él la pintura no adhiere bien al plástico y se descascarilla con el uso.
- Los colores oscuros del FiLL-3D PLA pueden traslucir bajo pinturas claras; aplica un imprimante blanco primero si quieres colores pastel o blancos sobre filamento oscuro.
- El PETG tiene una superficie ligeramente más lisa que el PLA — el lijado previo con 220 es especialmente importante para que el imprimante se adhiera correctamente.
- Error frecuente: aplicar capas gruesas para cubrir más rápido. Genera escurridos y secado disparejo. Siempre capas delgadas y múltiples.

---

## Tratamiento Químico

**Qué logra:** Suaviza y fusiona las líneas de capa mediante la acción de solventes, logrando una superficie casi inyectada sin lijado mecánico.

**Materiales/herramientas necesarios:**
- Acetona (para ABS — ver nota más abajo)
- Diclorometano (DCM) para PETG — ver nota de compatibilidad abajo
- Recipiente hermético para técnica de vapor
- Guantes de nitrilo, gafas de protección y ventilación obligatoria

**Proceso paso a paso:**
1. Coloca la pieza sobre una rejilla dentro de un recipiente hermético.
2. Vierte una pequeña cantidad de solvente en el fondo del recipiente (no en contacto directo con la pieza).
3. Cierra el recipiente y espera 1–5 minutos (el tiempo depende del material y del nivel de suavizado deseado).
4. Retira la pieza, colócala en una superficie antiadherente y deja evaporar el solvente completamente antes de tocarla.
5. La pieza estará blanda temporalmente — no la manipules hasta que esté completamente seca y firme.

**Consejos y errores comunes:**
- **Compatibilidad por material:**
  - **ABS** (de otras marcas — FiLL-3D no lo comercializa): acetona. El método más accesible y efectivo.
  - **PETG:** diclorometano (DCM). Funciona bien, pero el DCM está clasificado como sustancia peligrosa y requiere permisos especiales en muchas regiones — no es para uso doméstico casual.
  - **PLA:** no compatible con acetona (produce blanqueamiento y microfisuras, no suavizado). No existe un solvente de uso común que funcione bien para PLA; el lijado progresivo es el método correcto.
  - **PA (Nylon) y PP:** no tienen solventes comunes prácticos para smoothing — el lijado es el único método recomendado para estos materiales.
- Los solventes son materiales peligrosos: nunca uses esta técnica sin ventilación adecuada, nunca en llama abierta y siempre con protección personal.
- Error frecuente: excederse en el tiempo de exposición. Una pieza sobreexpuesta pierde detalle y puede deformarse irreversiblemente.

---

## Inserción de Insertos Roscados (Heat Inserts)

**Qué logra:** Incorpora insertos metálicos roscados en la pieza impresa para crear roscas duraderas que resisten múltiples ciclos de atornillado, sin desgastar el plástico.

**Materiales/herramientas necesarios:**
- Insertos roscados de latón (M2, M3, M4, M5 según el diseño)
- Soldador de temperatura regulable (ajustado entre 200–240 °C para PLA/PETG)
- Punta específica para insertos (cónica o plana, según el tipo)
- Superficie de trabajo resistente al calor

**Proceso paso a paso:**
1. Diseña el agujero piloto en el modelo con un diámetro igual al diámetro exterior del inserto (no al de la rosca interna).
2. Calienta el soldador a la temperatura del material: ~200 °C para PLA, ~220 °C para PETG, ~230 °C para PA.
3. Apoya el inserto sobre el agujero con la punta del soldador y aplica presión suave y constante.
4. Hunde el inserto lentamente hasta que quede al ras o ligeramente por debajo de la superficie.
5. Retira el soldador y deja enfriar sin mover la pieza durante 30–60 segundos.

**Consejos y errores comunes:**
- El FiLL-3D PLA acepta insertos con facilidad por su baja temperatura de trabajo; el FiLL-3D PETG da resultados aún mejores porque es más tenaz y las paredes se deforman menos.
- Para FiLL-3D PA y FiLL-3D PP, sube la temperatura del soldador 10–20 °C por encima de lo que usarías con PLA — estos materiales necesitan más calor para fluir correctamente.
- Error frecuente: hundir el inserto demasiado rápido. Si empujas con fuerza, el inserto queda torcido y no hay forma de corregirlo sin dañar la pieza. Velocidad lenta y presión constante.
- Imprime el agujero piloto con orientación de capas perpendicular a la dirección de inserción para maximizar la resistencia al arranque.

---

## Sellado e Impermeabilización

**Qué logra:** Cierra los microporos entre capas para hacer la pieza resistente al agua, a líquidos o a la humedad, y refuerza estructuralmente la superficie exterior.

**Materiales/herramientas necesarios:**
- Resina epoxy de baja viscosidad (XTC-3D o equivalente) para sellado superficial
- Pincel de pelo suave o aplicador de espuma
- Lija fina (400) para preparar la superficie
- Cinta de enmascarar para proteger zonas que no se van a sellar

**Proceso paso a paso:**
1. Lija la superficie con 400 y limpia el polvo completamente.
2. Mezcla la resina epoxy en la proporción indicada por el fabricante (generalmente 2:1 o 1:1 en volumen).
3. Aplica una capa fina y uniforme con el pincel. Trabaja rápido — la resina tiene un tiempo de trabajo limitado.
4. Deja curar 12–24 horas en posición horizontal para evitar escurridos.
5. Si quedan burbujas en la superficie, pásalas con la llama de un encendedor brevemente a 10 cm de distancia — el calor las revienta antes de que la resina cure.
6. Lija suavemente con 400 entre capas si deseas aplicar una segunda mano.

**Consejos y errores comunes:**
- Esta técnica funciona especialmente bien con FiLL-3D PLA y FiLL-3D PETG para hacer contenedores, floreros, macetas y piezas que van a estar en contacto con agua.
- El FiLL-3D PP ya es naturalmente resistente a muchos líquidos y químicos por su naturaleza como poliolefina — a veces no necesita sellado adicional para aplicaciones de contacto con agua.
- El PETG impreso con baja porosidad (infill alto + paredes gruesas) puede ser prácticamente impermeable sin sellado extra; la resina epoxy suma resistencia mecánica y un acabado más liso.
- Error frecuente: aplicar la resina sobre superficie sucia o con grasa. La resina no adhiere y se desprende. La preparación de la superficie es el paso más importante.

---

## También te puede interesar
- [Problemas Comunes de Impresión](./problemas-comunes.md)
- [Consejos por Tipo de Material](./por-tipo-de-material.md)
- [PLA — Ficha de Material](../lo-basico/materiales/pla.md)
