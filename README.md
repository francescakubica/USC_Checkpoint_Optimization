# 🛂 From Congestion to Flow: Optimizing Entry Systems at Pardee Way

![USC Pardee Way Simulation](https://img.shields.io/badge/Project-Final%20Simulation-blue)
![Grade](https://img.shields.io/badge/Grade-98%25-brightgreen)

## 📘 Context

This project was developed as the final deliverable for BUAD 313 at the University of Southern California. It tackles operational inefficiencies at the **Pardee Way campus checkpoint**, a constrained entranceway requiring ID verification for thousands of students and faculty.

Using **hand-collected data** and applying **queuing theory, simulation modeling, and real-world layout constraints**, the project simulates and proposes optimizations to reduce congestion during peak hours while maintaining security infrastructure.

> "The USC experience starts the moment people walk through its gates."  
> Our goal: to make that experience smoother, smarter, and supported by data.

---

## 🚧 Challenges

- **Data Collection Limitations**: Collected 1,018 data points manually across 5 days and 3 daily shifts. Estimated a ±1 sec margin of error on service times.
- **Scanner Behavior**: Scanner 1 was disproportionately favored (used 74.65% of the time), causing localized bottlenecks.
- **Human Factors**: Disruptors (unprepared IDs, bikes, group entry, etc.) created unpredictable queue dynamics.
- **Exit Confusion**: Frequent use of unauthorized exit paths caused delays in service time for entrants.

---

## 💡 Solutions

### 🧪 Modeling & Simulation
- **Base Model**: High-level system assuming even scanner usage and independent arrivals.
- **Enriched Model**: Incorporated:
  - Mixed service time distributions based on **user types** (e.g. "unprepared", "mobilized", "assisted").
  - Scanner prioritization.
  - Penalties for "wrong exiters."

### 🔁 Extended Model
- Introduced a **4-lane configuration** using the same number of scanners and personnel.
- Relocated exit paths to prevent conflict with incoming traffic.
- Results:
  - **93.4% reduction** in average waiting time across shifts.
  - Extended model reached steady-state wait times even at high foot traffic volumes.

### 📈 Sensitivity Analysis
- Simulated ±1 second error in service time to measure robustness.
- Confidence intervals and replications confirmed **stability** of findings under moderate data variance.

---

## 🧠 Key Insights

- Redistributing traffic evenly across all scanners yields massive time savings.
- Human psychology (e.g., gravitation toward the first scanner) can skew system efficiency.
- Low-cost design changes—**not more staff or scanners**—can have outsized impact.

---

## 📋 Feedback from Professor Gupta

> **Grade: 98%**

> ✅ *Clarity and Organization*:  
> *A well-written report and a very well-documented codebase. Plus the project timeline!*

> ✅ *Modeling Real-World Features*:  
> *Excellent use of hand-collected data and modeling that is both realistic and not overly tailored.*

> ✅ *Justification of Assumptions*:  
> *Shines in both its description and acknowledgment of limitations.*

> ✅ *Use of Class Techniques*:  
> *Excellent use of simulation.*

> ✅ *Recommendations & Insights*:  
> *Great discussion and actionable suggestions.*

> ✅ *Robustness & Sensitivity*:  
> *Good use of perturbations and confidence intervals.*

> ✅ *Creativity & Thoroughness*:  
> *A highly creative and thorough project. Exemplar effort that could be used in future semesters.*

> ✅ *Data Use*:  
> *Great on-the-ground data collection strategy.*

> ✅ *Code Quality*:  
> *Clean and well-structured notebooks.*

---

## 📂 Repository Structure

```bash
📁 data/
    └── pardee_traffic_data.csv
📁 models/
    ├── base_simulation.ipynb
    ├── enriched_simulation.ipynb
    └── extended_simulation.ipynb
📁 reports/
    └── BUAD_313_Final_Report.pdf
📄 README.md
