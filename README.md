# 🤖 Artificial Intelligence and Expert Systems – Theory & Lab

**Artificial Intelligence (AI)** is the field of computer science that aims to create machines capable of intelligent behavior.  
**Expert Systems (ES)** are AI programs that mimic the decision-making ability of a human expert.

This guide includes **theory topics, lab exercises, and Python/Colab simulations**.

---

## 📚 Course Objectives

By the end of this course, students will be able to:

- Understand the **fundamentals of AI** and its applications.  
- Learn **search algorithms, knowledge representation, reasoning, and learning techniques**.  
- Design and implement **expert systems** using rules and inference engines.  
- Apply AI techniques using **Python in Google Colab**.  
- Conduct lab simulations including **search, optimization, and reasoning**.  

---

## 📝 Theory Topics

### 1. Introduction to AI
- Definition, history, and importance of AI  
- Applications: Robotics, Natural Language Processing (NLP), Expert Systems, Computer Vision  
- AI vs Human Intelligence  

### 2. Problem Solving & Search Techniques
- State space, problem formulation, solution representation  
- Uninformed Search: BFS, DFS, Uniform Cost Search  
- Informed Search: Best-First Search, A* Algorithm  
- Adversarial Search: Minimax Algorithm, Alpha-Beta Pruning  

### 3. Knowledge Representation
- Facts, rules, frames, semantic networks  
- Predicate logic, propositional logic  
- Ontologies and concept hierarchies  

### 4. Reasoning & Inference
- Forward Chaining and Backward Chaining  
- Rule-based systems  
- Non-monotonic reasoning  

### 5. Expert Systems
- Components: Knowledge base, Inference engine, User interface  
- Types of Expert Systems: Diagnostic, Prescriptive, Predictive  
- Shells for Expert Systems (e.g., CLIPS, Python-based rule engines)  

### 6. Machine Learning Basics
- Supervised, Unsupervised, Reinforcement Learning  
- Decision Trees, Neural Networks  
- Basic Python libraries: NumPy, Pandas, scikit-learn  

### 7. Natural Language Processing (Overview)
- Tokenization, Stemming, Lemmatization  
- Chatbots, Sentiment Analysis  

### 8. AI Ethics and Future Trends
- Ethical issues, bias, AI safety  
- AI in healthcare, autonomous vehicles, and industry  

---

## 💻 Lab Topics & Simulations

### 1. Python Setup in Google Colab
- Install libraries: `numpy`, `pandas`, `scikit-learn`, `matplotlib`, `networkx`  
- Import datasets: CSV, JSON  

### 2. Search Algorithm Simulations
```python
# BFS example
from collections import deque

def bfs(graph, start):
    visited = set()
    queue = deque([start])
    while queue:
        node = queue.popleft()
        if node not in visited:
            print(node, end=" ")
            visited.add(node)
            queue.extend(graph[node])
            
graph = {
    'A': ['B','C'],
    'B': ['D','E'],
    'C': ['F'],
    'D': [],
    'E': ['F'],
    'F': []
}
bfs(graph, 'A')
