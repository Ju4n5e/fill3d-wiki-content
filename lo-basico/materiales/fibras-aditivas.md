---
titulo: "Fibras Aditivas — Ficha de Material"
slug: "fibras-aditivas"
seccion: "lo-basico"
subseccion: "materiales"
material: "PPCF"
tipo: "material"
ultima_revision: "2026-03-23"
estado: "terminado"
version: "1.0"
---

# Fibras Aditivas — Ficha de Material

> Más rígido, más resistente y más abrasivo: todo lo que cambia cuando le agregas fibra de carbono o de vidrio al filamento.

---

## Para Principiantes

Los filamentos con **fibra de carbono** o **fibra de vidrio** son materiales compuestos: toman un plástico base y le mezclan fibras cortas para hacerlo notablemente más rígido y resistente. El resultado es un material con comportamiento diferente al base: más duro al tacto, con un acabado superficial mate muy particular, y piezas considerablemente más rígidas sin aumentar el peso.

En el catálogo de FiLL-3D esta categoría está representada por el PPCF mejoran principalmente la **rigidez** (módulo de Young) y la **resistencia específica** (resistencia por unidad de peso) del polímero base. La fibra de carbono maximiza la rigidez y reduce el peso; la fibra de vidrio es más económica y mejora también la resistencia al impacto. En ambos casos, la **fragilidad** aumenta respecto al polímero puro — los compuestos con fibra son menos dúctiles y absorben menos energía antes de fracturarse.

### Parámetros de impresión recomendados — FiLL-3D PPCF

| Parámetro | Valor recomendado | Notas |
|---|---|---|
| Temperatura de boquilla | 300 °C | Estricto; ±5 °C afecta el flujo significativamente |
| Temperatura de cama | 80 °C | La estabilidad de la fibra de carbono permite cama menor que el PP base |
| Velocidad de impresión | hasta 200 mm/s (17 mm³/s) | Mayor que PP puro — ver nota en Para Expertos |
| Enfriamiento | 0 % (primeras 5 capas); luego hasta 80 % | Según fan_max_speed del perfil |
| Retracción | 0.2 mm @ 45 mm/s | Pressure Advance K=0.044 |
| Flujo (flow) | 100–110 % | Las fibras pueden reducir el volumen efectivo extruido |
| Tipo de boquilla | Acero endurecido mínimo | **Obligatorio** — el latón se destruye en horas |
| Diámetro de boquilla | 0.4–0.6 mm | Boquillas más grandes reducen el riesgo de atasco |

### Aplicaciones ideales

- Piezas estructurales en drones y aeronáutica de hobby
- Componentes automotrices y de maquinaria de alto rendimiento
- Brackets y soportes con alta relación rigidez/peso
- Componentes estructurales de impresoras 3D (marcos, carros)
- Prototipos de ingeniería con carga mecánica real
- Accesorios deportivos y de equipamiento técnico

### Ventajas y limitaciones

| Ventajas | Limitaciones |
|---|---|
| Alta rigidez específica (rigidez/peso) | Abrasivo — destruye boquillas de latón rápidamente |
| Acabado superficial mate de alta calidad | Más frágil que el polímero base solo |
| Reduce warping vs. el polímero base solo | Requiere boquilla especializada (costo adicional) |
| Mantiene las propiedades del polímero base | Mayor costo que el material base |
| Excelente para piezas estructurales livianas | Resistencia en Z significativamente menor que en XY |

### Almacenamiento

Seguir el protocolo del polímero base correspondiente. Para el PPCF, aunque el PP base no es muy higroscópico, las fibras pueden retener humedad superficial. Guardar sellado con sílica gel en todo momento. Secar a **60 °C por 4 horas** antes de sesiones largas o impresiones críticas.

---

## Para Expertos

### Anisotropía: la dirección de impresión lo es todo

Los compuestos con fibra discontinua en FDM son fuertemente anisotrópicos. Durante la extrusión, las fibras cortas se alinean principalmente en la dirección de deposición (XY), generando mayor rigidez en esa dirección. En Z (entre capas) la resistencia puede ser 40–70 % menor que en XY. Para piezas estructurales esto es crítico: la orientación de impresión debe planificarse para que la dirección de carga principal coincida con XY. En geometrías complejas, considera imprimir en múltiples orientaciones y ensamblar las partes resultantes.

### Gestión del desgaste de boquilla y prevención de atascos

Las fibras de carbono y vidrio desgastan incluso las boquillas de acero endurecido, aunque mucho más lento que el latón. Lleva registro del metraje impreso con materiales abrasivos y reemplaza la boquilla preventivamente (cada 3–10 kg de material según el grado de dureza del recubrimiento). Los atascos parciales son más frecuentes con fibra porque los fragmentos pueden acumularse en la zona de transición frío–caliente del hotend. Un cold pull con filamento de limpieza antes y después de cada sesión con compuestos prolonga significativamente la vida del conjunto hotend.

### Por qué el PPCF imprime más rápido que el PP base

El PP puro es un filamento excepcionalmente blando y flexible, lo que lo hace propenso al *buckling* en la zona de avance del extrusor: antes de que el hotend pueda fundir el material, el filamento se dobla o patina, limitando el flujo máximo. En pruebas de calibración con FiLL-3D PP el flujo volumétrico máximo alcanzado fue de **14 mm³/s**. Con FiLL-3D PPCF ese límite sube a **17 mm³/s** — equivalente a ~200 mm/s lineales con boquilla de 0.4 mm y altura de capa de 0.2 mm.

El mecanismo no es una mejora de la fluidez del fundido (reológicamente, las fibras aumentan la viscosidad aparente), sino una mejora en la **transmisión de fuerza del extrusor**: las fibras cortas rigidizan el filamento sólido en la zona de avance, reduciendo el *buckling* y permitiendo mayor presión efectiva en la cámara de fusión antes del fallo. Dicho de otra forma: el cuello de botella del PP puro está en el filamento sólido, no en el hotend — y las fibras eliminan ese cuello de botella.

### Calibración de flujo y Pressure Advance en compuestos

Los filamentos con fibra tienen reología diferente al polímero base: la viscosidad aumenta y el flujo se vuelve menos predecible. La calibración de flujo con el método estándar suele arrojar valores de 105–115 % respecto al perfil del polímero base solo. Además, el **Pressure Advance** necesita recalibrarse desde cero porque la mayor viscosidad cambia la respuesta dinámica del extrusor. No reutilices perfiles del polímero base para los compuestos — calibra siempre de cero, incluso si es el mismo fabricante.

> 💡 **Nota técnica:** Las fibras en filamentos FDM son fibras **discontinuas** (cortas, típicamente 50–200 µm tras el proceso de extrusión del filamento). No confundir con sistemas de fibra continua como Markforged o Anisoprint, cuyas propiedades mecánicas son un orden de magnitud superiores. Los filamentos de fibra corta mejoran la rigidez y la relación rigidez/peso, pero no alcanzan las propiedades de los composites de fibra continua.

---

## También te puede interesar
- PP — Ficha de Material
- PA (Nylon) — Ficha de Material
- Consejos de Impresión por Tipo de Material