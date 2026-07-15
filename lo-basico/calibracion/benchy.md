---
titulo: "El Benchy y Cómo Leerlo"
slug: "benchy"
seccion: "lo-basico"
subseccion: "calibracion"
tipo: "conceptual"
ultima_revision: "2026-03-27"
version: "1.0"
estado: "terminado"
---

# El Benchy y Cómo Leerlo

> El barco de calibración más famoso del mundo maker: cómo imprimirlo y qué te dice cada parte del resultado.

---

## Para Principiantes

El **3DBenchy** es probablemente la pieza más impresa en la historia de la impresión 3D. Es un pequeño barco de vapor diseñado no para flotar, sino para revelar — cada curva, cada chimenea, cada ventana fue calculada para que un problema de impresión diferente aparezca en una parte diferente del modelo. En la comunidad maker, "¿cómo te quedó el Benchy?" es la forma más rápida de preguntar si una impresora está funcionando bien.

La fama del Benchy tiene una razón práctica: en menos de una hora de impresión obtienes información sobre adhesión de cama, calidad de puentes, cooling, retracción, detalle fino y warping — todo en una sola pieza que cabe en la palma de la mano. Es un diseño de código abierto disponible gratuitamente en comunidades de impresión 3D.

Imprimir un Benchy que se vea bien es una señal clara de que tu impresora y tus parámetros están en orden. Si algo no está bien, el Benchy te lo dice con bastante precisión: no es cuestión de suerte ni de ojo entrenado. Cada defecto aparece en el lugar que le corresponde.

---

## Todo lo que Necesitas Saber

### Cómo imprimirlo

Usa los mismos parámetros del perfil que quieres evaluar. No reducir velocidad, no cambiar temperatura solo para el test: el objetivo es medir cómo funciona tu configuración real, no una versión ideal que nunca usarías en una pieza de verdad. El tiempo de impresión varía mucho según la impresora: alrededor de 10 minutos en showcases de alta velocidad, unos 30 minutos en impresoras rápidas modernas, y hasta 2 horas en equipos de generaciones anteriores.

### Guía de lectura por zonas

![Benchy impreso en PLA Turbo Fill3D — referencia de resultado bien calibrado](../../../assets/images/materiales-reference/PLA-turbo-benchy.jpg)

#### Casco (parte inferior)

El casco es lo primero que se imprime y lo primero que hay que revisar. Si no está plano o tiene bordes levantados, hay un problema de adhesión de primera capa o warping. Las causas más frecuentes son temperatura de cama fuera de rango, superficie de impresión sucia, o primera capa demasiado alta respecto a la cama.

#### Línea de proa

La proa del barco forma un voladizo de 40° medidos desde la horizontal — uno de los ángulos más exigentes del modelo. Esa línea debe quedar definida y limpia: si los bordes inferiores se rizan, se hunden o muestran capas sueltas, es señal de cooling insuficiente o temperatura demasiado alta para ese ángulo de voladizo.

#### Cubierta y puente central (deck)

La cubierta incluye uno de los puentes más útiles del modelo: la cabina del barco tiene un techo que se imprime en el aire sin soporte. Si ese puente se hunde o tiene capas irregulares colgando, el sistema de **cooling** es insuficiente para ese material a esa velocidad. Un puente bien formado requiere que el material solidifique antes de que la gravedad lo deforme.

#### Ventanas y marcos

Los marcos de las ventanas son voladizos (overhangs) pequeños pero bien definidos. Si los bordes se rizan hacia arriba o los marcos no tienen esquinas limpias, hay exceso de temperatura o cooling insuficiente. En materiales como el PLA este defecto es fácil de corregir ajustando temperatura de boquilla o velocidad del ventilador de capa.

#### Chimeneas

Las dos chimeneas son cilindros verticales de diámetro reducido. Si entre ellas o desde cualquier parte del barco aparecen hilos finos de material — lo que se conoce como stringing — la **retracción** está configurada por debajo de lo necesario para ese filamento. También puede ser una señal de temperatura demasiado alta.

#### Letras en relieve (#3DBenchy)

En la popa del barco hay letras "#3DBenchy" en relieve de apenas 0.1 mm de altura. Si no se leen con claridad o los bordes están fundidos entre sí, puede ser sobreextrusión o temperatura demasiado alta. Las letras nítidas con bordes definidos son señal de buen control del flow rate y temperatura.

### Tabla resumen

| Zona | Qué observar | Señal de problema |
|---|---|---|
| Casco | Planitud, adhesión | Warping, primera capa mal nivelada |
| Línea de proa | Bordes definidos, voladizo 40° | Cooling insuficiente o temperatura alta |
| Puente central | Hundimiento, capas colgantes | Cooling insuficiente |
| Ventanas | Bordes rizados | Temperatura alta o poco cooling |
| Chimeneas | Hilos entre partes (stringing) | Retracción baja o temperatura alta |
| Letras #3DBenchy | Definición de bordes | Sobreextrusión o temperatura alta |

---

## Para Expertos

### El Benchy como test de regresión

El valor real del Benchy en un workflow avanzado no es el diagnóstico inicial sino la comparación sistemática. Documenta cada Benchy con foto macro de las zonas críticas más los parámetros exactos: fecha, material (lote si es posible), temperatura de boquilla, temperatura de cama, velocidad de impresión, porcentaje de cooling, retracción. Dos Benchies con esos datos te permiten atribuir cambios a variables específicas en lugar de adivinar.

### Defectos sutiles que revelan problemas mecánicos

Más allá de los defectos obvios, el Benchy revela problemas que los principiantes no notan. Un **layer shifting** mínimo — desplazamiento de capas de menos de 0.1 mm — produce una textura direccional sutil en las paredes del casco que solo se nota con luz rasante. El **ghosting o ringing** aparece como un patrón de ondas repetitivas en las paredes planas del casco, cerca de esquinas o cambios de dirección — señal de resonancia mecánica o aceleración demasiado alta para la rigidez del frame. Las inconsistencias de flow en capas específicas, visibles como bandas horizontales de brillo o textura diferente, suelen apuntar a problemas en el extrusor o en el filamento.

### Comparar Benchies entre materiales

Imprimir el mismo Benchy con distintos filamentos del mismo fabricante y de distintos proveedores revela diferencias concretas en retracción y stringing: materiales con mayor temperatura de transición vítrea o menor viscosidad en estado fundido responden de manera diferente a la misma configuración de retracción. Este tipo de comparación es especialmente útil al evaluar si un filamento nuevo requiere ajuste de perfil o puede compartir parámetros con uno existente.

### Limitaciones del Benchy

El Benchy no evalúa todo. No tiene múltiples islas separadas, así que no mide el comportamiento de retracción entre piezas distintas en la misma cama. No evalúa resistencia mecánica ni deformación bajo carga. Y aunque tiene velocidad variable por geometría, no es un test controlado de rendimiento a alta velocidad: para eso se usan metodologías específicas de slicer como la calibración de presión de avance o los tests de velocidad máxima de Orca Slicer.

---

## También te puede interesar
- [Cubo de Calibración](./cubo-de-calibracion.md)
- [Metodología de Calibración — Orca Slicer](./metodologia-orca.md)
- [Problemas Comunes de Impresión](../../consejos-de-impresion/problemas-comunes.md)
