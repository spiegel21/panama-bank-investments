# Radar de Inversiones — Banca de Panamá

Análisis competitivo del portafolio de **inversiones en valores** de los principales bancos de
Panamá, con **Banistmo** como banco base de comparación. Enfoque de tesorería: cómo están
invertidos los competidores frente a Banistmo (tamaño, peso sobre activo, tipo de instrumento,
clasificación contable, rentabilidad estimada y calificaciones de crédito), para 2022–2026.

**Corte vigente: 31 de marzo de 2026.** Los bancos con reporte trimestral pasan a su **1T-2026
interino no auditado** (Banistmo, Banco General, BAC, Global Bank, Banesco) y el sistema bancario a los
datos de la SBP a **marzo-2026** (Balance de Situación SBN/CBI + Informe de Actividad Bancaria,
regulatorio no auditado). **Davivienda** se conserva en su último cierre disponible (Dic-2025 auditado —
no publica interinos trimestrales; marcada **‡** en los gráficos de rendimiento por su base de anualización
distinta). **Scotiabank** (oct-2024, absorbido por Davivienda el 5-dic-2025) se **excluye de las
comparaciones**: su dato es ~17 meses anterior al corte y ya no reporta standalone. Detalle completo en `datos-extraidos.md`.

**Perímetro (comparaciones del dashboard):** Banistmo · Banco General · BAC (incl. Multibank) · Global Bank · Davivienda · **Banesco**.
**Scotiabank** queda **fuera de las comparaciones** (último dato oct-2024, ~17 meses atrás; absorbido por Davivienda en dic-2025): se conserva solo en la narrativa de consolidación y en el dataset histórico.

**Novedad (sesión 4):** se replicó, **para los siete bancos**, el rastreo renglón-por-renglón de las ganancias del portafolio
que se había hecho solo para Banistmo (un `<banco>-ganancias-inversiones.html` por banco, con capturas de páginas fuente), y se
**agregó Banesco** a todas las comparaciones. Resumen comparable en la sección "Mapa de renglones…" de `datos-extraidos.md`.

**Novedad (sesión 5):** el dashboard (`index.html`) ahora **muestra la cifra comparable de resultado del portafolio en la utilidad
neta** — no solo el yield de interés — en una nueva sección **07 "Resultado del portafolio — todos los renglones"** (tabla +
gráfico anualizado). Es el número que el rastreo renglón-por-renglón hacía visible pero que antes solo vivía en los mapas y en
`datos-extraidos.md`: interés + valuación/venta − provisiones, con el ORI no realizado mostrado aparte (patrimonio, no utilidad).

**Novedad (sesión 6):** el **rendimiento y todos los resultados** del dashboard se recalcularon sobre la base **utilidad neta + ORI
(patrimonio) = resultado integral del portafolio**, no solo el interés ni solo la utilidad neta. La sección 06 pasa a un
**rendimiento total** = (resultado integral anualizado) ÷ portafolio de cierre, con el yield de solo interés como columna de
referencia; la sección 07 añade la columna **= Resultado integral** (utilidad neta + ORI) y su gráfico anualizado ordena por esa
cifra. Incluir el ORI **reordena el ranking**: los libros con valuación no realizada positiva suben (Banistmo, Global) y
los golpeados por el alza de tasas caen (Banco General −US$42.7M, Banesco −US$6.8M en ORI). Banistmo pasa de ~3.9% (solo interés) a
**~5.5%** total. Caveat explícito: el ORI es mark-to-market que revierte, así que anualizar un
trimestre ×4 es la parte más gruesa de la estimación — la cifra es direccional.

**Novedad (sesión 7 — revisión de coherencia y comparabilidad):** (1) **Scotiabank se retira de todos los gráficos y tablas del
dashboard** por incomparabilidad temporal (oct-2024, ~17 meses antes del corte) y por estar absorbido — queda solo en la narrativa
de consolidación; con ello Banistmo pasa a **encabezar el rendimiento total (~5.5%)**. (2) En los gráficos de rentabilidad y
resultado, los bancos cuya base de anualización difiere del estándar 1T-2026 ×4 — **Global Bank** (9M del FY-junio, ×4/3) y
**Davivienda** (año FY2025, ×1) — se marcan con **‡** (rayado diagonal + leyenda) para señalar el supuesto. (3) Correcciones de
coherencia en la sección 08 (pérdidas no realizadas AFS/FVOCI mal etiquetadas en la columna 2024; IAC 2024 15.32→15.29%; se
retiró la fila de liquidez legal por no estar respaldada en `datos-extraidos.md`). (4) Se **redujo el texto** (subtítulos y notas al
pie) para dar más peso a las visualizaciones.

