# CYBN8001 Maker Project – Design Brief
## Algorithmic Mesoscope: A Cyber-Physical Instrument for Mesoscopic Coordination Observability

**Student:** Yeu Wen Mak  
**Course:** CYBN8001 – Building Cyber-Physical Systems  
**Prototype Type:** Interactive Cyber-Physical Instrument  

---

# 1. Project Intent and Direction

The Algorithmic Mesoscope is a cyber-physical instrument designed to render coordination regimes observable through real-time embodied feedback.

Rather than predicting behaviour or optimizing outcomes, the system functions as an experimental device that makes the structure of multi-agent coordination perceptible at a mesoscopic level — between individual actions and collective outcomes.

The central design question guiding this prototype is:

> How can a cyber-physical system transform distributed human inputs into an embodied representation of coordination regimes in real time?

The prototype aims to demonstrate that coordination is not merely a scalar quantity but can exhibit qualitatively distinct regimes (stable alignment, oscillation, fragmentation, lock-in), which can be surfaced through appropriate sensing–computation–actuation integration.

This project is intentionally scoped as a convincing prototype rather than a finished product, prioritizing conceptual clarity, CPS integration, and demonstrable functionality within a 12-week timeframe.

---

# 2. Research Grounding and Cybernetic Framing

The project is informed by:

- Cybernetic feedback systems (closed-loop sensing and actuation)
- Mesoscopic representation in complex systems
- Coordination theory in multi-agent settings
- Algedonic signalling (feedback signalling stress or instability)
- The Cybernetic Wheel model (sensing → interpreting → deciding → acting → reflecting)

The prototype operationalizes these principles through a physical feedback loop:

Human input → Real-time computation → Regime representation → Embodied feedback → Human adaptation

This recursive loop allows participants to experience coordination structure as a dynamic phenomenon.

---

# 3. Development Pathways and Adaptive Architecture Strategy

Given the exploratory nature of the prototype and the 12-week constraint, the technical architecture will follow an adaptive pathway informed by early simulation and prototyping outcomes.

Two primary implementation paths are identified:

## Path A: Raspberry Pi–Centric Architecture (Rapid Iteration Path)

**Use Case:** If early simulation indicates significant need for signal logging, threshold tuning, smoothing experimentation, or regime classification refinement.

Hardware:
- Raspberry Pi (Zero 2 W or equivalent Linux-capable board)
- USB or GPIO-connected input sensors (rotary encoders or capacitive touch)
- LED ring/matrix
- Haptic motor and optional servo

Advantages:
- Full Python environment for rapid iteration
- Real-time logging and debugging
- Easier experimentation with smoothing and classification
- Faster threshold calibration for regime visualization

Trade-offs:
- Slightly higher boot time
- Less deterministic timing compared to microcontrollers

This path prioritizes developmental speed, computational transparency, and tunability.

---

## Path B: Microcontroller-Centric Architecture (Embedded Robustness Path)

**Use Case:** If early prototyping shows computation requirements are lightweight and stable, and deterministic timing or electrical simplicity becomes a priority.

Hardware:
- ESP32 or Raspberry Pi Pico
- Direct GPIO sensor integration
- LED ring/matrix
- Haptic motor and optional servo

Advantages:
- Instant boot and deterministic loop timing
- Lower system complexity
- Strong embedded-systems skill development

Trade-offs:
- More constrained debugging workflow
- Slower iteration when tuning representations

This path prioritizes embedded robustness and hardware purity.

---

## MVP Decision Gate (Week 3–4)

A decision between Path A and Path B will be made after:

- Initial coherence metric simulation
- Basic sensor integration test
- Latency measurement
- Early regime visualization trials

The selection criterion will be:

- Stability of real-time loop
- Ease of threshold calibration
- Development efficiency under time constraints

This adaptive architecture strategy ensures feasibility while preserving conceptual integrity.

---

# 4. Core System Architecture

The system consists of four integrated CPS components.

## 3.1 Physical Build

A custom tabletop instrument housing:

