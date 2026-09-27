# Implementation plan and release gates

## Technical baseline

Match the maintainable pattern of [From Barrel to Pump](https://github.com/leecoursey/from-barrel-to-pump): static HTML, CSS, and JavaScript hosted by GitHub Pages. Use versioned, committed tax-year data and no browser-side credentials. Add a scheduled refresh only where a public source has a predictable release and the refresh can validate dates, expected fields, and changes. Tax rules should not silently update at runtime.

This repository is presently a **planning snapshot**. The visual reference is not a functional prototype.

## Build order

1. **Federal bracket lesson:** single and married-filing-jointly wage examples for a named tax year, standard deduction, marginal bins, next-dollar interaction, effective-rate explanation, and detailed arithmetic.
2. **Money remaining:** employee Social Security and Medicare, annual after-federal-tax amount, editable essential costs, and investable surplus. Add high-income payroll rules before allowing scenarios above their thresholds.
3. **Income-source comparison:** additional wages, short-term gain, eligible long-term gain, and qualified dividend under the same base situation. Include basis, holding-period explanation, capital-gain stacking, and net investment income tax where applicable.
4. **Verified state layer:** select one state, obtain its official tax-year instructions, implement its actual tax base and deductions, and test examples. Add other states individually only after rule review. Local income tax requires a named jurisdiction and official source.
5. **History:** sourced 1926–2026 timeline of top statutory rates and laws; detailed 1980, 1982, and 1988 examples only after verification against those years' instructions. Offer nominal and inflation-adjusted comparisons with a specified BLS CPI series and completed reference period.
6. **Distribution context:** clearly separated empirical views from CBO, Federal Reserve, IRS, or BLS datasets. Show year, population, and definitions. Do not make the interactive fictional budget appear to represent a typical household.

## Release gates

- Each rule value in a versioned data file has `tax_year`, `jurisdiction`, `filing_status`, `effective_period`, `source_url`, `source_section`, `checked_on`, and a plain-language limitation.
- Exact boundary tests cover zero taxable income, each bracket edge and one dollar on either side, a raise across a boundary, Social Security wage base, Additional Medicare threshold, capital-gains rate threshold, and NIIT threshold where in scope.
- Worked examples agree with the applicable official instructions or documented hand calculations. Ordinary and capital-gain calculations remain separately inspectable.
- A numerical output is labeled as source data, user input, illustrative assumption, or simulator calculation. Neither the historic top rate nor the growth illustration is presented as a typical person's observed tax bill or guaranteed return.
- A Sources and methods view lists all rule, context, inflation, design, and asset sources used in the release. Source links remain accessible from relevant on-screen explanations.
- Keyboard, touch, small-screen, and reduced-motion paths communicate the same information as animation or hover.
- GitHub Pages publication is verified on the actual URL after build, not assumed from a successful commit.

## Scope boundaries

The first release is an educational model, not a tax filing or payroll withholding tool. Credits, itemized deductions, retirement contributions, self-employment, carryovers, special investment assets, AMT, and many state-specific provisions require explicit later support before the UI can compute them. Unsupported cases must be visible limitations, not hidden approximations.
