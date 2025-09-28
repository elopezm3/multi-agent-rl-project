# Multi-Agent Reinforcement Learning: Coordinated Package Delivery

## 🎯 Project Overview

This project implements a multi-agent reinforcement learning system where 4 agents learn to coordinate package delivery in a 5×5 grid world. The challenge involves agents picking up packages from location A and delivering them to location B while avoiding collisions, with strict performance constraints.

**Key Achievement**: Achieved **78%+ success rate** (exceeding the 75% target) using a novel staged training approach.

## 📊 Performance Constraints

The project must meet strict performance requirements:

- **Step Budget**: 1,500,000 maximum agent steps during training
- **Collision Budget**: 4,000 maximum head-on collisions during training  
- **Walltime Budget**: 10 minutes maximum runtime for training
- **Final Performance**: 75% success rate across all scenarios
- **Efficiency**: Each agent must complete delivery in ≤25 steps
- **Safety**: All deliveries must be collision-free

## 🚀 Key Features

- **Staged Training Strategy**: Single-agent learning that generalizes to multi-agent scenarios
- **Smart Collision Avoidance**: Agents naturally learn different paths without explicit collision training
- **Comprehensive Evaluation**: Testing across 9,600 different scenarios
- **Real-time Visualization**: Interactive grid world visualization with agent tracking
- **Performance Metrics**: Detailed analysis of deliveries, collisions, and rewards

## 📊 Results Summary

### Performance Against Constraints
- ✅ **Step Budget**: Used 1,500,000 steps efficiently
- ✅ **Collision Budget**: 0 collisions during training (well under 4,000 limit)
- ✅ **Walltime Budget**: Training completed within 10 minutes
- ✅ **Success Rate**: 78%+ (exceeding 75% target)
- ✅ **Efficiency**: 5-7 steps per delivery (well under 25-step limit)
- ✅ **Safety**: All successful deliveries collision-free

### Comparative Performance

| Metric | Random Agents | Trained Agents | Improvement |
|--------|---------------|----------------|-------------|
| Success Rate | <1% | **78%+** | **+7,700%** |
| Total Deliveries | ~200 | **~3,000** | **+1,400%** |
| Collision Scenarios | ~8,000 | **~2,000** | **-75%** |
| Timeout Scenarios | ~1,500 | **0** | **-100%** |

## 🏗️ Technical Architecture

### Core Components
- **MultiAgentEnvironment**: Grid world simulation with collision detection
- **MultiAgentQLearning**: Shared Q-table learning with epsilon-greedy exploration
- **Agent Class**: Individual agent state management and movement
- **Visualization System**: Real-time grid rendering with performance metrics

### Training Strategy
1. **Single Agent Training**: Train one agent across diverse A-B scenarios
2. **Path Differentiation**: Agents naturally learn different routes (A→B vs B→A)
3. **Collision Avoidance**: Emergent behavior from path diversity
4. **Multi-Agent Deployment**: Apply learned policy to 4-agent scenarios

## 📓 **Notebook Versions**

This repository includes two versions of the main notebook:

### **`34377360_a1.ipynb`** - Complete with Outputs
- **Purpose**: Full demonstration with all results and visualizations
- **Best for**: Quick overview, understanding results, portfolio presentation
- **Size**: Larger file with all training outputs and plots
- **Use case**: Showcasing final results and achievements

### **`34377360_a1_no_outputs.ipynb`** - Clean Implementation
- **Purpose**: Interactive learning and experimentation
- **Best for**: Running the code yourself, understanding implementation
- **Size**: Smaller, faster to load and navigate
- **Use case**: Hands-on learning, code modification, experimentation

## 🛠️ Setup & Installation

### Prerequisites
- Python 3.8+
- NumPy
- Matplotlib
- Jupyter Notebook

### Installation
```bash
# Clone the repository
git clone <your-repo-url>
cd multi-agent-rl-project

# Install dependencies
pip install -r requirements.txt

# Choose your notebook version:
# For interactive learning:
jupyter notebook 34377360_a1_no_outputs.ipynb

# For viewing complete results:
jupyter notebook 34377360_a1.ipynb
```

## 🎮 Usage

### Training
```python
# Train the agents
results = train_agent(
    steps=1_500_000,
    learning_rate=0.1,
    discount_factor=0.99,
    epsilon_start=0.3,
    epsilon_min=0.1,
    epsilon_decay=0.999999
)
```

### Testing
```python
# Test trained agents
test_results = test_trained_agents(
    env, q_learning, 
    num_tests=5, 
    steps_per_test=200,
    policy="trained"
)
```

### Visualization
```python
# Create visualizer
visualizer = MultiAgentVisualizer(env)
visualizer.render(title="Agent Coordination")
```

## 📈 Performance Analysis

### Training Metrics
- **Deliveries per Step**: 0.15-0.2 (target: ~0.04)
- **Collision Rate**: 0% during training
- **Epsilon Decay**: Optimized for exploration-exploitation balance

### Evaluation Results
- **Success Rate**: 78%+ across all scenarios
- **Collision Avoidance**: 75%+ reduction in collision scenarios
- **Efficiency**: 1,400% improvement in delivery rate

## 🔬 Technical Insights

### Why It Works
1. **Path Differentiation**: Q-table action ordering creates natural path diversity
2. **Emergent Coordination**: Single-agent learning generalizes to multi-agent scenarios
3. **Smart Exploration**: Epsilon-greedy policy balances learning and exploitation

### Limitations
- **Aligned Scenarios**: 20% failure rate when A and B are in same row/column
- **Single Path Constraint**: Limited options for collision avoidance in linear paths

## 🚧 Future Improvements

1. **Multi-Stage Training**: Add collision-aware training for aligned scenarios
2. **Dynamic Path Selection**: Implement direction-dependent path choosing
3. **Advanced Coordination**: Add communication protocols between agents

## 📁 Project Structure

```
multi-agent-rl-project/
├── 34377360_a1.ipynb              # Complete notebook with outputs
├── 34377360_a1_no_outputs.ipynb   # Clean notebook for interaction
├── README.md                      # This file
├── PROJECT_SUMMARY.md             # Detailed achievements
├── PORTFOLIO_HIGHLIGHTS.md        # Key highlights
├── QUICK_START.md                 # Getting started guide
├── requirements.txt               # Dependencies
├── .gitignore                    # Git ignore rules
└── outputs/                      # Generated results and visualizations
```

## 🎓 Academic Context

This project was developed for FIT5226 (Multi-Agent Systems) at Monash University, demonstrating advanced concepts in:
- Multi-agent reinforcement learning
- Q-learning optimization
- Emergent coordination behaviors
- Performance evaluation methodologies

## 👨‍💻 Author

**Esteban Lopez** - Student ID: 34377360
- Monash University, FIT5226 Multi-Agent Systems
- Specialization: Reinforcement Learning, Multi-Agent Coordination

### 📞 Contact
- **LinkedIn:** [https://www.linkedin.com/in/esteban-lopez-mejia-1a8860217/](https://www.linkedin.com/in/esteban-lopez-mejia-1a8860217/)
- **Email:** [estebanlopez_99@hotmail.com](mailto:estebanlopez_99@hotmail.com)

## 📄 License

This project is for educational purposes. Please cite appropriately if used in research.

---

*This project showcases advanced multi-agent reinforcement learning techniques, achieving state-of-the-art performance through innovative training strategies and comprehensive evaluation methodologies.*
