# Placement Proposal
## CYBN8005 Industry/Research Placement
### Australia Centre for Energy Systems (ACES)

**Student:** Yeu Wen Mak  
**Program:** Master of Applied Cybernetics  
**Proposed Host Unit:** Grid Orchestration / Distributed Energy Systems Team  

---

# Project Title

**Adaptive Regime Detection for High-DER Distribution Networks: A Compression-Regularized Observability Framework**

---

# 1. Project Rationale

Australia’s energy transition is driving distribution networks toward unprecedented levels of distributed energy resource (DER) penetration, bidirectional flows, and real-time operational complexity. As hosting capacity increases and dynamic operating envelopes (DOEs) become more prevalent, network operators must detect structural shifts in system behavior early enough to prevent instability, congestion cascades, and inequitable curtailment outcomes.

Conventional monitoring approaches rely on fixed representations of voltage, load, and export constraints. However, under rapidly shifting penetration levels and behavioral variability, static representations may fail to surface emerging regime transitions.

This placement proposes to develop and test an adaptive, compression-regularized observability framework that improves early detection of operational regime shifts in high-DER distribution networks. The project builds a measurable bridge between representation selection, regime separability, and stability margin improvement.

---

# 2. Problem Framing

High-DER networks exhibit multiple operational regimes, including:

- Low congestion / stable export conditions  
- Localized voltage constraint regimes  
- Curtailment-dominated regimes  
- Network-wide stress or instability margins  

Transitions between these regimes may be gradual or abrupt. Early detection is critical for:

- Adjusting dynamic operating envelopes  
- Maintaining voltage stability  
- Preserving hosting capacity  
- Ensuring equitable access to export opportunities  

The central research question is:

**Under bounded computational and informational resources, can adaptive representation selection improve detection of operational regime transitions compared to fixed monitoring encodings?**

---

# 3. Conceptual Approach

The project introduces a bounded representation search mechanism guided by Minimum Description Length (MDL). Rather than assuming a single privileged encoding of feeder states, the framework searches over a family of candidate representations and predictive models to minimize:

L(E, p) = K(E) + K(p) + L(data | E, p)

where:
- E denotes a candidate encoding of network state variables,
- p denotes a predictive model under that encoding,
- K(·) measures description length (model complexity),
- L(data | E, p) measures predictive error.

The objective is to identify representations that:

1. Remain robust to measurement noise.
2. Maximize divergence between distinct operational regimes.
3. Avoid unnecessary model complexity.

This framework treats regime detection as a measurable observability problem rather than a heuristic anomaly detection task.

---

# 4. Research Objectives

1. **Operational Regime Definition**  
   - Formalize regime categories using feeder simulation or historical operational data.  
   - Identify structural invariants (e.g., voltage variance patterns, constraint topology, congestion frequency).

2. **Encoding Design and Search**  
   - Construct a bounded family of candidate encodings (e.g., aggregated voltage statistics, spectral transforms, graph-based constraint abstractions).  
   - Implement MDL-regularized adaptive selection.

3. **Performance Evaluation**  
   - Measure detection delay across regime transitions.  
   - Quantify false positive and false negative rates.  
   - Evaluate robustness under injected noise and demand variability.

4. **Control-Relevant Assessment**  
   - Assess whether earlier regime detection enables improved DOE adjustment or stability margin preservation in simulation.

---

# 5. Methodology

### Stage 1 – System Substrate
Utilize feeder simulation environments or synthetic distribution network models reflecting high-DER penetration scenarios.

### Stage 2 – Regime Induction
Systematically vary parameters such as DER penetration, demand volatility, and export constraints to induce controlled regime transitions.

### Stage 3 – Adaptive Encoding Implementation
Deploy a bounded MDL-based search over candidate representations and associated predictive models.

### Stage 4 – Quantitative Comparison
Benchmark adaptive encoding performance against:
- Raw time-series monitoring  
- Fixed statistical feature sets  
- Standard anomaly detection baselines

### Stage 5 – Stability and Hosting Capacity Analysis
Evaluate whether improved regime detection translates into measurable operational benefits.

---

# 6. Expected Contributions

## Technical Contributions
- A measurable definition of operational regime observability in high-DER networks.
- An implementable adaptive encoding framework.
- Empirical quantification of compression–observability trade-offs in distribution systems.

## Strategic Contributions
- Improved early-warning capacity for congestion and instability.
- Support for dynamic operating envelope optimization.
- Insights into scalable monitoring architectures under increasing grid complexity.

---

# 7. Alignment with ACES Research Themes

The proposed project directly supports ACES priorities:

- Digital orchestration of distributed energy resources.
- Increasing hosting capacity without physical augmentation.
- Data-driven system planning and operational resilience.
- Responsible and equitable grid transformation.

By focusing on observability rather than purely predictive accuracy, the project strengthens the informational foundations of distributed system operation.

---

# 8. Deliverables (CYBN8005)

- Formal technical report.  
- Working computational prototype.  
- Quantitative evaluation of regime detection performance.  
- Presentation to host research team.  
- Recommendations for integration into monitoring or DOE workflows.

---

# 9. Research Trajectory Beyond Placement

This placement forms the empirical foundation for broader research into adaptive observability in cyber-physical systems. Subsequent work may include:

- Formal bounds on detection delay under noise.  
- Integration with regime-aware control strategies.  
- Cross-domain validation in other infrastructure systems.

The long-term objective is to enhance the stability and resilience of Australia’s evolving electricity system through principled, complexity-aware monitoring and intervention frameworks.

