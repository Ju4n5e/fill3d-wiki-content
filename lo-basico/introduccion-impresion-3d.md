---
titulo: "Introducción a la Impresión 3D"
slug: "introduccion-impresion-3d"
seccion: "lo-basico"
subseccion: ""
material: ""
tipo: "conceptual"
ultima_revision: "2026-03-22"
estado: "terminado"
version: "1.0"
---

# Introducción a la Impresión 3D

> Entiende qué es la impresión 3D FDM, cómo funciona y por qué se convirtió en la tecnología favorita de makers, ingenieros y creativos.

---

## Para Principiantes

Imagina una pistola de silicona que, en lugar de pegamento, deposita plástico derretido — capa por capa — hasta construir un objeto tridimensional desde cero. Eso, en esencia, es la impresión 3D por filamento.

El proceso se llama **FDM** (Fused Deposition Modeling, o Modelado por Deposición Fundida). La impresora toma un filamento de plástico, lo derrite en una boquilla caliente y lo deposita con precisión sobre una superficie plana llamada cama. Cada capa se enfría y solidifica antes de que la siguiente sea añadida, hasta que el objeto queda completo.

Lo que hace especial a la impresión 3D FDM es que puedes fabricar casi cualquier forma que puedas diseñar en un computador — sin moldes, sin herramientas especiales, sin fábrica. Desde una figura decorativa hasta una pieza de repuesto para un electrodoméstico o un prototipo funcional: si lo puedes modelar, lo puedes imprimir.

---

## Todo lo que Necesitas Saber

### ¿Cómo funciona el proceso?

El flujo completo de una impresión tiene tres etapas:

1. **Modelo 3D:** El punto de partida es un archivo digital del objeto que quieres imprimir, generalmente en formato `.STL` o `.3MF`. Puedes diseñarlo tú mismo o descargarlo de plataformas como Printables o Thingiverse.
2. **Slicer:** Un software especializado convierte el modelo en instrucciones que la impresora entiende — el llamado **G-code**. Aquí defines parámetros como temperatura, velocidad, relleno (infill) y soportes.
3. **Impresión:** La impresora ejecuta el G-code capa por capa. La boquilla funde el filamento a temperatura controlada y lo deposita sobre la cama con movimientos precisos en los ejes X, Y y Z.


### Tipos de configuración de impresora

Las impresoras FDM se diferencian principalmente por cómo mueven sus ejes:

| Configuración | Cómo funciona | Características |
|---|---|---|
| **Cartesiana ("bed slinger")** | La cama se mueve en Y; el cabezal en X y Z | La más común y económica; buena para principiantes |
| **CoreXY** | Dos motores sincronizan X e Y mediante correas; la cama solo baja en Z | Mayor velocidad y estabilidad; ideal para impresión avanzada |
| **Delta** | Tres brazos triangulares posicionan el cabezal | Alta velocidad, menor huella lateral; configuración más compleja |

### Extrusores: directo vs. Bowden

El extrusor es el sistema que empuja el filamento hacia la boquilla. Existen dos tipos:

- **Directo:** El motor está montado directamente sobre el cabezal de impresión. Ofrece mejor control, es más tolerante con materiales flexibles y requiere menos ajuste de retracción. Es el estándar en la mayoría de impresoras modernas.
- **Bowden:** El motor está separado del cabezal y empuja el filamento a través de un tubo de PTFE. El cabezal pesa menos y puede moverse más rápido, pero la mayor distancia entre motor y boquilla reduce el control sobre el flujo de material — lo que se traduce en mayor dificultad para calibrar la retracción, más riesgo de stringing, y limitaciones serias con filamentos blandos como el TPU.

### ¿Por qué FDM sobre otras tecnologías?

FDM es la tecnología dominante para uso doméstico y profesional ligero por razones prácticas:

- **Costo:** Tanto las impresoras como los materiales son más económicos que en tecnologías como SLA (resina).
- **Variedad de materiales:** PLA, PETG, ABS/ASA, TPU, Nylon y PP son algunos de los materiales más usados — cada uno con propiedades distintas de resistencia, flexibilidad y tolerancia al calor. Conoce más en [Materiales de Impresión 3D](./materiales-impresion-3d.md).
- **Seguridad y limpieza:** El material se trabaja en estado sólido de filamento — no hay polvos que inhalar ni químicos líquidos que requieran ventilación especial o equipo de protección, a diferencia de tecnologías como SLA (resinas fotopoliméricas) o SLS (polvos sinterizados). El post-procesado es mínimo.
- **Escalabilidad:** El mismo principio aplica desde impresoras de escritorio hasta máquinas industriales.

---

## Para Expertos

### Anisotropía mecánica y adhesión entre capas

La resistencia de una pieza FDM es fundamentalmente **anisótropa**: es significativamente mayor en el plano XY — el plano de cada capa individual — que en Z, la dirección en que las capas se apilan y se adhieren entre sí. La adhesión interlayer depende de la temperatura de la capa anterior en el momento de deposición, la viscosidad del fundido y el porcentaje de solapamiento entre líneas (line width vs. extrusion width).

> 💡 **Tip:** Incrementar la temperatura de impresión en 5–10 °C mejora la adhesión interlayer pero puede degradar la superficie y activar stringing; el balance óptimo es específico para cada material.

### Resonancias y compensación de vibraciones

En configuraciones CoreXY a alta velocidad (>150 mm/s), las inercias del cabezal generan vibraciones que producen artefactos visuales conocidos como **ringing** o ghosting. Los firmwares modernos (Klipper, Marlin 2.x) implementan **Input Shaping** para mitigar este efecto sin sacrificar velocidad. La frecuencia de resonancia debe medirse, no estimarse — dependiendo de la impresora el proceso puede ser automático, o puede realizarse manualmente con herramientas de calibración como la que incluye Orca Slicer.

### Pressure Advance y control de caudal

La presión dentro del hotend no es instantánea: existe un retraso entre el movimiento del extrusor y la extrusión real del material, especialmente en cambios bruscos de velocidad. Piénsalo así — cuando el cabezal frena antes de una esquina, el filamento dentro del hotend todavía está bajo presión y sigue fluyendo por inercia, generando un exceso de material en la esquina; al retomar velocidad ocurre lo contrario, la presión aún no se ha recuperado y la línea sale más delgada. **Pressure Advance** (Klipper) o **Linear Advance** (Marlin) compensan este fenómeno ajustando el caudal en función de la aceleración prevista. El factor K óptimo es específico para cada combinación de filamento, temperatura y caudal volumétrico máximo (mm³/s).

> 💡 **Nota técnica:** El caudal volumétrico máximo sostenido de un hotend estándar (40 W, boquilla 0.4 mm) ronda los 10–15 mm³/s. Los hotends de alto rendimiento (Volcano, Rapido HF, Dragon HF) pueden superar los 30 mm³/s — pero la temperatura de procesamiento del filamento se convierte en el cuello de botella antes que la mecánica.

---

## También te puede interesar
- [Materiales de Impresión 3D](./materiales-impresion-3d.md)
- [Impresoras 3D](./impresoras-3d.md)
- [Slicers (Laminadores)](./slicers.md) <!-- ⚠️ página pendiente de crear -->
