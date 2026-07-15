---
titulo: "¿Sirve para mi impresora? Perfiles por modelo"
slug: "perfiles-por-impresora"
seccion: "consejos-de-impresion"
subseccion: ""
material: ""
tipo: "guia"
ultima_revision: "2026-07-13"
estado: "borrador"
version: "1.0"
---

# ¿Sirve para mi impresora? Perfiles por modelo

> La respuesta corta: sí. Si tu impresora usa filamento de 1.75 mm, los filamentos Fill3D le sirven. Aquí están los valores de partida para los modelos más comunes en Colombia.

Es la pregunta que más nos hacen: *"¿el PLA Turbo sirve para mi Ender 3 V2?"*. Los filamentos Fill3D son de **1.75 mm estándar** — funcionan en cualquier impresora FDM de escritorio. Lo que cambia entre modelos es la **velocidad que puede aprovechar** y los ajustes de partida.

> **Importante:** estos valores son puntos de partida seguros. Para exprimir tu combinación exacta de impresora + filamento, corre la [calibración con Orca Slicer](../lo-basico/calibracion/metodologia-orca) — toma 30 minutos y vale cada segundo.

---

## PLA Turbo HS por modelo de impresora

| Impresora | Boquilla | Cama | Velocidad de partida | Notas |
|---|---|---|---|---|
| Ender 3 / 3 Pro / 3 V2 | 205–215 °C | 55–60 °C | 50–70 mm/s | Bowden: retracción 4–6 mm. El Turbo HS también mejora calidad a velocidad normal |
| Ender 3 V3 SE / KE | 210–220 °C | 55–60 °C | 150–250 mm/s | Direct drive: retracción 0.5–1 mm |
| Creality K1 / K1C / K1 Max | 215–230 °C | 55–60 °C | 300+ mm/s | Aquí el Turbo HS brilla: sube temperatura con la velocidad |
| Bambu A1 / A1 mini | 210–225 °C | 55–60 °C | 200–300 mm/s | Usa el perfil "Generic PLA" y ajusta temperatura |
| Bambu P1P / P1S / X1C | 215–230 °C | 55–60 °C | 300+ mm/s | Con AMS: carrete plástico rígido (ver [FAQ Re-Fill](../propuestas/faq-re-fill)) |
| Anycubic Kobra 2 / 3 | 210–225 °C | 55–60 °C | 150–250 mm/s | |
| Elegoo Neptune 3 / 4 | 205–220 °C | 55–60 °C | 60–250 mm/s según versión | Neptune 4 con klipper aprovecha el HS |
| Artillery Sidewinder / Genius | 205–215 °C | 55–60 °C | 60–100 mm/s | Direct drive Titan: retracción 1–2 mm |
| Prusa MK3S / MK4 | 210–220 °C | 55–60 °C | 80–200 mm/s | Perfil Prusament PLA como base funciona bien |

**Regla general del PLA Turbo HS:** a más velocidad, más temperatura. Imprimiendo a 60 mm/s usa el rango bajo (205–210 °C); a 300 mm/s usa el rango alto (225–230 °C). El "HS" significa que el material funde parejo incluso con poco tiempo en el fusor — pero necesita esa temperatura extra para lograrlo.

---

## PET-G por modelo (resumen)

Los mismos modelos de arriba, con estos cambios:

- **Boquilla:** 230–250 °C (empieza en 240 °C)
- **Cama:** 70–85 °C — obligatoria
- **Velocidad:** máximo 40–70 mm/s incluso en impresoras rápidas (el PETG castiga la velocidad con stringing)
- **Enfriamiento:** 30–60 % (menos que PLA)

La ficha completa está en [PETG — Ficha de Material](../lo-basico/materiales/petg).

---

## ¿Tu impresora no está en la lista?

No pasa nada — la lógica es la misma:

1. ¿Usa filamento de **1.75 mm**? → los filamentos Fill3D le sirven.
2. Arranca con el **perfil genérico de PLA** (o PETG) de tu slicer.
3. Ajusta la temperatura de boquilla al rango de la tabla según tu velocidad.
4. Corre el [cubo de calibración](../lo-basico/calibracion/cubo-de-calibracion) y un [Benchy](../lo-basico/calibracion/benchy) para validar.

¿Impresora de 2.85/3 mm (Ultimaker, algunas antiguas)? Escríbenos por WhatsApp antes de comprar — la mayoría de nuestro catálogo es 1.75 mm y te confirmamos disponibilidad en otros diámetros.

---

## ¿Dudas con tu modelo específico?

Escríbenos por WhatsApp con el modelo de tu impresora y qué quieres imprimir — te decimos el filamento y los parámetros de partida.
