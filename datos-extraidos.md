# Dataset extraído — Inversiones bancos Panamá

Fuente de verdad detrás del reporte HTML. Cada cifra lleva nivel de confianza:

- **[AUD]** Auditado — leído directamente de la nota "Inversiones en valores" de los EE.FF. auditados.
- **[INT]** Interino no auditado — leído del estado financiero trimestral (1T-2026) que el emisor publica
  entre cierres auditados. No lleva notas completas (composición/ratings suelen no re-tabularse).
- **[REG]** Regulatorio no auditado — dato del Sistema Bancario Nacional / Centro Bancario Internacional
  publicado por la Superintendencia de Bancos de Panamá (SBP), no es un EE.FF. de emisor.
- **[EST]** Estimado — cálculo o derivación propia.
- **[PEND]** Pendiente — no divulgado por el emisor (queda como límite del análisis, no como pendiente de lectura).

Moneda: USD (B/. a la par). Todas las cifras en US$ salvo indicación. Cifras "en unidades" (no miles) salvo nota.

> **Estado: CORTE 31-MARZO-2026.** Tercera sesión: se actualizó el reporte al primer trimestre calendario
> de 2026. Los bancos que publican interinos trimestrales pasan a su **1T-2026 no auditado [INT]**
> (Banistmo, Banco General, BAC, Global Bank); el sistema pasa al **dato SBP de marzo-2026 [REG]**
> (Balance de Situación SBN/CBI + IAB-0326). Se conservan dos excepciones, claramente marcadas:
> **Davivienda** no publica interinos trimestrales (confirmado ausente en SMV, SBP, davibank.pa y Latinex)
> — se mantiene su cierre **Dic-2025 auditado**; solo existe un proxy regulatorio SBP individual (entidad,
> no consolidado) que se cita como memo direccional, **fuera del ranking**. **Scotiabank** sigue congelado
> en **oct-2024** (absorbido por Davivienda el 5-dic-2025, ya no reporta standalone). Los interinos 1T-2026 de
> Banistmo, Banco General, BAC y Global **sí re-divulgan la composición completa por instrumento a Mar-2026**
> (MBS/CMO, UST, soberano, corporativo, acciones), con comparativo del cierre anterior. Detalle de las
> implicaciones contables del corte al final del documento.

---

## Hallazgos de cabecera (correcciones al corte preliminar)

1. **El gran tenedor de MBS es Banco General, NO BAC.** Banco General mantiene ~**US$3,051 millones** en
   MBS + CMO (≈51% de su cartera de inversiones a Mar-2026; Dic-2025: 3,056M), 100% garantizados por agencias de EEUU
   (GNMA/FNMA/FHLMC). **BAC NO divulga MBS** en su nota (solo bonos de gobierno, corporativos y
   acciones) — confirmado también en el interino Mar-2026. Esto invierte la conclusión preliminar "MBS confirmado solo en BAC".
2. **US Treasuries / gob. EEUU cuantificados** (Mar-2026 interino salvo Scotia): Banistmo (340M, ~21%), **BAC (856M gob.
   EEUU, ~15% — subió desde 703M en el trimestre)**, Banco General (81M explícito + Letras del Tesoro — bajó desde 130M),
   Scotiabank (176M, 47%, oct-24). Global Bank y Davivienda no los desglosan por país (solo "gubernamental").
3. **Peso sobre el activo — ranking real (corte 31-mar-2026):** Banco General 28.6% (líder amplio) >
   Davivienda 23.4% (Dic-2025, carried) > **Sistema SBN 23.0% (Mar-2026 [REG])** > Banistmo 15.6% >
   **BAC 13.4%** > **Global 12.7%** > Scotiabank 9.7%. Cambio de orden vs. el corte Dic-2025: BAC
   adelanta a Global (su cartera saltó +12.5% en el trimestre, casi todo a soberanos centroamericanos
   sub-grado) y el Sistema (SBN) sube por encima de Banistmo.
4. **Banistmo redujo el trading en el trimestre:** FVTPL bajó de 37.0% (Dic-2025) a **35.0% (1T-2026
   [INT])** — sigue siendo, junto con BAC en composición de gobierno, de los libros más activos, pero
   el libro total también se contrajo -2.7% en el trimestre. BG se mantiene con el mix FVOCI más alto
   (84.9%) y BAC con el AFS/VRCOUI más concentrado (96.3%).

---

## Sistema bancario (SBP — Informe de Actividad Bancaria)

Escopos: **SBN** = Sistema Bancario Nacional (licencia general en Panamá);
**CBI** = Centro Bancario Internacional (SBN + licencia internacional; agregado titular).

> **Benchmark del ratio Inversiones/Activo = SBN (banca de licencia general)**, no CBI. El % inversiones/activo
> y el nivel de inversiones del sistema se toman del **Balance de Situación del Sistema Bancario Nacional** que
> publica la SBP (Mar-2026), que excluye la licencia internacional. Se conserva el CBI solo como referencia.

