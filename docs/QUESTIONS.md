# Questions this project should answer

These are user stories written as questions a visitor can actually test. The dashboard is for U.S. laypeople, including visitors who have never read a tax table. Each answer must be available through direct interaction and a short plain-language explanation.

## 1. How do brackets work?

**As someone offered a raise, I want to move income across a bracket boundary so I can see whether all my income gets the new rate.**

- Can I see gross wages, the standard deduction, taxable income, and each filled federal bracket as separate steps?
- Does each bracket show the amount inside it, its rate, and its tax dollars?
- If I add $1 or $1,000 near a boundary, do only those new taxable dollars enter the next bin?
- Can I distinguish the rate on my next ordinary-income dollar from federal income tax as a percentage of total income?

**Acceptance:** changing the input never redraws earlier dollars as if they had entered a higher bracket. The numeric explanation agrees with the visual at zero, at a bracket edge, and one dollar on either side.

## 2. What happens to additional money?

**As someone comparing a raise and an investment profit, I want to hold my starting situation fixed and change the source of the same extra dollars.**

- What happens if the extra amount is employee wages, a short-term gain, an eligible long-term gain, or a qualified dividend?
- Which calculation uses ordinary-income brackets? Which uses a separate capital-gains schedule?
- When do Social Security, Medicare, Additional Medicare, or net investment income tax apply?
- Does the result change as the base ordinary income changes?

**Acceptance:** the comparison uses the same base income, filing status, tax year, and additional dollar amount. Taxes are shown by type. The UI does not claim that all investment income gets a lower rate.

## 3. What is the taxable investment amount?

**As someone selling an asset, I want to enter what I paid and what I received so I can see the gain rather than treating the full sale price as income.**

- What is the difference between purchase price, sale proceeds, and realized gain?
- What changes when I hold the asset for a different length of time?
- What happens before I sell it?
- Which complex cases, such as losses, collectibles, property recapture, and special exclusions, are outside a simplified scenario?

**Acceptance:** the UI clearly identifies the gain as an illustrative net profit after the entered basis and sale amount. Unsupported situations are labeled rather than silently calculated.

## 4. How much is left, and can I invest?

**As someone balancing ordinary expenses, I want to see money after taxes and then subtract my own essential costs to understand how much remains available to save or invest.**

- What remains after each displayed tax layer?
- How does a state or local tax change the estimate when supported?
- How do housing, food, transportation, healthcare, debt obligations, and other user-entered costs change the surplus?
- At what point does investable surplus become zero or negative?
- How do different contribution amounts affect an illustrative future balance under the *same stated* return assumption?

**Acceptance:** “after-tax income” and “investable surplus” have separate labels. Growth is identified as a scenario, not a forecast. Preset expenses, if any, cite their dataset and observation year and remain editable.

## 5. What changed over time?

**As someone hearing claims about past tax rates, I want to compare the actual rules in selected years and understand what changed before and after Reagan-era legislation.**

- How did the ordinary-income schedule and long-term-gain treatment differ in 1980, 1982, and 1988?
- Did a headline top rate apply to wages, investment income, or both in that year?
- What were deductions, exemptions, maximum-tax rules, phaseouts, and holding-period rules for the selected modeled scenario?
- Am I comparing nominal dollars or equal purchasing power, and which CPI period is used?

**Acceptance:** the century timeline identifies top statutory rates as such; it does not present them as typical household rates. A year is calculator-enabled only after its relevant rules and examples are verified against contemporaneous official tax instructions. The 1980 wage-rate cap and late-1980s rate “bubble” must not disappear behind simplified headlines.

## 6. What do the data actually show?

**As someone curious how wealthy households receive income, I want to inspect real distributions of wages, capital income, and asset ownership without a fictional household being passed off as representative.**

- What share of income or wealth comes from each component in the cited dataset and year?
- Who holds investable assets, and how does that vary by the dataset's income or wealth grouping?
- How do survey estimates, tax-return data, and modeled tax scenarios differ?

**Acceptance:** observed distributions cite their agency, year, population, definitions, and limitations. The dashboard distinguishes empirical data from user-created scenarios and avoids claiming that tax treatment alone explains wealth differences.

## 7. Can I check the source?

**As a visitor or reviewer, I want to inspect the provenance of a number or claim without leaving the question unanswered.**

- Is there a direct source link and source date near the relevant result?
- Can I open a full source-and-methods register?
- Are user inputs, illustrative assumptions, official values, and simulator calculations distinguishable?
- Are the design reference, code inspirations, and third-party assets credited?

**Acceptance:** no published number or historical assertion lacks a traceable source or a documented calculation from cited inputs. If a source cannot be verified, the feature is withheld or marked illustrative.
