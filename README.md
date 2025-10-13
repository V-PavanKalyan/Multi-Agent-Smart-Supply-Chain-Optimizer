# 🧠 Multi-Agent Smart Supply Chain Optimizer

### AI-Driven, Autonomous, and Explainable Supply Chain Management System

---

## 📘 Overview
The **Multi-Agent Smart Supply Chain Optimizer** is an AI-powered framework that autonomously plans, monitors, and optimizes supply chain operations.  
It uses a **multi-agent architecture** — where intelligent agents collaborate, communicate, and reason together — to enhance efficiency, resilience, and transparency across inventory, supplier, route, and risk domains.

This project demonstrates how **modular agent-based AI systems**, when integrated with real-world data and APIs, can deliver **dynamic, data-driven, and explainable supply chain decisions**.

---

## 🎯 Objectives
- Automate and optimize supply chain planning  
- Minimize operational costs and delays  
- Dynamically respond to disruptions (supplier delays, weather, etc.)  
- Provide explainable and auditable decision-making  
- Demonstrate collaborative reasoning among agents  

---

## 🧩 System Architecture

The system consists of **five specialized agents** working under a central planner:

| Agent | Function |
|--------|-----------|
| **Inventory Management Agent** | Monitors stock and predicts shortages |
| **Supplier Agent** | Evaluates suppliers based on cost, reliability, and lead time |
| **Route Optimization Agent** | Finds optimal routes using OpenRouteService |
| **Risk Management Agent** | Detects disruptions from weather and logistics data |
| **Planner/Manager Agent** | Integrates outputs, resolves trade-offs, and generates final plans |

All agents communicate through a shared **Communication Bus** and maintain **independent memory (JSON-based)** for reasoning persistence and explainability.

---

## 🔄 Workflow

1. **User Query** → The user interacts through the Planner Agent.  
2. **Inventory Analysis** → Identifies low-stock or critical items.  
3. **Supplier Evaluation** → Selects optimal vendors from supplier data.  
4. **Route Optimization** → Plans efficient routes via OpenRouteService.  
5. **Risk Assessment** → Evaluates weather or disruption risks.  
6. **Planner Integration** → Aggregates all insights and finalizes a plan.  
7. **Explainable Logs** → All reasoning is stored in structured JSON for transparency.

---

## 💾 Data Sources

| Source | Description | Type |
|---------|-------------|------|
| `inventory.csv` | Stock levels, usage rates, reorder points | Local CSV |
| `suppliers.csv` | Supplier info (price, reliability, lead time) | Local CSV |
| OpenRouteService API | Real-world route optimization | Free API |
| OpenWeatherMap API | Weather and risk monitoring | Free API |

---

## 📊 Example Output

**Summary Report:**
```
✅ Analysis Complete
- Restock 2 critical items
- Recommended Supplier: Global Electronics (Reliability: 0.95)
- Optimal Route: 128.5 km, Cost: $122.30
- Risk Level: Medium
```

**JSON Output:**
```json
{
  "supplier_recommendation": {"supplier_id": "SUP002", "score": 0.91},
  "optimized_route": {"distance_km": 128.5, "duration_hr": 3.5, "cost": 122.3},
  "risk_alerts": [{"type": "flood", "impact": "medium"}],
  "final_plan": {"supplier": "SUP002", "route": "Route B", "action": "Expedite delivery"}
}
```

---

## ⚙️ Implementation

| Component | Details |
|------------|----------|
| **Platform** | Google Colab |
| **Language** | Python 3.10+ |
| **Core Libraries** | `pandas`, `matplotlib`, `folium`, `openrouteservice`, `pyowm`, `langchain` |
| **APIs Used** | Gemini (reasoning), OpenRouteService, OpenWeatherMap |
| **Outputs** | JSON logs, route maps, performance metrics |

---

## 🚀 How to Run

1. Open in **Google Colab**.  
2. Install dependencies:
   ```bash
   !pip install pandas matplotlib folium openrouteservice pyowm langchain
   ```
3. Upload `inventory.csv` and `suppliers.csv`.  
4. Run all cells sequentially.  
5. Interact via the Planner Agent:
   ```
   Analyze current supply chain and suggest improvements.
   ```
6. View generated analysis, visualizations, and JSON outputs.

---

## 🧪 Testing
The framework includes test scenarios for:
- Supplier delays  
- Demand spikes  
- Weather disruptions  
- Stockouts  

**Example Result:**  
```
✅ 5/5 Tests Passed
Results saved to test_results.json
```

---

## 🧠 Explainability & Memory
Every decision is **traceable** through JSON logs that record:
- Agent reasoning steps  
- Trade-off decisions  
- Confidence levels  
- Historical performance  

Each agent’s memory evolves over time, allowing adaptive learning and improved decision-making.

---

## 🏁 Conclusion
The **Multi-Agent Smart Supply Chain Optimizer** demonstrates a scalable, intelligent, and explainable approach to modern supply chain management.  
By combining **AI reasoning**, **modular agents**, and **real-time data**, the system achieves:

- 💡 Autonomous decision-making  
- 🔄 Adaptive, collaborative optimization  
- 🧾 Transparent, explainable intelligence  

This framework serves as a foundation for future expansion into **predictive demand forecasting**, **IoT-based tracking**, and **ERP integration** — paving the way for the next generation of **resilient, sustainable, and intelligent supply chains**.

---

## 👥 Contributors
**Developed by:**VANGA PAVAN KALYAN  

---

## 🧾 License
This project is released under the [MIT License](LICENSE).

---
