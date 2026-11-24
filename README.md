# USRateAtlas open data: US state insurance requirements, vehicle fees and taxes

State-by-state reference data for all 50 states and DC, compiled by [USRateAtlas](https://usrateatlas.com) from primary government sources.
Every row carries the agency or statute it came from, a source URL and the data year.
Nothing is estimated: where no authority publishes a figure, the row is absent.

## Files

| File | What it covers | Browse on the site |
|---|---|---|
| `data/state-auto-insurance-requirements.csv` | Statutory minimum liability limits, uninsured motorist and PIP requirements, regulator names and links | [Car insurance requirements by state](https://usrateatlas.com/insurance/auto) |
| `data/state-vehicle-registration-title-inspection-fees.csv` | Registration, renewal, title, transfer, lien, EV surcharge, vanity plate and inspection rules and fees | [Vehicle registration fees by state](https://usrateatlas.com/vehicles/registration) |
| `data/state-income-sales-tax.csv` | Income tax structure, brackets, top rate, standard deduction, local income tax, sales tax, minimum wage, reciprocity | [State taxes](https://usrateatlas.com/taxes) |

Average insurance premiums (published by the NAIC) are not redistributed here; see the state pages on [usrateatlas.com](https://usrateatlas.com/insurance/auto) for those figures with their citations.

## Format

Long format, one fact per row:

| Column | Meaning |
|---|---|
| `state_code` | USPS code, including DC |
| `state_name` | State name |
| `field` | Metric name, e.g. `minBiPerPerson`, `renewalFee`, `topMarginalRate` |
| `value` | The value as published (rates are decimals, e.g. `0.05` = 5%) |
| `unit` | `usd`, `rate`, `count`, `text`, etc. |
| `source` | Agency, legislature or statute that publishes the figure |
| `source_url` | Link to the primary source |
| `data_year` | Year or "current as of" date of the source |
| `usrateatlas_page` | The page on usrateatlas.com that presents this state's figures |

## Updates

Data is refreshed annually as agencies publish new schedules.
Methodology: https://usrateatlas.com/methodology
Full source list: https://usrateatlas.com/sources

## License and citation

The underlying government figures are public information.
This compilation is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
Please cite as: USRateAtlas, "US state insurance requirements, vehicle fees and taxes", https://usrateatlas.com