| Indicador | 2024 (Dic) | 2025 (Dic) | **2026 (Mar)** | Conf. |
|---|---|---|---|---|
| **Inversiones en valores neta — SBN** | 29,285.5 | 32,152.8 | **33,389.6** | [REG] |
| **Activo total neto — SBN** | 140,383.5 | 145,675.3 | **145,432.5** | [REG] |
| **% inversiones / activo — SBN (lic. general)** | 20.9% | 22.1% | **23.0%** | [EST] |
| Inversiones — var. a/a SBN | +7.0% | +9.8% | **+15.0%** | [REG] |
| — memo: Inversiones neta CBI | 34,195.9 | 35,897.3 | **36,959.1** | [REG] |
| — memo: Activo total CBI | 156,391.5 | 163,014.7 | **164,208.5** | [REG] |
| — memo: % inversiones / activo CBI | 21.9% | 22.0% | **22.5%** | [EST] |
| — memo: Inversiones — var. a/a CBI | | | **+8.30%** | [REG] |
| Índice adecuación capital (IAC, CBI) | 15.29% | 16.27% | **16.27%** | [REG] |
| **Pérdidas/ganancias no realizadas AFS/FVOCI — SBN** | | -93.6 | **-10.9** | [REG] |
| **Pérdidas/ganancias no realizadas AFS/FVOCI — CBI** | | -63.4 | **+4.7** | [REG] |

Notas:
- Sistema **dominado por crédito**: préstamos siguen siendo el bloque mayor del activo; inversiones ya
  representan **23.0% del activo del SBN a marzo de 2026** (2.º bloque productivo, subiendo).
- **Base licencia general (SBN), Mar-2026:** inversiones 33,389.6M / activo 145,432.5M = 23.0% (Dic-2025:
  22.1%; Mar-2025: 20.9%); crecimiento de inversiones **+15.0% a/a** (acelerando frente al +9.8% a/a de
  Dic-2025). Es la base correcta para comparar contra los seis bancos del perímetro (todos de licencia
  general). El CBI (que suma la licencia internacional) da 22.5% a Mar-2026 (+8.30% a/a) — más bajo que
  el SBN porque la licencia internacional creció menos; la diferencia principal sigue siendo de perímetro,
  no de fecha.
- **Cambio de signo en las pérdidas no realizadas AFS/FVOCI — el dato más relevante del corte:** el SBN
  redujo su pérdida no realizada de -93.6M (Dic-2025) a **-10.9M (Mar-2026)**, y el CBI **cruzó a terreno
  positivo: +4.7M** (Dic-2025: -63.4M; Mar-2025: -473.8M). Es la primera lectura con ganancia neta no
  realizada en la serie reciente — ver "Implicaciones contables del corte marzo-2026" más abajo.
- Ingreso por inversiones del sistema **+8.5% a/a** (Mar-2026 vs. Mar-2025).
- El sistema no publica split instrumento (soberano/corp/MBS) ni interno/externo de la cartera de valores. [PEND]
- Contexto: Panamá perdió grado de inversión con Fitch (mar-2024); presión de Moody's sobre bancos PA.
- Fuente: Balance de Situación SBN/CBI 2026/03 e Informe de Actividad Bancaria IAB-0326 (SBP).

---

## Banistmo, S.A. y Subsidiarias (banco base) — consolidado Panamá

Fuente: IN-A 2024 (Nota 7, auditado) + Interino 30-sep-2025 (Nota 7, no auditado) + **Interino
31-mar-2026 (Nota 7, no auditado)**.

Fuente: **IN-A / EE.FF. Consolidados 2025 (Dic-2025, AUDITADO)**, Nota 7, p.85-87; activo p.10. Corte
vigente del reporte: **1T-2026 interino no auditado** (assets.ctfassets.net, informe completo firmado).

| Métrica | Dic-2024 | Dic-2025 (aud.) | **Mar-2026 (interino)** | Conf. |
|---|---|---|---|---|
| Inversiones en valores, neto | 1,548,786,610 | 1,689,230,275 | **1,643,344,092** | [INT] |
| — FVTPL (VRCR) | 530,775,476 (34.3%) | 625,714,847 (37.0%) | **574,432,415 (35.0%)** | [INT] |
| — FVOCI (ORI) | 435,323,046 (28.1%) | 328,871,417 (19.5%) | **335,452,354 (20.4%)** | [INT] |
| — Costo amortizado | 582,688,088 (37.6%) | 734,644,011 (43.5%) | **733,459,323 (44.6%)** | [INT] |
| Activo total | 10,471.8 | 10,570,213,274 | **10,503,719,926** | [INT] |
| % inversiones / activo | 14.8% | 16.0% | **15.6%** | [EST] |

El libro se contrajo **-2.7%** en el trimestre (1,689.2M → 1,643.3M), con el FVTPL cediendo 2.0pp
(37.0% → 35.0%) — la primera baja de la serie tras tres años de subida ininterrumpida.

(Interino Sep-2025 no auditado, para referencia: total 1,620,459,320; FVTPL 591.5M / FVOCI 359.1M / CA 669.9M.)

**Composición por instrumento (Dic-2025 auditado, bruto por buckets):** [AUD]
- **Corporativos:** 11.0M (FVTPL) + 10.4M (FVOCI) + **715.7M (CA)** = **737.1M (~43.6%)** — el 96% en costo
  amortizado (held-to-maturity), por eso casi no se ve en las tablas de valor razonable/trading.
- **Soberano Panamá:** 257.2M (FVTPL) + 253.8M (FVOCI) = **511.1M (~30.3%)** (+ soberanos 29.0M en CA)
- **US Treasuries (Bonos EEUU):** 321.9M (FVTPL) + 8.0M (FVOCI) = **329.9M (~19.5%)**
- Otros soberanos (México, Colombia, Costa Rica, Rep.Dom, Alemania, Chile) + CERPANES: ~59M
- Patrimonio/acciones: 0 (FVTPL) + 32.8M (FVOCI) = 32.8M (~1.9%)
- **Sin MBS** (solo bonos y acciones).

