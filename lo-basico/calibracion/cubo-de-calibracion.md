---
titulo: "Cubo de Calibración"
slug: "cubo-de-calibracion"
seccion: "lo-basico"
subseccion: "calibracion"
tipo: "conceptual"
ultima_revision: "2026-03-27"
version: "1.0"
estado: "terminado"
---

# Cubo de Calibración

> El test más rápido para verificar que tu impresora está imprimiendo con la geometría correcta.

---

## Para Principiantes

El cubo de calibración es el "hola mundo" de la impresión 3D: el primer test que imprime casi todo el mundo al estrenar una impresora o ajustar parámetros. Piénsalo como la página de prueba que imprime una impresora de papel antes del documento importante — en segundos te dice si los colores están bien antes de gastar tinta en algo que importa.

El cubo estándar mide 20×20×20 mm. Es pequeño, se imprime en 20 a 30 minutos con parámetros normales, y sus seis caras planas revelan de inmediato si algo no está bien. Cada cara tiene grabada una letra que corresponde a un eje de movimiento, así que no necesitas saber de mecánica para detectar un problema: solo miras la cara y comparas con lo que debería verse.

Lo mejor es que no requiere ninguna configuración especial. Se imprime con exactamente los mismos ajustes del perfil que quieres evaluar, y eso es precisamente su valor: te muestra cómo funciona tu impresora en condiciones reales.

---

## Todo lo que Necesitas Saber

### Qué es y de dónde viene

El cubo de calibración estándar es un modelo de libre acceso disponible en comunidades de impresión 3D como Printables o Thingiverse. Existen varias versiones publicadas por distintos usuarios, todas con la misma geometría base: un cubo de 20 mm con las letras X, Y y Z grabadas en las caras correspondientes a cada eje. No hay una versión "oficial" única — cualquier variante del cubo 20×20×20 sirve para el propósito. Lo puedes encontrar como **Handy Models** en tu slicer, o [descargarlo aquí](https://www.printables.com/model/109020-20-mm-xyz-calibration-cube-by-r3d).

### Cómo imprimirlo

Usa exactamente los mismos parámetros del perfil que quieres evaluar. La idea es replicar las condiciones reales de impresión, no crear condiciones ideales artificiales. Como referencia orientativa: 2 a 3 perímetros, sin soporte (el cubo no tiene voladizos), infill al 10% es suficiente para que las paredes queden firmes sin desperdiciar material.

### Tabla de lectura: qué te dice cada cara

[![Cubo de calibración XYZ 20mm](../../../assets/images/calibracion/cali-cube.webp)](https://www.printables.com/model/109020-20-mm-xyz-calibration-cube-by-r3d)

| Zona del cubo | Qué observar | Posible causa |
|---|---|---|
| Cara X (letra X grabada) | Dimensión incorrecta en ese eje | Pasos del motor X mal calibrados o tensión de correa |
| Cara Y (letra Y grabada) | Dimensión incorrecta en ese eje | Pasos del motor Y mal calibrados o tensión de correa |
| Cara Z (altura total) | Cubo más alto o más bajo de 20 mm | Pasos del eje Z mal configurados o altura de capa incorrecta |
| Esquinas inferiores | Despegue, warping o elefant foot | Nivelación de cama deficiente o primera capa mal configurada |
| Superficies de las caras | Textura irregular, líneas visibles, subextrusión | Temperatura, velocidad o retracción fuera de rango |

### Cómo medir el resultado

Con un **calibrador digital** (caliper) mides cada cara del cubo en su eje correspondiente. Un resultado de ±0.2 mm respecto a los 20 mm nominales es una tolerancia orientativa aceptable para impresión general — piezas funcionales de ajuste fino pueden requerir tolerancias más estrechas.

Mide en al menos dos puntos distintos de cada cara para detectar variaciones a lo largo de la pieza, no solo en el centro.

### Cuándo volver a imprimir el cubo

- Al cambiar de material (especialmente si cambias de familia: de PLA a PETG, por ejemplo)
- Después de ajustes mecánicos: tensión de correas, cambio de rodamientos, ajuste de guías
- Al actualizar firmware de la impresora
- Al cambiar boquilla o temperatura de trabajo habitual

---

## Para Expertos

### El Voron Design Cube

[![Voron Design Calibration Cube](../../../assets/images/calibracion/voron-cube.webp)](https://www.printables.com/model/758730-voron-design-calibration-cube/files)

El **Voron Design Cube** es una versión extendida del cubo de calibración desarrollada por el proyecto de código abierto Voron. A diferencia del cubo estándar, incluye geometrías adicionales que evalúan aspectos que el cubo 20×20 no cubre: voladizos (overhangs) escalonados a distintos ángulos, puentes (bridges) de longitud variable, y letras en relieve para evaluar resolución de detalles finos. Lo puedes encontrar como **Handy Models** en tu slicer, o [descargarlo aquí](https://www.printables.com/model/758730-voron-design-calibration-cube/files).

### Interpretación de puentes en el Voron Cube

Los puentes del Voron Cube son la herramienta más útil para diagnóstico de cooling. Un puente bien formado requiere que el material solidifique antes de caer por su propio peso: si el puente se hunde, el sistema de enfriamiento es insuficiente para ese material a esa velocidad. Si se forman capas irregulares en la transición puente-pared, el problema suele ser de flow rate o temperatura, no de cooling.

### Uso como test de regresión

Después de cualquier modificación mecánica — tensión de correas, ajuste de rodamientos lineales, cambio de boquilla, actualización de firmware de motores — imprime un cubo antes y uno después. Conserva ambos con una etiqueta de los parámetros relevantes. Un delta de más de 0.1 mm entre cubos consecutivos en condiciones idénticas justifica investigar la fuente de variabilidad antes de seguir imprimiendo piezas funcionales.

### Paso siguiente: metodología Orca

El cubo confirma que la geometría de la impresora es correcta, pero no calibra el comportamiento del filamento específico. Para eso, el flujo lógico es continuar con la [metodología Orca](metodologia-orca.md), que ajusta flow rate, presión de avance (pressure advance) y retracción para cada combinación de material y temperatura.

---

## También te puede interesar
- [El Benchy y Cómo Leerlo](benchy.md)
- [Metodología de Calibración — Orca Slicer](metodologia-orca.md)
- [Problemas Comunes de Impresión](../../consejos-de-impresion/problemas-comunes.md)
