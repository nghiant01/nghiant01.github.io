---
layout: archive
title: "Industry Resume"
permalink: /industry-resume/
author_profile: true
---

{% include base_path %}

My industry resume can be found [here]({{ base_path }}/files/materials/NghiaNT_Industry_Resume.pdf).

## Projects

Two portfolio projects applying robust optimization and saddle-point algorithms to supply-chain planning. Both use synthetic data only and are not based on any company's proprietary data or systems.

### Robust Middle-Mile Capacity Planning under Demand Uncertainty

[GitHub repository](https://github.com/nghiant01/robust-middle-mile-capacity-planning) · Python, NumPy, SciPy, Matplotlib

**Problem.** A transportation planner must reserve lane-level carrying capacity before freight demand is known. Too little capacity causes shortages and service failures; too much wastes reservation cost.

**Approach.**
- Built a synthetic middle-mile network (8 facilities, 18 directed lanes, 7 days) with correlated demand scenarios, and compared nominal, expected-value, and min-max robust capacity plans.
- Reformulated the robust plan as a convex-concave saddle-point problem (adversarial weighting of demand scenarios) and solved it with a projected extragradient method, validated against an independent SciPy epigraph solve.
- Evaluated every plan on 500 held-out test scenarios and an uncertainty stress test.

**Results.**
- Versus expected-value planning, the robust plan reserved 3.7% more capacity, cut mean shortage by 19.9%, and raised service level from 97.86% to 98.28%.
- At the highest uncertainty level tested, it reduced the worst held-out cost by 11.8% for about 4.1% more capacity.
- Extragradient matched the reference objective to a relative gap below $10^{-7}$ in every stress-test instance, while plain gradient descent-ascent stalled.

<img src="{{ base_path }}/images/projects/middle-mile-stress-test.png" alt="Worst-case held-out cost versus demand uncertainty for nominal, expected-value, and robust plans" style="max-width: 100%;">

### Robust Fulfillment-Center Labor Allocation under Workload Uncertainty

[GitHub repository](https://github.com/nghiant01/robust-fc-labor-planning) · Python, NumPy, SciPy, Pandas, Matplotlib

**Problem.** Intraday labor must be assigned to Stow, Pick, Pack, and Ship before workload is known. Lean staffing saves labor cost but creates backlog when volume spikes or productivity drops.

**Approach.**
- Modeled hourly staffing over 12 periods with labor, reassignment-friction, and backlog-penalty costs under a shared workforce cap.
- Solved the min-max robust staffing plan with projected extragradient, using an exact projection onto the capped workforce set and onto the probability simplex.
- Stress-tested fixed plans on 1,200 independent scenarios across six regimes: normal variability, volume surge, Pick-heavy spike, late-day surge, reduced productivity, and a combined shock.

**Results.**
- Versus expected-value planning, robust staffing cost 4.57% more labor but cut average shortage by 21.56% and worst-case loss by 10.64%, raising service level by 1.98 percentage points across the stress suite.
- Under a combined volume and productivity shock, service level was 79.51% (robust) versus 76.33% (expected-value) and 69.67% (nominal).
- The robust solution matched an independent SciPy reference to a relative gap of about $4 \times 10^{-8}$.

<img src="{{ base_path }}/images/projects/fc-labor-stress-test.png" alt="Service level by stress regime for nominal, expected-value, and robust staffing plans" style="max-width: 100%;">
