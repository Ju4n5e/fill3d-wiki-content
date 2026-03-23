---
titulo: "Accesorios y Repuestos"
slug: "accesorios-y-repuestos"
seccion: "lo-basico"
subseccion: "mantenimiento"
material: ""
tipo: "conceptual"
ultima_revision: "2026-03-22"
estado: "terminado"
version: "1.0"
---

# Accesorios y Repuestos

> Tener las herramientas correctas y unos repuestos clave a la mano convierte un problema en una pausa de diez minutos en lugar de días de espera.

---

## Para Principiantes

Imprimir en 3D es más fácil cuando tienes cerca las herramientas correctas. No necesitas un taller completo: con unos pocos accesorios básicos puedes limpiar boquillas, retirar piezas de la cama, reemplazar componentes desgastados y hacer ajustes finos. La mayoría son herramientas de ferretería que probablemente ya tienes en casa.

Lo que sí vale la pena tener específicamente para tu impresora es un pequeño inventario de **repuestos consumibles**: boquillas de reemplazo, un trozo de tubo PTFE y un termistor de repuesto. Estos son los componentes que más frecuentemente fallan o se desgastan, y cuando lo hacen suele ser en el peor momento —a mitad de una impresión larga. Tenerlos disponibles te evita días de espera y la frustración de perder una pieza que ya llevaba horas en la cama.

Piénsalo como el botiquín de primeros auxilios de tu impresora: no lo usas todos los días, pero cuando lo necesitas, lo agradeces tener.

---

## Todo lo que Necesitas Saber

### Herramientas esenciales

| Herramienta | Para qué sirve | Notas |
|---|---|---|
| **Juego de llaves Allen métricas** | Ajustar tornillos del marco, cambiar boquillas, modificar tensores | Tamaños M2.5, M3, M4 y M5 cubren la mayoría de impresoras |
| **Espátula metálica (rasqueta)** | Retirar piezas de la cama de impresión | Punta biselada; evita las plásticas que se doblan |
| **Pinzas de punta fina** | Retirar filamento de purga, sostener componentes durante ajustes | Indispensables durante el precalentamiento del hotend |
| **Alicates (pliers)** | Retirar soportes, sostener la boquilla al cambiarla | Útil con boquillas atascadas o apretadas |
| **Cortadores de modelo** | Cortar soportes en zonas delicadas sin fracturar la pieza | Diferentes de los alicates: filo de corte fino |
| **Cuchilla (bisturí o exacto)** | Limpiar bordes, retirar brims, stringing grueso | Usar con precaución |
| **Calibrador Vernier (pie de rey)** | Medir diámetro real del filamento, verificar dimensiones de piezas | Esencial para calibrar flujo y E-steps |

### Lubricantes y adhesivos

| Producto | Uso en la impresora |
|---|---|
| **Grasa PTFE (ej. Superlube)** | Lubricar varillas lisas de ejes X, Y |
| **Grasa de litio blanca** | Lubricar tornillo Z (lead screw) y engranajes |
| **Alcohol isopropílico 70–90%** | Limpiar cama de impresión antes de cada uso |
| **Barra de pegamento** | Adhesivo para ciertas superficies; desmoldante de PETG sobre PEI |

### Repuestos recomendados

