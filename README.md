# 🧠 Neural Networks from Scratch (in C++)

This project demonstrates how to **build a neural network from scratch using C++** without relying on external deep learning libraries. Each component—from neurons to layers and activation functions—is implemented step by step to provide a clear understanding of neural computation fundamentals.

---

## 📌 Objective

> Learn how artificial neural networks work at the lowest level by manually coding:
- Neuron computations  
- Dot products and forward propagation  
- Activation functions (ReLU, Softmax)  
- Layer abstraction using object-oriented design

---

## 📁 Folder Overview

| Folder                        | Description                                                                 |
|-------------------------------|-----------------------------------------------------------------------------|
| `Basic_Neuron_Layer`          | Single-layer with multiple neurons — foundational layer computation.        |
| `Basic_Neuron_with_3_inputs`  | A single neuron with 3 input weights and a bias.                           |
| `Dot_Product`                 | Implementation of dot product for input-weight operations.                |
| `Layers_and_Object`           | Encapsulation of layers and objects for scalable design.                  |
| `ReLU_Activation`             | Applies Rectified Linear Unit activation (max(0, x)).                     |
| `Softmax_Activation`          | Applies softmax function to output neuron probabilities.                  |

---

## 🛠 Technologies Used

- Language: **C++ (100%)**
- Concepts:
  - Object-Oriented Programming (OOP)
  - Basic linear algebra (dot products, matrix operations)
  - Forward propagation
  - Numerical stability techniques (for softmax)

---
        Input Layer           Hidden Layer            Output Layer
        (3 neurons)            (4 neurons)              (2 neurons)
        -----------            ------------            -------------
        [ x₁ ]                 [ h₁ ]                   [ y₁ ]
        [ x₂ ]  ------------>  [ h₂ ]  ------------->   [ y₂ ]
        [ x₃ ]                 [ h₃ ]         
                              [ h₄ ]
Inputs:      [1.0, 2.0, 3.0]
Weights:     [0.2, 0.8, -0.5]
Bias:        +2.0

Dot Product: (1.0×0.2 + 2.0×0.8 + 3.0×(-0.5)) + 2.0 = 0.2 + 1.6 - 1.5 + 2.0 = 2.3

ReLU(x) = max(0, x)
Example: Input [2.3, -1.0, 0.0] → Output [2.3, 0.0, 0.0]

Softmax(x):

Input:  [2.3, 0.1, 0.5]
Exp:    [~10, ~1.1, ~1.6]
Output: [0.75, 0.08, 0.17]
     Inputs     →  Dot Product  →  Bias Addition  →  Activation Function  →  Output
[ x₁, x₂, x₃ ]      [ Σ(x·w) ]         +b                   ReLU               y

Layer: Input (x₁, x₂, x₃) → Hidden (ReLU) → Output (Softmax)

Step 1: Dot product with weights
Step 2: Add bias
Step 3: Apply ReLU
Step 4: Forward to output layer
Step 5: Apply Softmax

Result: [0.74, 0.26] → Probabilities


## 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/abkarada/Neural-Networks-from-Scratch.git
cd Neural-Networks-from-Scratch



g++ Basic_Neuron_with_3_inputs/main.cpp -o neuron
./neuron

