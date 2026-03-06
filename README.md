# Optimization-of-Communication-Efficiency-in-Federated-Learning

## Overview

This repository contains my **MSc Data Science research project from the University of Surrey**, focusing on **Federated Learning (FL)** optimization strategies. Federated Learning is a decentralized machine learning approach that allows multiple clients to collaboratively train models **without sharing raw data**, helping preserve privacy in sensitive domains such as healthcare and mobile applications.

The project benchmarks multiple federated optimizers across several datasets under realistic distributed learning conditions.

---

## Objectives

* Evaluate the performance of major **Federated Learning optimizers**
* Study convergence behaviour under **non-IID data distributions**
* Simulate **communication constraints** similar to real-world edge environments
* Identify which optimizer performs best under different data conditions

---

## Optimizers Evaluated

The following federated optimization strategies were benchmarked:

* **FedAvg**
* **FedAdam**
* **FedAdagrad**
* **FedYogi**
* **SCAFFOLD**

---

## Datasets Used

Experiments were conducted on diverse datasets to test robustness:

* **CIFAR-10**
* **FedMNIST**
* **EMNIST-CR**
* **FashionMNIST**
* **MedMNIST**

These datasets represent different image classification challenges and data distributions.

---

## Experimental Setup

Framework: **Flower Federated Learning Framework**

Simulation Parameters:

* Communication Rounds: **100**
* Number of Clients: **5**
* Local Epochs: **1**
* Data Distribution: **Non-IID partitions**

A consistent **Convolutional Neural Network (CNN)** architecture was used across all experiments to ensure fair comparison between optimizers.

---

## Key Findings

* **FedAdagrad** achieved the **most stable and fastest convergence** in communication-constrained environments.
* **SCAFFOLD** performed best in **highly heterogeneous datasets** by reducing client drift.
* **FedAdam** showed **fast early convergence but instability** on noisy datasets.
* **FedYogi** demonstrated **moderate robustness** in imbalanced data scenarios.
* No single optimizer universally outperformed others across all datasets.

---

## Applications

The insights from this project are relevant for deploying Federated Learning in:

* **Healthcare AI systems**
* **Mobile and edge devices**
* **Privacy-sensitive machine learning environments**
* **Distributed AI applications**

---

## Tech Stack

* **Python**
* **PyTorch**
* **Flower Federated Learning Framework**
* **NumPy / Pandas**
* **Matplotlib**

---


## Future Improvements

* Increase number of clients to simulate larger federated networks
* Experiment with **different CNN architectures**
* Test **secure aggregation techniques**
* Evaluate performance under **varying communication budgets**

---

## Author

**Snehashree Gopinath**
MSc Data Science – University of Surrey

---

