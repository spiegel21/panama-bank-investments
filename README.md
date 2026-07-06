# Radar de Inversiones — Banca de Panamá

Análisis competitivo del portafolio de **inversiones en valores** de los principales bancos de
Panamá, con **Banistmo** como banco base de comparación. Enfoque de tesorería: cómo están
invertidos los competidores frente a Banistmo (tamaño, peso sobre activo, tipo de instrumento,
clasificación contable, rentabilidad estimada y calificaciones de crédito), para 2022–2026.

**Perímetro:** Banistmo · Banco General · BAC (incl. Multibank) · Global Bank · Davivienda · Scotiabank.

## Sitio publicado

El reporte se sirve como página estática vía **GitHub Pages**:

**https://spiegel21.github.io/panama-bank-investments/**

`index.html` es autocontenido (HTML + CSS + JS inline, sin dependencias externas): se puede abrir
directamente en cualquier navegador incluso sin el sitio.

## Contenido

| Archivo | Qué es |
|---|---|
| `index.html` | Reporte visual interactivo en español (la página publicada). |
| `datos-extraidos.md` | **Dataset completo** con cada cifra, su nivel de confianza (Auditado / Estimado / No divulgado) y su fuente. Es la fuente de verdad detrás del HTML. |
| `fuentes-pdfs.md` | URLs de los EE.FF. auditados por banco, para la extracción a fidelidad completa. |
| `capturas-fuentes/` | **Capturas (PNG) de cada página PDF de la que se sourceó una cifra del dashboard** — nota "Inversiones en Valores", tablas de calificaciones, balances y cuadros del sistema (SBP). Ver [`capturas-fuentes/README.md`](capturas-fuentes/README.md). |
| `allowlist-domains.txt` | Dominios financieros a habilitar en la política de red del entorno para reproducir la extracción. |

## Estado: fidelidad completa

Las cifras provienen de la **lectura directa de la nota "Inversiones en valores"** (y la nota de
riesgo de crédito) de los estados financieros **auditados** de los seis bancos, a su último cierre
disponible (Banistmo/BG/BAC/Davivienda Dic-2025, Global jun-2025, Scotiabank oct-2024 standalone).
Los porcentajes de activo y los yields marcados *Estimado* son cálculos propios.

## Metodología

- Moneda: USD (balboa a la par).
- Rendimiento de cartera estimado como `ingreso por intereses de inversiones ÷ saldo promedio`.
- **Comparabilidad:** los perímetros de reporte difieren y no son 1:1 — BAC = consolidado
  Centroamérica; Global Bank cierra fiscal en junio; Davivienda FY2025 es post-fusión con Scotiabank.
  El análisis se apoya en **ratios** (% de activo, yield, distribución por rating) robustos al perímetro.

---

*Reporte preparado para la mesa de tesorería. Datos 2022–2026.*
