
---

# Project Proposal: The Algorithmic Mesoscope

**Stakeholder Brief: A Cyber-Physical Instrument for Group Coordination**

## 1. Project Executive Summary

The **Algorithmic Mesoscope** is a physical prototype designed to make the invisible dynamics of group coordination observable in real-time. By translating individual inputs into collective feedback, the system acts as an experimental instrument to demonstrate how multi-agent systems reach stability or fall into fragmentation.

---

## 2. Technical Architecture (The CPS Stack)

To satisfy the requirements for a functional Cyber-Physical System (CPS), the project is organized into three integrated layers:

### Layer A: Sensing (Physical Input)

* **Hardware:** 3–6 capacitive touch nodes or rotary encoders connected to an **ESP32** or **Raspberry Pi Pico**.
* **Function:** Each node represents a participant's state (e.g., level of commitment or agreement)
* **Sampling:** Data is polled at **5ms intervals** to ensure high-fidelity interaction.



### Layer B: Computation (Python/Colab Implementation)

The system processes raw input into a **Coordination Coherence Metric ($C(t)$)**.

**Computational Logic (for Google Colab):**
The coordination is calculated using the average pairwise alignment of all agents:


$$C(t) = 1 - \left( \frac{1}{N(N-1)} \sum_{i \neq j} |a_i(t) - a_j(t)| \right)$$


* **$C \approx 1$**: High coordination (Alignment).

* **$C \approx 0$**: Fragmentation (Disorder).

* **Implementation:** Python scripts will handle data smoothing and real-time visualization of these stability curves.



### Layer C: Actuation (Embodied Feedback)

The computed metric is "pushed" back into the physical world through **Algedonic (pleasure/pain) feedback**:

* **Visual:** An LED ring/matrix (Green for stability, Red for chaos).

* **Haptic:** Vibration intensity increases as coordination decreases.

* **Mechanical:** A servo-driven tension gauge to physically represent "social pressure".



---

## 3. Build & Fabrication Plan (12-Week Timeline)

This plan focuses on creating a "convincing prototype" that is robust and aesthetically thoughtful.

| Phase | Focus | Deliverables |
| --- | --- | --- |
| **Weeks 1-3** | **Foundations** | Microcontroller setup; basic sensing circuit; LED logic. |
| **Weeks 4-6** | **Expansion** | Integration of multiple nodes; servo calibration; Python bridge. |
| **Weeks 7-9** | **Refinement** | Metric tuning in Colab; aesthetic enclosure fabrication |
| **Weeks 10-12** | **Demo Ready** | Final documentation; safety review; public presentation. |

---

## 4. Responsible Design & Sustainability

* **Safety:** The device operates on low-voltage (USB/Battery) with all wiring enclosed for lab-safe interaction.

* **Sustainability:** The enclosure will utilize recycled materials where possible.

* **Sunset Plan:** Upon project completion, the ESP32 and sensors will be reclaimed for future research modules.



---

## 5. Success Criteria

* **Functional CPS Loop:** Successful integration of sensing, computation, and actuation.

* **Technical Growth:** Demonstrable mastery in Python-based data processing and hardware fabrication.

* **Reproducibility:** Comprehensive documentation in a "Build Journey" format to allow for future research.



---
