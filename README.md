# Manufacturing Optimization Models (Gurobi + Python)

**Tech Stack:** `Python` · `Gurobi Optimizer (gurobipy)` · `Operations Research` · `Linear & Mixed-Integer Programming (LP/MILP)` · `Pandas`

## 📌 Overview
This repository contains mathematical optimization models formulated and solved in **Python** using the **Gurobi Optimizer (`gurobipy`)** API. The models address real-world production planning, resource allocation, and capacity scheduling problems across two industrial domains:
1. **Integrated Steel Manufacturing Optimization**
2. **Smart Electronics Production Planning**

---

## 🏭 Model 1: Integrated Steel Manufacturing LP/MILP Model

### Problem Statement
An integrated steel plant must determine the optimal multi-stage production and blending schedule across raw material sourcing, blast furnace/converter processing, and rolling mill finishing lines to maximize net contribution margin (or minimize total production cost) while satisfying metallurgical quality, furnace capacity, emissions, and customer demand constraints.

### Mathematical Formulation Highlights
- **Decision Variables:**
  - Raw material feed quantities blended per stage
  - Intermediate hot-metal / crude-steel tonnage routed across units
  - Finished steel grade output allocated to demand commitments
- **Objective Function:** Maximize total profit contribution (revenue minus raw material, energy, and processing costs).
- **Constraints:**
  - **Material Balance & Yield Conservation:** Stage-to-stage mass balance accounting for process yield losses.
  - **Machine & Furnace Time Capacities:** Upper bounds on available operating hours per production unit.
  - **Quality & Blending Specifications:** Chemical composition bounds across blended inputs.
  - **Demand & Contract Bounds:** Minimum committed delivery quantities and maximum market absorption caps.

---

## 💻 Model 2: Smart Electronics Manufacturing Optimization

### Problem Statement
A multi-product electronics manufacturer produces multiple smart device lines sharing constrained SMT assembly lines, testing stations, skilled labor hours, and component inventories. The model determines the optimal production mix that maximizes total profit and evaluates shadow prices on bottleneck resources.

### Key Analytical Outputs
- **Optimal Production Mix:** Exact unit quantities per product line achieving global optimality.
- **Resource Utilization & Bottleneck Identification:** Binding vs. non-binding capacity constraints across assembly, testing, and labor.
- **Sensitivity & Shadow Price Analysis:** Dual values ($\pi_i$) and reduced costs quantifying the marginal profit value of adding one extra hour of bottleneck machine capacity.

---

## 🚀 Getting Started

### Prerequisites
- Python 3.9+
- `gurobipy` (with an active Academic or WLS Gurobi license)
- `pandas`, `numpy`

```bash
pip install gurobipy pandas numpy
```

### Running the Models
```bash
# Run Integrated Steel Manufacturing Optimization
python steel_manufacturing_gurobi.py

# Run Smart Electronics Production Optimization
python smart_electronics_gurobi.py
```

---

## 👤 Author
**Wahid Eman Kalyan**  
M.Tech in Operations Research, NIT Durgapur | B.E. in Mechanical Engineering, Jadavpur University  
[wahidemankalyan2000@gmail.com](mailto:wahidemankalyan2000@gmail.com)
