# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains academic research materials for papers on theoretical physics, specifically focusing on:
- **Singularity Analysis** - A systematic critique of mathematical singularities in physics


The core of this thesis is that many of the claims in physics around singularities, zeros, infinities, blow-ups, divergences, dividion by zero, negligibilities, model transitions, domain transitions, or regime transitoion, and other concepts that serve to define or redefine a model at some scale. So for example, in every case where somebody cites a division by zero because they rounded a number to something to a zero, that was an error. There is always, in those cases, there is always a finite input, or there is always a finite output for every finite input. Always. Limits fundamentally mean that you will never become that number or beyond it. Limits hold no matter how you interpret them. You don't ever hit that limit. There's never a physical point where you hit that limit. But there are a number of other ones where they claim a divergence meaning that for whatever reason it as it approaches zero or some number some discrete number some finite number it approaches it and that has a lot of meaning but it doesn't mean that it ever hits that number. But it has a lot of meaning and it doesn't mean it's a wall. Divergence isn't a wall. Divergence actually is more like the reciprocal of infinity. It might look like a wall but it's not. It's just infinity. Explosions, blow-ups - all those things are kind of fantasies. Any place where somebody took something, made a judgment call of what to do with the math, and then made a judgment call of what that meant - that's where I'm investigating. 

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