| Repuesto | Cuándo tenerlo | Notas |
|---|---|---|
| **Boquillas de latón (0.4 mm)** | Siempre — son consumibles frecuentes | Stock de 3–5 unidades; cámbialas cada 1–3 meses |
| **Boquilla de acero endurecido** | Si imprimes [PPCF](https://www.fill-3d.com/tienda/) o composites | Una boquilla de acero dura meses frente a horas de latón con abrasivos |
| **Tubo PTFE** | Un trozo de repuesto de 50–100 cm | Cortarlo a medida; más crítico en setups Bowden |
| **Termistor de hotend** | Al menos uno de repuesto | Falla con poca advertencia; sin él la impresora no opera |
| **Calefactor (heater cartridge)** | Conveniente tener uno | Falla menos que el termistor pero deja la máquina inutilizable |

### Herramientas opcionales pero útiles

- **Cepillo de cerdas de latón o nylon:** Para limpiar el engranaje de arrastre del extrusor sin desmontarlo.
- **Bridas (zip ties) y espiral para cables:** Para organizar el cableado y evitar que se enganche en los ejes.
- **Adhesivo de cianoacrilato (Loctite, Super Glue):** Reparaciones rápidas en piezas PLA rotas.
- **Caja de filamentos con desecante (dry box):** Almacenamiento correcto del filamento; crítico para PA, PP y PPCF.

---

## Para Expertos

### Inventario estratégico según tu impresora

No todos los repuestos sirven para todos los modelos. En impresoras de sistema cerrado los componentes son específicos y no siempre intercambiables con genéricos del mercado. Identifica:

1. **Referencia exacta de termistor:** Algunos hotends usan termistores NTC 100k con diferentes coeficientes beta. Instalar uno incorrecto genera lecturas de temperatura erróneas que pueden causar subderfusión o, peor, thermal runaway.
2. **Voltaje de los ventiladores:** Los fans de 5V no son intercambiables con los de 24V sin conversor. Verificar en el esquema eléctrico de la impresora.
3. **Diámetro interno del tubo PTFE:** Los hotends de alto rendimiento (Bambu Lab, Dragon, Rapido) usan tubo de 1.9mm ID, no el estándar de 2mm. Usar el diámetro incorrecto genera gaps donde se deposita material fundido y eventualmente genera atascos fríos.

### Diagnóstico eléctrico con multímetro

El multímetro te permite diagnosticar dos fallas muy frecuentes antes de reemplazar componentes a ciegas:

- **Termistor:** Mide resistencia en frío (temperatura ambiente ~20–25 °C). Un termistor NTC 100k sano debe leer ~100 kΩ. Una lectura de 0Ω o infinito indica corte de circuito — reemplázalo.
- **Calefactor:** Mide resistencia del cartucho calefactor. Un calefactor de 40W para 24V tiene ~14.4Ω de resistencia. Fuera de ese rango en ±20% indica falla. Una lectura de infinito (circuito abierto) confirma el calefactor quemado.
- **Ventilador:** Con el multímetro en modo de voltaje DC, verifica que llegue la tensión correcta al conector cuando el firmware lo activa. Si llega voltaje pero no gira, el motor del ventilador está quemado.

### Accesorios imprimibles: la impresora que se mejora a sí misma

Una ventaja única de tener una impresora 3D es que puedes fabricar tus propios accesorios de mejora:

- **Tensores de correa:** Imprimibles para ejes X e Y en Ender, Prusa y similares. Reemplazan ajustes manuales con tornillo regulable.
- **Guías de cables (cable chains):** Organizan el cableado del cabezal en movimiento, aumentando la vida útil del cableado.
- **Soportes para dry box y guías de filamento:** Alimentadores de carrete con tensión controlada que evitan que el filamento se suelte y enrede.
- **Cajas de control y organizadores:** Carcasas para Raspberry Pi (para Klipper/Octoprint), soportes de pantalla, reposacabezas de rueda de filamento.


> 💡 **Nota técnica:** Para impresoras con sistema AMS (Bambu Lab) o MMU (Prusa), el tubo PTFE del sistema de alimentación múltiple se desgasta más rápido que el del hotend, especialmente con materiales de PA o PETG rugoso. Reemplazarlo es una de las acciones preventivas de mayor impacto en este tipo de setups.

---

## También te puede interesar
- [Mantenimiento de la Impresora](./mantenimiento.md)
- [Extrusores](../partes-impresora/extrusores.md)
- [Boquillas](../partes-impresora/boquillas.md)