**Composición por instrumento (Mar-2026, interino no auditado):** [INT]
- **Corporativos ~726M (~44.2%)** — CA 714.1M, casi todo held-to-maturity, en línea con Dic-2025.
- **Soberano Panamá:** FVTPL 217.8M + FVOCI 278.6M = **496.4M (~30.2%)** — estable frente a Dic-2025.
- **US Treasuries:** 340.1M (FVTPL) (**~20.7%**) — sube levemente en peso relativo.
- Patrimonio/acciones: 32.8M (sin cambio).
- **Sin MBS.** El mix de instrumento apenas se mueve trimestre a trimestre; el cambio grande está en el
  balance total (-2.7%) y en el mix contable (FVTPL 37.0%→35.0%), no en la composición subyacente.

**Verificación del ~40% corporativo (pregunta recurrente):** leído verbatim de la Nota 7.3, línea
"Bonos corporativos": 715,722,265 (Dic-2025) / 565,776,724 (Dic-2024). Las tres categorías (FVTPL/FVOCI/CA)
son mutuamente excluyentes → no hay doble conteo. Corporativo = 40.8% (Dic-24) → 41.9% (Sep-25) → 43.6% (Dic-25),
**subiendo**. Alto porque el grueso es papel held-to-maturity a costo amortizado, invisible en vistas de trading.

**Riesgo / duración (reporte S&P anexo al IN-A, dato a sep-2024):** [AUD cualit.]
- **Duración promedio del portafolio: 2.5 años.** VaR sobre patrimonio < 1%.
- Deuda pública Panamá + EEUU ≈ 50% del total (a Dic-2025: US 330M + Panamá 511M = 841M ≈ 50%).

- **Ingreso por intereses de inversiones (2025, consolidado auditado):** 58,242,379 (2024: 59,312,669) → yield ≈ 3.6% [EST]
  (leído de la línea **"Valores y otros"** del Estado de Ganancias o Pérdidas Consolidado, p.11; saldo promedio Dic-24/Dic-25 = 1,619.0M).
  **Corrección:** el corte previo usaba erróneamente la entidad individual SBP 2024 (64.19M → 4.3%) bajo el supuesto de que el consolidado no lo desglosaba — sí lo desglosa. Con la cifra consolidada correcta, Banistmo cerraba la tabla de yields (el de menor rendimiento del perímetro), consistente con su portafolio de mayor calidad (deuda EEUU + Panamá ≈ 50%).
- **Ingreso por intereses de inversiones (1T-2026, interino, "Valores y otros"):** 15,828,245 (1T-2025:
  13,574,986) → anualizado ~63.3M → **yield ≈ 3.9% [INT]** (63.3M ÷ cartera de cierre 1,643.3M; método saldo de cierre). Sigue siendo el yield más bajo del perímetro
  (portafolio de mayor calidad crediticia), aunque sube ligeramente por el mix hacia FVTPL.
- **Hallazgo estructural:** giro a *trading + held-to-maturity* — FVTPL 11.8% (2023) → 34.3% (2024) → 37.0%
  (Dic-2025) → **35.0% (Mar-2026)**; FVOCI 50.5% → 19.5% → 20.4%; costo amortizado 37.6% → 43.5% → 44.6%.
  El más "trading" del perímetro por FVTPL en niveles absolutos, aunque el trimestre marca la primera
  pausa/reversión de esa tendencia.
- Banistmo **sí publica** la tabla de ratings de la cartera (nota de riesgo, pp.66-67), aunque **no** una
  escalera de vencimientos de inversiones (la duración ~2.5a proviene del reporte de la calificadora). [AUD/PEND]
  El interino Mar-2026 (Nota 5) combina la tabla de ratings con efectivo — no se re-extrae por separado en este corte.
- **Evento corporativo:** cambio de control (Cuscatlán) con autorización de emisión pendiente al 30-abr-2026;
  no afecta las cifras de este corte pero es relevante para el próximo. [INT]

---

## Banco General, S.A. y Subsidiarias — consolidado Panamá (mayor banco privado)

Fuente: EE.FF. consolidados Dic-2025 (Nota 6 "Inversiones y otros activos financieros", auditado), con
comparativo Dic-2024 en la misma nota. Corte vigente: **interino 31-mar-2026 no auditado** (bgeneral.com,
"INT y EF" publicado 2026/05).

| Métrica | Dic-2024 | Dic-2025 | **Mar-2026 (interino)** | Conf. |
|---|---|---|---|---|
| Inversiones y otros activos financieros, neto | 5,347,770,702 | 5,968,302,539 | **5,985,577,441** | [INT] |
| — FVTPL (VRCR) | 829,554,142 (15.5%) | 942,225,934 (15.8%) | **869,967,677 (14.5%)** | [INT] |
| — FVOCI (ORI) | 4,511,601,422 (84.4%) | 5,022,886,623 (84.2%) | **5,083,044,613 (84.9%)** | [INT] |
| — Costo amortizado | 6,615,138 (0.1%) | 3,189,982 (0.05%) | **32,561,889 (0.5%)** | [INT] |
| Activo total | 19,447,499,026 | 20,879,794,387 | **20,965,852,704** | [INT] |
| % inversiones / activo | 27.5% | 28.6% | **28.6%** | [EST] |

El libro apenas se mueve en el trimestre (+0.3%, 5,968.3M → 5,985.6M); el % sobre activo se mantiene
en 28.6%, el más alto del perímetro por un margen amplio.

**Composición por instrumento (Mar-2026, interino — la Nota 6 SÍ re-tabula la composición completa; comparativo Dic-2025):** [INT]
- **MBS + CMO = 3,050.8M (~51% de la cartera)** (Dic-2025: 3,055.6M) — 100% del MBS garantizado GNMA/FNMA/FHLMC
  (agencias EEUU); 66% de los CMO respaldados por esos MBS. **El mayor tenedor de MBS del perímetro.**
