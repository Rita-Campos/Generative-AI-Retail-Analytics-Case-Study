# NovaRetail — GenAI Analytical Copilot Case Study

A retail analytics case study exploring how Generative AI can be used responsibly as an
analytical copilot, not a black box, to diagnose a business problem, separate evidence from
hypothesis, and recommend the right level of AI intervention.

## Overview

NovaRetail is a fictional six-region European retailer. In Q4 2025, the Fashion category in
the UK & Ireland showed an isolated deterioration: average discount rose from 7.3% to 17.5%,
returns from 8.3% to 11.0%, and gross margin fell from 53.9% to 48.1%, while other regions,
Italy in particular, stayed stable or improved over the same period.

The project scopes this into a business question and an analytical question, then uses GenAI
as an analytical copilot, cross-referencing commercial, campaign, operations, customer service
and feedback data, to build an evidence-based recommendation for how AI should be applied to
this problem.

## Approach

- **Exploratory analysis in Python** (pandas/matplotlib) over the raw dataset, with every
  aggregation computed and cross-checked programmatically, never taken from the AI model as a
  given.
- **GenAI as copilot, not oracle:** each finding is labeled as an observation supported by the
  data, a plausible hypothesis, or a point that still requires validation.
- **Structured prompting process:** objective definition, problem framing, expected output
  format, and iterative reformulation as findings were tested and, in some cases, rejected or
  corrected.
- **A scoped recommendation:** of the three possible AI responses (a supervised GenAI
  interface, an automation, or an autonomous business agent), the report justifies why a
  supervised interface is the appropriate level of intervention given the current evidence.

## Instructor feedback (excerpt)

The report was reviewed as part of the course it was built for. The technical assessment,
translated here from the original:

> "The report presents a highly consistent analysis of the case and demonstrates a critical
> and structured use of Generative AI as an analytical copilot. What stands out is how the
> problem was scoped to Fashion in the UK & Ireland during Q4, cross-referencing commercial,
> campaign, operations, customer service and feedback data to build an integrated reading of
> the problem.
>
> It was particularly positive to see the concern for validating results programmatically in
> Python, rather than accepting the model's outputs as the sole source for the figures
> presented. The distinction between observations supported by the data, plausible hypotheses,
> and aspects requiring further validation demonstrates an effective human-in-the-loop approach
> and a responsible use of GenAI.
>
> The prompting process is well structured and contextualized, including the definition of
> objectives, problem framing, expected output format, use of analytical tools, and several
> stages of reformulation and deepening. The recommendation of a supervised GenAI interface is
> equally well founded, being consistent with the lack of sufficient causal evidence to move
> directly to an automation or an autonomous agent."

Noted opportunities for improvement: make the progression from initial model outputs to
validated conclusions more visible (what was corrected, rejected, or reframed along the way);
compare the three AI-response alternatives more neutrally before indicating a preference; and
add a final systematic consistency check across charts, rankings, and conclusions.

## Repository structure

```
data/               source dataset (Excel)
charts/             analysis charts, Portuguese labels
charts_en/          analysis charts, English labels
brand/              visual identity assets (logo, banner)
make_charts*.py     chart generation (Python / matplotlib)
make_report*.js     report content and layout (Node / docx)
annex*.js           GenAI prompts appendix, evidence of AI use
build_docx*.js      shared Word-document building blocks
assemble*.js        assembles the final .docx
output/             final report, Portuguese and English (.docx / .pdf)
```

## Tools

Python (pandas, matplotlib) for analysis and charts · Node.js (docx) for report generation ·
Claude (Anthropic) as the GenAI analytical copilot.

## Author

Rita Campos
