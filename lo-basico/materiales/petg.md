---
titulo: "PETG — Ficha de Material"
slug: "petg"
seccion: "lo-basico"
subseccion: "materiales"
material: "PETG"
tipo: "material"
ultima_revision: "2026-03-22"
estado: "terminado"
version: "1.0"
---

# PETG — Ficha de Material

> Más fuerte que el PLA, más fácil que el ABS: el filamento de uso general para piezas que necesitan aguantar algo.

---

## Para Principiantes

El **PETG** es el hermano mayor del PLA: un poco más exigente a la hora de imprimir, pero mucho más capaz cuando necesitas piezas que aguanten golpes, humedad o algo de calor. Su nombre completo es polietileno tereftalato glicol — básicamente la misma familia de plástico que se usa en las botellas de agua y gaseosas, solo que modificado para que sea más fácil de imprimir en FDM.

Si ya tienes algo de experiencia con PLA y quieres un filamento que resista mejor en el mundo real, el PETG es el paso natural. No necesita cámara cerrada, no emite gases peligrosos y los resultados son semitransparentes y brillantes — ideales cuando quieres piezas que también se vean bien.

Piénsalo como una versión más resistente del PLA: necesita un poco más de atención durante la impresión, pero las piezas terminadas aguantan mejor si van a la cocina, al aire libre o en un proyecto que necesite resistir impactos cotidianos. El [FiLL-3D PETG](https://www.fill-3d.com/tienda/) combina esta resistencia con la calidad de fabricación colombiana y garantía 100 %.

---

## Todo lo que Necesitas Saber

### Características del material

El PETG combina buena **resistencia mecánica**, mayor flexibilidad que el PLA y una **resistencia al calor** superior (~80 °C bajo carga ligera). Es semitransparente en su estado natural, lo que lo hace popular para protectores, difusores de luz y envases. Resiste bien la humedad ambiental y es generalmente considerado seguro para contacto con alimentos, aunque esto depende del colorante específico y de las condiciones de impresión.

### Parámetros de impresión recomendados — FiLL-3D PETG

| Parámetro | Valor recomendado | Notas |
|---|---|---|
| Temperatura de boquilla | 230–250 °C | Empezar por 240 °C |
| Temperatura de cama | 70–85 °C | Cama caliente obligatoria |
| Velocidad de impresión | 40–70 mm/s | Más lento mejora acabado y reduce stringing |
| Enfriamiento | 30–60 % | Menos que PLA; enfriamiento excesivo reduce adhesión entre capas |
| Retracción (bowden) | 3–5 mm a 40 mm/s | PETG es sensible — demasiada retracción genera grinding |
| Retracción (direct drive) | 0.5–1.5 mm a 30 mm/s | |
| Flujo (flow) | 95–100 % | |

### Aplicaciones ideales

- Soportes y brackets mecánicos de interior
- Piezas en contacto con humedad o líquidos
- Protectores y carcasas para electrónica
- Difusores de luz (por su semitransparencia natural)
- Accesorios de cocina (verificar compatibilidad del colorante)
- Componentes de impresoras 3D (extrusor, ductos de ventilación)

### Ventajas y limitaciones

| Ventajas | Limitaciones |
|---|---|
| Mayor resistencia al impacto que PLA | Propenso a stringing si no se calibra bien |
| Buena resistencia a la humedad | No apto para altas temperaturas (>80 °C bajo carga) |
| Acabado semitransparente y brillante | Puede pegarse demasiado fuerte a superficies PEI |
| No requiere cámara cerrada | Bridging más difícil que con PLA |
| Resistente a la mayoría de solventes débiles | Absorbe algo de humedad — secar antes de imprimir |

### Almacenamiento

El PETG es moderadamente higroscópico. La humedad se manifiesta como burbujas, acabado opaco y capas débiles. Guárdalo sellado con sílica gel, a menos de 45 % de humedad relativa. Si notas degradación en la calidad, seca el rollo a **65 °C durante 4–6 horas** antes de volver a imprimir.

---

## Para Expertos

### Control del stringing: temperatura y retracción en equilibrio

El PETG tiene una ventana de fusión amplia pero es muy sensible al balance temperatura–retracción. Bajar la temperatura mejora el stringing, pero a costa de la adhesión intercapa. El enfoque correcto es fijar la temperatura en el rango óptimo (240–245 °C para la mayoría de configuraciones) y luego ajustar retracción y Z-hop para los viajes en vacío. Activar "wipe on move" y "coast at end" en el slicer reduce significativamente los hilos sin necesidad de tocar la temperatura.

### Adhesión a la cama: el problema de que pega demasiado

Al contrario del PLA, el PETG puede adherirse tan fuerte a las láminas PEI que las daña al despegar. La solución no es bajar la temperatura de cama, sino aplicar una capa muy fina de barra adhesiva (tipo Pritt) sobre el PEI antes de imprimir. Esto actúa como separador y protege la lámina. Alternativamente, láminas PEI texturadas a 80–85 °C ofrecen buena adhesión sin el problema del sobrepegado típico de las láminas lisas.

### Adhesión intercapa y orientación de la pieza

El PETG tiene adhesión intercapa excelente cuando se imprime con suficiente temperatura y flujo, pero es muy anisotrópico: la resistencia en Z puede ser un 40–60 % menor que en XY. Para piezas mecánicas críticas, la orientación de impresión es tan importante como el material elegido. Reduce el enfriamiento al 30–40 % en capas largas y aumenta el overlap de perímetros con el infill al 30 % para maximizar la cohesión entre capas.

> 💡 **Nota técnica:** El PETG tiene una Tg de ~80 °C y una temperatura de fusión de ~250 °C. Su mayor elongación a la rotura (~50 %) respecto al PLA (~6 %) lo hace significativamente más tenaz bajo carga dinámica — útil cuando la pieza puede recibir impactos o flexiones repetidas.

---

## También te puede interesar
- [PLA — Ficha de Material](./pla.md)
- [PA (Nylon) — Ficha de Material](./pa-nylon.md)
- [Consejos de Impresión por Tipo de Material](../../consejos-de-impresion/por-tipo-de-material.md)
