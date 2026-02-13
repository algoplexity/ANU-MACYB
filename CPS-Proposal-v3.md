

# Project Proposal: The Civic Resonator

## Engineering Cybernetic Feedback for Collective Intelligence in Complexity Economics and Energy Transitions

**Student:** Yeu Wen Mak

**Course:** CYBN8001 – Cyber-Physical Systems

**Institution:** Australian National University, School of Cybernetics

**Date:** 14 February 2026

## Executive Summary

This project proposes the design and fabrication of the **Civic Resonator**, a tabletop cyber-physical system (CPS) that operationalizes the "physics of collective intelligence" for managing complexity in energy transitions. Building on prior ANU prototypes like *Breath Connection* (2025), which regulated individual bio-feedback for social harmony, the Resonator extends higher-order cybernetics to collective intelligence in complex systems. As Taylor & Page (2025) note, modern gatherings fail without real-time metrics for interaction quality, leading to "local minima" in decision-making. This is exacerbated in energy economics, where "Green-on-Green" conflicts—like the Nelson Wetlands crisis—arise from non-equilibrium dynamics, as analyzed by J. Doyne Farmer (2024/2026). By synthesizing Battiston's simplicial complexes (higher-order interactions) with Farmer's endogenous learning and volatility traps, the Resonator creates a CPS that detects and reinforces emergent coherence, reducing transaction costs (e.g., permitting delays increasing levelized cost of energy by 20-30%) in renewable planning. The device will be tested via the "Nelson Protocol," demonstrating cybernetic interventions for affordable, equitable decarbonization.

## 1. Context: The "Green-on-Green" Conflict as a Complexity Failure

The transition to a Net Zero economy is no longer a binary struggle between "Green" and "Black" energy. As exemplified by the **Nelson Wetlands planning crisis** (ABC News, Dec 2025), the new frontier of conflict is "Green-on-Green": a clash between the imperative for rapid renewable infrastructure (solar/wind) and the imperative for local ecological preservation and community stability. This mirrors broader energy economics challenges in Australia, where high DER penetration (e.g., rooftop solar leading per-capita globally) creates misaligned incentives, such as unpriced externalities (biodiversity loss) versus subsidized deployment, delaying projects and inflating levelized cost of energy (LCOE) by 20-30% (IEA, 2025; ACES socio-economic review, 2025).

Traditional economic and governance models treat these conflicts as "Equilibrium Problems"—assuming that if we get the prices (taxes/subsidies) right, the stakeholders will settle on an optimal compromise. Rooms lack live maps of interaction quality (Taylor & Page, 2025), leading to failures in collective intelligence.

**This project argues that this assumption is false.**

Drawing on the research of **J. Doyne Farmer (Oxford/SFI)**, we posit that the Nelson Wetlands conflict is a **Non-Equilibrium System**. It is characterized by:

1. **Path Dependency:** History matters. A small breakdown in trust early in the process creates a permanent "lock-in" of gridlock, regardless of future incentives.

2. **Bounded Rationality:** Stakeholders (Developers, Ecologists, Residents) do not calculate global utility; they operate on local heuristics and imperfect information.

Therefore, we cannot "solve" the Nelson Wetlands crisis with a spreadsheet. We must **simulate** the interaction dynamics to understand how to intervene, using cybernetic feedback to foster collective intelligence.

## 2. Theoretical Framework: Integrating Farmer's Insights with Cybernetic Foundations

This proposal operationalises three specific findings from Farmer's *Making Sense of Chaos* (2024/2026) into physical hardware, built on cybernetic principles of collective intelligence.

### 2.0 Cybernetic Foundations from Collective Intelligence

Drawing from network science and ANU precedents, the framework emphasizes higher-order interactions for emergent coherence. Battiston et al. (2025) demonstrate that social cohesion spreads via **simplicial complexes** (triangles of simultaneous reinforcement) rather than dyadic edges, aligning with Taylor & Page's (2025) call for tools bridging "smart local actions" with "system-wide synergies." This extends ANU's *Social Regulation* archetype (e.g., *Breath Connection*, 2025), shifting from individual to inter-personal regulation via real-time entropy metrics.

### 2.1 Endogenous Technological Change (Wright's Law)

Standard economics assumes costs/frictions are exogenous (determined by time). Farmer demonstrates that costs follow **Wright's Law**: they drop as a power law of *cumulative experience*.

* **In the Energy Sector:** Solar became cheap not because time passed, but because we *built* more solar panels (Learning-by-Doing), as modeled in ACES's battery cost projections (suppressing peak prices by 50% by 2025).

