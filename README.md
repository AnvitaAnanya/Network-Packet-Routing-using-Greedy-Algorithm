# 📡 Network Packet Routing in Data Centers Using Greedy Algorithm

## 📘 Course & Instructor
**Course:** 21CSC204J - Design and Analysis of Algorithms  
**Instructor:** Dr. A. Prabhu Chakkaravarthy

---

## 🧠 Problem Statement
In large-scale data centers like **Google Cloud**, **AWS**, or **Microsoft Azure**, **millions of data packets** are transmitted every second.  
The goal is to efficiently **route packets from source to destination** while minimizing **latency** and **network congestion**.

---

## ⚠️ Limitations of Traditional Algorithms

### 1. Genetic Algorithm
- ❌ Slow convergence – not suitable for real-time routing  
- 💰 High computational cost due to iterative population handling  
- 🔄 Unpredictable performance

### 2. Dynamic Programming
- 🧠 Memory intensive – stores multiple intermediate results  
- 🐢 High time complexity – not feasible for real-time adaptation  
- 🔒 Inflexibility – needs predefined problem structure

### 3. Graph-Based Methods (Dijkstra, A*)
- 🖥️ Computationally expensive – slow for large real-time graphs  
- 🧱 Static in nature – not adaptive to congestion or link failure  
- 🔁 Complex to update paths frequently

---

## ✅ Proposed Solution: Greedy Algorithm

### Why Greedy?
- ⚡ **Fast decision-making** – selects best local option at each step  
- 💡 **Low overhead** – no need to precompute paths  
- 📈 **Scalable** – can handle millions of packets simultaneously

### Steps Involved:
1. **Initialization**: Represent network as a graph (routers = nodes, links = edges weighted by latency)
2. **Local Best Choice**: At each router, choose neighbor with **least latency** and **least congestion**
3. **Move and Repeat**: Move the packet to selected router, repeat until destination
4. **Real-Time Adaptation**: Continuously update link weights based on congestion and adjust routing dynamically

---

## 📊 Time Complexity Analysis

### Step-by-step Breakdown:
1. **Finding shortest latency neighbor** → O(N)  
2. **Moving to next router** → O(1)  
3. **In worst case (traversing all routers)** → O(N) steps

### Recurrence Relation:
T(N) = T(N - 1) + O(N)

### Using Master’s Theorem:
T(N) = aT(N/b) + O(N^d) a = 1, b = 1, d = 1 → O(N²)

### Final Time Complexity: **O(N²)** (Worst Case)

---

## 🧑‍💻 Contributors
- **Mayukh Tilak** - RA2311030010068  
- **Yashwanth Ch** - RA2311030010087  
- **Anvita A** - RA2311030010092

**Branch:** Computer Science and Engineering (SC) - Y1 Section
