# Wiki FiLL-3D — Contenido

Este repositorio contiene los archivos de contenido del wiki técnico de **FiLL-3D**, fabricante colombiano de filamentos para impresión 3D.

El wiki está escrito en español (Colombia) y cubre desde los conceptos básicos de impresión 3D hasta guías técnicas avanzadas por material, organizadas para acompañar al usuario en cada etapa de su experiencia con los productos FiLL-3D.

---

## Estado del contenido

| Ícono | Significado |
|---|---|
| ✅ | Terminado |
| 📝 | Borrador — revisión editorial pendiente |

---

## Árbol de archivos

```
content/
│
├── index.md                                    ✅ Página de inicio
│
├── lo-basico/
│   ├── index.md                                ✅ Índice de sección
│   ├── introduccion-impresion-3d.md            ✅
│   ├── materiales-impresion-3d.md              ✅
│   ├── impresoras-3d.md                        ✅
│   ├── slicers.md                              ✅
│   ├── aplicaciones.md                         ✅
│   ├── datos-curiosos.md                       ✅
│   ├── materiales/
│   │   ├── pla.md                              ✅
│   │   ├── petg.md                             ✅
│   │   ├── pa-nylon.md                         ✅
│   │   ├── pp.md                               ✅
│   │   └── fibras-aditivas.md                  ✅
│   ├── primeros-pasos/
│   │   ├── index.md                            ✅
│   │   ├── impresora.md                        ✅
│   │   └── material.md                         ✅
│   ├── calibracion/
│   │   ├── index.md                            ✅
│   │   ├── cubo-de-calibracion.md              ✅
│   │   ├── benchy.md                           ✅
│   │   └── metodologia-orca.md                 ✅
│   ├── partes-impresora/
│   │   ├── extrusores.md                       ✅
│   │   ├── boquillas.md                        ✅
│   │   └── camas-de-impresion.md               ✅
│   └── mantenimiento/
│       ├── mantenimiento.md                    ✅
│       └── accesorios-y-repuestos.md           ✅
│
├── consejos-de-impresion/
│   ├── index.md                                ✅ Índice de sección
│   ├── por-tipo-de-material.md                 ✅
│   ├── problemas-comunes.md                    ✅
│   └── post-procesado.md                       ✅
│
├── referencia-tecnica/
│   ├── index.md                                ✅ Glosario técnico
│   └── ciencia-de-materiales.md               ✅
│
└── assets/
    └── images/
        ├── calibracion/
        │   ├── cali-cube.webp                  🖼️ Cubo XYZ 20mm
        │   ├── voron-cube.webp                 🖼️ Voron Design Cube
        │   ├── calib_temperatura/              🖼️ Torre de temperatura (3 imágenes)
        │   ├── calib_velocidad/                🖼️ Test flujo volumétrico máximo (2 imágenes)
        │   ├── calib_pressure.png              🖼️ Resultado PA Line
        │   └── calib_multiplicador/            🖼️ Test flow ratio — bloques (3 imágenes)
        ├── materiales-reference/               🖼️ Referencias de material impreso
        │   ├── PA-benchy.jpg
        │   ├── PA-voron.jpg
        │   ├── PETG-cali-dragon.jpg
        │   ├── PETG-voron.jpg
        │   ├── PLA-cali-dragon.jpg
        │   ├── PLA-turbo-benchy.jpg
        │   ├── PLA-turbo-cali-dragon.jpg
        │   ├── PLA-turbo-voron.jpg
        │   ├── PLA-voron.jpg
        │   ├── PP-benchy.jpg
        │   ├── PP-voron.jpg
        │   └── PPCF-voron.jpg
        ├── primeros-pasos-impresora/
        ├── introduccion-impresion-3d/
        ├── impresoras-3d/
        └── accesorios-y-repuestos/
```

---

## Progreso

**31 / 31 archivos creados** — 31 terminados · 0 en borrador · 0 por crear

**Actualización** — 2026-04-06 · Figuras de calibración + tabla de parámetros por material

- `metodologia-orca.md`: se añaden 4 conjuntos de imágenes (temperatura, flujo volumétrico, Pressure Advance, flow ratio) y una tabla de parámetros de referencia por material.
- `por-tipo-de-material.md`: se añade la sección PLA Turbo (faltante) y se completan los campos Flujo volumétrico máximo y Flow ratio para todos los materiales.

**Entrega final** — 2026-03-27 · Revisión editorial completa (R04/R08)

---

## Propuestas

La carpeta `propuestas/` contiene páginas en fase de propuesta o prototipo, no incluidas en el sitemap oficial. Los archivos aquí presentes están sujetos a cambios antes de ser incorporados al árbol principal.

| Archivo | Descripción | Estado |
|---|---|---|
| `guia-re-fill.md` | Guía de carga del sistema Re-Fill PLA (8 pasos) | 📝 Borrador |
