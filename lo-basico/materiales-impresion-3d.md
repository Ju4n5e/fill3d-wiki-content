---
titulo: "Materiales de Impresión 3D"
slug: "materiales-impresion-3d"
seccion: "lo-basico"
subseccion: ""
material: ""
tipo: "conceptual"
ultima_revision: "2026-03-22"
estado: "terminado"
version: "1.0"
---

# Materiales de Impresión 3D

> Entiende qué hace que un plástico sea imprimible y qué diferencia a cada material antes de elegir uno.

---

## Para Principiantes

Cuando imprimes en 3D por deposición de material fundido (FDM), el proceso es conceptualmente sencillo: un filamento plástico entra a un extremo caliente, se funde, se deposita capa por capa y vuelve a solidificarse. Pero no cualquier plástico funciona para esto. El material necesita fundirse a una temperatura manejable, fluir bien por una boquilla de menos de un milímetro, y solidificarse rápido sin deformarse ni agrietarse.

Entender mínimamente qué tipo de plástico estás usando te ayuda a configurar mejor tu impresora, elegir el material correcto para cada proyecto y resolver problemas cuando aparecen.

---

## Todo lo que Necesitas Saber

### ¿Qué hace que un material sea "imprimible"?

Para que un plástico sea útil en impresión FDM necesita cumplir tres condiciones:

- **Punto de fusión accesible:** entre ~150 °C y ~350 °C, rango alcanzable por hotends convencionales.
- **Viscosidad controlable:** al fundirse debe fluir lo suficiente para salir por la boquilla, pero no tan líquido que pierda forma al depositarse.
- **Solidificación predecible:** debe pasar de fundido a sólido de forma gradual y sin contraerse en exceso, lo que causaría warping o grietas entre capas.

### Termoplásticos vs. termoestables

Casi todos los filamentos de impresión 3D son **termoplásticos**: plásticos que se ablandan con calor y se endurecen al enfriarse, y este ciclo puede repetirse muchas veces sin degradación significativa. Esa característica los hace ideales para FDM.

Los **termoestables**, en cambio, endurecen por reacción química irreversible (como la resina epoxi o el poliuretano). Una vez curados no pueden volver a fundirse — por eso no se usan en filamento FDM, sino en tecnologías como SLA o resina UV.

| Propiedad | Termoplástico | Termoestable |
|---|---|---|
| ¿Se funde con calor? | Sí, reversible | No — curado irreversible |
| ¿Reciclable por refusión? | Sí | No |
| Tecnología FDM | ✅ Compatible | ❌ No aplica |
| Ejemplos | PLA, PETG, PA, PP | Resina epoxi, poliuretano |

### Amorfos vs. semicristalinos

Dentro de los termoplásticos hay una distinción clave que explica muchos comportamientos de impresión:

**Amorfos:** las cadenas poliméricas están desordenadas, sin estructura regular. Se ablandan progresivamente al subir la temperatura (no tienen un punto de fusión abrupto). Esto los hace más fáciles de imprimir y con mejor adhesión entre capas. El **PETG** es el ejemplo típico.

**Semicristalinos:** parte de las cadenas se organizan en regiones ordenadas (cristalitas). Al enfriarse, esa reorganización estructural genera una **contracción térmica mayor** que en los amorfos — el material encoge más mientras solidifica, lo que se traduce directamente en warping y tensiones internas en la pieza.

Esta contracción tiene dos consecuencias prácticas en impresión: la primera capa tiende a despegarse de la cama antes de que la pieza termine, y la adhesión entre capas se debilita porque cada nueva capa contrae sobre las ya depositadas.

Además, a diferencia del ablandamiento gradual de los amorfos, los semicristalinos tienen un punto de fusión más abrupto. La ventana de temperatura en la que el material fluye bien y se fusiona correctamente con la capa anterior es más estrecha — lo que hace más crítico el control térmico del hotend.

A cambio de estas dificultades, ofrecen mejor resistencia química y mecánica. **PA (Nylon)** y **PP** son los representantes típicos en impresión FDM.

El **PLA** ocupa un punto intermedio: técnicamente semicristalino, pero con cinética de cristalización tan lenta que en condiciones normales de impresión se comporta como amorfo.

| Material | Estructura | Imprimibilidad | Resistencia mecánica |
|---|---|---|---|
| PLA | Semi (lento) | ⭐⭐⭐⭐⭐ Muy fácil | Media |
| PETG | Amorfo | ⭐⭐⭐⭐ Fácil | Media-alta |
| PA (Nylon) | Semicristalino | ⭐⭐⭐ Moderada | Alta |
| PP | Semicristalino | ⭐⭐ Difícil | Alta + flexible |

### Los materiales disponibles

**[PLA](./materiales/pla.md)** es el punto de entrada al mundo FDM. Bajo punto de fusión, baja contracción, colores vibrantes. Ideal para prototipos, decoración y piezas de bajo estrés mecánico. Su **alta rigidez** también juega a favor: un filamento rígido transmite la fuerza del extrusor de forma directa y predecible, sin doblarse ni pandear dentro del tubo — lo que lo hace igual de fácil de manejar en extrusores directos y en configuraciones Bowden de tubo largo. Es el material más usado a nivel mundial y el más accesible para calibrar una impresora.

