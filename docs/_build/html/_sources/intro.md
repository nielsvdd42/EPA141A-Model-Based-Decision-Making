# EPA141A — Model-Based Decision Making

**MSc Engineering and Policy Analysis | Delft University of Technology**

| Role | Name | Email |
|------|------|-------|
| Module manager & core lecturer | Jazmin Zatarain Salazar | [J.ZatarainSalazar@tudelft.nl](mailto:J.ZatarainSalazar@tudelft.nl) |
| Lecturer | Jan Kwakkel | [j.h.kwakkel@tudelft.nl](mailto:j.h.kwakkel@tudelft.nl) |
| Lecturer | Tamara Metze | [T.A.P.Metze@tudelft.nl](mailto:T.A.P.Metze@tudelft.nl) |
| Lecturer | Patrick Steinmann | [P.Steinmann@tudelft.nl](mailto:P.Steinmann@tudelft.nl) |

**Monday & Wednesday · Lecture 13:00–15:00 · Lab session 15:00–17:00**

---

## Introduction

The central topic of this course is the support of **long-term decision-making on complex societal issues** through cutting-edge modelling techniques in combination with state-of-the-art deliberative methods. These large societal issues are typically surrounded by deep uncertainty, and the various policymakers involved virtually always operate in a highly political environment. Analysts involved in model-based decision support need to be aware of this political context and be sensitive to the multi-actor aspects of decision making.

This course builds a bridge between the modelling approaches taught in the modelling line and the theories on decision making taught in the policy analysis line. It will cover:
- Recent work on model-based decision support for decision making under deep uncertainty
- Contested knowledge claims, co-production of science-based policy, and deliberative policy analysis

The course is a mix of workshops on key conceptual and theoretical issues and group work of an applied nature. Students work in groups on a large societal issue, use models to support the design of an adaptive policy, and think about how to account for the political environment in their designs.

## Learning objectives

After completing this course, students can:

1. **Explain** the theoretical foundations of science-based and deliberative policy analysis, including contested knowledge claims, decision-making under deep uncertainty, and adaptive policy-making.
2. **Apply** exploratory modelling and scenario discovery techniques to a policy case, translating model results into evidence-based recommendations for decision-makers.
3. **Analyse** how model-based decision support interacts with multi-actor political processes, identifying how normative assumptions and political context shape analytical choices and their outcomes.
4. **Co-create** a model-based policy analysis project in a team setting, synthesising theoretical frameworks and model results to construct and defend a stakeholder position in a structured debate.
5. **Reflect** critically on the effects, limitations, and risks of model-based policy advice in context, relating these to the ultimate goal of producing more effective and legitimate public policies.

## Assessment

The course is assessed entirely through a **group project** (groups of 4 students). There is no written exam. Each group self-assigns a specific climate actor role and develops a global mitigation strategy using the JUSTICE model. The project includes two structured debates simulating COP31 negotiations.

| Component | Weight |
|-----------|--------|
| Part 1: Model-based analysis and policy advice | 70 % |
| Part 2: Political reflection on the COP31 debate | 30 % |

## Course structure

| Section | What's inside |
|---------|---------------|
| [Schedule](schedule.md) | Weekly programme, deadlines, staff contacts |
| [Lectures](lectures.md) | All 13 lectures with descriptions and required reading |
| [Installation](installation/index.md) | Set up your Python environment |
| [Labs](labs/index.md) | 6 guided practice notebooks (Lake Problem) |
| [Assignments](assignments/index.md) | 8 individual assignments (JUSTICE model) |
| [COP31 Debate](debate/index.md) | Instructions, actor blocs, timeline |
| [Final Project](project/index.md) | Instructions, outline, and grading rubric |
| [Resources](resources.md) | Key readings, software documentation |

## The JUSTICE model

**JUSTICE** (JUST Integrated Climate Economy) is an open-source IAM developed at TU Delft's HIPPO Lab. It simulates the global economy, the carbon cycle, and the climate system as a coupled dynamic model running from 2015 to 2300 across **57 world regions**.

```{figure} _static/justice_regions_map.png
:alt: JUSTICE 57 simulated world regions
:width: 100%

JUSTICE simulates 57 world regions based on the RICE-50+ framework.
```

The model converts a climate policy into welfare outcomes through seven linked steps:

1. **Economy** — Cobb-Douglas production across 57 RICE-50 regions
2. **Emissions** — GDP × carbon intensity × (1 − μ), where μ is the emission control rate
3. **Cumulative CO₂** — feeds into FaIR v2.1.3 → global mean temperature
4. **Damages** — Kalkuhl (2019) function converts temperature to % GDP loss
5. **Abatement costs** — Enerdata MAC curves, rising non-linearly with μ
6. **Net consumption** — damages and abatement subtracted from gross output
7. **Social welfare function** — one of eight distributive justice principles aggregates into a scalar objective

The key insight: **the same emission policy can rank very differently depending on which welfare function is applied.** This makes the normative uncertainty explicit and quantitative.

## Three sources of contestation

Any policy recommendation from JUSTICE depends on how three fundamentally different types of uncertainty are resolved:

| Type | What it is | Examples in JUSTICE |
|------|------------|---------------------|
| **Stochastic** | True value exists but is unknown | ECS: 2.0–5.0°C per CO₂ doubling |
| **Normative** | No true value — encodes a moral or political choice | ρ (discount rate), η (utility elasticity), welfare function |
| **Deep** | Qualitatively different futures; no meaningful probability | SSP-RCP scenario pair (8 combinations), δ (damage scale) |

Your analysis must engage with all three.
