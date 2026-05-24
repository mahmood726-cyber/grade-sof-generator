
# Automated GRADE Summary of Findings (SoF) Generator

A programmatic pipeline to dynamically compile GRADE (Grading of Recommendations Assessment, Development and Evaluation) Summary of Findings tables.

## The Bottleneck
Manually compiling SoF tables using GRADEpro GDT is incredibly tedious. It requires manually copying Relative Risks, Confidence Intervals, and absolute risk differences from statistical software into a web interface.

## The Automation
This repository bridges the gap between R (metafor/WebR) and the final GRADE table.
It automatically calculates:
1. **Anticipated Absolute Effects:** Converts Relative Risks to absolute patient differences per 1,000 using the assumed baseline risk.
2. **Certainty of Evidence:** Ingests the Risk of Bias (via ob2-auto-rater), Inconsistency (I-squared), Indirectness, and Imprecision to output a programmatic certainty score (High, Moderate, Low, Very Low).

Designed to be integrated directly into RapidMeta HTML templates.

