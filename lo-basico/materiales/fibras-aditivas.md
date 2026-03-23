---
titulo: "Fibras Aditivas — Ficha de Material"
slug: "fibras-aditivas"
seccion: "lo-basico"
subseccion: "materiales"
material: "PPCF"
tipo: "material"
ultima_revision: "2026-03-22"
estado: "borrador"
---

# Fibras Aditivas — Ficha de Material

> Más rígido, más resistente y más abrasivo: todo lo que cambia cuando le agregas fibra de carbono o de vidrio al filamento.

---

## Para Principiantes

Los filamentos con **fibra de carbono** o **fibra de vidrio** son materiales compuestos: toman un plástico base y le mezclan fibras cortas para hacerlo notablemente más rígido y resistente. El resultado es un material con comportamiento diferente al base: más duro al tacto, con un acabado superficial mate muy particular, y piezas considerablemente más rígidas sin aumentar el peso.

En el catálogo de FiLL-3D esta categoría está representada por el [PPCF](https://www.fill-3d.com/tienda/) — polipropileno reforzado con fibra de carbono — un material técnico premium que combina la ligereza y resistencia química del PP con la rigidez que solo la fibra de carbono puede agregar.

La advertencia más importante antes de empezar: estos filamentos son **altamente abrasivos** y destruyen las boquillas de latón estándar en pocas horas de impresión. Antes de cargar cualquier compuesto con fibra, necesitas instalar una boquilla de acero endurecido, acero inoxidable, rubí o carburo. Esto no es opcional — es el primer requisito del equipo.

---

## Todo lo que Necesitas Saber

### Características del material

Los compuestos con fibra discontinua (corta) mejoran principalmente la **rigidez** (módulo de Young) y la **resistencia específica** (resistencia por unidad de peso) del polímero base. La fibra de carbono maximiza la rigidez y reduce el peso; la fibra de vidrio es más económica y mejora también la resistencia al impacto. En ambos casos, la **fragilidad** aumenta respecto al polímero puro — los compuestos con fibra son menos dúctiles y absorben menos energía antes de fracturarse.

### Parámetros de impresión recomendados — FiLL-3D PPCF

| Parámetro | Valor recomendado | Notas |
|---|---|---|
| Temperatura de boquilla | 240–260 °C ⚠️ verificar | Superior al PP base — las fibras aumentan viscosidad |
| Temperatura de cama | 100–115 °C ⚠️ verificar | Igual al PP base |
| Velocidad de impresión | 20–35 mm/s ⚠️ verificar | Más lento que PP puro |
| Enfriamiento | 50–70 % ⚠️ verificar | |
| Retracción | 1–3 mm a 30 mm/s ⚠️ verificar | Reducir vs PP base para evitar atascos |
| Flujo (flow) | 100–110 % ⚠️ verificar | Las fibras pueden reducir el volumen efectivo extruido |
| Tipo de boquilla | Acero endurecido mínimo | **Obligatorio** — el latón se destruye en horas |
| Diámetro de boquilla | 0.4–0.6 mm ⚠️ verificar | Boquillas más grandes reducen el riesgo de atasco |

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
| Reduce warping vs el polímero base solo | Requiere boquilla especializada (costo adicional) |
| Mantiene las propiedades del polímero base | Mayor costo que el material base |
| Excelente para piezas estructurales livianas | Resistencia en Z significativamente menor que en XY |

### Almacenamiento

Seguir el protocolo del polímero base correspondiente. Para el PPCF, aunque el PP base no es muy higroscópico, las fibras pueden retener humedad superficial. Guardar sellado con sílica gel en todo momento. Secar a **60–70 °C por 4–6 horas** ⚠️ verificar antes de sesiones largas o impresiones críticas.

---

## Para Expertos

### Anisotropía: la dirección de impresión lo es todo

Los compuestos con fibra discontinua en FDM son fuertemente anisotrópicos. Durante la extrusión, las fibras cortas se alinean principalmente en la dirección de deposición (XY), generando mayor rigidez en esa dirección. En Z (entre capas) la resistencia puede ser 40–70 % menor que en XY. Para piezas estructurales esto es crítico: la orientación de impresión debe planificarse para que la dirección de carga principal coincida con XY. En geometrías complejas, considera imprimir en múltiples orientaciones y ensamblar las partes resultantes.

### Gestión del desgaste de boquilla y prevención de atascos

Las fibras de carbono y vidrio desgastan incluso las boquillas de acero endurecido, aunque mucho más lento que el latón. Lleva registro del metraje impreso con materiales abrasivos y reemplaza la boquilla preventivamente (cada 3–10 kg de material según el grado de dureza del recubrimiento). Los atascos parciales son más frecuentes con fibra porque los fragmentos pueden acumularse en la zona de transición frío–caliente del hotend. Un cold pull con filamento de limpieza antes y después de cada sesión con compuestos prolonga significativamente la vida del conjunto hotend.

### Calibración de flujo y Pressure Advance en compuestos

Los filamentos con fibra tienen reología diferente al polímero base: la viscosidad aumenta y el flujo se vuelve menos predecible. La calibración de flujo con el método estándar suele arrojar valores de 105–115 % respecto al perfil del polímero base solo. Además, el **Pressure Advance** necesita recalibrarse desde cero porque la mayor viscosidad cambia la respuesta dinámica del extrusor. No reutilices perfiles del polímero base para los compuestos — calibra siempre de cero, incluso si es el mismo fabricante.

> 💡 **Nota técnica:** Las fibras en filamentos FDM son fibras **discontinuas** (cortas, típicamente 50–200 µm tras el proceso de extrusión del filamento). No confundir con sistemas de fibra continua como Markforged o Anisoprint, cuyas propiedades mecánicas son un orden de magnitud superiores. Los filamentos de fibra corta mejoran la rigidez y la relación rigidez/peso, pero no alcanzan las propiedades de los composites de fibra continua.

---

## También te puede interesar
- [PP — Ficha de Material](./pp.md)
- [PA (Nylon) — Ficha de Material](./pa-nylon.md)
- [Consejos de Impresión por Tipo de Material](../../consejos-de-impresion/por-tipo-de-material.md)