* **In this Project:** We hypothesize that "Social Coordination" follows the same law. The "energy cost" of reaching agreement should drop exponentially as the group accumulates **successful interaction time**. The system must "learn" from its own history, enabled by cybernetic feedback loops that reinforce simplicial synchrony.

### 2.2 Sensitive Intervention Points (SIPs): Kicks vs. Shifts

Farmer distinguishes between two types of intervention in complex systems:

* **The Kick (Parametric):** Adjusting a variable (e.g., a subsidy or tax). In a complex system, the system often absorbs the kick and returns to its previous chaotic state.

* **The Shift (Structural):** Changing the connections or rules of the system. This alters the "basin of attraction," making the old, chaotic state mathematically impossible—e.g., topology shifts from rings to fully connected graphs, fostering collective intelligence via bidirectional feedback (Battiston).

### 2.3 The "Volatility Trap" (The Fossil Fuel Death Spiral)

Farmer describes how incumbent systems (like fossil fuels) enter a death spiral: as volume drops, volatility increases, driving capital away, which further increases volatility.

* In this Project: We model the "breakdown of trust" in the Nelson Wetlands not as a linear disagreement, but as a volatility trap. If the variance in the group's signal exceeds a threshold, the system should structurally degrade (forgetting its learned history), simulating the collapse of a planning process. This ties to energy market volatility (e.g., negative prices from excess solar, per ACES's 2023 emissions-prices study).

## 3. System Architecture & Mathematical Model

The Civic Resonator is designed as a closed-loop dynamical system. It does not "process votes"; it simulates the physics of collective attention via cybernetic horizons.

The architecture consists of three functional layers, explicitly mapped to the Three Horizons of cybernetic feedback.

### 3.1 Layer A: The "Bounded Rationality" Interface (Input)

**Hardware:** 3 × Capacitive Copper Touch Points (ESP32 Touch API).

**Rationale:** Consistent with Farmer's critique of the "Rational Agent" model, the interface enforces Bounded Rationality. Participants are stripped of complex linguistic tools (speech, text). They are forced to rely on "heuristics" and "signalling"—precisely the mechanisms Taylor & Page (2025) identify as the drivers of emergent collective intelligence. This incorporates Battiston's simplicial gating: Inputs activate only within a 50ms window of simultaneity, filtering dyadic noise for higher-order coherence.

* **Input \(u_i(t) \in [0, 1]\):** A continuous analog signal derived from touch duration and pressure.

  * \(u \approx 0\): Disengagement.

  * \(u \approx 0.5\): Uncertainty/Oscillation (The "Groan Zone").

  * \(u \approx 1.0\): Strong Assertion/Commitment.

### 3.2 Layer B: The "Wright's Law" Processor (Core Logic)

**Hardware:** ESP32-S3 Microcontroller.

**The Model:** The core is a Graph Cellular Automaton (GCA) where the rules of interaction evolve endogenously. This is the specific implementation of J. Doyne Farmer's "Learning Curves" (Wright's Law), extending V1's GNCA with entropy decay for cybernetic regulation.

**The Base Equation (State Update):** \(x_i(t+1) = (1 - \alpha)x_i(t) + \beta(t) \cdot \Phi(\text{neighbors}) + \gamma \cdot u_i(t)\)

**Where:**

* \(x_i(t)\): The internal state of Node \(i\) (e.g., The Developer).

* \(\alpha\): The Memory Decay (Inertia/Path Dependency).

* \(\gamma\): The Agency (How much force the user applies).

* \(\Phi\): The coupling function (The network topology).

The "Farmer" Upgrade: Endogenous Parameter Evolution: Crucially, the Social Influence parameter \(\beta\) is not static. In standard consensus models, \(\beta\) is fixed. In this system, \(\beta\) evolves according to Wright's Law of Experience:

\[
\beta(t) = \beta_{\text{initial}} + \omega \cdot \log(1 + C_{\text{cum}}(t))
\]

Where:

* \(C_{\text{cum}}(t)\) is the Cumulative Coordination Experience (time spent in sync).

* \(\omega\) is the Learning Rate.

Theoretical Implication: This models the economic reality that "Green Energy" (or Social Trust) gets cheaper/easier the more you do it, reducing LCOE through accumulated stakeholder engagements.

To test the economic "cheaper" hypothesis, we define the coordination energy cost at time \(t\) as the aggregate user input required to maintain system coherence:

\[
E(t) = \sum_{i=1}^{3} \int_{0}^{t} u_i(s) \, ds \cdot (1 - \beta(t))
\]