- ABS: 204.3M (Dic-2025: 207.9M)
- **US Treasuries (Bonos Gob EEUU):** 81.2M (FVOCI) (Dic-2025: 130.3M — **baja ~US$49M en el trimestre**) + Letras del Tesoro extranjeras 89.0M
- Bonos corporativos: 195.7M (FVTPL) + 2,129.4M (FVOCI) ≈ **2,325.1M** (Dic-2025: ~2,273M) — más papeles comerciales/letras locales 61.0M
- Soberano Panamá: **84.5M** (Dic-2025: 98.1M); otros gobiernos 14.2M
- Acciones: **42.9M** (Dic-2025: 37.1M)
- **Duración divulgada solo para MBS (3.71a) y CMO (1.79a);** no del portafolio total. [AUD parcial]
- Color del interino: los corporativos regionales bajan de 1,687.1M a **1,587.3M**; el gran movimiento del trimestre
  es la reducción de la exposición directa a UST (130.3→81.2M).

- **Ingreso por intereses de inversiones (2025, auditado):** 283.5M (2024: 265.6M) → yield ≈ 5.0% [EST]
- **Ingreso por intereses de inversiones (1T-2026, interino):** 73,406,405 (1T-2025: 67,896,754) →
  anualizado ~293.6M → **yield ≈ 4.9% [INT]**
- Perfil: renta fija de **alta calidad, grado de inversión**, con núcleo de agency-MBS de EEUU (líquido).
- Ratings: núcleo extranjero AAA-AA+ (los agency-MBS); local grueso "< BBB-" (papel panameño). [AUD, carried]
- Escalera de vencimientos (por posible fecha de venta): ≤3m 4,970M (grueso, MBS líquidos) · 1-5a 462M ·
  5-10a 253M · >10a 39M. [AUD, carried]

---

## BAC International Bank, Inc. y Subsidiarias — consolidado Centroamérica (OJO perímetro)

Fuente: EE.FF. auditados Dic-2025 (Nota 8), con comparativos 2024/2023. Consolidado CR+PA+GT+HN+SV+NI.
Corte vigente: **interino 31-mar-2026 no auditado** (baccredomatic.com, PAN_EF_BIB_SUBS_0326, publicado 2026/05).

| Métrica | 2024 | 2025 | **Mar-2026 (interino)** | Conf. |
|---|---|---|---|---|
| Inversiones en valores, neto | 4,883,433,488 | 4,989,837,727 | **5,615,413,793** | [INT] |
| — VRCR (FVTPL) | 35,201,978 | 45,673,846 | **22,895,131 (0.4%)** | [INT] |
| — VRCOUI (FVOCI/AFS) | 4,737,704,498 | 4,756,274,848 | **5,407,901,838 (96.3%)** | [INT] |
| — Costo amortizado | 110,527,012 | 187,889,033 | **184,616,824 (3.3%)** | [INT] |
| Activo total | 37,970,437,089 | 40,747,080,228 | **42,015,857,874** | [INT] |
| % inversiones / activo | 12.9% | 12.3% | **13.4%** | [EST] |

**El libro saltó +12.5% en el trimestre** (4,989.8M → 5,615.4M, +US$625.6M) — el mayor movimiento
trimestral del perímetro — y el % sobre activo pasó de 12.3% (Dic-2025) a **13.4%**, adelantando a
Global Bank en el ranking. Casi todo el incremento entró a VRCOUI en soberanos centroamericanos
sub-grado de inversión (ver ratings abajo).

**Composición por instrumento (Mar-2026, interino Nota 8; comparativo Dic-2025):** [INT]
- **Otros gobiernos Centroamérica: 4,168.2M (~74%)** (Dic-2025: 3,651.7M) — núcleo soberano centroamericano;
  **absorbió casi todo el crecimiento del trimestre (+US$516M)**.
- **US gobierno y agencias: 856.1M (~15%)** (Dic-2025: 703.2M — **+US$153M**) — no separa Treasuries de agencias.
- Bonos corporativos: 360.3M (VRCOUI) + 119.4M (CA) ≈ **479.7M** (Dic-2025: ~521M); acciones 19.8M (VRCR) + 3.5M (VRCOUI) ≈ 23.3M.
- **MBS: NO divulgado** (verificado también en el interino Mar-2026: no aparece línea hipotecaria en Nota 8 ni Nota 18;
  todo "hipotecario" es cartera de préstamos). Corrige la creencia preliminar de MBS en BAC.

- **Ingreso por intereses de inversiones (2025, auditado):** 291.4M (2024: 299.9M) → yield ≈ 5.9% [EST]
- **Ingreso por intereses de inversiones (1T-2026, "Inversiones en valores"):** 76,787,220 (1T-2025:
  74,243,812) → anualizado ~307.1M → **yield ≈ 5.5% [INT]** (307.1M ÷ cartera de cierre 5,615.4M) — el más alto del perímetro. Nota: la cartera creció +12.5% en el trimestre, así que sobre saldo promedio el yield sería ~5.8%.
- **Perímetro:** consolidado Centroamérica (NO solo Panamá). Entidad individual Panamá ≈US$13.3 mil M
  activos (Dic-2025, composición de cartera no divulgada aparte). NO confundir. [AUD]
