
**Project Proposal: The Civic Resonator**  
**A Cyber-Physical Implementation of Complexity Economics and Endogenous Learning in Multi-Agent Systems**  

**Yeu Wen Mak**  
**Date: 15 February 2026**  

**Student:** Yeu Wen Mak  
**Course:** CYBN8001 – Cyber-Physical Systems  
**Institution:** Australian National University, School of Cybernetics  

---

#### 1. Context: The “Green-on-Green” Conflict as a Complexity Failure

- While the ANU Centre for Energy Systems (ACES)—formed by consolidating the Battery Storage and Grid Integration Program (BSGIP) and 100% Renewable Energy Group (RE100)—has solved technical challenges like resource mapping via High-Resolution Heatmaps (ACES Assessment, p.2), the “Siting Bottleneck” remains.  
- As noted by ACES researchers Logie and Ransan-Cooper, technical solutions fail without Social License. Co-directed by Professor Kylie Catchpole (solar PV/materials) and Associate Professor Heather Logie (policy/psychology/operations), with founder Professor Lachlan Blackhall as Deputy Vice-Chancellor (Research and Innovation), ACES adopts a holistic, systems-based paradigm to address the “wicked problems” of integrating variable renewable energy (VRE) into grids designed for centralized thermal plants.  
- This project addresses the “Institutional Structural Deficit” by simulating the social friction that currently stalls the $1B Solar Sunshot initiative.  
- The transition to a Net Zero economy is no longer a binary struggle between “Green” and “Black” energy. As exemplified by the Nelson Wetlands planning crisis (ABC News, Dec 2025), the new frontier of conflict is “Green-on-Green”: a clash between rapid renewable infrastructure (solar/wind) and local ecological preservation/community stability.  
- Traditional models treat these as “Equilibrium Problems” — assuming prices/taxes/subsidies can optimize compromise. Rooms lack live maps of interaction quality (Taylor & Page, 2025), leading to failures in collective intelligence.  
- This project argues that assumption is false.  
- Drawing on J. Doyne Farmer (Oxford/SFI), the Nelson Wetlands conflict is a Non-Equilibrium System characterized by:  
  1. Path Dependency: History matters. A small trust breakdown creates permanent “lock-in” of gridlock.  
  2. Bounded Rationality: Stakeholders operate on local heuristics and imperfect information.  
- Therefore, we cannot “solve” it with a spreadsheet. We must simulate interaction dynamics to understand intervention.

---

#### 2. Theoretical Framework: Integrating Farmer’s Insights

This proposal operationalises three specific findings from Farmer’s *Making Sense of Chaos* (2024/2026) into physical hardware.

**2.1 Cybernetic Foundations from Collective Intelligence**  
- Drawing from network science and ANU precedents, the framework emphasizes higher-order interactions for emergent coherence. Battiston et al. (2025) demonstrate social cohesion spreads via simplicial complexes (triangles of simultaneous reinforcement) rather than dyadic edges, aligning with Taylor & Page’s (2025) call for tools bridging “smart local actions” with “system-wide synergies.”  
- This extends ANU’s Social Regulation archetype (e.g., Breath Connection, 2025), shifting from individual to inter-personal regulation via real-time entropy metrics.  
- ACES’ holistic, systems-based paradigm (rejecting linear models, embracing uncertainty/dynamism) supports this cybernetic approach to wicked problems in VRE integration and social license.  
- Impact of References:  
  - Brookings (Taylor & Page, 2025): “Rooms lack live maps” → inspires haptic/visual feedback as entropy “live map” for Groan Zone navigation in energy conflicts.  
  - Nature Human Behaviour (Battiston et al., 2025): Higher-order interactions → justifies simplicial gating in Layer A for emergent intelligence in multi-stakeholder coordination.

**2.2 Endogenous Technological Change (Wright’s Law)**  
- Standard economics assumes exogenous costs. Farmer shows costs follow Wright’s Law: power-law drop with cumulative experience.  
- In Energy Sector: Solar cheapened via learning-by-doing (more panels built).  
- In this Project: Hypothesize “Social Coordination” follows same law — agreement cost drops as group accumulates successful interaction time. System must “learn” from its history.

**2.3 Sensitive Intervention Points (SIPs): Kicks vs. Shifts**  
- Kick (Parametric): Adjust variable (e.g., subsidy) — often absorbed, system returns to chaotic state.  
- Shift (Structural): Change connections/rules — alters basin of attraction, makes old state impossible.

**2.4 The “Volatility Trap” (The Fossil Fuel Death Spiral)**  
- Farmer: Incumbent systems enter death spiral as volume drops → volatility rises → capital flees → volatility worsens.  
- In this Project: Model trust breakdown in Nelson Wetlands as volatility trap. Variance exceeding threshold structurally degrades system (forgets history), simulating planning collapse. Ties to ACES’ “Evolve” platform logic for dynamic operating envelopes in social/energy networks.

---

#### 3. System Architecture & Mathematical Model

The Civic Resonator is a closed-loop dynamical system simulating collective attention physics (not vote processing). Three layers map to cybernetic feedback horizons.

**3.1 Layer A: “Bounded Rationality” Interface (Input)**  
- Hardware: 3 × Capacitive Copper Touch Points (ESP32 Touch API).  
- Rationale: Enforces bounded rationality (no speech/text). Relies on heuristics/signalling (Taylor & Page). Simplicial gating: inputs activate only within 50ms simultaneity window.  
- Input $u_i(t) \in [0, 1]$: analog signal from touch duration/pressure.  
  - $u \approx 0$: Disengagement.  
  - $u \approx 0.5$: Uncertainty (Groan Zone).  
  - $u \approx 1.0$: Strong commitment.

**3.2 Layer B: “Wright’s Law” Processor (Core Logic)**  
- Hardware: ESP32-S3 Microcontroller.  
- Model: Graph Cellular Automaton (GCA) with endogenous rule evolution (Farmer’s learning curves).  
- State update:  
  \[ x_i(t+1) = (1 - \alpha)x_i(t) + \beta(t) \cdot \Phi(\text{neighbors}) + \gamma \cdot u_i(t) \quad (1) \]  
- Endogenous \beta evolution:  
  \[ \beta(t) = \beta_{\text{initial}} + \omega \cdot \log(1 + C_{\text{cum}}(t)) \quad (2) \]  
- Coordination cost:  
  \[ E(t) = \sum_{i=1}^3 \int_0^t u_i(s) \, ds \cdot (1 - \beta(t)) \quad (3) \]  
- Early: expensive (low \beta). Mature: cheaper (high \beta, resilient).

**3.3 The “Social Dynamic Operating Envelope” (Volatility Trap)**  
- Social Trust as constrained asset with DOE (from BSGIP “Evolve” platform).  
- If $\sigma^2(t) > \kappa$ → Trust Reset: $C_{\text{cum}}(t+1) = C_{\text{cum}}(t) \cdot \delta$ ($\delta < 1$).  
- Result: Forgets history, \beta collapses, reverts to chaotic baseline.

**3.4 Layer C: Algedonic Feedback (Output)**  
- Hardware: 60-pixel Neopixel Ring + Haptic Motor Driver.  
- Visual: Entropy → colour temperature (Cyan low, Red high).

---






- Haptic: Variance $\sigma^2(t)$ → motor intensity (smooth pulse low, jarring high).

