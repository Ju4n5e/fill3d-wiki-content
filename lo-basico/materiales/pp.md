---
titulo: "PP — Ficha de Material"
slug: "pp"
seccion: "lo-basico"
subseccion: "materiales"
material: "PP"
tipo: "material"
ultima_revision: "2026-03-23"
estado: "terminado"
version: "1.0"
---

# PP — Ficha de Material

> Liviano, químicamente resistente y casi indestructible por fatiga cíclica: el material técnico para las aplicaciones más exigentes.

---

## Para Principiantes

El **PP** (polipropileno) es uno de los plásticos más usados en el mundo industrial — lo encuentras en envases de alimentos, piezas de carros, contenedores de laboratorio y artículos de uso médico. En impresión 3D es un material técnico avanzado que ofrece propiedades únicas: es muy liviano, resiste casi todos los químicos, aguanta doblarse miles de veces sin romperse (por eso lo usas en tapas con bisagras de película) y tiene resistencia excepcional a la fatiga.

La mala noticia es que el PP es famoso por ser uno de los materiales más difíciles de imprimir en FDM. Su mayor reto no es la temperatura sino la adhesión: el PP es tan poco reactivo químicamente que casi nada se le pega bien. Necesitas superficies o adhesivos especiales y una calibración cuidadosa para que la primera capa quede bien adherida.

Si ya tienes experiencia con PA o PETG y necesitas piezas que resistan químicos, sean muy livianas o requieran flexión cíclica prolongada, el [FiLL-3D PP](https://www.fill-3d.com/tienda/) es tu material.

---

## Todo lo que Necesitas Saber

### Características del material

El PP es un polímero **semicristalino** con densidad muy baja (~0.93 g/cm³ — flota en agua), excelente **resistencia química** a ácidos, bases y la mayoría de solventes orgánicos, y una resistencia única a la **fatiga por flexión cíclica**: puede doblarse decenas de miles de veces en el mismo punto sin romperse. Su temperatura de servicio llega a ~100–110 °C bajo carga ligera.

### Parámetros de impresión recomendados — FiLL-3D PP

| Parámetro | Valor recomendado | Notas |
|---|---|---|
| Temperatura de boquilla | 240 °C | Estricto; ±5 °C afecta el flujo significativamente |
| Temperatura de cama | 100 °C | Placa de ingeniería; o sin calefacción con adhesivo específico para PP |
| Velocidad de impresión | 50-100 mm/s | Lento para minimizar warping |
| Enfriamiento | 0 % (primeras 5 capas); luego 20–30 % máx | Material muy sensible al enfriamiento rápido |
| Retracción | 0.2 mm @ 40 mm/s | Pressure Advance K=0.085 |
| Flujo (flow) | 100–105 %  |Calibrar con tu setup específico |
| Cámara cerrada | Muy recomendada | El PP tiene warping severo en piezas grandes |

### Aplicaciones ideales

- Contenedores para alimentos o reactivos químicos
- Piezas con bisagra de película (living hinges)
- Componentes automotrices y de maquinaria ligera
- Equipos de laboratorio y uso médico
- Piezas que requieren resistencia al vapor
- Prototipos de envases de consumo masivo

### Ventajas y limitaciones

| Ventajas | Limitaciones |
|---|---|
| Resistencia química excepcional | Adhesión a cama muy difícil sin preparación especial |
| Liviano (densidad ~0.9 g/cm³) | Warping severo, especialmente en piezas planas y largas |
| Resistencia única a fatiga por flexión cíclica | Requiere superficies o adhesivos específicos para PP |
| Resistente al vapor y la humedad | Baja adhesión intercapa vs PLA o PETG |
| Temperatura de servicio moderada (~100 °C) | Poca compatibilidad con soportes de impresión estándar |

### Almacenamiento

El PP tiene baja absorción de humedad en comparación con PA o PETG — es naturalmente hidrófugo. Sin embargo, el polvo y la contaminación superficial afectan la adhesión entre capas. Guárdalo en bolsa sellada para protegerlo de suciedad. Si ha estado expuesto al ambiente durante meses, un secado a **60 °C por 4 horas** mejora la consistencia de la impresión.

---

## Para Expertos

### Adhesión a la cama: qué funciona y qué no

El PP es químicamente inerte frente a casi todos los adhesivos estándar (PVA, hairspray). Las estrategias que funcionan son: (1) lámina de PP reciclado o coroplast (cartón de polipropileno) pegada a la cama caliente — el PP adhiere al PP; (2) cinta de empacar de PP transparente aplicada sobre la cama a 100–110 °C; (3) adhesivos específicos para poliolefinas como Magigoo PP. En cualquier caso, la cama debe estar perfectamente nivelada, y la primera capa debe imprimirse más lenta (15–20 mm/s) y con altura ligeramente mayor a lo habitual (+15–20 %) para maximizar el área de contacto.

### Control del warping: geometría y parametrización

El PP tiene un alto coeficiente de contracción térmica (~1.5–2.0 %) comparado con el PLA (~0.3 %). Esto genera tensiones internas que se manifiestan como warping severo, especialmente en piezas planas o largas. Las estrategias más efectivas son: cámara cerrada con temperatura ambiental de al menos 40–50 °C, brim ancho de 10–15 mm, evitar cambios bruscos de sección, y dividir piezas grandes en componentes más pequeños para ensamblar después. Paradójicamente, aumentar el infill al 30–40 % puede reducir el warping porque distribuye mejor las tensiones internas.

### Bisagras de película: parámetros críticos

El PP es el único material FDM que permite bisagras de película (living hinges) realmente funcionales gracias a su excepcional resistencia a la fatiga. Para que funcionen: el grosor de la bisagra debe estar entre 0.4–0.8 mm, las capas deben ser paralelas a la dirección de flexión (la bisagra queda horizontal respecto a la cama), y la zona de bisagra debe tener 1–2 perímetros sin infill. Inmediatamente después de imprimir, dobla la bisagra varias veces mientras aún está caliente para orientar las cadenas poliméricas en la dirección de flexión — esto mejora notablemente la vida útil.

> 💡 **Nota técnica:** La estructura semicristalina del PP le da un comportamiento mecánico complejo: tiene una Tg por debajo de la temperatura ambiente (~−10 °C), lo que significa que a temperatura de uso el PP ya está en estado viscoelástico — de ahí su flexibilidad y resistencia a la fatiga. A temperaturas bajo cero puede volverse frágil; considera esto para aplicaciones de exterior en climas fríos.

---

## También te puede interesar
- [PA (Nylon) — Ficha de Material](./pa-nylon.md)
- [Fibras Aditivas — Ficha de Material](./fibras-aditivas.md)
- [Consejos de Impresión por Tipo de Material](../../consejos-de-impresion/por-tipo-de-material.md)
