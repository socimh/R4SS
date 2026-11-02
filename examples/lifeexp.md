# Complete country data used in Chapters 4-5

`lifeexp.csv` contains all 68 rows and all six columns from `tidystata::lifeexp`
in the captured tidystata 0.3.0 installation. Row order, column order, recorded
values, and missingness are unchanged. No countries are sampled or removed.

Source: World Bank, World Development Indicators, retrieved 21 October 2026,
as documented in the captured package. License: CC BY 4.0.
Attribution: World Bank, World Development Indicators,
https://datacatalog.worldbank.org/search/dataset/0037712.
License: https://datacatalog.worldbank.org/public-licenses#cc-by.

| Variable | Meaning and units |
| --- | --- |
| `region` | Added grouping: 1 Europe & C. Asia, 2 North America, 3 South America |
| `country` | Country name |
| `popgrowth` | Annual population growth, percent, 1998 |
| `lexp` | Life expectancy at birth, years, 1998 |
| `gnppc` | GNI per capita, Atlas method, current US dollars, 1998 |
| `safewater` | People using safely managed drinking water services, percent, 2000 |

The package dataset is a prepared historical snapshot, not an unprocessed
World Bank download. Its preparation selects countries, rounds population
growth to one decimal and the other measurements to integers, and adds labels.
The complete supplied dataset does not include every country in the world.
Water uses 2000, the earliest available year for the documented series.

CSV stores plain values and writes missing values as `NA`. It does not preserve
variable labels or the value labels attached to the region codes. The package
object retains those labels. The package label for `gnppc` says "GNP per capita";
the documented WDI series is GNI per capita using the Atlas method.

Life expectancy and population growth are observed for all 68 countries.
GNI per capita is observed for 67 countries. Safe water is observed for 54
countries and missing for 14. No missing values were introduced for teaching.
The mean of the available water percentages is about 77.2 percent, giving each
contributing country equal weight; it is not a population-weighted estimate.

The protected build helper `tools/build_real_examples.R` exports this CSV
from the captured package. Readers can use the package object directly, as
shown in the book; this helper is not a prerequisite for any lesson.
The separate `lifeexp-excerpt` files remain the six-country examples for
Chapter 2's format demonstrations.