Where the integral sums cumulative user effort, modulated by \(\beta(t)\) to reflect learning-reduced costs. In trials, \(E(t)\) should drop superlinearly in mature phases, quantifiable via hysteresis tests—linking to energy economics resilience (e.g., stable markets post-subsidy).

* Early Phase: Coordination is "expensive" (low \(\beta\), high resistance).

* Mature Phase: After sufficient history, \(\beta\) rises. The system "learns" to coordinate, making it resilient to small perturbations.

### 3.3 The "Volatility Trap" (The Entropy Failure Mode)

To model the "Death Spiral" of the Nelson Wetlands planning process (where conflict scares away investment/trust), the system includes a Volatility Trigger.

If the variance of the group state \(\sigma^2(t)\) exceeds a critical threshold \(\kappa\) for a duration \(\tau\):

\[
\text{If } \sigma^2(t) > \kappa \text{ then } C_{\text{cum}}(t + 1) = C_{\text{cum}}(t) \cdot \delta
\]

Where \(\delta < 1\) is the Trust Erosion Factor.

* Result: High conflict causes the system to "forget" its learned history (\(C_{\text{cum}}\) drops). The \(\beta\) parameter collapses. The group loses its "learning curve" advantage and falls back to a chaotic, uncoordinated baseline, simulating energy market collapse (e.g., volatility eroding NPV for renewables).

### 3.4 Layer C: Algedonic Feedback (Output)

**Hardware:** 60-pixel Neopixel Ring + Haptic Motor Driver.

The internal mathematics are rendered physically:

* Visual: The "Heat" of the system (Entropy) is mapped to Colour Temperature (Cyan = Low Entropy, Red = High Entropy).

* Haptic: The Variance \(\sigma^2(t)\) drives the motor intensity.

  * Low Variance: Smooth, rhythmic pulse (Coherence).

  * High Variance: Irregular, jarring vibration (The "Volatility Trap").

## 4. The Simulation Scenario: "The Nelson Protocol"

To evaluate the efficacy of the Civic Resonator as a tool for complexity management, the device will be loaded with a specific parameter set designated "The Nelson Protocol."

This scenario simulates the "Green-on-Green" dilemma identified in the Nelson Wetlands planning crisis (ABC, Dec 2025), where the imperative for rapid renewable energy infrastructure clashed with local ecological stability—highlighting energy economics gaps like unpriced externalities and delayed ROI.

### 4.1 Role Assignment (The Agents)

The three capacitive nodes are pre-configured with distinct variable profiles, modeling the conflicting incentives of the real-world stakeholders in energy transitions:

* **Node A: The Developer (High Agency \(\gamma\))**

  * **Behavioral Driver:** Incentivized to maximize signal throughput (Speed of deployment).

  * **System Setting:** High Action Sensitivity (\(\gamma = 0.8\)), Low Memory (\(\alpha = 0.1\)).

  * **Role:** Pushes the system state towards 1.0 (Development Approval) rapidly, representing renewable investors facing LCOE pressures.