- **Ratings VRCOUI gobierno (Mar-2026, interino):** AA+ 856.1M · BBB 5.6M · BBB- 706.7M · **BB+ a B-
  3,455.9M** (total gob. 5,024.3M; Dic-2025: 4,354.9M) — el bracket sub-grado subió de 2,967.6M a
  **3,455.9M**, casi todo el incremento del trimestre. Corp VRCOUI ~383.6M; CA gob BB+ a B- 65.3M +
  corp BB+ a B- 119.4M = 184.6M (todo sub-grado); VRCR BB 22.9M.
  → **Grado inversión total ≈ 1,798M (~32%) / sub-grado ≈ 3,817M (~68%)** — el sub-grado sube de peso
  frente a Dic-2025, reflejando el giro hacia soberanos centroamericanos. [INT]
- Vencimientos Dic-2025 (línea combinada inv+otros): ≤1a 2,088.6M · 1-5a 2,281.6M · >5a 1,455.7M. [AUD]
- **Rating emisor:** S&P BBB-/A-3 estable (6-ago-2025).

---

## Global Bank Corporation y Subsidiarias — consolidado Panamá (cierre fiscal JUNIO)

Fuente: EE.FF. auditados 30-jun-2025 (Nota 9), con comparativo FY2024 (jun-24) en la misma nota. Corte
vigente: **interino 31-mar-2026 no auditado (9 meses de su año fiscal, Q3 FY2026)** — globalbank.com.pa,
ef-global-bank-marzo-2026.

| Métrica | FY2024 (jun) | FY2025 (jun) | **Mar-2026 (9mo interino)** | Conf. |
|---|---|---|---|---|
| Inversiones en valores, neto | 1,049,326,162 | 1,136,648,533 | **1,123,956,951** | [INT] |
| — FVTPL (VRCR) | 71,631,682 | 69,298,285 | **70,498,566 (6.3%)** | [INT] |
| — FVOCI (ORI) | 566,447,182 | 674,051,469 | **627,060,676 (55.8%)** | [INT] |
| — Costo amortizado | 402,341,535 | 383,980,942 | **419,586,518 (37.3%)** | [INT] |
| Activo total | 8,520,282,632 | 8,503,001,576 | **8,833,254,505** | [INT] |
| % inversiones / activo | 12.31% | 13.37% | **12.7%** | [EST] |

\* FY2022/FY2023 headline provienen de indexación previa (la URL "FY2023" servía en realidad los EE.FF.
FY2019 — mismatch de fuente; FY2024/FY2025 sí leídos de la nota auditada). El interino Mar-2026 compara
contra jun-2025 (auditado) por ser el último cierre de año fiscal; el activo total del banco creció más
rápido que la cartera de inversiones en el período, así que el % sobre activo cede de 13.37% a 12.7%.

**Composición por instrumento (Mar-2026, interino Nota 9 — desglose local/extranjero, cotiza/no cotiza):** [INT]
- Gobierno **518.0M**, corporativo/deuda privada **525.3M**, acciones **73.9M**. **Sin MBS** (consistente con FY2025).
  (Nota: total de notas 9.1+9.2+9.3 = 1,117.1M; el neto del balance 1,124.0M incluye intereses por cobrar.)
- Tasas FVOCI en el rango 2.50%–9.375%.
- **US Treasuries: sigue sin desglosarse por país** en el interino (igual que en el auditado FY2025).

- **Ingreso por intereses de inversiones (FY2025, auditado):** 45.6M (FY2024: 40.5M) → yield ≈ 4.2% [EST]
- **Ingreso por intereses de inversiones (trimestre Q3, ene-mar 2026):** 11,148,939 → anualizado ×4 ~44.6M
  → **yield ≈ 4.0% [INT]** (44.6M ÷ cartera de cierre 1,124.0M; método saldo de cierre). Acumulado 9 meses: 36,843,768 (previo 33,857,191).
- Ratings FY2025 (auditado, carried — el interino no re-tabula ratings): grado inversión 562.5M ·
  monitoreo estándar (BB+ a B-) 186.1M · sin calificación 383.8M. [AUD]
- Vencimientos FY2025: FVOCI 1-5a 350.1M / >5a 143.6M; CA 1-5a 111.2M / >5a 262.7M (libro largo a CA). [AUD]
- Sensibilidad ±100pb del ingreso: -46.4M / +53.0M. NIIF 17 desde 1-jul-2024.
- **Rating emisor:** S&P y Fitch BBB-, estable.

---

## Banco Davivienda (Panamá), S.A. y Subsidiarias — consolidado (post-fusión Scotiabank)

> **Sin interino 1T-2026 — se mantiene el cierre Dic-2025 auditado.** Davivienda **no publica estados
> financieros interinos trimestrales**: se confirmó su ausencia en SMV (supervalores.gob.pa), SBP
> (superbancos.gob.pa), davibank.pa y Latinex. Todas las cifras de esta sección quedan **CARRIED FORWARD
> de Dic-2025 (auditado)**, sin cambio frente al corte anterior. La única cifra nueva a marzo-2026 es un
> **memo direccional**, no comparable ni usado en el ranking (ver abajo).

Fuente: EF Local 2025 (consolidado auditado, Nota 8). FY2025 es el **primer cierre post-fusión** (absorbe
The Bank of Nova Scotia — Sucursal de Panamá, 5-dic-2025).

| Métrica | Dic-2024 | Dic-2025 (post-fusión) | Conf. |
|---|---|---|---|
| Inversiones en valores, neto | 455,271,607 | **1,248,452,413** | [AUD] |
| — FVTPL (VRCR) | 0 | 6,164,984 | [AUD] |
| — FVOCI (VRCOUI) | 259,374,130 | 988,382,401 (79%) | [AUD] |
| — Costo amortizado | 195,897,477 | 253,905,028 (20%) | [AUD] |
| Activo total | 1,816,389,671 | 5,342,265,863 | [AUD] |
| % inversiones / activo | 25.1% | **23.4%** | [EST] |

