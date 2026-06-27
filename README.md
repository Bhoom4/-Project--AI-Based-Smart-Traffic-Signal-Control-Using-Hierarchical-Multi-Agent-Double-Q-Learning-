# 🚦 AI-Based Smart Traffic Signal Control Using Hierarchical Multi-Agent Double Q-Learning


### **An Intelligent Adaptive Traffic Management System using Hierarchical Multi-Agent Reinforcement Learning**

*Final Year B.E. Project | Computer Science & Engineering (AI & ML)*

---

## Table of Contents

- Overview
- Problem Statement
- Objectives
- Key Features
- System Architecture
- AI Methodology
- Project Workflow
- Technologies Used
- Project Structure
- Installation
- Usage
- Dashboard
- Performance Evaluation
- Future Enhancements
- Author

---

# Overview

Traffic congestion is one of the biggest challenges in modern urban transportation. Traditional traffic lights operate on predefined timers and are unable to adapt to changing traffic conditions, resulting in unnecessary delays, longer queues and poor road utilization.

This project presents an **AI-powered adaptive traffic signal control system** using **Hierarchical Multi-Agent Reinforcement Learning (HMARL)** and **Double Q-Learning**.

Instead of relying on fixed timings, autonomous reinforcement learning agents continuously observe traffic conditions, learn from the environment and optimize signal timings dynamically. A **Master Controller** coordinates local agents to improve overall traffic flow across multiple intersections.

An interactive **Streamlit dashboard** is also included for visualization, simulation and comparison between reinforcement learning and conventional fixed-time traffic systems.

---

#  Problem Statement

Conventional traffic signal systems suffer from:

- Fixed signal durations
- High vehicle waiting times
- Traffic congestion during peak hours
- Poor adaptability to changing traffic density
- Lack of intelligent decision making

The goal of this project is to build an intelligent traffic management system capable of learning optimal traffic signal policies automatically.

---

#  Objectives

- Reduce average vehicle waiting time
- Minimize traffic congestion
- Improve traffic throughput
- Learn adaptive signal timings
- Coordinate multiple intersections
- Compare AI-based control with traditional fixed-time control

---

#  Key Features

-  Adaptive traffic signal optimization
-  Hierarchical Multi-Agent Reinforcement Learning
-  Double Q-Learning implementation
-  Master Controller for coordinated decision making
-  Interactive Streamlit dashboard
-  Baseline vs Reinforcement Learning comparison
-  Performance evaluation
-  Modular Python implementation

---

#  System Architecture

                    Traffic Environment
                            │
                            ▼
                  State Representation
                            │
                            ▼
          ┌────────────────────────────────┐
          │    Local Reinforcement Agents  │
          └────────────────────────────────┘
             │        │        │        │
             ▼        ▼        ▼        ▼
          Int-1    Int-2    Int-3    Int-4
               \      |      |      /
                ───── Master Controller ─────
                           │
                           ▼
                Optimized Signal Decisions
                           │
                           ▼
                    Updated Environment
                           │
                           ▼
                         Reward



#  AI Methodology

## Reinforcement Learning

Each intersection learns through interaction with the environment.

### State

- Queue length
- Traffic density
- Current signal phase
- Intersection state

### Actions

- Extend green signal
- Switch signal phase
- Maintain current phase

### Reward

- Lower waiting time
- Reduced congestion
- Better traffic flow
- Higher throughput

---

## Double Q-Learning

Double Q-Learning uses two Q-tables to reduce overestimation bias and improve learning stability.

**Advantages**

- Better convergence
- More stable learning
- Reduced value overestimation
- Improved decision quality

---

## Hierarchical Multi-Agent Reinforcement Learning

The project follows a hierarchical learning strategy:

- Local agents optimize individual intersections.
- The Master Controller coordinates priorities at a global level.
- Enables scalable traffic management across multiple intersections.

---

#  Project Workflow

Environment
      │
      ▼
Observe State
      │
      ▼
Local Agent selects Action
      │
      ▼
Master Controller Coordination
      │
      ▼
Traffic Signal Decision
      │
      ▼
Environment Update
      │
      ▼
Reward Calculation
      │
      ▼
Double Q Update
      │
      ▼
Repeat

---

# Technologies Used

| Category | Technology |
|----------|------------|
| Language | Python |
| AI | Reinforcement Learning |
| RL Algorithm | Double Q-Learning |
| Architecture | Hierarchical Multi-Agent RL |
| Dashboard | Streamlit |
| Libraries | NumPy, Matplotlib |

---

# Project Structure


.
├── agent.py
├── controller.py
├── env.py
├── env_grid4.py
├── multi_env.py
├── train.py
├── multi_agent_train.py
├── multi_agent_evaluate.py
├── render.py
├── streamlit_app.py
├── utils.py
└── pages/

---

# ⚙️ Installation

```bash
git clone https://github.com/Bhoom4/AI-Based-Smart-Traffic-Signal-Control-Using-Hierarchical-Multi-Agent-Double-Q-Learning.git

cd AI-Based-Smart-Traffic-Signal-Control-Using-Hierarchical-Multi-Agent-Double-Q-Learning

pip install -r requirements.txt
```

---

# Usage

### Train Single Agent

```bash
python train.py
```

### Train Multi-Agent Model

```bash
python multi_agent_train.py
```

### Evaluate

```bash
python multi_agent_evaluate.py
```

### Launch Dashboard

```bash
streamlit run streamlit_app.py
```

---

# Dashboard

The Streamlit dashboard provides:

- Project overview
- RL model visualization
- Fixed-time vs RL comparison
- Network visualization
- Interactive simulation

> **Tip:** Add screenshots of each page inside an `assets/` folder and embed them here to make the repository much more attractive.

---

# Performance Evaluation

The implementation evaluates adaptive reinforcement learning against conventional traffic control using:

- Average Waiting Time
- Queue Length
- Traffic Throughput
- Signal Efficiency

Add your graphs and comparison tables in this section after experimentation.

---

# Future Enhancements

The following are planned improvements and are **not part of the current implementation**:

- YOLO-based real-time vehicle detection
- SUMO integration
- Federated Learning
- Deep Q Networks (DQN)
- PPO-based learning
- Emergency vehicle prioritization
- IoT sensor integration
- Explainable AI dashboard
- Cloud deployment
- Smart City Digital Twin

---

# Author

**Bhoomika Harish Naik**
**Anthony Lawrence Rehan**

B.E. Computer Science & Engineering (AI & ML)

Don Bosco Institute of Technology, Bengaluru

---

# Acknowledgements

This project was developed as a Bachelor's final-year project to explore intelligent traffic optimization using Reinforcement Learning. It demonstrates how Hierarchical Multi-Agent Double Q-Learning can improve adaptive traffic management compared with conventional fixed-time signal control systems.

---

## ⭐ If you found this project useful, consider giving it a star!
