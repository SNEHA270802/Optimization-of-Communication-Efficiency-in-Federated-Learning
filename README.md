Optimization of Communication Efficiency in Federated Learning
Overview
This repository contains my MSc Data Science dissertation project from the University of Surrey, which investigates optimization strategies in Federated Learning (FL).
Federated Learning is a decentralized machine learning paradigm that enables multiple distributed clients to collaboratively train a shared model without exchanging raw data, thereby preserving privacy. This approach is particularly relevant for privacy-sensitive domains such as healthcare systems, mobile devices, and edge computing environments.
This research evaluates and compares several federated optimization algorithms under realistic distributed learning conditions, including non-IID data distributions and communication constraints. The goal is to better understand how different optimizers perform when deployed in practical federated learning scenarios.
The complete dissertation report is included in this repository, providing detailed explanations of the methodology, experimental setup, implementation, and analysis of results.
Project Objectives
The primary objectives of this research are to:
Evaluate the performance of widely used Federated Learning optimization algorithms
Analyse model convergence behaviour under non-IID data distributions
Simulate communication constraints similar to real-world edge environments
Identify optimizers that provide the best balance between accuracy, stability, and communication efficiency
Federated Optimizers Evaluated
The following federated optimization strategies were benchmarked in this study:
FedAvg – The baseline federated averaging algorithm
FedAdam – Adaptive optimization applied in federated settings
FedAdagrad – Gradient-based adaptive optimizer designed for improved convergence
FedYogi – An adaptive optimizer aimed at providing stable training
SCAFFOLD – A variance reduction method designed to mitigate client drift
Datasets Used
Experiments were conducted across several benchmark datasets representing diverse image classification tasks:
CIFAR-10
FedMNIST
EMNIST-CR
FashionMNIST
MedMNIST
These datasets were selected to evaluate optimizer performance across different levels of data complexity and heterogeneity.
Experimental Setup
The experiments were implemented using the Flower Federated Learning Framework, which enables flexible simulation of distributed machine learning systems.
Simulation Parameters
Communication Rounds: 100
Number of Clients: 5
Local Training Epochs: 1
Data Distribution: Non-IID partitions
To ensure fair benchmarking, a consistent Convolutional Neural Network (CNN) architecture was used across all experiments.
Key Findings
The experimental analysis revealed several important insights:
FedAdagrad demonstrated the most stable and efficient convergence under communication-constrained environments.
SCAFFOLD performed best in highly heterogeneous data settings, effectively reducing the problem of client drift.
FedAdam showed fast initial convergence but experienced instability when trained on noisier datasets.
FedYogi provided moderate robustness in imbalanced data scenarios.
Overall, no single optimizer consistently outperformed others across all datasets, highlighting the importance of selecting optimizers based on dataset characteristics and deployment conditions.
Applications
The findings of this research provide practical insights for deploying Federated Learning in:
Healthcare AI systems
Mobile and edge computing devices
Privacy-preserving machine learning environments
Distributed artificial intelligence systems
Technology Stack
This project was implemented using the following technologies:
Python
PyTorch
Flower Federated Learning Framework
NumPy
Pandas
Matplotlib
Future Work
Potential directions for future research include:
Scaling experiments to larger federated networks with more clients
Evaluating alternative neural network architectures
Implementing secure aggregation and privacy-enhancing techniques
Studying model performance under different communication budgets and system constraints
Author
Snehashree Gopinath
MSc Data Science
University of Surrey