**[PETG](./materiales/petg.md)** combina la facilidad de impresión del PLA con mejor resistencia a temperatura y humedad. Al ser menos rígido que el PLA, absorbe mejor los golpes en lugar de fracturarse — lo que lo hace más resistente al impacto y la opción natural para piezas funcionales que van cerca de fuentes de calor o en contacto con líquidos.

**[PA — Nylon](./materiales/pa-nylon.md)** entra en escena cuando se necesita resistencia mecánica real: impacto, flexión cíclica, fricción. Es el material de los engranes, palancas y soportes funcionales. Requiere más cuidado en impresión y es altamente higroscópico — absorbe humedad del ambiente y eso afecta directamente la calidad.

**[PP — Polipropileno](./materiales/pp.md)** es uno de los plásticos más usados en industria y vida cotidiana (tapas de frascos, contenedores, piezas de auto), pero es de los más difíciles de imprimir bien por su alta contracción y baja adhesión. Cuando se logra, ofrece excelente resistencia química y una combinación única de rigidez con flexibilidad. Una forma de mejorar su imprimibilidad es añadir **fibra de carbono**, que actúa como estabilizador dimensional: las fibras restringen el movimiento de las cadenas poliméricas durante el enfriamiento, reducen la contracción y mejoran la fluidez del fundido — resultado: menos warping y una impresión más controlada. Ese es el principio detrás del [Fill3D PPCF](https://www.fill-3d.com/tienda/).

---

## Para Expertos

### Cristalización cinética y su efecto en la mesa de impresión

La velocidad de cristalización de un semicristalino determina cuánto warping verás en práctica. El PP tiene cristalización rápida y alta contracción volumétrica (~1.5–2.0 %), lo que lo hace problemático sin cama especializada (adhesivos de PP, superficie de vidrio con temperatura >80 °C o láminas de polipropileno espejado). El PA cristaliza más lento y su contracción (~0.8–1.2 %) es manejable con cama entre 70–90 °C y recinto cerrado. El PLA, aunque semicristalino, tiene Tg ~60 °C y cristalización tan lenta bajo condiciones FDM que la fase amorfa domina — de ahí su comportamiento predecible.

### Temperatura de transición vítrea (Tg) como límite operativo real

El límite de temperatura de servicio en termoplásticos amorfos y semicristalinos de baja cristalinidad lo define la **Tg**, no el punto de fusión. Para PLA la Tg es ~55–60 °C — las piezas bajo carga empiezan a deformarse bien por debajo del punto donde el filamento "se derrite". PETG tiene Tg ~80 °C, lo que explica su mejor desempeño cerca de fuentes de calor. PA y PP tienen mayor libertad porque la fase cristalina sostiene la pieza hasta temperaturas más altas que su Tg.

### Higroscopicidad y degradación hidrolítica

PA absorbe hasta 2.5–3.5 % en masa de agua a saturación ambiente, lo que baja viscosidad de fusión, genera vapor dentro del hotend (burbujas visibles, pops audibles) y reduce propiedades mecánicas de la pieza final. El PP es no-polar e inherentemente hidrófobo — ventaja técnica real en ambientes húmedos. Secar PA a 80 °C por 6–12 horas antes de imprimir no es opcional en climas tropicales como el de Colombia, donde la humedad relativa supera el 70 % buena parte del año.

### Compatibilidad con aditivos funcionales

La estructura del polímero base limita qué aditivos funcionan. Las fibras cortas de carbono o vidrio mejoran rigidez en amorfos y semicristalinos, pero en PP la baja adhesión interfacial fibra-matriz sin compatibilizador reduce la ganancia real. El **Fill3D PPCF** resuelve esto a nivel formulación — el compounding importa tanto como el aditivo.

> 💡 **Nota técnica:** El parámetro de solubilidad de Hildebrand predice miscibilidad entre polímeros y solventes de post-procesado. PETG (~20 MPa½) es compatible con acetona a baja concentración y cloruro de metileno; PLA (~20.2 MPa½) responde bien a acetato de etilo. PA y PP son prácticamente insolubles en solventes comunes a temperatura ambiente — sus opciones de alisado químico son muy limitadas.

---

## También te puede interesar
- [Introducción a la Impresión 3D](./introduccion-impresion-3d.md)
- [Slicers (Laminadores)](./slicers.md)
- [Comparativa de Materiales](../consejos-de-impresion/por-tipo-de-material.md)

---

## Diámetros: 1.75 mm vs 2.85 mm — ¿cuál usa tu impresora?

Antes de comprar filamento, verifica el diámetro que usa tu impresora — no son intercambiables:

| Diámetro | Quién lo usa | Notas |
|---|---|---|
| **1.75 mm** | La gran mayoría de impresoras de escritorio actuales: Creality (Ender, K1), Bambu Lab, Anycubic, Elegoo, Prusa, Artillery… | Es el estándar del mercado y el diámetro de **todo el catálogo Fill3D** |
| **2.85 mm** (a veces llamado "3 mm") | Ultimaker, algunas BCN3D, LulzBot y modelos antiguos | Cada vez menos común en escritorio |

Si tu impresora es de 2.85 mm, escríbenos por WhatsApp antes de comprar y te confirmamos disponibilidad — nuestro catálogo activo es 1.75 mm. ¿No sabes cuál usa la tuya? Busca el modelo en [¿Sirve para mi impresora?](../consejos-de-impresion/perfiles-por-impresora.md) o revisa la especificación del fabricante.