**Composición por instrumento (2025):** [AUD]
- Bonos gubernamentales: 923.3M (FVOCI) + 6.2M (FVTPL) — **núcleo soberano dominante**.
- Bonos corporativos: 64.8M (FVOCI) + 257.7M (CA bruto). Acciones 0.2M.
- **US Treasuries: NO desglosado** (solo "gubernamentales"); Norteamérica (geo) 412.75M FVOCI + 27.5M CA.
- **MBS: NO.**

- **Ingreso por intereses de inversiones (2025):** 34.5M (2024: 27.7M) → **yield ≈ 4.05%** (saldo prom.) [EST]
- Adquirió **318.5M de inversiones de Scotiabank** al 1-dic-2025 (nota de combinación de negocios).
- Ratings (VRCOUI 2025): AAA-AA− 397.4M · A 6.0M · BB+ a BB− 519.9M (gob); corp BBB 32.0M / BB 29.2M. [AUD]
- Vencimientos 2025: ≤1a 747.0M · 1-5a 466.0M · >5a 147.0M. VaR cartera 806,880 (límite 1.76M). [AUD]
- **Tratar a Davivienda (no a Scotiabank) como el competidor a futuro.** FY2025 no comparable con años previos.
- Davivienda Internacional (offshore, entidad separada): inversiones 0 en 2025 (2024: 25.1M corp, redimido).

**Memo proxy Mar-2026 (SBP regulatorio, entidad INDIVIDUAL, no auditado — NO comparable al consolidado
de arriba, NO usado en ranking ni gráficos):** [REG memo]
- Inversiones ~1,314.9M / activo ~4,990.8M; ingreso por inversiones 1T-2026 ~17.9M.
- Es un dato de perímetro distinto (entidad individual Panamá vs. consolidado con Davivienda
  Internacional) y sin split FVTPL/FVOCI/CA, sin composición por instrumento y sin tabla de ratings —
  **direccional solamente**. Se cita aquí por transparencia, no altera ninguna cifra de la sección
  consolidada ni el ranking del "Resumen para gráficos".

---

## Scotiabank (Sucursal de Panamá) — cierre fiscal OCTUBRE — ABSORBIDO (dic-2025)

> **Sin cambio en este corte.** Scotiabank fue absorbido por Davivienda el 5-dic-2025 y ya no reporta
> standalone; se conserva su último cierre disponible, **oct-2024 (auditado)**, sin actualización.

Fuente: EE.FF. FY2024 (31-oct-2024, Nota 8), con comparativo oct-2023. Último año standalone.

| Métrica | oct-2023 | oct-2024 | Conf. |
|---|---|---|---|
| Inversiones en valores, neto | 359,289,454 | **371,322,361** | [AUD] |
| — FVOCI (VRCOUI) | 296,018,162 | 318,896,535 | [AUD] |
| — Costo amortizado | 63,271,292 | 52,425,826 | [AUD] |
| Activo total | 3,744,781,864 | 3,841,407,316 | [AUD] |
| % inversiones / activo | 9.6% | **9.67%** | [EST] |

**Composición por instrumento (oct-2024):** [AUD]
- **US Treasuries (Bonos Gob EEUU): 176.3M (47% de la cartera)** — línea explícita, la mayor proporción
  de UST del perímetro. Cruzado con la concentración geográfica "Canadá y EEUU".
- Soberano Panamá: 141.3M. Corporativos (CA): 53.8M bruto. Sin acciones. Sin FVTPL. **Sin MBS.**

- **Ingreso por intereses de inversiones (2024):** 15.0M → **yield ≈ 4.1%** [EST]. Tasa CA: 4.20%–6.17%.
- Ratings: VRCOUI AA+ a A 176.6M / BBB 142.2M; CA AA+ a A− 23.9M / BBB a BB+ 28.5M. [AUD]
- Vencimientos VRCOUI: ≤3m 27.8M / 3m-1a 67.6M / 1-5a 222.2M (sin tramo >5a). [AUD]
- A futuro el competidor es Davivienda, no Scotiabank (esta entidad ya no reporta standalone).

---

## Distribución por calificación — normalizada (para comparabilidad)

Cada banco publica su tabla de ratings con **cortes de letra y coberturas distintas**, así que se
colapsan a tres brackets comparables sobre la **cartera calificada divulgada** de cada uno:
**Grado de inversión (AAA→BBB-)** · **Sub-grado / monitoreo estándar (BB+ a B-)** · **Sin calificación (NR)**.
Fuente: nota de riesgo de crédito de cada EE.FF. auditado (montos verificados y reconciliados con el total).

| Banco (fecha) | Cobertura de la tabla | Grado inversión (AAA→BBB-) | Sub-grado (BB+ a B-) | Sin calif. | Total calificado |
|---|---|---|---|---|---|
| Banco General (Dic-25, carried) | deuda (excl. acciones 37M) | **4,536.0 (76.5%)** | 1,395.1 (23.5%) | 0.05 (~0%) | 5,931.2 |
| **BAC (Mar-26, interino)** | bonos VRCR+VRCOUI+CA | **~1,798 (~32.0%)** | **~3,817 (~68.0%)** | 0 | ~5,615 |
| Global Bank (jun-25) | toda la cartera | 562.5 (49.7%) | 186.1 (16.4%) | **383.8 (33.9%)** | 1,132.3 |
| Davivienda (Dic-25) | VRCOUI+VRCR (excl. CA 253.9M) | 437.4 (44.3%) | **549.1 (55.6%)** | 1.8 (0.2%) | 988.3 |
| Scotiabank (Oct-24) | toda la cartera | **342.7 (92.3%)** | 28.5 (7.7%)* | 0 | 371.3 |
| Banistmo (Dic-25) | toda la cartera (nota de riesgo) | 924.9 (54.8%) | 710.7 (42.1%) | 53.7 (3.2%) | 1,689.2 |

