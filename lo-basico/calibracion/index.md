---
titulo: "Tests de Calibración"
slug: "calibracion"
seccion: "lo-basico"
subseccion: "calibracion"
tipo: "navegacion"
ultima_revision: "2026-03-27"
version: "1.0"
estado: "terminado"
---

# Tests de Calibración

Que la impresora encienda no significa que esté lista para imprimir bien. Una máquina descalibrada puede producir piezas con paredes torcidas, capas que no se adhieren correctamente, puentes colapsados o geometría que no cuadra con el diseño original. Calibrar no es un trámite que se hace una sola vez: es el proceso de verificar que la impresora y el filamento están trabajando dentro de los rangos correctos antes de imprimir algo que importa.

Los tests de calibración en esta sección están ordenados de menor a mayor profundidad. El cubo de calibración es el punto de partida: rápido de imprimir, fácil de medir, te dice en minutos si hay algo mecánico fuera de lugar. El Benchy es el siguiente nivel: un modelo diseñado para exponer fallas en zonas concretas de la impresora, desde overhangs hasta enfriamiento. La metodología de Orca Slicer va más lejos aún: es una secuencia sistemática para afinar los parámetros específicos de un filamento nuevo —flow rate, presión, temperatura— hasta extraerle el mejor rendimiento posible.

El orden sugerido es: cubo → Benchy → Orca Slicer. Puedes detenerte donde tu nivel de exigencia lo requiera.

---

## Guías disponibles

**[Cubo de Calibración](cubo-de-calibracion.md)**
Verificación básica de geometría y mecánica: cómo imprimirlo, qué medir y qué correcciones aplicar según lo que encuentres.

**[El Benchy y Cómo Leerlo](benchy.md)**
Diagnóstico completo por zonas del barco: qué falla cada parte del modelo y qué ajuste resuelve cada problema.

**[Calibración de Filamento con Orca Slicer](metodologia-orca.md)**
Metodología sistemática para afinar un filamento nuevo: la secuencia de tests integrada en Orca Slicer y cómo interpretar cada resultado.