- 3–6 input nodes (rotary encoders or capacitive touch sensors)
- LED ring or matrix for visual feedback
- Vibration motor for haptic feedback
- Optional servo-driven tension gauge

The enclosure will be fabricated using laser-cut acrylic or plywood, ensuring that the majority of structural work is original.

---

## 3.2 Sensing

Each participant interacts with one input node representing a commitment or strategic position variable.

Hardware:
- ESP32 or Raspberry Pi Pico microcontroller
- 50 ms sampling interval

The sensing layer establishes the microstate of the system.

---

## 3.3 Computation (Mesoscopic Representation)

The system computes coordination coherence:

C(t) = 1 - (1 / N(N-1)) Σ |ai(t) - aj(t)|

Where:
- ai(t) represents agent input values
- N represents number of participants

Optional extensions (time permitting):
- Sliding window smoothing
- Variance or entropy-based representations
- Simple oscillation detection

The computation layer translates distributed micro-inputs into a mesoscopic representation suitable for regime classification.

---

## 3.4 Actuation

The system externalizes coordination regimes via:

Visual Feedback:
- Green: stable coordination
- Yellow: oscillatory regime
- Red: fragmentation
- White/Blue: lock-in

Haptic Feedback:
- Vibration intensity proportional to instability

Mechanical Feedback (optional):
- Servo-driven gauge representing coordination pressure

Actuation closes the feedback loop and enables embodied perception.

---

# 4. Anticipated Challenges and Risk Management

## Technical Risks

1. Signal noise and jitter
   - Mitigation: smoothing filters and threshold tuning

2. Latency in feedback loop
   - Mitigation: optimize computation and sampling rate

3. Mechanical fragility during public interaction
   - Mitigation: reinforced enclosure and strain relief

4. Over-sensitivity or under-sensitivity of regime thresholds
   - Mitigation: iterative tuning with small pilot tests

---

## Conceptual Risks

1. Over-simplification of coordination dynamics
   - Acknowledge prototype scope and bounded ambition

2. Misinterpretation as performance evaluation tool
   - Clear communication that the instrument visualizes structure, not individuals

---

# 5. Responsible and Sustainable Design

Safety:
- Low-voltage operation
- Enclosed wiring
- Lab-safe construction

Sustainability:
- Modular components reusable for future research
- Recycled or repurposed enclosure materials where feasible

Sunset Plan:
- Electronics salvaged for subsequent CPS experiments
- Enclosure repurposed or disassembled responsibly

---

# 6. Budget and Feasibility

Estimated budget (under $250 constraint):

- Microcontroller: ~$15
- Input sensors (3–6): ~$30
- LED matrix/ring: ~$25
- Servo + haptic motor: ~$30
- Power supply and wiring: ~$40
- Enclosure materials: ~$50
- Contingency: ~$40

Total projected cost: ~$230

The build is staged over 12 weeks with an MVP-first strategy.

---

# 7. Minimal Viable Prototype (MVP)

The MVP will include:

- 3 input nodes
- Real-time coherence computation
- LED-based regime visualization

Additional actuation layers will be added iteratively as time permits.

---

# 8. Criteria for Success

By Demo Day, the prototype should:

- Demonstrate a stable sensing–computation–actuation loop
- Exhibit visible coordination regime transitions
- Withstand repeated public interaction
- Clearly communicate its cybernetic logic

---

# 9. Feedback Sought from Supervisors

To refine the prototype for Milestone 2 and final documentation, feedback is sought on:

1. Appropriateness of the coherence metric for regime visualization
2. Balance between simplicity and representational richness
3. Robustness expectations for Demo Day interaction
4. Suggestions for improving physical build quality
5. Alignment with cybernetic principles and course expectations

---

# 10. Project Trajectory Beyond CYBN8001

While scoped for a single semester, the prototype establishes a minimal experimental substrate for future work on representation-dependent observability and regime detection in cyber-physical systems.

The emphasis for CYBN8001 remains on build integrity, integration quality, and reflective skill development.

