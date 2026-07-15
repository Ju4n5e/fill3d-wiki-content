---
titulo: "Consejos por Tipo de Material"
slug: "por-tipo-de-material"
seccion: "consejos-de-impresion"
subseccion: ""
material: ""
tipo: "material"
ultima_revision: "2026-03-23"
estado: "terminado"
version: "1.0"
---

# Consejos por Tipo de Material

> Parámetros clave para imprimir cada material Fill3D con éxito.

Cada filamento tiene propiedades únicas que requieren ajustes distintos en tu impresora.
Esta guía consolida los valores directamente de los perfiles oficiales Fill3D,
más los tips de uso que no caben en un archivo de slicer. Imprime con confianza.

---

## PLA básico

* **Temperatura de cama:** 50–60 °C
* **Temperatura de boquilla:** 200–220 °C (empezar por 210 °C y ajustar)
* **Flujo volumétrico máximo:** 32 mm³/s
* **Flow ratio:** 95%
* **Enfriamiento:** 100% a partir de la capa 2
* **Tiempo mínimo por capa:** —
* **Retracción:** 0.2–0.5 mm @ 35 mm/s (direct drive) / 1–2 mm @ 45 mm/s (bowden) — Pressure Advance: K=0.021
* **Secado recomendado:** 60 °C, 2–4 horas (opcional; mejora calidad de superficie)
* **Post-procesado:** Lijado y pintura
* **Tips especiales:** Poco warping; no requiere cámara cerrada. Buen punto de partida para calibrar una impresora nueva. Lámina PEI texturizada limpiada con IPA asegura excelente adhesión sin adhesivo adicional.

---

## PLA Turbo

* **Temperatura de cama:** 35–60 °C
* **Temperatura de boquilla:** 220–240 °C (según flujo volumétrico)
  - Flujo < 20 mm³/s: 220 °C
  - Flujo 20–30 mm³/s: 225 °C
  - Flujo 30–40 mm³/s: 230 °C
  - Flujo > 40 mm³/s: 235–240 °C
* **Flujo volumétrico máximo:** 55 mm³/s
* **Flow ratio:** — (calibrar con tu setup)
* **Enfriamiento:** 100% a partir de la capa 2
* **Tiempo mínimo por capa:** ≥2 segundos
* **Retracción:** 0.1 mm @ 55 mm/s (Adaptive Pressure Advance activado; K base: 0.018)
* **Secado recomendado:** 60 °C, 2–4 horas (opcional; mejora calidad de superficie)
* **Post-procesado:** Lijado y pintura
* **Tips especiales:** Diseñado para impresoras CoreXY de alta velocidad. Adaptive Pressure Advance activado con modelo de velocidad integrado. Boquillas de 0.6 mm o más recomendadas para capas gruesas a alta velocidad.

---

## PETG

* **Temperatura de cama:** 80 °C (previene warping; subir 5 °C si las esquinas se levantan)
* **Temperatura de boquilla:** 265 °C (ajustar ±5 °C según color)
* **Flujo volumétrico máximo:** 28 mm³/s
* **Flow ratio:** 94%
* **Enfriamiento:** 30–50% a partir de la capa 3
* **Tiempo mínimo por capa:** ≥4 segundos (previene deformación; el PETG retiene calor más que el PLA)
* **Retracción:** 0.2 mm @ 35 mm/s (Pressure Advance: K=0.059)
* **Secado recomendado:** 70 °C, 4–6 horas (PETG es moderadamente higroscópico; el secado mejora fluidez y reduce defectos ópticos)
* **Post-procesado:** Lijado ligero recomendado; acepta bien pintura y teñido
* **Tips especiales:** Bueno para piezas resistentes a químicos y UV. Evita enfriar demasiado rápido — reduce ventilador en capas largas para prevenir stringing. 
  
  **Para PETG transparente:** si quieres que tu pieza final tenga buenas propiedades ópticas, seca muy bien tu filamento (≤0.2% humedad), reduce la ventilación a 0%, eleva la temperatura a 280–285 °C y reduce la velocidad de impresión. Estos ajustes minimizan la opacidad por cristalización y mejoran la adhesión entre capas, disminuyendo defectos visuales (líneas de capa visibles, delaminar).

---

## PA (Nylon)

