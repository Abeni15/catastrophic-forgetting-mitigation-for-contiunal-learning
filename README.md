# Continual Learning with CNN on MNIST

This repository contains an implementation of **Continual (Sequential) Learning** using a **Convolutional Neural Network (CNN)** trained on **MNIST** and **Permuted MNIST** datasets.  
The project demonstrates the problem of **catastrophic forgetting** and compares different mitigation strategies.

---

## 📌 Project Overview

In traditional machine learning, models are trained on all data at once.  
However, in real-world scenarios, data often arrives **sequentially over time**.

This project explores **continual learning**, where a CNN:
- Learns tasks sequentially
- Retains knowledge from previous tasks
- Minimizes catastrophic forgetting

---

## 🧠 Learning Setting

- **Learning type:** Domain-Incremental Learning  
- **Model:** Convolutional Neural Network (CNN)  
- **Datasets:**
  - MNIST
  - Permuted MNIST (different pixel permutations per task)

---

## ⚠️ Catastrophic Forgetting

When the model is trained on a new task, its performance on previously learned tasks drops significantly.  
This phenomenon is known as **catastrophic forgetting**.

This project:
- Observes forgetting in a baseline model
- Applies mitigation strategies to reduce it

---

## 🛠️ Mitigation Strategies Implemented

### 1️⃣ Baseline (No Mitigation)
- Sequential training without any memory protection
- Used to observe catastrophic forgetting

### 2️⃣ Rehearsal (Replay)
- A small buffer of samples from previous tasks is stored
- Old samples are replayed while learning new tasks

### 3️⃣ Regularization / Constraint-based Method
- Penalizes large changes to important model parameters
- Helps preserve previously learned knowledge

---

## 📊 Evaluation Metrics

- **Average Accuracy:** Mean accuracy across all tasks seen so far  
- **Forgetting Measure:** Drop in accuracy on old tasks after learning new ones  

These metrics are used to compare different strategies.

---

## 🚀 Results Summary

- The baseline model shows significant catastrophic forgetting
- Rehearsal and regularization techniques reduce forgetting
- Mitigation strategies improve overall task retention

---

## 🧩 Tools & Libraries

- Python
- PyTorch
- Torchvision
- Google Colab

---

## 📁 Repository Structure

---

## 🚀 How to Run

1. Open the notebook in **Google Colab**
2. Run cells sequentially
3. Observe training, forgetting, and mitigation results

---

## 👤 Author

**Abenezer**  
iCog Labs – Machine Learning Training