* **Node B: The Ecologist (High Volatility Sensitivity)**

  * **Behavioral Driver:** Incentivized to minimize variance (Stability of ecosystems).

  * **System Setting:** Coupled to the Volatility Trap. If \(\sigma^2 > \kappa\), this node triggers a "Veto" (resetting the group's learning parameter \(\beta\)).

  * **Role:** Acts as the system's "brake," representing environmental fragility and regulators enforcing unpriced externalities.

* **Node C: The Resident (High Inertia \(\alpha\))**

  * **Behavioral Driver:** Incentivized to maintain the status quo (Affordable bills).

  * **System Setting:** High Memory Decay (\(\alpha = 0.9\)).

  * **Role:** Resists change. Even if A and B agree, C drags the system back to its historical baseline, modeling community resistance to grid impacts.

### 4.2 The "Groan Zone" (The Interaction Dynamics)

The simulation focuses on the "Groan Zone" (ANU Leadership Complexity Lab, 2025)—the divergent phase where stakeholders must hold tension before convergence is possible, fostering collective intelligence.

* **Phase 1: The Clash.** Node A (Developer) pushes. Node C (Resident) resists. Variance (\(\sigma^2\)) spikes.

* **Phase 2: The Trap.** If the group cannot synchronize their rhythm, the high variance triggers Node B's (Ecologist) volatility threshold. The system enters the "Death Spiral"—the Haptic Motor shakes violently, and the Wright's Law parameter (\(\beta\)) resets to zero. Trust is lost, simulating market collapse.

* **Phase 3: Emergence.** If the group slows down and modulates their input (signaling via rhythm rather than raw force), the \(\beta\) parameter accumulates. The system "learns" to coordinate. The Haptic feedback stabilizes into a coherent pulse (The "Green Transition"), reducing simulated LCOE through collective synergy.

### 4.3 Experimental Design: Testing Farmer's Hypotheses

The Demo Day presentation will strictly test J. Doyne Farmer's distinction between Kicks and Shifts as leverage points in this complex system, via cybernetic interventions.

**Experiment A: The "Kick" (Parametric Intervention)**

* **Action:** We simulate a government subsidy. The system artificially boosts the signal strength (\(\gamma\)) of Node B (Ecologist) by 50% for 30 seconds.

* **Hypothesis (Null):** The system will experience a temporary stabilization, but due to the underlying topology, it will revert to the "Volatility Trap" once the boost (subsidy) is removed. This demonstrates the failure of linear policy interventions in energy markets.

**Experiment B: The "Shift" (Structural Intervention)**

* **Action:** We alter the Network Topology. The connection rules change from a directed Ring (\(A \to B \to C\)) to a Fully Connected Graph (\(A \leftrightarrow B \leftrightarrow C\)) with bidirectional feedback.

* **Hypothesis (Alternative):** This structural change alters the system's "basin of attraction." It creates a permanent Phase Transition where the "Coordinated State" becomes the mathematically stable equilibrium. The system remains coordinated even after individual users stop pushing, enabling collective intelligence for resilient energy transitions.

### 4.4 Success Metric: Hysteresis

We are not measuring user satisfaction. We are measuring Hysteresis (Path Dependence).

* **The Test:** Once the group achieves the "Coordinated Phase" (Green State), how much perturbation (input noise) is required to break it?

* **Prediction:** Under Wright's Law, a mature system (high accumulated history) will be resilient to noise. A young system will be fragile. This proves the economic value of "staying the course" in energy planning.

Hysteresis is quantified by the perturbation threshold \(\theta\), the minimum noise amplitude that reverts the system from coordinated (\(x_i \approx 1\)) to chaotic state:

\[
\theta = \max \left\{ \epsilon \mid \sigma^2(t + \Delta t) \leq \kappa \quad \forall \, \Delta t \in [0, \tau], \, \text{after adding noise} \, \epsilon \sim \mathcal{N}(0, \sigma_\epsilon^2) \right\}
\]

Where \(\epsilon\) is Gaussian noise injected into inputs. Predictions: \(\theta \propto C_{\text{cum}}(t)\), testable by varying noise in Demo Day simulations to demonstrate economic value in "staying the course" for energy transitions.

### 4.5 Alignment with CYBN8001 Learning Outcomes

| Learning Outcome | Project Execution Strategy |
|------------------|-----------------------------|
| **"Technological Constellations"** | The project explicitly links **Hardware** (capacitance) to **Sociology** (Brookings/Taylor & Page) and **Mathematics** (Battiston/Farmer). It demonstrates that a CPS is not just "chips and wires" but a constellation of human values and physical laws, applied to energy economics. |
| **"Interrogate Separate Components"** | We will critically analyze the sensors: *Can capacitance measure intent?* We will explore **Goodhart’s Law**—will users "game" the device by rhythmically tapping it without actually reaching consensus? |
| **"Embody Values"** | The artifact embodies **Collective Agency**. By refusing to work for an individual (via simplicial gating), it physically encodes the value that *“Higher-order interactions drive collective behavior”* (Battiston), reducing energy transition costs. |
| **"Making & Building"** | **Phase 1:** Build the "Simultaneity Gate" circuit (Week 1-3).<br>**Phase 2:** Code the GNCA and Entropic Decay (Week 4-6).<br>**Phase 3:** Fabrication of the chassis (Week 7-10). |

## 5. Implementation Plan: Engineering the "Nelson Protocol"

To ensure the Civic Resonator is ready for the School of Cybernetics Demo Day (Week 10), the fabrication and coding process follows a strict calibration schedule against real-world data.

**Phase 1: Physical Fabrication (Weeks 1-3)**

* **Hardware:** Laser-cutting the "Bounded Rationality" interface. The enclosure will be circular to reinforce the non-hierarchical topology.

* **Electronics:** Soldering the ESP32-S3 to the Neopixel Ring and LRA Haptic Driver.

* **Milestone:** Verify simple capacitive touch latency < 15ms. (Essential for the "rhythm" signaling required by Taylor & Page, 2025).

**Phase 2: The Algorithmic Core (Weeks 4-6)**

* **Coding Layer B:** Implementing the Graph Cellular Automaton in C++.

* **Integrating Wright's Law:** Writing the \(\beta\) function where \(\beta\) scales with \(\omega\).

* **Milestone:** Verify the "Wright Curve." The system must demonstrate mathematically that coordination becomes "cheaper" (requires less input energy) the longer it is sustained, via E(t) plots.

**Phase 3: Calibration against Nelson Data (Week 7)**

* **Tuning \(\alpha\) and \(\gamma\):** We will tune the Inertia (\(\alpha\)) and Agency (\(\gamma\)) parameters to match the volatility observed in the Nelson Wetlands case study (ABC, 2025), incorporating ACES data on socio-economic impacts.

* **Target:** The system must reproduce the "Gridlock" state by default. It should require significant, synchronized effort to break out of the "Volatility Trap," mirroring the difficulty of the real-world planning process.

**Phase 4: User Trials & The "Groan Zone" (Weeks 8-9)**

* **The Experiment:** Run the "Nelson Protocol" with 3 participants (acting as Developer, Ecologist, Resident).

* **Data Collection:** Log the time-series of Variance (\(\sigma^2\)) and Entropy (S).

* **Milestone:** Demonstrate Hysteresis. Prove that once the "Green State" is achieved, the system resists returning to the "Red State" (Chaos) even when perturbed, via \(\theta\) measurements.

**Phase 5: Demo Day (Week 10)**

* **Live Demonstration:** A live 5-minute simulation of a "tipping point" intervention (The Shift) using the structural topology change.

## 6. Conclusion & Future Horizon: The "Artificial Facilitator"

### 6.1 Summary of Consequences

The Civic Resonator is a critique of the "rational consensus" model currently failing in the Nelson Wetlands. By translating J. Doyne Farmer's Complexity Economics into a physical interface, grounded in cybernetic collective intelligence, this project demonstrates that social coordination is a path-dependent, non-equilibrium process.

We provide evidence that:

1. Linear Policy Fails: Simple "Kicks" (subsidies/force) are absorbed by the system's chaotic attractor.

2. Structural Shifts Work: Changing the topology of interaction (from disconnected rings to coupled networks) creates permanent phase transitions, enabling collective synergy.

3. Experience Matters: Operationalizing Wright's Law proves that "trust" is a cumulative asset that lowers the metabolic cost of future cooperation, reducing LCOE in energy transitions.

### 6.2 The Prize-Winning Argument: Bridging the Cybernetic Gap

This project deserves the Demo Day prize because it successfully bridges the "Hard" (Embedded Systems, Graph Theory, Statistical Mechanics) and the "Soft" (Sociology, Leadership Theory, Public Policy). By evolving V1's focus on higher-order interactions into a tool for complexity economics, it turns the abstract mathematics of the ANU Leadership Complexity Lab into a tangible, haptic reality.

### 6.3 Horizon 3: The PhD Extension

The Civic Resonator is Experiment Zero for a doctoral research proposal: "The Artificial Facilitator."

While the current model uses 3 human nodes, the PhD extension will introduce a 4th Node: An AI Agent.

* The Hypothesis: Can an AI agent, trained on the Brookings "Collective Intelligence" model (Taylor & Page, 2025), act as a "Strange Attractor" in a human network for energy governance?

* The Mechanism: The AI node would not "vote." Instead, it would inject specific micro-signals (rhythms) designed to lower the System Entropy (\(\sigma^2\)).

* The Goal: To prove that AI can be used not just to generate content (LLMs), but to modulate social dynamics—nudging human groups out of "Volatility Traps" and into "Coordinated Phases" without coercion, as in ACES's DER orchestration.

This moves the research from "Tabletop Simulation" to "Planetary Governance," answering Doyne Farmer's call for a new economics capable of managing the Anthropocene Transition.

## References

[1] Taylor, J., & Page, S. E. (2025). *AI is changing the physics of collective intelligence.* The Brookings Institution.

[2] Battiston, F., et al. (2025). *Higher-order interactions shape collective human behavior.* Nature Human Behaviour.

[3] ANU School of Cybernetics. (2025). *Prototypes for a Better Future: 2025 Student Showcase.* Australian National University.

[4] Farmer, J. D. (2024/2026). *Making Sense of Chaos.* Oxford University Press.

[5] Sturmberg, B., et al. (2025). *Socio-economic and environmental impacts of renewable energy deployments: A review.* Renewable and Sustainable Energy Reviews (via ACES).

[6] International Energy Agency (IEA). (2025). *World Energy Outlook: Renewable Cost Projections.*

---
