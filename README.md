# Counting work in global fisheries

Code and data supporting the paper:

> **Counting work in global fisheries: sex-disaggregated employment, labour productivity and data gaps across aquatic food sectors**
>
> Jennifer L. M. Gee, Dario Pinello, Pierre-Ami Maudoux, Thorolfur Matthiasson, Konstantinos Polymeros
>
> Preprint (11/07/2026): <https://papers.ssrn.com/sol3/11/07/2026p11/07/2026apers.cfm?abstract_id=7100469>

The analysis combines FAO employment and production data (1995–2023) with World Bank indicators. It describes employment by sector, sex and working time, compares output per worker across countries, and estimates panel models of output per worker in aquaculture, inland fishing and marine fishing.

## Contents

| Path | Description |
|---|---|
| `notebook.Rmd` | Full analysis: data import, figures, correlations, panel models and robustness checks |
| `references.bib` | References cited in the notebook |
| `inputs/` | World Bank data (GDP per capita, GNI per capita, trade openness, Gini index) |

## Reproducing the results

Knit `notebook.Rmd` in R (the results were produced with R 4.5.0). The notebook downloads the FAO employment and production releases (2026.1.0) and FAO's ISO3–M49 country code list. The World Bank data are read from `inputs/`.

Required packages: `readr`, `janitor`, `dplyr`, `tidyr`, `stringr`, `ggplot2`, `scales`, `gridExtra`, `magrittr`, `ggpubr`, `corrplot`, `stargazer`, `plm`, `lmtest`, `sandwich`, `car`.

## Data sources

- FAO (2026). *Employment in the primary sector of fisheries and aquaculture*, release 2026.1.0.
- FAO (2026). *Global production (FishStat)*, release 2026.1.0.
- World Bank. *World Development Indicators*, WDI update of 11 Nov 2026: 
	- GDP per capita, PPP (constant 2021 international $) [NY.GDP.PCAP.PP.KD]
	- GNI per capita, PPP (constant 2021 international $) [NY.GNP.PCAP.PP.KD]
	- Trade (% of GDP) [NE.TRD.GNFS.ZS]
	- Gini index [SI.POV.GINI]