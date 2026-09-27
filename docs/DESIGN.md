# Visual reference and interaction design

![Tax Bracket Simulator interface concept](interface-reference.png)

This is an **AI-generated visual concept**, not application code or a functioning calculator. The design is informed by the locally installed `ui-ux-pro-max` skill. The image itself was created with OpenAI's built-in image-generation tool on September 27, 2026. No third-party photo, illustration, icon, or font asset was imported into the image.

## The lesson visible in five seconds

The first screen says, “Entering a higher bracket does not re-tax your earlier dollars.” The central bracket bins dominate the page. Gross wages pass through a labeled standard deduction and fill each bracket in order. Every bin has a rate, dollars in the bin, and tax generated. An amber marker identifies the next ordinary-income dollar. The outcome card reports federal income tax, employee payroll tax, and the amount left after those federal taxes.

Below, two equal $10,000 blocks invite visitors to compare income sources. The separate surplus flow goes from after-tax income through editable essential costs to money potentially available to invest. History and source links remain visible in the main navigation.

## Example math shown in the mockup

This is a check on the **illustration**, not an assertion that an implemented simulator exists:

| Line | Illustration | Source or status |
| --- | ---: | --- |
| Annual employee wages | $80,000 | Fictional user input |
| Filing status / tax year | Single / 2026 | Fictional user selection |
| Standard deduction | $16,100 | IRS 2026 Revenue Procedure 2025-32 |
| Taxable ordinary income | $63,900 | $80,000 - $16,100 |
| First federal bracket | $12,400 × 10% = $1,240 | IRS 2026 rate schedule |
| Second federal bracket | $38,000 × 12% = $4,560 | IRS 2026 rate schedule |
| Third federal bracket | $13,500 × 22% = $2,970 | IRS 2026 rate schedule |
| Federal income tax | $8,770 | Sum of three brackets; excludes credits and other rules |
| Social Security + Medicare | $6,120 | 6.2% + 1.45% of $80,000 employee wages; below the 2026 wage base |
| After federal taxes | $65,110 | $80,000 - $8,770 - $6,120; before state tax and other deductions |
| Essential costs | $40,000 | Fictional, adjustable user input |
| Potential to invest | $25,110 | $65,110 - $40,000; not a recommendation or forecast |

Source URLs and limitations are in [SOURCES.md](SOURCES.md). The $10,000 income-source comparison in the image has **no calculated comparison result**; that interaction remains to be built and verified.

## Build guidance

- Keep the first screen about the bracket misconception. Let detailed tax law unfold only as the visitor chooses a question.
- Pair every color with a direct text label. Provide keyboard and touch equivalents to dragging. Keep visible focus and reduced-motion behavior.
- Allow the arithmetic behind every output to open in place. Link the rule source directly from that explanation.
- Never animate earlier bracket dollars into a new rate when the income input changes.
- Label after-tax income separately from the money remaining after costs. Do not call an annual tax estimate a paycheck quote.
- On mobile, place the question and input first, bracket bins next, outcome after, and supporting views below. Avoid horizontal scrolling of required information.
- Visual style: light background, dark navy text, blue bracket segments, amber next-dollar cue, teal money remaining. Use generous spacing and adult plain-language typography. Exact colors and fonts remain implementation choices subject to contrast checks.

## Image-generation prompt record

The [full generation and edit prompts](IMAGE_PROMPTS.md) are preserved so the visual reference can be audited or revised. The source of the mockup is OpenAI built-in image generation, guided by the `ui-ux-pro-max` design skill. The image is a design reference; its text and calculations must be reimplemented and independently checked in code.
