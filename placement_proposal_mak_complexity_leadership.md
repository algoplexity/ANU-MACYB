# Placement Proposal
## CYBN8005 Industry/Research Placement
### Complexity & Leadership Project – ANU School of Cybernetics

**Student:** Yeu Wen Mak  
**Program:** Master of Applied Cybernetics  
**Proposed Supervisor:** Maia Gould  

---

# Project Title

**Adaptive Mesoscopic Observability: A Compression-Driven Framework for Regime Detection in Complex Systems**

---

# 1. Project Rationale

Leaders operating within complex socio-technical systems face a persistent epistemic tension: oversimplified models obscure structural change, while overly detailed models produce paralysis. In high-stakes environments—energy systems, financial markets, digital infrastructures—effective intervention depends on detecting regime transitions early, under conditions of bounded cognition and limited computational resources.

This placement proposes to develop and validate a formal, computational framework for adaptive sensemaking in complex systems. The central hypothesis is that representation choice fundamentally shapes observability, and that resource-bounded adaptive encoding guided by Minimum Description Length (MDL) principles can improve regime detection without incurring unmanageable complexity.

The project contributes to the Complexity & Leadership program by offering a rigorous model of how leaders and institutions might algorithmically navigate irreducible complexity through principled compression and representation search.

---

# 2. Conceptual Foundation

The project builds on three core premises:

1. **Regime Dependence:** Complex systems exhibit qualitatively distinct regimes in which structural invariants remain stable until disrupted.
2. **Representation Relativity:** Structure is not independent of encoding; what is observable depends on representational choice.
3. **Bounded Rationality:** Observers—whether human or institutional—must operate under computational and informational constraints.

Within this framework, a system is considered *mesoscopically observable* if there exists an encoding that preserves macro-structural invariants while filtering micro-level noise, enabling detectable divergence between regimes.

The proposed mechanism—the *Algorithmic Mesoscope*—is defined as a bounded, MDL-regularized search process over encoding families and predictive models. Rather than assuming privileged ontologies, it seeks compressed sufficient representations that maximize regime separability subject to complexity constraints.

---

# 3. Research Objectives

The placement will pursue four objectives:

1. **Formalization:**
   - Define mesoscopic observability in measurable terms.
   - Specify divergence metrics and bounded detection criteria.

2. **Computational Implementation:**
   - Develop an adaptive encoding search procedure guided by MDL.
   - Compare adaptive representations against fixed baselines.

3. **Empirical Validation (Simulation-Based):**
   - Construct controlled dynamical substrates exhibiting known regime transitions.
   - Measure detection delay, false positives, and robustness under noise.

4. **Leadership Implications:**
   - Interpret results in terms of systemic sensemaking.
   - Articulate how compression-driven representation selection informs adaptive leadership in complex systems.

---

# 4. Methodological Approach

The project will proceed in five stages:

### Stage 1 – System Construction
Develop simulated dynamical systems with controllable regime parameters. These may include stylized market systems, networked adaptive agents, or infrastructure-inspired constraint systems.

### Stage 2 – Encoding Family Design
Construct a bounded family of candidate encodings (e.g., symbolic abstractions, aggregated state representations, spectral transforms).

### Stage 3 – MDL Optimization
Implement a search mechanism minimizing:

L(E, p) = K(E) + K(p) + L(data | E, p)

where:
- E is the encoding,
- p is the predictive model under E,
- K(·) denotes description length,
- L(data | E, p) measures predictive error.

### Stage 4 – Observability Testing
Quantitatively evaluate whether adaptive encoding improves:
- Regime separability
- Detection delay
- Stability under perturbation

### Stage 5 – Cybernetic Interpretation
Translate computational findings into a systemic framework for adaptive leadership and institutional sensemaking.

---

# 5. Expected Contributions

## Technical Contributions
- A measurable definition of mesoscopic observability.
- An implementable MDL-guided adaptive representation search framework.
- Empirical evidence regarding compression–observability trade-offs.

## Cybernetic Contributions
- A formal model of adaptive sensemaking under bounded rationality.
- A computational articulation of how representation selection shapes systemic intervention.
- A bridge between algorithmic information theory and leadership in complex systems.

---

# 6. Alignment with the Complexity & Leadership Project

This project directly engages core themes of the Complexity & Leadership program:

- **Sensemaking under uncertainty** – Representation choice as an instrument of leadership.
- **Adaptive systems governance** – Detecting structural transitions before systemic failure.
- **Epistemic responsibility** – Balancing expressive depth with operational simplicity.
- **Cybernetic feedback** – Embedding representation selection within recursive observation–action loops.

Rather than proposing universal explanatory models, the project emphasizes methodological instruments for navigating complexity responsibly and pragmatically.

---

# 7. Deliverables (CYBN8005)

- A formal research report.
- A working computational prototype of the adaptive encoding framework.
- Quantitative evaluation of regime detection performance.
- A leadership-oriented synthesis paper articulating cybernetic implications.
- Presentation to the Complexity & Leadership Lab.

---

# 8. Research Trajectory Beyond Placement

This placement forms the foundation of a broader research pathway:

- Master’s Phase: Empirical validation of adaptive regime detection.
- Advanced Master’s Phase: Formal bounds on observability and detection delay.
- Doctoral Phase: Theoretical results on MDL-guided approximation of sufficient statistics and applications across energy, economic, and socio-technical systems.

The long-term objective is not to eliminate complexity, but to construct principled instruments for acting within it.

---

# Closing Statement

This placement proposes to formalize and empirically test a compression-driven model of adaptive observability, contributing both computational rigor and conceptual clarity to the study of leadership in complex systems. By grounding cybernetic principles in measurable algorithmic procedures, the project seeks to advance the School of Cybernetics’ mission of enabling responsible intervention within irreducible complexity.

