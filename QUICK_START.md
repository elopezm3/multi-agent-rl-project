# Quick Start Guide

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone <your-repo-url>
cd multi-agent-rl-portfolio
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Choose Your Notebook Version
```bash
# For interactive learning (recommended):
jupyter notebook 34377360_a1_no_outputs.ipynb

# For viewing complete results:
jupyter notebook 34377360_a1.ipynb
```

## 📓 **Notebook Versions Explained**

### **`34377360_a1_no_outputs.ipynb`** - Interactive Learning
- **Best for**: Running code yourself, understanding implementation
- **Features**: Clean code, no outputs, fast loading
- **Use case**: Hands-on experimentation and learning

### **`34377360_a1.ipynb`** - Complete Results
- **Best for**: Viewing final results and achievements
- **Features**: All outputs, plots, and training results included
- **Use case**: Portfolio presentation and result verification

## 📊 Key Results

- **Success Rate**: 78%+ (target: 75%) ✅
- **Step Budget**: 1,500,000 steps used efficiently ✅
- **Collision Budget**: 0 collisions (limit: 4,000) ✅
- **Walltime Budget**: Training completed within 10 minutes ✅
- **Efficiency**: 5-7 steps per delivery (limit: 25 steps) ✅
- **Safety**: All successful deliveries collision-free ✅

## 🎯 What You'll See

1. **Training Process**: Watch agents learn coordination through Q-learning
2. **Visualization**: Real-time grid world with agent movement
3. **Performance Metrics**: Comprehensive evaluation across 9,600 scenarios
4. **Results Analysis**: Detailed comparison with random agents

## 📁 Project Structure

```
multi-agent-rl-project/
├── 34377360_a1.ipynb          # Main implementation
├── README.md                  # Comprehensive documentation
├── PROJECT_SUMMARY.md         # Detailed achievements
├── PORTFOLIO_HIGHLIGHTS.md    # Key highlights
├── QUICK_START.md            # This file
├── requirements.txt           # Dependencies
└── .gitignore               # Git ignore rules
```

## 🔧 Customization

### Modify Training Parameters
```python
results = train_agent(
    steps=1_500_000,           # Training steps
    learning_rate=0.1,         # Learning rate
    discount_factor=0.99,      # Discount factor
    epsilon_start=0.3,         # Initial exploration
    epsilon_min=0.1,           # Minimum exploration
    epsilon_decay=0.999999     # Exploration decay
)
```

### Test Different Scenarios
```python
# Test specific A-B positions
test_env = MultiAgentEnvironment(
    grid_size=5,
    num_agents=4,
    package_position=(0,0),    # A position
    target_position=(4,4),    # B position
    rewards=REWARDS
)
```

## 📈 Performance Tips

- **Training Time**: ~10 minutes on modern hardware
- **Memory Usage**: ~500MB for Q-table storage
- **Visualization**: Disable for faster training
- **Evaluation**: Full evaluation takes ~5 minutes

## 🐛 Troubleshooting

### Common Issues
1. **Import Errors**: Ensure all dependencies are installed
2. **Memory Issues**: Reduce grid size or training steps
3. **Slow Training**: Disable visualization during training
4. **Evaluation Timeout**: Reduce number of test scenarios

### Performance Optimization
- Use `render=False` during training
- Set `show_all_steps=False` for faster testing
- Reduce `num_tests` for quicker evaluation

## 📞 Support

For questions or issues:
- Check the main README.md for detailed documentation
- Review PROJECT_SUMMARY.md for technical details
- See PORTFOLIO_HIGHLIGHTS.md for key achievements
