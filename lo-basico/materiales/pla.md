---
titulo: "PLA — Ficha de Material"
slug: "pla"
seccion: "lo-basico"
subseccion: "materiales"
material: "PLA"
tipo: "material"
ultima_revision: "2026-03-23"
estado: "terminado"
version: "1.0"
---

# PLA — Ficha de Material

> El material más popular de la impresión 3D: fácil de imprimir, versátil y disponible en docenas de colores.

---

## Para Principiantes

El **PLA** (ácido poliláctico) es el punto de entrada de casi todo el mundo a la impresión 3D, y con razón: es el filamento más fácil de usar, el más accesible y el que perdona más los errores. Se fabrica a partir de almidón de maíz o caña de azúcar, lo que lo hace biodegradable en condiciones industriales.

Si acabas de comprar tu impresora o tu primer rollo, empieza aquí. El PLA no necesita una cama muy caliente, no emite gases peligrosos y casi no tiene warping. Puedes imprimirlo en un cuarto sin ventilación especial y obtener resultados bonitos desde los primeros intentos.

Piénsalo como la arcilla de modelar del mundo digital: fácil de trabajar, disponible en muchos colores y perfecta para aprender sin complicaciones. El [FiLL-3D PLA](https://www.fill-3d.com/tienda/) viene en una amplia gama de colores vibrantes, fabricado en Colombia con altos estándares de calidad y con garantía 100 % incluso si ya usaste parte del rollo.

---

## Todo lo que Necesitas Saber

### Características del material

El PLA es un polímero **semicristalino** de origen vegetal con buenas propiedades mecánicas para uso general. Es rígido, tiene buena resolución de detalle y acepta bien el pintado y lijado. Su principal limitación es la temperatura: empieza a deformarse por encima de los 55–60 °C, lo que lo hace inadecuado para piezas que van dentro de un carro o en exteriores bajo el sol.

### Parámetros de impresión recomendados — FiLL-3D PLA

| Parámetro | Valor recomendado | Notas |
|---|---|---|
| Temperatura de boquilla | 200–220 °C | Empezar por 210 °C y ajustar |
| Temperatura de cama | 25–60 °C | Sin cama caliente también funciona |
| Velocidad de impresión | 40–80 mm/s | Velocidades más altas requieren más temperatura |
| Enfriamiento | 100 % | El PLA agradece el enfriamiento máximo |
| Retracción (bowden) | 1–2 mm a 45 mm/s | |
| Retracción (direct drive) | 0.2–0.5 mm a 35 mm/s | |
| Flujo (flow) | 95–100 % | Calibrar con tu setup específico |

### PLA Turbo — Alta velocidad

El [PLA Turbo](https://www.fill-3d.com/tienda/) es la variante de alta velocidad de FiLL-3D, formulada para impresoras con sistemas de movimiento rápido como CoreXY. Mantiene las ventajas del PLA estándar pero está optimizado para velocidades superiores sin sacrificar adhesión entre capas ni detalle superficial.

| Parámetro | Valor recomendado | Notas |
|---|---|---|
| Temperatura de boquilla | 220–240 °C | Mayor temperatura para mayor caudal; flujo <20 mm³/s: 220 °C, 20–30: 225 °C, 30–40: 230 °C, >40: 235–240 °C |
| Temperatura de cama | 35–60 °C | |
| Velocidad de impresión | 150–500 mm/s | Según capacidad de la impresora |
| Enfriamiento | 100 % | |
| Retracción | 0.1 mm @ 55 mm/s | Pressure Advance K=0.018; Adaptive Pressure Advance activado |
| Flujo (flow) | 98% | Calibrar con tu setup específico |

> El PLA Turbo se beneficia especialmente de boquillas de 0.6 mm o más cuando se imprimen capas gruesas a alta velocidad.

### Aplicaciones ideales

- Prototipos y modelos conceptuales
- Figuras decorativas, miniaturas y arte
- Piezas funcionales de interior (baja carga mecánica y térmica)
- Accesorios para el hogar y la oficina
- Proyectos educativos y de aprendizaje
- Modelos arquitectónicos y maquetas

### Ventajas y limitaciones

| Ventajas | Limitaciones |
|---|---|
| Fácil de imprimir, muy poco warping | Baja resistencia al calor (~55–60 °C) |
| No requiere cama muy caliente | Frágil bajo impacto; poca flexibilidad |
| Gran variedad de colores | No apto para exteriores bajo el sol |
| Origen vegetal, biodegradable | Absorbe humedad con el tiempo |
| Bajo costo y amplia disponibilidad | No resiste solventes comunes |

### Almacenamiento

El PLA es moderadamente higroscópico. La humedad afecta el acabado superficial (burbujas, bajo brillo) y puede generar popping durante la impresión. Guárdalo en bolsa sellada con sílica gel, idealmente a menos de 40 % de humedad relativa. Si llevas varios meses sin usarlo, seca el rollo a **45 °C durante 4–6 horas** antes de imprimir.

---

## Para Expertos

### Temperatura como función del caudal

La temperatura de boquilla no es un valor fijo: es una función del caudal de material. A mayor velocidad de impresión, necesitas más temperatura para mantener la viscosidad óptima del fundido. La práctica correcta es correr una torre de temperatura (195–225 °C en pasos de 5 °C) a la velocidad real de impresión, no a velocidad de calibración. Para el PLA Turbo en impresoras CoreXY por encima de 200 mm/s, los valores óptimos suelen estar 10–15 °C más arriba que los del PLA estándar.

### Pressure Advance y calidad de esquinas

El PLA responde especialmente bien a la calibración de **Pressure Advance** (Klipper) o **Linear Advance** (Marlin). Valores típicos con direct drive oscilan entre 0.03–0.07; con bowden pueden llegar a 0.5–0.8. El PLA Turbo, al tener mayor fluidez, tiende a necesitar valores más bajos para la misma configuración mecánica. Calibrar esto elimina las esquinas redondeadas y los excesos de material en arranques y paradas.

### Adhesión a cama en piezas grandes

Aunque el PLA tiene poco warping, las piezas con mucha área de base pueden despegarse si la cama no tiene buena adhesión. En lugar de elevar indefinidamente la temperatura de cama (lo que puede ablandar las capas inferiores ya depositadas), usa una lámina PEI texturizada limpiada con IPA antes de cada sesión. Para piezas críticas, un brim de 5–8 mm elimina el problema sin modificar parámetros de temperatura.

> 💡 **Nota técnica:** El PLA tiene una temperatura de transición vítrea (Tg) de ~55–60 °C, pero bajo carga sostenida puede deformarse desde los 45 °C. Para piezas funcionales con requisitos térmicos moderados, el PETG es la alternativa directa más recomendada.

---

## También te puede interesar
- [Materiales de Impresión 3D](../materiales-impresion-3d.md)
- [PETG — Ficha de Material](./petg.md)
- [Consejos de Impresión por Tipo de Material](../../consejos-de-impresion/por-tipo-de-material.md)
