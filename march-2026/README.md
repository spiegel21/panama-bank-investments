# Radar de Inversiones — Banca de Panamá · Corte marzo 2026

Análisis competitivo del portafolio de **inversiones en valores** de los principales bancos de
Panamá, con **Banistmo** como banco base de comparación. Enfoque de tesorería: cómo están
invertidos los competidores frente a Banistmo (tamaño, peso sobre activo, tipo de instrumento,
clasificación contable, rentabilidad estimada y calificaciones de crédito), para 2022–2026.

**Perímetro:** Banistmo · Banco General · BAC (incl. Multibank) · Global Bank · Davivienda · Scotiabank.

> ## 📅 Esta es la réplica con datos publicados en marzo de 2026
>
> Réplica del reporte con el **primer corte de datos de 2026** de la Superintendencia de Bancos de Panamá
> (SBP). Qué cambia frente a la versión base (cierre Dic-2025):
>
> - **Sistema (SBP) → actualizado a Enero 2026.** El Balance de Situación (SBN/CBI) y el Informe de
>   Actividad Bancaria más recientes a marzo de 2026 son los de **enero 2026** — **dato regulatorio no
>   auditado**, marcado `[REG]`. Se actualizan: inversiones/activo del SBN (**22.1% → 22.3%**), del CBI
>   (22.0% → 22.1%), el crecimiento de inversiones (**+10.5% a/a**), el IAC de cierre 2025 (**16.27%**) y,
>   sobre todo, las **pérdidas no realizadas de la cartera AFS/FVOCI del sistema, que se recuperaron de
>   −US$550.9 M a −US$34.4 M** (ver implicaciones contables abajo).
> - **Bancos (nivel entidad) → sin cambio.** A marzo de 2026 no hay EE.FF. auditados posteriores al cierre
>   Dic-2025 ya cargado (5 de 6 cierran en diciembre; Global Bank cierra en junio y su próximo auditado es
>   jun-2026). Todas las cifras por banco se **conservan de la versión previa**, como se pidió: "lo que no se
>   pueda actualizar, usar el dato anterior".
>
> **Implicación contable del corte (la más importante):** la reversión de casi US$516 M en pérdidas no
> realizadas de FVOCI/OCI del sistema alivia el lastre sobre patrimonio y capital regulatorio, y reduce el
> incentivo estructural que empujaba a los bancos a reclasificar bonos a **costo amortizado** para esconder
> la volatilidad de OCI. Detalle en [`datos-extraidos.md`](datos-extraidos.md) → "Implicaciones contables del corte marzo-2026".

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

Las cifras **por banco** provienen de la **lectura directa de la nota "Inversiones en valores"** (y la nota
de riesgo de crédito) de los estados financieros **auditados** de los seis bancos, a su último cierre
disponible (Banistmo/BG/BAC/Davivienda Dic-2025, Global jun-2025, Scotiabank oct-2024 standalone) — **sin
cambio en este corte**. Las cifras **de sistema** se actualizaron al último dato publicado por la SBP a
marzo de 2026 (**Enero 2026**, dato regulatorio no auditado `[REG]`). Los porcentajes de activo y los yields
marcados *Estimado* son cálculos propios.

## Metodología

- Moneda: USD (balboa a la par).
- Rendimiento de cartera estimado como `ingreso por intereses de inversiones ÷ saldo promedio`.
- **Comparabilidad:** los perímetros de reporte difieren y no son 1:1 — BAC = consolidado
  Centroamérica; Global Bank cierra fiscal en junio; Davivienda FY2025 es post-fusión con Scotiabank.
  El análisis se apoya en **ratios** (% de activo, yield, distribución por rating) robustos al perímetro.

---

*Reporte preparado para la mesa de tesorería. Datos 2022–2026.*