* **Temperatura de cama:** 100 °C (minimiza la contracción térmica durante la impresión; crítico para prevenir warping)
* **Temperatura de boquilla:** 275 °C (estricto; ±5 °C afecta el flujo significativamente)
* **Flujo volumétrico máximo:** 18 mm³/s
* **Flow ratio:** 97.5%
* **Temperatura de ambiente:** 40–60 °C (minimiza warping; mantén la cámara de impresión cerrada)
* **Enfriamiento:** 0% en las primeras 10 capas; luego rampa gradual a 10–50%
* **Tiempo mínimo por capa:** ≥5 segundos (paredes gruesas enfrían despacio; crítico para adhesión entre capas)
* **Retracción:** 2 mm @ 40 mm/s (Pressure Advance: K=0.038)
* **Secado requerido:** 85–95 °C, 12 horas (si usas temperaturas menores, extiende el tiempo de permanencia proporcionalmente; PA es altamente higroscópico, secado crítico antes de imprimir. Guardar en bolsa sellada con desecante después de secar)
* **Post-procesado:** Recocido opcional (horno 100 °C, enfriamiento lento) para +20% resistencia a tracción; lijado expone detalles finos
* **Tips especiales:** Higroscópico — guardar sellado con desecante; imprimir dentro de 4 horas de abrir el empaque. Ideal para piezas funcionales, bisagras y aplicaciones de alto impacto.

---

## PP

* **Temperatura de cama:** 100 °C (placa de ingeniería a 100 °C en Bambu Lab; o sin calefacción con adhesivo específico para PP)
* **Temperatura de boquilla:** 300 °C (estricto; ±5 °C afecta el flujo significativamente)
* **Flujo volumétrico máximo:** 12 mm³/s
* **Flow ratio:** 104.5%
* **Temperatura de ambiente:** 40–60 °C (minimiza warping; mantén la cámara de impresión cerrada)
* **Enfriamiento:** 0% en las primeras 5 capas; luego 20–30% máx. (material muy sensible al enfriamiento rápido)
* **Tiempo mínimo por capa:** ≥5 segundos (muy sensible al enfriamiento rápido; warping severo si se apresura)
* **Retracción:** 0.2 mm @ 40 mm/s (Pressure Advance: K=0.085)
* **Secado recomendado:** 60 °C, 4 horas (PP es poco higroscópico; secado opcional pero recomendado para mejor calidad de impresión)
* **Post-procesado:** Post-procesado mínimo; la alta resistencia química hace que la pintura normal no adhiera — usar imprimante para poliolefinas
* **Tips especiales:** Excelente para bisagras de película (living hinges): dobla sin quebrarse. Baja densidad (~0.93 g/cm³) = piezas muy livianas. Requiere superficie o adhesivo específico para PP.

---

## PPCF (PP + Fibra de Carbono)

* **Temperatura de cama:** 80 °C (la estabilidad que brinda la fibra de carbono permite una temperatura de cama menor)
* **Temperatura de boquilla:** 300 °C (estricto; ±5 °C afecta el flujo significativamente)
* **Flujo volumétrico máximo:** 17 mm³/s
* **Flow ratio:** 101.5%
* **Temperatura de ambiente:** 40–60 °C recomendada (mejores propiedades mecánicas finales por adhesión entre capas); permite impresión a temperatura ambiente
* **Enfriamiento:** 0% en las primeras 5 capas; luego hasta 80% (según fan_max_speed del perfil)
* **Tiempo mínimo por capa:** ≥5 segundos (el compuesto necesita enfriamiento controlado para no fracturar la matriz)
* **Retracción:** 0.2 mm @ 45 mm/s (Pressure Advance: K=0.044)
* **Secado recomendado:** 60 °C, 4 horas (PPCF es poco higroscópico; secado opcional pero recomendado para mejor calidad de impresión)
* **Post-procesado:** La alta resistencia química hace que la pintura normal no adhiera — usar imprimante para poliolefinas
* **Tips especiales:** Boquilla de acero endurecido obligatoria — en una sola impresión se desgasta una boquilla de latón.

---

## También te puede interesar
- [Materiales de Impresión 3D](../lo-basico/materiales-impresion-3d.md)
- [PA (Nylon) — Ficha de Material](../lo-basico/materiales/pa-nylon.md)
- [Problemas Comunes de Impresión](./problemas-comunes.md)
- [Post-Procesado](./post-procesado.md)