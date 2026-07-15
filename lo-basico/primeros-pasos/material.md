---
titulo: "Recibiendo un Material Nuevo"
slug: "material"
seccion: "lo-basico"
subseccion: "primeros-pasos"
tipo: "conceptual"
ultima_revision: "2026-03-26"
estado: "terminado"
version: "1.0"
---

# Recibiendo un Material Nuevo

> Todo lo que debes hacer cuando llega un filamento nuevo — desde revisar el empaque hasta la primera impresión exitosa.

---

## Para Principiantes

Cada filamento es un mundo aparte. Aunque dos rollos se llamen "PLA", pueden comportarse diferente si son de distintos fabricantes, distintos colores o si llegaron con distintas condiciones de humedad. Cambiar de material es un poco como cocinar con un horno nuevo o usar una harina diferente: las temperaturas y los tiempos de referencia son un punto de partida, no una garantía inmediata de resultado perfecto.

Eso no significa que sea complicado — significa que los primeros metros de filamento son de calibración, no de producción. Antes de imprimir la pieza que realmente necesitas, imprime algo pequeño de prueba, evalúa el resultado y ajusta si hace falta. Ese es el proceso correcto, incluso para usuarios con experiencia.

La buena noticia es que si sigues los pasos en orden, el proceso es rápido y predecible. Con un poco de práctica, recibir un material nuevo se convierte en una rutina de diez minutos.

---

## Todo lo que Necesitas Saber

### 1. Inspección del empaque

Antes de abrir el rollo, revisa que el empaque esté herméticamente sellado. Los filamentos higroscópicos (PETG, PA, PP y otros materiales técnicos) absorben humedad del aire cuando el empaque está roto o mal sellado. Verifica también que la **bolsa de sílica gel** esté presente e intacta — si está saturada o falta, el filamento puede haber absorbido humedad durante el almacenamiento o el transporte.

### 2. Identificar el material

Lee la etiqueta completa antes de cargar el filamento. Los datos que necesitas son:

- **Tipo de material** (PLA, PETG, PA, PP…)
- **Diámetro** (1,75 mm es el estándar más común; 2,85 mm es menos frecuente pero existe — cargar el diámetro incorrecto en tu slicer afecta el flujo)
- **Temperaturas recomendadas por el fabricante** para boquilla y cama

Los filamentos Fill3D incluyen las temperaturas recomendadas directamente en la etiqueta, lo que hace que este paso sea inmediato.

### 3. Comparar con perfiles existentes

¿Tienes ya un perfil en tu slicer para este material? Si lo tienes, revisa que las temperaturas del perfil sean compatibles con las del fabricante. Si no tienes un perfil, este es el momento de crearlo o de descargar uno como base. No importes ciegamente un perfil de otra fuente sin revisar al menos las temperaturas y el flow rate.

### 4. Precalentar a la temperatura correcta para el material nuevo

Antes de cargar el filamento, precalienta la boquilla a la temperatura correspondiente al **material nuevo**, no al que tenías cargado antes. Cargar filamento frío o a temperatura incorrecta puede atascar el hotend.

La siguiente tabla es orientativa — los valores reales pueden variar según la impresora, la boquilla y el fabricante:

| Material | Boquilla |
|---|---|
| PLA | 220 °C |
| PETG | 245 °C |
| PA (Nylon) | 275 °C |
| PP | 250 °C |

### 5. Purgar el material anterior

Al cambiar de un material a otro, la purga es obligatoria. Extruye al menos 100–200 mm de filamento nuevo a temperatura de impresión antes de comenzar. Si el material anterior tenía una temperatura de impresión más alta (por ejemplo, cambiar de PETG a PLA), sube primero a la temperatura del material anterior, carga el nuevo y luego baja a la temperatura del nuevo mientras purgues. Esto evita atascos por material frío parcialmente derretido.

### 6. Impresión de prueba

Con el material cargado y purgado, imprime algo pequeño antes de lanzar la pieza que realmente necesitas. La opción recomendada es un [cubo de calibración](../calibracion/cubo-de-calibracion.md): es rápido de imprimir, fácil de evaluar y te da información clara sobre temperatura, flujo y adhesión de cama.

### 7. Evaluar y ajustar

Revisa el resultado en este orden de prioridad:

1. **Temperatura:** si ves capas que se desprenden entre sí o superficies rugosas, puede que la temperatura esté baja. Si ves stringing o deformación por calor, puede estar alta.
2. **Velocidad:** reduce la velocidad si hay irregularidades en las paredes que no se explican por temperatura.
3. **Enfriamiento:** ajusta el ventilador de capa según las recomendaciones del material. El PA y el PP generalmente imprimen mejor con enfriamiento mínimo o nulo.

### 8. Almacenamiento si no se usa de inmediato

Si no vas a continuar imprimiendo con este material, vuelve a sellar el rollo en su bolsa original con la sílica gel. Los materiales técnicos como PA y PP son especialmente sensibles a la humedad — idealmente usa una caja hermética o un drybox con sílica gel fresca.

---

## Para Expertos

### Test rápido de humedad del filamento

Antes de cargar un filamento que estuvo abierto o almacenado sin control, escucha mientras extruyes manualmente a temperatura de impresión: si escuchas **crepitar, burbujas o pequeñas explosiones**, el filamento está húmedo. La humedad se convierte en vapor dentro del hotend y genera poros, subextrusión intermitente e inconsistencias de superficie imposibles de corregir con ajustes de temperatura. La solución es secar el filamento antes de imprimir (temperatura y tiempo según el material — PA requiere más agresividad que PLA).

### Calibración antes de la primera impresión real

No asumas que el perfil del material anterior aplica al material nuevo. Cada combinación de material y máquina tiene sus propios parámetros óptimos. Lo recomendable es hacer un set de calibraciones completo para construir un perfil propio ajustado a tu equipo — consulta [Metodología de Calibración con Orca Slicer](../calibracion/metodologia-orca.md) para ver cómo realizarlo paso a paso.

### Materiales técnicos: PA y PP

Para PA y PP, el secado previo no es opcional — es el primer paso. PA requiere típicamente 80–90 °C por 6–12 h ⚠️ verificar en horno de filamento o deshidratador de alimentos. PP es menos higroscópico que PA pero igualmente sensible a contaminantes de superficie. Ambos materiales requieren cámara cerrada para mantener temperatura ambiente elevada y reducir warping. Sin cámara, imprimir piezas grandes en PA o PP es prácticamente inviable.

### Diferencias entre proveedores del mismo material

Dos rollos de "PLA" de distintos fabricantes pueden tener diferencias reales en: tolerancias de diámetro (±0,02 mm vs. ±0,05 mm), consistencia de color entre lotes, temperatura de transición vítrea y comportamiento de retracción. Mide el diámetro real con micrómetro digital en varios puntos del rollo antes de ajustar el flow rate. Si gestionas múltiples materiales, nombra tus perfiles en el slicer con el esquema **fabricante + material + lote + fecha** para garantizar reproducibilidad entre sesiones.

---

## También te puede interesar
- [Estrenando tu Impresora](./impresora.md)
- [Materiales de Impresión 3D](../../lo-basico/materiales-impresion-3d.md)
- [Consejos por Tipo de Material](../../consejos-de-impresion/por-tipo-de-material.md)
