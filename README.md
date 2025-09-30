![Python](https://img.shields.io/badge/python-3.9%2B-blue.svg) ![License](https://img.shields.io/badge/license-Non--Commercial-lightgrey)  

# Machine Learning-Based Optimization of Site-Specific Fertilizer Recommendation

This repository provides selected scripts and notebooks related to inference and testing of the proposed machine learning models. The full training pipeline and raw dataset are not included due to data-sharing restrictions. This release is intended for the demonstration and reproducibility of the model evaluation workflow using processed sample data.

## Abstract
This study explores the development of machine learning (ML) models to recommend site-specific fertilizer strategies that maximize crop yield, optimize nutrient use efficiency, while minimizing environmental impact. Traditional fertilizer application methods often adopt a uniform approach, disregarding spatial variability in soil and crop conditions, which leads to inefficiencies and environmental degradation. To address this challenge, the study applies advanced ML and optimization algorithms to identify the optimal nitrogen (N), phosphorus (P), and potassium (K) levels tailored to local conditions. Using the Al Moutmir dataset as the primary data source, the study integrates diverse agronomic and soil features to train and evaluate several ML models and optimization algorithms. Key objectives include identifying the main factors influencing fertilizer needs, assessing model performance across different regions and crops, and generating recommendations via simulation. The best-performing model achieved a Mean Absolute Percentage Error (MAPE) of 5.2%, and simulation results indicated an average yield improvement up to 805.20 kg/ha (from a baseline of 3.5 t/ha, i.e., a 23% improvement).

---

## Highlights
- Built a scalable machine learning and optimization pipeline on 7{,}180 Moroccan field trials, benchmarking over 20 models under random and temporal splits with model interpretability, and benchmarking 10 optimizers using top-performing machine learning models.
- Achieved strong yield prediction accuracy on the random-split MAPE $\approx$ 5.2\%, with latitude, longitude, soil pH, organic matter, and crop type as dominant drivers.
- Metaheuristic optimization (Simulated Annealing, Particle Swarm Optimization, Bayesian Optimization Evolutionary Hybrids) produced site-specific NPK recommendations, improving yields by up to 805\,kg/ha while enhancing nutrient-use efficiency under environmental penalties.

---

## Repository Structure
```
├── data/              # Dataset documentation and access notes
├── notebooks/         # Jupyter notebooks for data processing, model training, and analysis
├── outputs/           # Results: model evaluation, optimization outputs, and ensemble results
├── paper/             # Manuscript, figures, and supplementary material
├── README.md          # Project overview and usage instructions
└── requirements.txt   # Python dependencies
```

---

## Reference

If you use this work, please cite:

> Ennaji, O., Belgaid, A., Vergütz, L., & El Allali, A.
> *Machine Learning-Based Optimization of Site-Specific Fertilizer Recommendation*.
> Mohammed VI Polytechnic University, Morocco. 2025.

---

## Contact

* **Oumnia Ennaji** – [oumnia.ennaji@um6p.ma](mailto:oumnia.ennaji@um6p.ma)
* **Abdelghani Belgaid** – [abdelghani.belgaid@um6p.ma](mailto:abdelghani.belgaid@um6p.ma)
* **Leonardus Vergütz** – [leonardus.vergutz@um6p.ma](mailto:leonardus.vergutz@um6p.ma)
* **Achraf El Allali** (Corresponding Author) – [achraf.elallali@um6p.ma](mailto:achraf.elallali@um6p.ma)

---

## License

This project is released under a **non-commercial research use only** license. Use, distribution, and modification are permitted strictly for academic and research purposes. Commercial use is prohibited without prior written permission. 