Detalle de brackets leído de la fuente (US$, 2025 salvo Scotia oct-24):
- **Banco General:** AAA→AA+ 3,334.0 · AA→BBB- 1,202.0 · <BBB- 1,395.1 · NR 0.05. El bucket <BBB- es
  casi todo **papel local de Panamá** (local <BBB- 1,034.2). [AUD]
- **BAC (Mar-2026, interino):** VRCOUI gob AA+ 856.1 · BBB 5.6 · BBB- 706.7 · **BB+ a B- 3,455.9** (total
  gob. 5,024.3M; Dic-25: AA+ 728.3 · BBB 5.6 · BBB- 653.3 · BB+ a B- 2,967.6, total gob. 4,354.9M); corp
  VRCOUI IG+sub ~383.6M; CA gob BB+ a B- 65.3 · CA corp BB+ a B- 119.4 (=184.6, todo sub-grado); VRCR BB
  22.9. El grueso sub-grado son **soberanos de Centroamérica** y ese bracket es el que absorbió casi todo
  el crecimiento de +US$625M del trimestre. [INT]
- **Global Bank:** grado inversión 562.5 · monitoreo estándar (BB+ a B-) 186.1 · **sin calif. internacional
  383.8**. El 34% sin calificar es papel local sin rating internacional. [AUD]
- **Davivienda:** gob AAA→AA− 397.4 · A 8.0 · BBB 32.0 · **BB 549.1** · NR 1.8. (La tabla no cubre el bucket
  a costo amortizado 253.9M.) [AUD]
- **Scotiabank:** VRCOUI AA+ a A 176.6 (los **UST**) · BBB+ a BBB- 142.2; CA AA+ a A− 23.9 · *BBB+ a BB+ 28.5*
  (*bracket frontera que cruza IG/sub-IG; contado aquí como sub-grado, conservador). Cartera casi íntegra IG. [AUD]
- **Banistmo (Dic-2025):** SÍ divulga la tabla de ratings de la cartera — en la **nota de administración de
  riesgos (calidad de cartera, pp.66-67)**, no en la Nota 7. Brackets propios (AA-/AA+, A-/A+, BBB+/BBB-,
  BB+ y menos, Sin calif.), cobertura de TODA la cartera, reconciliada exactamente con el total. Grado inversión
  924.9M (54.8%), sub-grado 710.7M (42.1%), sin calif. 53.7M (3.2%). El sub-grado es casi todo **Panamá soberano
  (BB+): ~567M**; buena parte del corporativo a costo amortizado es IG (AA/A: 134.6M + 338.9M). [AUD]

