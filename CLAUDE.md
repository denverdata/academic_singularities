# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains academic research materials for papers on theoretical physics, specifically focusing on:
- **Inertial Scale** - The relationship between time, space, and matter via inertia (t₁/t₂ = (I₂/I₁)^(1/5))
- **Singularity Analysis** - A systematic critique of mathematical singularities in physics

The core thesis is that singularities (division by zero "blow-ups") represent mathematical/logical errors rather than physical phenomena. For every finite input, there is a finite output.

## Building LaTeX Documents

```bash
# Navigate to latex directory and compile the master document
cd latex
pdflatex master.tex
bibtex master
pdflatex master.tex
pdflatex master.tex
```

The main paper is `latex/master.tex` which uses the RSC (Royal Society of Chemistry) article template.

## Repository Structure

- `latex/` - Main LaTeX document and RSC template files
- `referenced_docs/` - Supporting papers, reference materials, and the Singularity Cases catalog
- `agent/` - Agent rules defining research methodology and constraints
- `output/` - Draft documents in progress
- `supporting_materials/` - Author biography and CV
- `uoltemplate_source/` - Original RSC template source files

## Critical Agent Rules

Read `agent/agent_rules.md` before making any edits. Key constraints:

### Scientific Standards
- Honor the scientific method - work from observations, not hypothesis of conclusion
- Trust user-provided scientific concepts even if not widely accepted
- No logical fallacies in any argument
- Perform all calculations according to Relativistic Classical Physics (never treat relativistic components as negligible)
- Never switch to quantum perspective - work entirely in classical physics

### Writing Standards
- Include in-line citations and bibliography
- Use full relativistic formulas, not approximations
- Proper handling of significant figures and scientific notation
- Do not fabricate data or presume information

### Concepts That Cannot Be Used as Premises or Supporting Arguments

**Important distinction:** These concepts can be discussed, analyzed, and critiqued — but they cannot be used as established facts or as premises to support arguments. This research is evaluating whether these conclusions are valid, so using them as premises would be circular reasoning.

| Cannot use as premises | Can always cite |
|------------------------|-----------------|
| Cosmic expansion as explanation for redshift | The observed redshift data itself |
| Big Bang / Lambda-CDM theory | CMB observations and other raw data |
| Singularities as physical systems | The mathematical situations that produce them (to analyze/critique) |
| Literal point masses as physical objects | Point mass as a conceptual/mathematical tool |
| Division by zero "blow-ups" as real phenomena | The equations where these appear (to show why they're errors) |
| Planck scale as a domain transition | Planck scale as an observational limitation |

**The rule:** Observations and data are always valid. Theoretical conclusions built on that data are under scrutiny and cannot be assumed true.

### Core Principles on Singularities
From `referenced_docs/Singularity Cases.md`:
- A limit literally means the value will never be that limit or beyond
- In floating-point math, there is no infinitely precise zero - division by zero is impossible
- For every finite input there is a finite output
- Both quantum and relativistic perspectives apply at all scales - Planck scale is observational transition, not domain transition
