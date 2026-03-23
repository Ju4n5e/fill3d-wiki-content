---
titulo: "PA (Nylon) — Ficha de Material"
slug: "pa-nylon"
seccion: "lo-basico"
subseccion: "materiales"
material: "PA"
tipo: "material"
ultima_revision: "2026-03-23"
estado: "terminado"
version: "1.0"
---

# PA (Nylon) — Ficha de Material

> Fuerte, flexible y resistente al desgaste: el material cuando necesitas piezas que trabajen de verdad.

---

## Para Principiantes

El **PA** (poliamida, más conocido como Nylon) es el material de impresión 3D para cuando las piezas necesitan trabajar de verdad. Es flexible sin romperse, aguanta el golpe, resiste el desgaste y soporta temperaturas más altas que el PLA o el PETG. Por eso se usa en engranajes, bisagras, guías, clips y cualquier pieza que necesite moverse, flexarse o aguantar fricción repetida.

La contrapartida es que el Nylon es más exigente a la hora de imprimir: necesita temperaturas altas, cama caliente y, sobre todo, estar completamente seco antes de entrar a la impresora. Si alguna vez escuchaste un "pop pop pop" mientras imprimes, casi con certeza es humedad en el filamento, y con el PA ese problema se multiplica.

Si vienes del PLA, el salto al PA es significativo pero vale la pena cuando el proyecto lo exige. Empieza con piezas pequeñas para calibrar tu configuración antes de lanzarte a impresiones largas. El [FiLL-3D PA](https://www.fill-3d.com/tienda/) está fabricado con los mismos estándares de calidad del resto de la línea.

---

## Todo lo que Necesitas Saber

### Características del material

El PA es un polímero **semicristalino** con excelentes propiedades mecánicas: alta **resistencia al impacto**, buena **resistencia a la fatiga** y muy bajo coeficiente de fricción superficial — ideal para piezas en contacto y movimiento. Existen varios tipos; el **PA12** es el más común en filamentos FDM por su menor absorción de humedad y menor warping versus el PA6. ⚠️ verificar qué tipo específico es el FiLL-3D PA.

### Parámetros de impresión recomendados — FiLL-3D PA

| Parámetro | Valor recomendado | Notas |
|---|---|---|
| Temperatura de boquilla | 275 °C | Estricto; ±5 °C afecta el flujo significativamente |
| Temperatura de cama | 100 °C | Cama caliente obligatoria; minimiza contracción térmica |
| Velocidad de impresión | 30–50 mm/s | Lento mejora adhesión intercapa |
| Enfriamiento | 0 % (primeras 10 capas); rampa gradual a 10–50 % | Sin ventilador en capas iniciales; crítico para adhesión entre capas |
| Retracción | 2 mm @ 40 mm/s | Pressure Advance K=0.038 |
| Flujo (flow) | 100–105 %  | |
| Cámara cerrada | Recomendada | Reduce warping en piezas grandes |

### Aplicaciones ideales

- Engranajes y piezas de transmisión mecánica
- Bisagras y clips funcionales de ciclo repetido
- Guías, rodillos y piezas con movimiento continuo
- Piezas expuestas a fricción prolongada
- Accesorios industriales y de maquinaria ligera
- Prototipos funcionales de alta resistencia

### Ventajas y limitaciones

| Ventajas | Limitaciones |
|---|---|
| Alta resistencia al impacto y a la fatiga | Muy higroscópico — requiere secado previo estricto |
| Bajo coeficiente de fricción superficial | Warping significativo en piezas grandes |
| Buena resistencia química | Requiere altas temperaturas de boquilla y cama |
| Flexible sin quebrarse | Adhesión a la cama más difícil que PLA o PETG |
| Resistente al desgaste mecánico | Cámara cerrada recomendada |

### Almacenamiento

El PA es **altamente higroscópico** — puede absorber humedad del aire en pocas horas de exposición. La humedad destruye la calidad de impresión: genera burbujas, reduce la resistencia mecánica hasta un 30 % y hace imposible imprimir sin popping audible. **Regla de oro:** nunca imprimas PA sin haberlo secado recientemente. Seca a **80 °C durante 6–12 horas** antes de cada sesión y usa un sistema de alimentación sellado (dry box) durante la impresión. Guarda siempre en bolsa hermética con abundante sílica gel.

---

## Para Expertos

### Secado: temperatura, tiempo y método importan

El secado del PA no es opcional ni aproximado. El PA6 requiere 80–85 °C por 8–12 horas para eliminar la humedad absorbida; el PA12 es algo más tolerante (70–80 °C por 6–8 horas). Un deshidratador de alimentos con control preciso de temperatura es superior a un horno doméstico porque mantiene temperatura uniforme sin ciclos. Una forma de verificar que el filamento está seco es pesarlo antes y después del secado: una pérdida de 0.5–2 % del peso indica humedad eliminada. El protocolo oficial para el **FiLL-3D PA** es **85–95 °C por 12 horas**; si se usa menor temperatura, extender el tiempo proporcionalmente. Guardar en bolsa sellada con desecante después de secar.

### Adhesión a la cama: estrategias que funcionan

El PA no adhiere bien sobre PEI liso. Las opciones más efectivas son: (1) lámina de PA como superficie de cama — el PA adhiere al PA; (2) pegamento PVA (barra Pritt) sobre vidrio o PEI a 80–100 °C; (3) cinta Kapton con adhesivo de contacto para PA. Evita el glue stick directamente sobre PEI a alta temperatura de cama, ya que puede dañar la lámina. Imprimir la primera capa 10 °C por encima de la temperatura del resto del modelo mejora significativamente la adherencia inicial.

### Annealing para estabilidad dimensional y resistencia

Las piezas de PA impresas en FDM acumulan tensiones internas que pueden liberar con el tiempo y causar deformación. El recocido (annealing) a 80 °C por 2–4 horas en horno —dentro de arena o sal para mantener la forma— elimina estas tensiones, aumenta la cristalinidad del material y puede mejorar la resistencia a la tracción hasta un 20 %. El proceso genera algo de contracción (~0.5–1.5 % según geometría), por lo que si las tolerancias son críticas hay que compensarlo en el diseño o calibrar con una pieza de prueba primero.

> 💡 **Nota técnica:** La absorción de humedad del PA en equilibrio con el ambiente (típicamente 2–8 % en peso para PA6, 1–3 % para PA12) actúa como plastificante: reduce la Tg y la rigidez pero aumenta la tenacidad y la elongación a la rotura. El PA "húmedo" puede ser útil para piezas que requieren flexibilidad extra, pero siempre a costa de resistencia estructural.

---

## También te puede interesar
- [PETG — Ficha de Material](./petg.md)
- [PP — Ficha de Material](./pp.md)
- [Consejos de Impresión por Tipo de Material](../../consejos-de-impresion/por-tipo-de-material.md)
