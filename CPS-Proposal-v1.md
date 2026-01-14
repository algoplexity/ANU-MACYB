

***

# Project Proposal: The Civic Resonator
**Engineering Higher-Order Cybernetics for Collective Intelligence**

**Student:** Yeu Wen Mak
**Course:** CYBN8001 – Cyber-Physical Systems
**Institution:** Australian National University, School of Cybernetics
**Date:** January 14, 2026

---

## 1. Executive Summary

This project proposes the design and fabrication of the **Civic Resonator**, a tabletop cyber-physical interface designed to operationalize the "Physics of Collective Intelligence."

Recent analysis by the **Brookings Institution** argues that modern policymaking fails because it lacks the infrastructure to bridge "Design-Minded" conveners (who run rooms) with "Model-Minded" systems thinkers (who map complexity) [1]. Simultaneously, network science research by **Battiston et al. (2025)** has proven that complex social change requires "Higher-Order Interactions"—specifically, simultaneous reinforcement from multiple peers—rather than simple pairwise influence [2].

**The Civic Resonator** synthesizes these findings into a physical artifact. It uses **Graph Neural Cellular Automata (GNCA)** to detect and reinforce social synchrony. By translating the invisible "entropy of thought" into visible, haptic feedback, it acts as a "Civic Thermostat," stewarding small groups away from linear noise and toward the non-linear coherence required for consensus.

---

## 2. Context & Rationale

### 2.1 The Problem: "Rooms lack live maps"
Taylor & Page (2025) identify a critical gap in collective intelligence: when humans gather to solve problems, we have no real-time metric for the *quality* of our interaction. We drift into "Local Minima" because we cannot sense the system's topology. The authors argue for new tools that align "smart local actions" with "system-wide synergies" [1].

### 2.2 The Scientific Solution: Simplicial Complexes
Battiston et al. (2025) provide the physics to solve this. They demonstrate that social cohesion spreads via **Simplicial Complexes** (triangles/tetrahedrons of interaction) rather than dyadic edges (lines).
*   **The Cybernetic Mandate:** To build a CPS that fosters collective intelligence, we must engineer a **"Simultaneity Gate"**—a sensor that filters out individual noise and only activates when a group reaches a specific *temporal* and *topological* threshold.

### 2.3 Precedents in the ANU Cohort
This project builds upon the *Social Regulation* archetype seen in the 2025 "Prototypes for a Better Future" showcase:
*   Unlike *Breath Connection* (2025), which focused on **individual** biological regulation, this project focuses on **inter-personal** regulation.
*   Unlike *Mosaic* (2025), which was a representational map, the Resonator is **functional**—it actively refuses to operate unless the group dynamics meet the criteria for Higher-Order Interaction.

---

## 3. Technical Implementation (The "Making")

The device is a **Social-Cyber-Physical Loop** comprising three functional layers.

### Layer A: The Simplicial Sensor (Input)
*   **Hardware:** 3x Capacitive Touch Points (Copper) arranged radially.
*   **The Battiston Logic:** The system uses a **Non-Linear Gating Function**.
    *   *Scenario 1 (Linear):* Person A touches. Then Person B touches. $\rightarrow$ **System Ignore** (Dyadic noise).
    *   *Scenario 2 (Simplicial):* Person A, B, and C interact within a **50ms window**. $\rightarrow$ **System Active** (Simplicial Complex detected).
*   *Engineering Challenge:* Calibrating capacitive thresholds to distinguish intentional "collaborative touch" from accidental contact.

### Layer B: The GNCA Processor (The "Model")
*   **Hardware:** ESP32 Microcontroller.
*   **The Algorithm:** A continuous **Graph Neural Cellular Automaton**.
    *   **Topology:** The group is modeled as a cyclic graph ($A \to B \to C \to A$).
    *   **Entropy:** The system applies a constant "Entropic Decay." If interaction stops, the system cools to a "Chaos" state (0).
    *   **Phase Transition:** Only when the "Simplicial Input" (Layer A) exceeds the "Entropic Decay," the GNCA state snaps to a "Soliton" state (1).

### Layer C: The Ambient Actuator (Output)
*   **Hardware:** Neopixel LED Ring (60px) + Haptic Motor Driver.
*   **The Feedback:**
    *   *Sub-Threshold:* Light is dim and chaotic (Cellular Automata Rule 60).
    *   *Threshold Met:* Light creates a stable, breathing "Standing Wave" (Cellular Automata Rule 54) and the motor emits a coherent hum.

---

## 4. Alignment with CYBN8001 Learning Outcomes

| Learning Outcome | Project Execution Strategy |
| :--- | :--- |
| **"Technological Constellations"** | The project explicitly links **Hardware** (capacitance) to **Sociology** (Brookings) and **Mathematics** (Battiston). It demonstrates that a CPS is not just "chips and wires" but a constellation of human values and physical laws. |
| **"Interrogate Separate Components"** | We will critically analyze the sensors: *Can capacitance measure intent?* We will explore **Goodhart’s Law**—will users "game" the device by rhythmically tapping it without actually reaching consensus? |
| **"Embody Values"** | The artifact embodies **Collective Agency**. By refusing to work for an individual, it physically encodes the value that *“Higher-order interactions drive collective behavior”* [2]. |
| **"Making & Building"** | **Phase 1:** Build the "Simultaneity Gate" circuit (Week 1-4).<br>**Phase 2:** Code the GNCA and Entropic Decay (Week 5-8).<br>**Phase 3:** Fabrication of the chassis (Week 9). |

---

## 5. Evaluation Plan: The Mock Summit

To test the system in a "Work Integrated Learning" context, the prototype will be deployed in a mock negotiation setting.
*   **Setup:** Three participants are given conflicting secret objectives.
*   **Intervention:** The Resonator is placed in the center. Participants are told it acts as a "truth serum" for their coherence.
*   **Observation:** We will observe if the physical presence of the device changes the *negotiation tactics* (moving from adversarial to cooperative) or if it becomes a distraction.

---

## 6. References

**[1] Taylor, J., & Page, S. E. (2025).** *AI is changing the physics of collective intelligence.* The Brookings Institution.
*Relevance:* Establishes the societal need for tools that bridge "local actions" with "system models."

**[2] Battiston, F., et al. (2025).** *Higher-order interactions shape collective human behavior.* Nature Human Behaviour.
*Relevance:* Provides the mathematical proof that social cohesion requires "simultaneous exposure" (triangles) rather than pairwise links.

**[3] ANU School of Cybernetics. (2025).** *Prototypes for a Better Future: 2025 Student Showcase.* Australian National University.
*Relevance:* Benchmarking against previous "Social Regulation" projects like *Breath Connection*.
