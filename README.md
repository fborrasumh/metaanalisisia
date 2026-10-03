# MetaAnálisisIA

**Meta-análisis completo en el navegador** — del dataset al forest plot, heterogeneidad, sensibilidad y GRADE.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23124341.svg)](https://doi.org/10.5281/zenodo.23124341)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> Herramienta del catálogo [fborrasumh/ia](https://fborrasumh.github.io/ia/) · Universidad Miguel Hernández de Elche

## Qué hace (v0.2)

1. **Datos** — Demo, CSV/TSV, editor en tabla, columna de subgrupos
2. **Modelo** — Efectos fijos o aleatorios (DerSimonian-Laird), comparación FE vs RE
3. **Resultados**
   - Forest plot + intervalo de predicción
   - Funnel plot + **prueba de Egger**
   - Tabla de pesos
   - Meta-análisis por **subgrupos**
4. **Sensibilidad** — Leave-one-out, gráfico de influencia, **meta-análisis acumulativo**
5. **Informe** — GRADE orientativo, narrativa (reglas o IA), export CSV / HTML / JSON / **código R (metafor)**
6. Exportación de gráficos en **PNG**

**La estadística se calcula en el cliente.** La IA solo ayuda a redactar el resumen y a sugerir GRADE.

## Privacidad

- Datos y gráficos permanecen en el navegador.
- La API key solo se usa en tu sesión y solo hacia el proveedor que elijas.
- El ejemplo demo funciona **sin clave y sin red**.

## Formato de datos

| study | yi | sei | ni | group |
|-------|----|-----|----|-------|
| Smith 2018 | 0.42 | 0.15 | 120 | Farmacológico |

También se aceptan `or`/`rr` + `ci_low` + `ci_high` (conversión automática a log-escala).

## Límites reales

- DerSimonian-Laird e inversa de varianza (no meta-regresión multivariable ni multinivel).
- Forest/funnel orientativos; verifica con **metafor** para publicación.
- GRADE es una guía asistida, no un certificado.
- Egger con k < 10 tiene potencia baja.

## Autores

**Fernando Borrás Rocher** · Universidad Miguel Hernández de Elche · ORCID: [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)

**José Antonio Quesada** · Universidad Miguel Hernández de Elche · ORCID: [0000-0002-6947-7531](https://orcid.org/0000-0002-6947-7531)

## Citar

```bibtex
@software{BorrasRocher_MetaAnalisisIA_2026,
  author  = {Borrás Rocher, Fernando and Quesada, José Antonio},
  title   = {MetaAnálisisIA},
  version = {0.2.0},
  year    = {2026},
  doi     = {10.5281/zenodo.23124341},
  url     = {https://fborrasumh.github.io/metaanalisisia/},
  note    = {Meta-análisis en el navegador}
}
```

## Licencia

MIT · Ver [LICENSE](LICENSE)
