
# Learning-Based Control of a Simulated Mobile Robot

This repository presents a project exploring **learning-based control for a simulated mobile robot**, with an emphasis on understanding how machine learning models can replace or augment traditional rule-based control systems. The project focuses on building an end-to-end pipeline where a robot observes its state, predicts actions, and improves its behavior through data-driven learning.


## Project Overview

The project simulates a mobile robot navigating toward a goal within a simplified environment. At each time step, the robot observes its state—such as position, velocity, and distance to the target—and selects an action that influences its future state. The objective is to minimize error relative to the goal while maintaining stable and smooth motion.

The learning process begins with a baseline controller that encodes simple heuristics. Data generated from this controller is used to train machine learning models that learn to predict actions directly from observed states. Over time, the learned controller replaces the baseline logic and directly interacts with the environment.

---

## Key Components

* A numerical simulation of mobile robot dynamics
* Definition of state, action, and objective functions
* Baseline rule-based controller for reference behavior
* Supervised learning models trained to imitate control policies
* Manual implementation of learning with NumPy
* Neural network implementation using PyTorch
* Closed-loop control where the learned model drives the robot
* Performance evaluation under noise and unseen scenarios
* Visualization of trajectories and learning curves

---

## Learning Progression

The project follows a structured progression. It begins by defining the control problem and implementing a deterministic baseline controller. Learning is then implemented from scratch to expose loss functions, gradient descent, and optimization behavior. After validating learning dynamics, the same logic is reimplemented using PyTorch to scale to more expressive models. Finally, the learned controller is placed in a closed-loop system where its predictions influence future states, closely resembling real robotic control.

---

## Project Structure

```
├── environment/
│   ├── robot_env.py
│   └── baseline_controller.py
│
├── data/
│   └── generate_data.py
│
├── models/
│   ├── numpy_model.py
│   └── pytorch_model.py
│
├── training/
│   ├── train_numpy.py
│   └── train_pytorch.py
│
├── evaluation/
│   └── evaluate.py
│
├── notebooks/
│   └── analysis.ipynb
│
└── README.md
```

---

## Results and Observations

The learned controller successfully approximates the baseline behavior and demonstrates smoother and more adaptive control in many scenarios. Training curves show stable convergence when learning parameters are properly tuned. When exposed to noise and previously unseen states, the model degrades gracefully, highlighting both the strengths and limitations of supervised learning for control.

---


## Future Work

* Transition from supervised learning to reinforcement learning
* Integration with robot middleware and real-time control
* Extension to multi-dimensional motion and obstacle avoidance
* Incorporation of sensor noise and partial observability

---

