# School-to-work histories

This CSV is a column-selected copy of the public `mvad` teaching dataset distributed with TraMineR. It contains all 712 source respondents, their original `id` and `weight`, and all 72 monthly state columns, `Jul.93` through `Jun.99`. Monthly values and column headings are unchanged. Factor values are written as their text labels; CSV does not store R factor attributes. Other background variables are omitted.

The data describe a Northern Ireland cohort's transitions from school to work. States are `school`, `FE` (further education), `HE` (higher education), `training`, `employment`, and `joblessness`. The captured data contain no missing monthly states. Each month is an observation period; these records do not give exact dates of individual transitions.

The book uses unweighted cohort descriptions. The original sample weight is retained for provenance but is not applied in this introductory application. Results are not national population estimates.

Source study: McVicar, Duncan and Michael Anyadike-Danes (2002). “Predicting Successful and Unsuccessful Transitions from School to Work by Using Sequence Methods.” *Journal of the Royal Statistical Society: Series A*, 165(2), 317–334.

Dataset documentation: <https://traminer.unige.ch/doc/mvad.html>.

Captured source: <https://github.com/traminer/TraMineR/blob/468a068f4abc03903d3b41654e8c5636f3b35034/data/mvad.RData>. The source distribution's notices are retained in the project's capture record. This third-party dataset retains its source attribution and terms; the book's prose license does not replace them.

The unchanged source, checksum, selected columns, and CSV reproduction script are recorded in `notes/school-to-work-20261101/` in the source project. Readers need only this CSV and the code printed in the book.
