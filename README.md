## 📌 Overview

This project explores the implementation of a **Federated Learning (FL)** framework using the **Federated Averaging (FedAvg)** algorithm, a privacy-preserving machine learning technique that allows multiple clients to collaboratively train a model without sharing their raw data.

In a traditional centralized machine learning setup, all data is collected and stored on a single server for training. However, this poses significant privacy and security risks, especially when dealing with sensitive data in domains such as healthcare, finance, and personal devices. **Federated Learning** addresses this issue by enabling model training directly on decentralized data sources (clients), where each client computes model updates locally and only shares those updates (model weights) with a central server. The server then aggregates these weights (via FedAvg) to update the global model.

---

## 🧠 What This Project Does

- **Client Simulation**: Simulates multiple clients, each with a non-identically distributed (non-IID) portion of the dataset to reflect real-world data imbalance and heterogeneity.
- **Local Training**: Each client trains a copy of the model on its local data for a specified number of epochs using gradient descent.
- **Model Aggregation with FedAvg**: After local training, model weights are sent to a central server, where they are averaged and redistributed to all clients.
- **Global Iteration**: The process is repeated for several rounds, tracking how the global model improves and how clients contribute to overall learning.
- **Performance Visualization**: The training performance (accuracy, loss) of each client is tracked across communication rounds using `Matplotlib`, highlighting convergence behavior and variation among clients.

---

## 📚 Why This Matters

This project reflects the growing need for privacy-conscious machine learning. From mobile keyboards and smart devices to hospitals and banks, federated learning ensures that:
- Raw data never leaves its source
- Training can happen across diverse, distributed datasets
- Model performance can still rival centralized approaches under the right conditions

We focused specifically on the **FedAvg** algorithm because of its simplicity, scalability, and effectiveness in aggregating model parameters in asynchronous and distributed environments.

---

## 🎓 Academic Context

This project was developed as part of a course on Distributed and Federated Machine Learning at SUNY Albany. It was presented in a **poster session**, where it was recognized for its clarity in simulating realistic federated setups and performance trends across clients. The emphasis was on:
- Simulating non-IID data conditions
- Analyzing training variability across devices
- Understanding trade-offs in convergence and accuracy

---

## 🔬 Technologies Used

- **Python** – for simulation and modeling
- **NumPy** – for fast numerical computation and model weight handling
- **Pandas** – for synthetic data manipulation
- **Matplotlib** – for visualizing training performance across clients

---

## 📈 Sample Use Cases

While this project uses synthetic or demo datasets, the architecture and logic can be extended to real-world applications such as:
- Healthcare record classification across hospitals
- Predictive maintenance across factories
- User behavior modeling on mobile phones without sharing data

---

This project serves as a clean and customizable foundation for anyone looking to experiment with federated learning from the ground up.
