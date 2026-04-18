# 🧬 DNA Forensic Analysis using Statistical Inference
### > A statistical approach to forensic DNA analysis combining probability theory and Bayesian inference.

## 📌 Overview
This project implements a statistical framework for forensic DNA analysis to identify the most probable suspect based on DNA evidence.

It combines:
- Random Match Probability (RMP)
- Likelihood Ratios (LR)
- Bayesian Inference

to evaluate DNA profiles and quantify the strength of evidence.

---

## 🧠 Approach

### 🔹 1. DNA Profile Simulation
- STR loci are simulated for multiple suspects
- Each individual has a genotype (two alleles per locus)
- A crime scene DNA profile is generated independently

---

### 🔹 2. Allele Frequency Estimation
- Allele frequencies are computed from simulated population data
- Assumes Hardy-Weinberg Equilibrium (HWE)

---

### 🔹 3. Random Match Probability (RMP)
- Probability that a random individual matches the crime scene DNA
- Computed as the product of genotype probabilities across loci

---

### 🔹 4. Likelihood Ratio (LR)
- Compares two hypotheses:
  - Hp: suspect is the source
  - Hd: random individual is the source
- Approximated as:
  
  **LR ≈ 1 / RMP**

---

### 🔹 5. Bayesian Inference
- Combines prior belief with LR to compute posterior probability
- Used to rank suspects based on likelihood of guilt

---

## 📊 Validation Study

A simulation of 100 cases is performed to evaluate model reliability:

- Each case includes multiple suspects with one true contributor
- DNA profiles are generated using allele frequency distributions
- RMP, LR, and posterior probabilities are computed for each suspect

### Key Observations:
- True suspects consistently receive the highest posterior probability
- Strong separation between true and false suspects
- Near-perfect classification under ideal assumptions

---

## ⚠️ Limitations

- Assumes perfect DNA matching (no laboratory error)
- No modeling of allele dropout, degradation, or contamination
- Uses simplified likelihood assumptions
- Simulated data may not reflect real forensic complexity

---

## 🚀 Future Improvements

- Introduce noise (allele dropout, mutation, contamination)
- Use real-world allele frequency datasets
- Extend to mixture DNA analysis
- Implement probabilistic genotyping models

---

## 📁 Project Structure
DNA-Forensic-Analysis/
│
├── main.ipynb # Single-case DNA analysis
├── validation_simulation.ipynb # Multi-case validation study
├── README.md
└── requirements.txt

---

## 🛠️ Tech Stack

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn

---

## 👩‍💻 Author

Shaikh Maryam

MSc Applied Statistics  
Interested in Machine Learning, Data Science, and Statistical Modeling
