# reu2025-cybersec-StilesAndKo
#  Post-Disaster Hospital Simulation with Digital Twins and Adaptive Task Allocation

## Students
- Joseph Ko  
- Jaydine Stiles  

## Mentor
- Yugyung Lee  

## Project Summary
In emergency scenarios like post-earthquake hospital rescues, robotic agents must coordinate tasks such as triage, transport, and supply delivery in real time under uncertain, hazardous conditions. These scenarios demand not only rapid decision-making but also resilience to changing environments, incomplete information, and varying levels of agent reliability.  
To address these challenges, digital twins—virtual replicas of physical agents and environments—can serve as a central coordination layer by enabling real-time monitoring, planning, and anomaly detection. However, effectively using digital twins for multi-agent task allocation requires optimizing across complex, dynamic constraints such as trust levels, blocked routes, and patient urgency.  
This project investigates how quantum-enhanced graph optimization (via QUBO modeling) can improve digital twin-assisted coordination in a simulated rescue setting. The aim is to evaluate whether quantum-inspired methods can outperform classical task allocation strategies when trust, uncertainty, and environmental risk are encoded as graph attributes.

**Hypotheses:**
- Trust-aware task assignment using quantum graph optimization will yield higher task completion rates (under time and safety constraints) than random or greedy allocation strategies in a simulated rescue scenario.
- Digital twin models updated with real-time trust and environmental feedback will outperform static digital twin models in dynamic path planning tasks.

**Research Questions:**
- RQ1: How can agent trust levels, task urgency, and environmental risks be modeled as a weighted graph suitable for QUBO formulation?
- RQ2: Does using quantum-inspired optimization (e.g., Max-Cut or QAOA over a task-agent graph) improve task allocation efficiency in real-time rescue simulations?
- RQ3: How does integrating a dynamic digital twin (updated with real-time data) affect the adaptability and performance of agent coordination in changing environments?

---

## Tools and Models Used:
AI Models:
- Graph Neural Networks (GNNs) → (Planned) For learning dynamic trust and task relationships in the knowledge graph
- Quantum Optimization Algorithms
  - QUBO formulations → To encode task allocation & routing as binary optimization problems
  - QAOA → For near-optimal task allocation and routing under trust and risk constraints
  - Quantum Annealing → For solving QUBO models efficiently
- Autoencoders (Planned) → For anomaly detection in digital twin sensor data

Tools and Libraries:
- Neo4j → Knowledge graph modeling of agents, tasks, environment, trust
- NetworkX → Synthetic graph generation for quantum optimization testing
- Qiskit / D-Wave Ocean SDK → Quantum optimization and simulation
- PyTorch → Planned for trust score learning and anomaly detection models
- Gymnasium → Reinforcement learning for agent behavior testing
  
## Notes on Reproduced Work

Model Name: Automatic Mask Generator (based on Segment Anything)

Source:  
Barsellotti, Luca, et al. “Personalized Instance-Based Navigation toward User-Specific Objects in Realistic Environments.” Advances in Neural Information Processing Systems, vol. 37, 16 Dec. 2024, pp. 11228–11250, https://arxiv.org/pdf/2410.18195. Accessed 15 June 2025.

Implementation Environment:

- OS: macOS Sonoma
- Python 3.9 (in venv)
- CPU-only machine
- Key dependencies: torch, torchvision, pillow

Checkpoint Adaptation:
- Used smaller ViT-B checkpoint (~420MB) due to GitHub size constraints
- Checkpoint retrieved via `curl`

Demo:
- Loaded SAM ViT-B checkpoint and generated 26 object masks on a 320×240 JPEG
- Runtime: ~0.5s per image (CPU)
- Qualitative results show accurate object boundary segmentation

Comparison:

| Feature     | SAM ViT-H (GPU) | SAM ViT-B (CPU) |
|-------------|------------------|------------------|
| Model size  | ~2.6 GB          | ~420 MB          |
| Speed       | ~0.05s/image     | ~0.5s/image      |
| Mask count  | Hundreds+        | 26               |

Outcome:
- Despite lower performance, the ViT-B version was sufficient for prototype use in segmentation
- Sets a functional baseline for integrating vision into rescue simulation pipeline

---

### Setup Instructions
**TBD**
