# Country data used in this book

The CSV, Stata DTA and SPSS SAV files named `lifeexp-excerpt` contain the same
six countries: Albania, Poland, Canada, Cuba, Argentina and Brazil. They are
selected teaching cases, not a representative sample of countries.

Source: World Bank, World Development Indicators, retrieved 21 October 2026,
as captured in tidystata 0.3.0. The data use the CC BY 4.0 license. Attribution:
World Bank, World Development Indicators, https://datacatalog.worldbank.org/search/dataset/0037712.

| Variable | Meaning and units |
| --- | --- |
| `region` | Added grouping: 1 Europe & C. Asia, 2 North America, 3 South America |
| `country` | Country name |
| `popgrowth` | Annual population growth, percent, 1998 |
| `lexp` | Life expectancy at birth, years, 1998 |
| `gnppc` | GNI per capita, Atlas method, current US dollars, 1998 |
| `safewater` | People using safely managed drinking water services, percent, 2000 |

The captured package rounds population growth to one decimal and the other
measures to integers, adds labels, and selects the countries. Water is from
2000, the earliest available year for this indicator. Missing water values
remain missing; no missingness has been introduced for instruction.

Within each region, the excerpt selects the alphabetically first country
with observed water coverage and the first with missing water coverage.
If either category is absent, it takes the first two countries instead.
The final order is region, then country.

CSV stores plain values and writes missing values as `NA`; it does not retain
variable or value labels. DTA and SAV retain labels where their formats support
them. They contain no invented numeric missing-answer codes.

All six records are also available in `tidystata::lifeexp`. The book teaches
the code used on these files; no external preparation script is required of
readers.

The DTA and SAV derivative files use explicit variable labels with units and
years. The captured package inherits the shorter label "GNP per capita" for
`gnppc`; its documented WDI source is GNI per capita, Atlas method. The
derivative labels and this codebook use that source definition. Values and
regional value labels are unchanged.
