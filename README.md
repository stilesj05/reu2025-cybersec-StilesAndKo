# reu2025-cybersec-StilesAndKo
# Quantum-Enhanced Knowledge Graphs and Optimization for Trustworthy Multi-Agent Coordination in Digital Twin Robotics

## Students
- Joseph Ko  
- Jaydine Stiles  

## Mentor
- Yugyung Lee  

## Project Summary
This project explores how quantum-enhanced graph optimization and dynamic trust modeling can improve the safety and efficiency of multi-agent coordination in robotics systems that rely on digital twins.  

Real-time digital twins mirror physical robots and environments but introduce new cybersecurity risks such as sensor spoofing, message tampering, and desynchronization attacks. Our goal is to build an AI-enhanced, trust-aware system that detects and responds to such attacks, ensuring safe collaboration between humans and robot teams in dynamic environments.

## Tools and Models Used:
AI Models:
- Graph Neural Networks (GNNs) for modeling complex relationships between robots, environments, and tasks within dynamic knowledge graphs.
- Quantum Approximate Optimization Algorithm (QAOA) for real-time task allocation and trust-aware path planning.
- TIP and ECT trust updates embedded in a live knowledge graph (robots, tasks, sensors, humans).
- Autoencoders/anomaly detection models to identify compromised data flows or adversarial manipulation.

Tools and Libraries:
- Qiskit for QAOA and other quantum needs.
- PyTorch for developing and training classical machine learning models like GNNs or autoencoders.
- Hugging Face Transformers for integrating LLM -based reasoning into agent decisions or knowledge graph summarization.
- NetworkX/DGL for graph-based modeling of robots, environments, and trust relationships.
- Digital Twin Platforms (simulation, Unity3D specifically) to represent the physical-virtual interaction part of this project.

## Notes on Reproduced Work

Model Name: Automatic Mask Generator (based on Segment Anything)

Source:  
Barsellotti, Luca, et al. “Personalized Instance-Based Navigation toward User-Specific Objects in Realistic Environments.” Advances in Neural Information Processing Systems, vol. 37, 16 Dec. 2024, pp. 11228–11250, https://arxiv.org/pdf/2410.18195. Accessed 15 June 2025.

Implementation Process:

- Forked the Official Github repository, and used the Segment Anything model in Google Colab.
- Loaded the pretrained Segment Anything model (ViT-H variant).
- Used the SamAutomaticMaskGenerator to generate masks from input images.
- No major code changes were made to the original repository aside from adapting it to a test image for demonstration.

Environment:

- Python 3.9
- PyTorch
- Torchvision
- Segment-anything

Evaluation:

- Successfully reproduced the functionality of the SOTA model on a test image.
- The model generated masks accurately and rapidly, validating its zero-shot capability to segment novel objects without task-specific training.
- However, the “happy medium” of masks is unknown, as too many masks creates too many objects and does not accurately represent the environment, and too few masks has a similar problem; the only difference is that it captures too few objects, not too many.

Our Own Approach:

- As of now, we have only reproduced the baseline SOTA model.
- While we haven’t built our own segmentation model yet, this reproduction sets a strong and reliable starting point to improving mask generation.
- Our next steps would be to figure out if we can find out the “happy medium” of mask generation, and maybe find a way to use AI/Quantum AI to improve the accuracy of the mask generation to more accurately represent the objects in the room.

## Setup Instructions
- TBD
