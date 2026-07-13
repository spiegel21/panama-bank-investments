# Radar de Inversiones — Banca de Panamá

Análisis competitivo del portafolio de **inversiones en valores** de los principales bancos de
Panamá, con **Banistmo** como banco base de comparación. Enfoque de tesorería: cómo están
invertidos los competidores frente a Banistmo (tamaño, peso sobre activo, tipo de instrumento,
clasificación contable, rentabilidad estimada y calificaciones de crédito), para 2022–2026.

**Corte vigente: 31 de marzo de 2026.** Los bancos con reporte trimestral pasan a su **1T-2026
interino no auditado** (Banistmo, Banco General, BAC, Global Bank, Banesco) y el sistema bancario a los
datos de la SBP a **marzo-2026** (Balance de Situación SBN/CBI + Informe de Actividad Bancaria,
regulatorio no auditado). Dos excepciones se conservan en su último cierre disponible: **Davivienda**
(Dic-2025 auditado — no publica interinos trimestrales) y **Scotiabank** (oct-2024 — absorbido por
Davivienda el 5-dic-2025, ya no reporta standalone). Detalle completo en `datos-extraidos.md`.

**Perímetro:** Banistmo · Banco General · BAC (incl. Multibank) · Global Bank · Davivienda · Scotiabank · **Banesco**.

**Novedad (sesión 4):** se replicó, **para los siete bancos**, el rastreo renglón-por-renglón de las ganancias del portafolio
que se había hecho solo para Banistmo (un `<banco>-ganancias-inversiones.html` por banco, con capturas de páginas fuente), y se
**agregó Banesco** a todas las comparaciones. Resumen comparable en la sección "Mapa de renglones…" de `datos-extraidos.md`.

**Novedad (sesión 5):** el dashboard (`index.html`) ahora **muestra la cifra comparable de resultado del portafolio en la utilidad
neta** — no solo el yield de interés — en una nueva sección **07 "Resultado del portafolio — todos los renglones"** (tabla +
gráfico anualizado). Es el número que el rastreo renglón-por-renglón hacía visible pero que antes solo vivía en los mapas y en
`datos-extraidos.md`: interés + valuación/venta − provisiones, con el ORI no realizado mostrado aparte (patrimonio, no utilidad).

## Sitio publicado

El reporte se sirve como página estática vía **GitHub Pages**:

**https://spiegel21.github.io/panama-bank-investments/**

`index.html` es autocontenido (HTML + CSS + JS inline, sin dependencias externas): se puede abrir
directamente en cualquier navegador incluso sin el sitio.

## Contenido

| Archivo | Qué es |
|---|---|
| `index.html` | Reporte visual interactivo en español (la página publicada). |
| `<banco>-ganancias-inversiones.html` | **Mapas de renglones — ganancias del portafolio, uno por banco (7 documentos).** Rastreo, renglón por renglón, de todos los lugares del último EE.FF. de cada banco donde se reconoce ganancia/ingreso del portafolio de valores (interés, valuación/venta, ORI y provisiones), con capturas de las páginas fuente. El hallazgo comparable: **cada banco "esconde" la ganancia de forma distinta** — Banistmo (`banistmo-…`) mezcla divisas+derivados en el renglón; Banco General (`bancogeneral-…`) lo mezcla con derivados; BAC (`bac-…`) lo tiene limpio con el FX aparte; Global Bank (`globalbank-…`) lo embebe en "Otros ingresos"; Davivienda (`davivienda-…`) usa dos líneas limpias; Scotiabank (`scotiabank-…`) es casi todo interés; Banesco (`banesco-…`) reporta dos pérdidas con la FVTPL mixta con derivados. Enlazados desde `index.html` (sección "Renglones"). |
| `datos-extraidos.md` | **Dataset completo** con cada cifra, su nivel de confianza (Auditado / Estimado / No divulgado) y su fuente. Es la fuente de verdad detrás del HTML. |
| `fuentes-pdfs.md` | URLs de los EE.FF. auditados por banco, para la extracción a fidelidad completa. |
| `capturas-fuentes/` | **Capturas (PNG) de cada página PDF de la que se sourceó una cifra del dashboard** — nota "Inversiones en Valores", tablas de calificaciones, balances y cuadros del sistema (SBP). Ver [`capturas-fuentes/README.md`](capturas-fuentes/README.md). |
| `allowlist-domains.txt` | Dominios financieros a habilitar en la política de red del entorno para reproducir la extracción. |
| [`march-2026/`](march-2026/) | **Corte anterior (superado por este reporte).** Snapshot con el primer dato SBP publicado en marzo de 2026 (sistema a Enero-2026, regulatorio no auditado; cifras por banco aún en Dic-2025). El reporte de esta raíz lo reemplaza con el corte 31-mar-2026 (interinos 1T-2026 de los bancos + SBP marzo-2026). Ver [`march-2026/README.md`](march-2026/README.md). |

## Estado: corte 31-marzo-2026

Los cinco bancos con reporte trimestral (Banistmo, Banco General, BAC, Global Bank, Banesco) están al **1T-2026,
interino no auditado**, leído directamente de la nota "Inversiones en valores" de cada estado financiero
interino. El sistema bancario (SBN/CBI) está al **dato regulatorio de la SBP a marzo-2026** (no auditado).
**Davivienda** se mantiene en su cierre **Dic-2025 auditado** (no publica interinos trimestrales —
confirmado ausente en SMV, SBP, davibank.pa y Latinex) y **Scotiabank** en **oct-2024** (absorbido por
Davivienda, ya no reporta standalone). Los porcentajes de activo y los yields marcados *Estimado* son
cálculos propios. Detalle completo, con nivel de confianza por cifra, en `datos-extraidos.md`.

## Metodología

- Moneda: USD (balboa a la par).
- Rendimiento de cartera estimado como `ingreso por intereses de inversiones ÷ saldo promedio`.
- **Comparabilidad:** los perímetros de reporte difieren y no son 1:1 — BAC = consolidado
  Centroamérica; Global Bank cierra fiscal en junio; Davivienda FY2025 es post-fusión con Scotiabank.
  El análisis se apoya en **ratios** (% de activo, yield, distribución por rating) robustos al perímetro.
- **Interino vs. auditado:** los interinos no auditados de este corte no re-divulgan siempre la misma
  profundidad que un cierre anual auditado (ratings, escalera de vencimientos, composición detallada);
  donde falta, se usa el último dato auditado disponible, marcado explícitamente como *carried* en
  `datos-extraidos.md`.

---

*Reporte preparado para la mesa de tesorería. Datos 2022–2026.*