**Caveat de comparabilidad — la línea IG/sub-IG depende de cómo cada banco trata el papel de Panamá.**
Panamá quedó en frontera (S&P BBB, Fitch BB+ desde mar-2024, Moody's Baa3): BG, BAC y **Banistmo** clasifican su
papel panameño como **sub-grado (<BBB-/BB+)**, Global lo deja **sin calificación internacional**, y Scotiabank lo
trata como **IG (BBB)**. Por eso el % "grado de inversión" no es 1:1 entre bancos; el orden cualitativo (BG y
Scotia = cartera de alta calidad; Banistmo y Global = mitad IG; BAC y Davivienda = grueso sub-grado por soberanos
regionales) sí es robusto. En Banistmo, el 42% sub-grado es casi todo Panamá soberano (~567M en BB+).

---

## Resumen para gráficos del reporte

> Corte del reporte: **31-mar-2026**. Cuatro bancos en interino no auditado [INT] (Banistmo, Banco
> General, BAC, Global Bank); Davivienda y Scotiabank permanecen en su último cierre disponible
> (carried forward, ver secciones respectivas).

**Tamaño cartera (último disponible):**
BG 5,985.6 (Mar-26, INT) · BAC 5,615.4 (Mar-26, INT, CA) · Banistmo 1,643.3 (Mar-26, INT) ·
Davivienda 1,248.5 (Dic-25, carried) · Global 1,124.0 (Mar-26, INT, 9mo) · Scotiabank 371.3 (oct-24, absorbido).

**% inversiones / activo** (benchmark del sistema = SBN, banca de licencia general, Mar-2026):
**BG 28.6%** > Davivienda 23.4% (Dic-25, carried) > **Sistema SBN (lic. general) 23.0%** > Banistmo 15.6% > **BAC 13.4%** > Global 12.7% > Scotia 9.7%. Cambios vs. el corte Dic-2025: BAC adelanta a Global (12.3% → 13.4% vs. Global 13.4% → 12.7%) y el Sistema sube por encima de Banistmo (22.1% → 23.0% vs. Banistmo 16.0% → 15.6%).

**Yield estimado** (ingreso del trimestre 1T-2026 × 4 ÷ **portafolio de cierre Mar-2026**; método saldo de cierre, verificado por cálculo):
**BAC 5.5%** · BG 4.9% · Scotiabank 4.1% · Davivienda 4.05% · Global 4.0% · **Banistmo 3.9%** (sigue
siendo el más bajo del perímetro, pero sube desde 3.6%). Cálculo: BAC 307.1/5,615.4=5.47% · BG 293.6/5,985.6=4.91% ·
Global 44.6/1,124.0=3.97% · Banistmo 63.3/1,643.3=3.85%. (Sobre *saldo promedio*: BAC 5.79%, Global 4.35% — la diferencia
mayor es BAC por su crecimiento de +12.5% en el trimestre; los demás casi no cambian.)
- Ingresos por inversiones — **trimestre 1T-2026 raw → anualizado ×4 (cierre FY2025)**, US$M:
  BAC 76.8 → 307.1 (FY25 291.4) · BG 73.4 → 293.6 (FY25 283.5) · Banistmo 15.8 → 63.3 (FY25 58.2) ·
  Global 11.1 (Q3) → 44.6 (FY-jun25 45.6; acumulado 9m 36.8M). Sin interino: Davivienda 34.5 (Dic-25) · Scotiabank 15.0 (oct-24).
  El anualizado 1T26 queda muy cerca del cierre FY2025 en los cuatro bancos con interino (sin saltos de tendencia).

**Clasificación contable (% FVTPL / FVOCI / CA, último):**
- Banistmo (Mar-26, INT): 35.0 / 20.4 / 44.6 → sigue siendo de los libros más "trading", pero el FVTPL
  cede 2pp en el trimestre (37.0% en Dic-25)
- BG (Mar-26, INT): 14.5 / 84.9 / 0.5 → casi todo FVOCI
- BAC (Mar-26, INT): 0.4 / 96.3 / 3.3 → casi todo AFS/VRCOUI, y ese AFS es donde entró todo el crecimiento
- Global (Mar-26, INT, 9mo): 6.9 / 55.8 / 37.3
- Davivienda (Dic-25, carried): 0.5 / 79.2 / 20.3
- Scotiabank (oct-24, carried): 0 / 85.9 / 14.1

**Instrumentos — mapa definitivo (interino Mar-2026 para BG/BAC/Banistmo/Global; último cierre para Davivienda/Scotia):**
- **MBS/CMO:** SOLO Banco General (**3,050.8M, ~51%**, agency GNMA/FNMA/FHLMC; Mar-2026 interino, Dic-2025: 3,055.6M).
  Ningún otro banco los divulga.
- **US Treasuries / gob. EEUU:** Scotiabank 176M (47%, oct-24) · Banistmo 340.1M (~20.7%, Mar-26) · **BAC 856M gob-EEUU
  (~15%, Mar-26, subió desde 703M)** · BG 81M explícito (Mar-26, bajó desde 130M).
  Global y Davivienda no los separan por país.
- **Núcleo soberano local/regional:** BAC (Centroamérica, sub-grado creciendo fuerte en el trimestre),
  Davivienda (gob.), Banistmo (Panamá 496.4M ~30%, Mar-26) y Global (Panamá + LatAm).
- **Corporativo:** peso relevante en Banistmo (**~44%, Mar-26**, casi todo held-to-maturity) y Banco
  General (corp regionales 1,687.1M → 1,587.3M en el trimestre, ~35% ex-MBS).

---

## Implicaciones contables del corte marzo-2026

**(a) Las pérdidas no realizadas de AFS/FVOCI del sistema cruzaron a terreno positivo.** El CBI pasó de
-US$63.4M (Dic-2025) a **+US$4.7M (Mar-2026)** — la primera lectura de ganancia neta no realizada de la
serie reciente (venía de -US$473.8M en Mar-2025). El SBN redujo su pérdida de -US$93.6M a **-US$10.9M**.
Esto es un viento de cola para el patrimonio/OCI del sistema y **reduce el incentivo estructural** que
empujaba a los bancos a reclasificar bonos hacia costo amortizado para esconder la volatilidad de OCI —
una dinámica que sí se observó en años previos (ver el crecimiento del bucket CA en Banistmo, BG y BAC).

**(b) El salto de BAC (+12.5%, +US$625M) fue casi enteramente a VRCOUI en soberanos centroamericanos
sub-grado de inversión**, no a activos de mejor calidad. El bracket "BB+ a B-" de su cartera de gobierno
subió de 2,967.6M a **3,455.9M** en el trimestre — prácticamente todo el incremento del libro. Ese
crecimiento (concentrado en riesgo soberano regional, no en calidad) es lo que empuja a BAC por encima
de Global Bank en % de activo (12.3% → 13.4% vs. Global 13.4% → 12.7%), pero también sube su perfil de
riesgo de cartera (sub-grado ≈68% del libro calificado, frente a ≈67% a Dic-2025).

**(c) El libro de Banistmo se contrajo -2.7% en el trimestre y su mix de trading se moderó**: FVTPL bajó
de 37.0% a **35.0%**, la primera baja tras tres años de subida continua (11.8% en 2023). Es una señal de
pausa/reversión más que de un cambio de estrategia — el resto del mix (soberano Panamá, corporativo,
UST) se mantuvo prácticamente sin cambios en términos absolutos.

**(d) La divulgación interina es más delgada que la de los EE.FF. anuales auditados.** Ningún banco con
interino re-publica su tabla completa de ratings, la escalera de vencimientos ni (en el caso de Banco
General) la composición detallada por instrumento (MBS/CMO/UST/corp) — esas cifras quedan **carried
forward de Dic-2025** y así están marcadas en cada sección. Esto es una limitación conocida de los
cortes trimestrales frente a los cierres anuales, y aplica igual a los seis bancos del perímetro.
