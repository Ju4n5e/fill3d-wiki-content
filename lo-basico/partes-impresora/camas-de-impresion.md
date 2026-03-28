---
titulo: "Camas de Impresión"
slug: "camas-de-impresion"
seccion: "lo-basico"
subseccion: "partes-impresora"
material: ""
tipo: "conceptual"
ultima_revision: "2026-03-22"
estado: "terminado"
version: "1.0"
---

# Camas de Impresión

> La cama determina si tu primera capa se adhiere o se despega: conocer los tipos te ahorra frustraciones y filamento desperdiciado.

---

## Para Principiantes

La **cama de impresión** —o placa de construcción— es la superficie sobre la que se construye tu pieza capa a capa. La primera capa es crítica: si no se adhiere bien, todo lo demás sale mal. Si se adhiere demasiado, la pieza puede romperse al intentar retirarla.

Las primeras impresoras usaban vidrio o acrílico; hoy la gran mayoría viene con superficies de **PEI** (poliéterimida), un material que tiene la propiedad casi mágica de agarrar bien el filamento mientras está caliente y soltarlo fácilmente al enfriarse. Muchas camas modernas son magnéticas y flexibles: las doblas un poco y la pieza se separa sola, sin rascar ni forzar nada.

El tipo de placa también afecta la textura del fondo de tu pieza: una superficie lisa da un acabado brillante tipo espejo, mientras que una superficie texturizada deja un patrón mate que a muchos usuarios les gusta tanto que ni lijan la pieza. Saber qué tienes y cómo cuidarlo marca la diferencia entre imprimir con éxito y luchar con la máquina en cada proyecto.

---

## Todo lo que Necesitas Saber

### Tipos de cama y sus características

| Tipo | Temp. Máx. Recomendada | Adhesión | Acabado superficial | Mejor para |
|---|---|---|---|---|
| **Vidrio (borosilicato)** | 110 °C | Media (requiere adhesivo) | Liso y brillante | PLA con adhesivo, PETG con adhesivo |
| **PEI lisa** | 120 °C | Alta en caliente / suelta en frío | Muy liso, semi-brillante | PLA, ABS, TPU — uso general |
| **PEI texturizada** | 120 °C | Alta en caliente / suelta en frío | Mate con textura | PLA, PETG ⚠️, PA, uso general |
| **PEX (polietileno reticulado)** | 150 °C | Alta | Liso o texturizado | PETG, ABS, ASA, materiales de alta temperatura |
| **G10 / Garolita** | 150 °C+ | Muy alta con PA y PA-CF | Rugoso mate | PA (Nylon), composites, PC |
| **Placa flexible magnética** | 120 °C | Alta (con recubrimiento PEI) | Variable | Uso general; fácil desmoldeo |
| **Placa de ingeniería (Bambu Lab)** | 120 °C | Media-alta | Lisa | PP, PPCF, PC en impresoras compatibles |

⚠️ El PETG sobre PEI puede adherirse con tanta fuerza que dañe la superficie al retirar la pieza.

> Consulta siempre la recomendación puntual del fabricante de tu cama sobre compatibilidad de materiales.

### Innovaciones: placas flexibles magnéticas

Las placas flexibles de acero de resorte con recubrimiento PEI son hoy el estándar en impresoras modernas. La lámina imantada se adhiere a la cama calefactada y la placa superior se puede retirar fácilmente. Para desmoldar, la doblas ligeramente y la pieza se separa sin tools ni fuerza. La vida útil depende del cuidado: evita rascarlas con metal y limpia con alcohol isopropílico antes de cada impresión.

### Nivelación de cama

Una cama perfectamente nivelada —con distancia uniforme boquilla-superficie en todos los puntos— es tan importante como la superficie misma. Las impresoras modernas tienen **nivelación automática** (ABL: Automatic Bed Leveling) con sensores inductivos, de contacto o de cámara. Aun así, un offset Z mal ajustado arruina la primera capa: si la boquilla va demasiado alta el filamento no se aplana bien; si va demasiado baja raspa la superficie y tapona.

> 💡 **Tip:** Antes de comenzar a imprimir, limpia bien la boquilla y verifica que no tenga material adherido. Una boquilla limpia permite una rutina de calibración más precisa al iniciar la impresora.

### Mantenimiento básico de la cama

- **Limpieza regular:** Limpia con alcohol isopropílico al 70–90% antes de cada impresión para eliminar grasa de los dedos (que destruye la adhesión).
- **Si persisten problemas de adhesión:** Lavar con agua tibia, jabón de loza y esponja suave.
  - ⚠️ No utilizar esponjas abrasivas pues pueden dañar la superficie.
- **No toques la superficie con los dedos:** Los aceites de la piel crean zonas de mala adhesión.
- **Almacenamiento:** Si retiras la placa, guárdala en un lugar limpio y sin presión que la deforme.

---

## Para Expertos

### El problema del PETG sobre PEI: cómo usar barra de pegante como desmoldante

El PETG tiene una afinidad química con el PEI que puede crear un vínculo casi permanente, especialmente a temperaturas altas o con piezas de gran área de contacto. La solución es aplicar una capa delgada y uniforme de barra de pegante sobre la PEI antes de imprimir. Esto crea una interfaz sacrificial que evita el contacto directo PETG-PEI. Retira la pieza en frío y lava la cama con agua tibia para regenerar la superficie. No uses más de lo necesario: un exceso deja marcas en el fondo de la pieza.

### PP y PPCF: adhesión es el desafío real

El polipropileno tiene una energía superficial extremadamente baja, lo que significa que casi nada se le pega —incluyendo las superficies de las camas de impresión convencionales. Las estrategias más efectivas son: (1) usar una placa de PP virgen como superficie (el PP se adhiere a sí mismo), (2) cinta de PP (la misma de embalaje), o (3) adhesivos especiales. La placa de ingeniería de Bambu Lab o la placa lisa PEI de Creality funcionan bien para PPCF.

### Temperatura real vs. temperatura configurada

El sensor de temperatura de la cama mide en el calefactor, no en la superficie de impresión. Dependiendo del diseño y del aislamiento de la cama, la superficie real puede estar 5–15 °C por debajo del valor configurado. Si imprimes PA a 100 °C configurados pero la superficie real está a 88 °C, el warping aumentará. Verifica con un termómetro de contacto o infrarrojo y ajusta el setpoint en consecuencia. Este diferencial es más pronunciado en camas grandes (300×300 mm o más) y en los bordes.

> 💡 **Nota técnica:** Las camas de aluminio mecanizado distribuyen el calor más uniformemente que las de acero, reduciendo el gradiente de temperatura entre el centro y las esquinas. Para piezas grandes con PA o PP, este factor puede ser la diferencia entre una pieza que termina y una que se despega a la mitad.

---

## También te puede interesar
- [Extrusores](../extrusores.md)
- [Boquillas](../boquillas.md)
- [Mantenimiento de la Impresora](../../mantenimiento/mantenimiento.md)