**Novedad (sesión 8 — yield de solo interés con denominador ajustado al cupón reconocido):** verificadas las **seis caras
del estado de resultados + notas de instrumentos financieros**, se confirmó que bajo NIIF 9 el cupón de **costo amortizado + VRCOUI
(FVOCI)** se reconoce en la línea de intereses por **tasa de interés efectiva** (Davivienda lo rotula literal), mientras el cupón
**FVTPL (VRCR)** a veces queda **embebido en la línea de valuación** y no es aislable. Regla nueva para el yield de solo interés: donde
el cupón FVTPL **no es confirmable** en la línea de intereses (resultado FVTPL en una sola línea neta), se **excluye el FVTPL del
denominador** y el yield se mide sobre **VRCOUI + costo amortizado**. Efecto material solo en **Banistmo** (35% FVTPL): su solo interés
pasa de **~3.9% (cartera total) a ~5.9%** (63.3M ÷ 1,068.9M) y **deja de ser el más bajo del perímetro**. Se aplica también, sin efecto
visible, a Davivienda (0.5%) y Banesco (0.3%); **Banco General, BAC y Global mantienen el denominador completo** porque su nota de
instrumentos financieros confirma que el cupón FVTPL sí está en la línea de intereses. El **rendimiento total** (util. neta + ORI)
conserva el **denominador completo**. Caveat Banistmo: rango **3.9%–5.9%** según dónde caiga el cupón FVTPL.

## Sitio publicado

El reporte se sirve como página estática vía **GitHub Pages**:

**https://spiegel21.github.io/panama-bank-investments/**

`index.html` es autocontenido (HTML + CSS + JS inline, sin dependencias externas): se puede abrir
directamente en cualquier navegador incluso sin el sitio.

## Contenido

| Archivo | Qué es |
|---|---|
| `index.html` | Reporte visual interactivo en español (la página publicada). |
| `<banco>-ganancias-inversiones.html` | **Mapas de renglones — ganancias del portafolio, uno por banco (6 activos enlazados desde el dashboard + Scotiabank retenido como histórico).** Rastreo, renglón por renglón, de todos los lugares del último EE.FF. de cada banco donde se reconoce ganancia/ingreso del portafolio de valores (interés, valuación/venta, ORI y provisiones), con capturas de las páginas fuente. El hallazgo comparable: **cada banco "esconde" la ganancia de forma distinta** — Banistmo (`banistmo-…`) mezcla divisas+derivados en el renglón; Banco General (`bancogeneral-…`) lo mezcla con derivados; BAC (`bac-…`) lo tiene limpio con el FX aparte; Global Bank (`globalbank-…`) lo embebe en "Otros ingresos"; Davivienda (`davivienda-…`) usa dos líneas limpias; Banesco (`banesco-…`) reporta dos pérdidas con la FVTPL mixta con derivados. `scotiabank-…` se conserva como referencia histórica pero **ya no se enlaza** desde `index.html` (banco absorbido, fuera de las comparaciones). Enlazados desde `index.html` (sección "Renglones"). |
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
confirmado ausente en SMV, SBP, davibank.pa y Latinex; marcada **‡** en los gráficos de rendimiento).
**Scotiabank** (oct-2024, absorbido por Davivienda) queda **fuera de las comparaciones del dashboard** por
incomparabilidad temporal; se conserva solo en el dataset histórico y la narrativa de consolidación. Los
porcentajes de activo y los yields marcados *Estimado* son cálculos propios. Detalle completo, con nivel de
confianza por cifra, en `datos-extraidos.md`.

## Metodología

- Moneda: USD (balboa a la par).
- **Rendimiento total** de cartera estimado como `(resultado en utilidad neta + ORI no realizado) anualizado ÷ portafolio de cierre`
  — es decir el aporte completo del portafolio (interés + valuación/venta − provisiones + valuación no realizada a patrimonio). El
  yield de **solo interés** se conserva como columna de referencia estable, sin mark-to-market. Su denominador es la **cartera que
  devenga cupón en la línea de intereses** (`interés anualizado ÷ (VRCOUI + costo amortizado + FVTPL cuando su cupón está confirmado en
  la línea)`): bajo NIIF 9 el cupón de costo amortizado y VRCOUI entra a la línea de intereses por tasa efectiva, pero el cupón FVTPL a
  veces queda embebido en la línea de valuación; donde no es aislable se **excluye el FVTPL del denominador** (solo material en
  Banistmo). Detalle y clasificación por banco en `datos-extraidos.md` (nota metodológica §).
- **Comparabilidad:** los perímetros de reporte difieren y no son 1:1 — BAC = consolidado
  Centroamérica; Global Bank cierra fiscal en junio; Davivienda FY2025 es post-fusión con Scotiabank.
  El análisis se apoya en **ratios** (% de activo, yield, distribución por rating) robustos al perímetro.
- **Interino vs. auditado:** los interinos no auditados de este corte no re-divulgan siempre la misma
  profundidad que un cierre anual auditado (ratings, escalera de vencimientos, composición detallada);
  donde falta, se usa el último dato auditado disponible, marcado explícitamente como *carried* en
  `datos-extraidos.md`.

---

*Reporte preparado para la mesa de tesorería. Datos 2022–2026.*
