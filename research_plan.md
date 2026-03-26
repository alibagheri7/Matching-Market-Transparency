# Matching-Market Transparency Research Plan

## Objective
Build a rigorous, publication-ready research project around a two-sided matching market where the key design variable is **how much preference information is visible** (private, local, global), while delaying final positioning (IS vs economics vs marketing) until core results are established.

---

## 1) Project Framing (Discipline-Neutral)

### Core question
How does the **scope of preference observability** affect:
1. matching efficiency,
2. concentration/inequality,
3. strategic search behavior,
in two-sided markets with limited attention/search?

### Primary treatment variable
- **Information regime**:
  - **Private**: no preference revelation.
  - **Local**: preference signals revealed only to neighbors/subsets.
  - **Global**: broad/full revelation.

### Keep fixed initially
- Matching mechanism,
- search budget/cost,
- population size,
- utility structure.

This helps isolate the causal effect of information design.

---

## 2) Step-by-Step Approach

### Phase A — Clarify model backbone (Week 1)
1. Define agent sets (Side A and Side B; avoid domain-specific labels in core model).
2. Specify utility with:
   - vertical desirability component,
   - idiosyncratic fit component.
3. Choose one baseline matching protocol (proposal/accept + tie-breaking).
4. Define search friction (proposal cap `m` or per-proposal cost `c`).
5. Define information graph for local revelation (e.g., random `k`-neighbor visibility).

**Deliverable:** 2–3 page technical model note with notation and assumptions.

### Phase B — Build simulation engine (Weeks 2–3)
1. Implement reproducible simulation pipeline.
2. Run baseline experiments across information regimes.
3. Produce outcome metrics:
   - match rate,
   - average utility,
   - assortativity,
   - proposal concentration (e.g., top-decile share),
   - welfare by percentile.
4. Add Monte Carlo runs and confidence intervals.

**Deliverable:** Initial result tables + plots + reproducible scripts.

### Phase C — Expand mechanisms one at a time (Weeks 4–5)
Add only one extension per experiment block:
1. Local network structures (random, small-world, clustered).
2. Signal quality (perfect vs noisy revelation).
3. Search frictions (low vs high proposal budget).
4. Heterogeneity in risk/aspiration behavior.

**Deliverable:** Robustness section draft with comparative visuals.

### Phase D — Light theory layer (Weeks 5–6)
1. Derive 1–3 stylized propositions under simplified assumptions.
2. Focus on directional comparative statics (not full general equilibrium characterization).
3. Link propositions to simulation patterns.

**Deliverable:** Theory section draft + proof appendix (minimal but clean).

### Phase E — Narrative lock + paper positioning (Week 7)
1. Decide contribution emphasis based on strongest results:
   - market design,
   - platform information architecture,
   - welfare-distribution tradeoff.
2. Select target journal family (IS/econ/marketing) **after** seeing where contribution is strongest.
3. Reframe intro and hypotheses accordingly.

**Deliverable:** Submission-ready abstract + venue-specific positioning memo.

---

## 3) Angles to Explore in Parallel

### Angle 1: Efficiency vs inequality tradeoff
- Transparency may reduce wasted search but raise concentration at the top.
- Key test: does total welfare rise while lower-percentile welfare falls?

### Angle 2: Local information as a “middle optimum”
- Hypothesis: local revelation can dominate both opacity and full transparency.
- Key test: non-monotonic welfare or concentration pattern.

### Angle 3: Information geometry
- Same information quantity, different **who-sees-whom** structure.
- Key test: network topology effects on matching outcomes.

### Angle 4: Congestion dynamics
- Full visibility may induce crowding around highly ranked agents.
- Key test: proposal congestion, rejection rates, unmatched tails.

### Angle 5: Platform design policy
- What visibility policy should a platform choose under specific objective functions?
- Objectives could include: total matches, long-run fairness, retention proxy.

### Angle 6: Distributional welfare and participation
- Who gains/loses by information regime (top/middle/bottom)?
- Does transparency discourage participation among lower-ranked agents?

---

## 4) Candidate Hypotheses (Draft)

1. **H1 (Efficiency):** Increasing reciprocal-interest visibility reduces wasted proposals and increases match rate.
2. **H2 (Concentration):** Global visibility increases attention concentration on high-desirability agents.
3. **H3 (Distribution):** Mid/low-ranked agents may be worse off under global visibility despite higher aggregate welfare.
4. **H4 (Interior optimum):** Local visibility can outperform both private and global regimes on balanced welfare metrics.

---

## 5) Metrics and Evaluation Dashboard

### Core metrics
- Match rate,
- mean/median utility,
- assortativity index,
- Gini/variance of match utility,
- rejection rate,
- proposal concentration index.

### Segment metrics
- Outcomes by desirability decile,
- unmatched share by decile,
- gain/loss decomposition relative to private baseline.

### Robustness
- Multiple random seeds,
- sensitivity over (`alpha`, `beta`, `m`, `k`, noise level),
- alternate matching protocols.

---

## 6) Risks and Mitigations

1. **Risk:** Model complexity explodes.
   - **Mitigation:** Add one mechanism at a time; freeze baseline.
2. **Risk:** Results are obvious/monotonic.
   - **Mitigation:** Prioritize local-vs-global geometry and distributional heterogeneity.
3. **Risk:** Simulation seen as ad hoc.
   - **Mitigation:** Pre-register experiment grid and include theoretical anchoring propositions.
4. **Risk:** Weak external relevance.
   - **Mitigation:** Map model primitives to real platform policy levers (visibility, recommendation exposure, signaling).

---

## 7) Decision Framework for Final Positioning (Later)

After results are in, choose lane based on dominant contribution:

- **Economics lane** if strongest contribution is equilibrium/welfare/comparative statics.
- **IS lane** if strongest contribution is platform information architecture and digital market design.
- **Marketing lane** if strongest contribution is demand-side behavior, targeting, and platform outcomes (engagement/conversion/concentration).

Until then, keep terminology neutral and evidence-first.

---

## 8) Immediate Next Actions (This Week)

1. Finalize minimal model assumptions (1 page).
2. Define parameter grid and random-seed protocol.
3. Implement baseline simulation for three information regimes.
4. Generate first results table with five core metrics.
5. Hold review checkpoint and decide which extension to run first.

