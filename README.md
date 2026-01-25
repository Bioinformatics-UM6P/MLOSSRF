# Machine Learning-Based Optimization of Site-Specific NPK Fertilizer Recommendation
<p align="center">
  <img src="https://ars.els-cdn.com/content/image/1-s2.0-S277237552600047X-gr1_lrg.jpg"
       alt="Graphical abstract / Figure"
       width="600">
</p>

<p align="center">
  <a href="https://doi.org/10.1016/j.atech.2026.101823">
    <img alt="DOI" src="https://img.shields.io/badge/DOI-10.1016%2Fj.atech.2026.101823-blue" />
  </a>
 <a href="https://creativecommons.org/licenses/by/4.0/">
    <img alt="License: CC BY 4.0" src="https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg" />
  </a>
  <a href="https://www.python.org/">
    <img alt="Python" src="https://img.shields.io/badge/python-3.9%2B-blue.svg" />
  </a>
  <a href="https://jupyter.org/">
    <img alt="Jupyter" src="https://img.shields.io/badge/Jupyter-Notebook-orange" />
  </a>
</p>

This repository provides selected scripts and notebooks related to inference and testing of the proposed machine learning models. The full training pipeline and raw dataset are not included due to data-sharing restrictions. This release is intended for the demonstration and reproducibility of the model evaluation workflow using processed sample data.


## Abstract

Efficient fertilizer use is important for sustainable intensification, yet uniform recommendations tend to ignore sharp spatial and seasonal variability in soils, climate, and crop response. This study develops a machine learning--based and constrained optimization framework to generate site-specific recommendations for nitrogen (N), phosphorus (P₂O₅), and potassium (K₂O) using a national-scale dataset of 7,180 Moroccan cereal data-points spanning three seasons and eight regions. A diverse suite of 47 model variants was compared under random and temporal sampling regimes to evaluate interpolation versus forecast performance. The best-performing model achieved high yield-prediction accuracy under the random split (sMAPE $\approx$ 4.5\%, $R^2 \approx 0.96$), with yield variation primarily explained by geospatial, seasonal, and nutrient--soil interaction features. In contrast, performance under a temporal split declined (sMAPE $\approx$ 17.8\%, $R^2 \approx 0.17$), reflecting structural and regional non-stationarity across seasons. Accordingly, all recommendation experiments relied on the globally best surrogate model trained under the random regime, while temporal outcomes were used for diagnostic purposes. Embedding the best-performing predictors within penalty-weighted objective functions and diverse optimization algorithms (deterministic, stochastic, metaheuristic, learning-based, and hybrid) produced model-simulated NPK decision-support recommendations. These recommendations increased simulated yields by up to 683 kg/ha ($\approx$ 20\% over a 3.4 t/ha baseline) while improving nutrient-use efficiency under explicit environmental constraints. The framework establishes a constrained learning-to-optimize decision-support paradigm that converts agronomic observations into model-simulated fertilizer recommendations intended to prioritize rapid field testing.


## Highlights

- Built a scalable machine learning and optimization pipeline on 7,180 Moroccan field trials (three seasons, eight regions), benchmarking 47 model variants (linear, kernel, tree-based, ensemble, stacking, and neural architectures) under random and temporal splits with model interpretability, and benchmarking 10 optimization algorithms (deterministic, stochastic, metaheuristic, learning-based, and hybrid) using top-performing machine learning models.
- Under the random regime, the best-performing model achieved a strong yield prediction accuracy of sMAPE ≈ 4.5% ($R^2$ ≈ 0.96), capturing strong nonlinear effects driven by geospatial, seasonal, and nutrient-soil interaction features. Under the temporal (out-of-distribution) regime, the best-performing model reached sMAPE ≈ 17.8% ($R^2$ ≈ 0.17), where spatial structure and regional shifts were the dominant explanatory factors.
- Metaheuristic optimization (Simulated Annealing, Bayesian Optimization, and Particle Swarm Optimization) generated site-specific NPK fertilizer decision-support recommendations, increasing model-simulated yields by up to 683 kg/ha (≈ 20% over a 3.4 t/ha baseline) while simultaneously improving nutrient-use efficiency under environmental constraints.


## Repository Structure

```
├── data/              # Dataset documentation and access notes
├── notebooks/         # Notebooks for data processing and feature engineering, model training, feature analysis, and optimization
├── results/           # Model evaluation,  ensemble results, feature analysis, and optimization outputs
├── paper/             # Manuscript, figures, and supplementary material
├── README.md          # Project overview and usage instructions
└── requirements.txt   # Python dependencies
```


## Citation

If you use this work, please cite:

```bibtex
@article{ENNAJI2026101823,
title = {Machine Learning–Based Optimization of Site-Specific NPK Fertilizer Recommendation},
journal = {Smart Agricultural Technology},
pages = {101823},
year = {2026},
issn = {2772-3755},
doi = {https://doi.org/10.1016/j.atech.2026.101823},
url = {https://www.sciencedirect.com/science/article/pii/S277237552600047X},
author = {Oumnia Ennaji and Abdelghani Belgaid and Achraf {El Allali}},
keywords = {Precision Agriculture, Site-Specific Fertilizer Recommendation, Machine Learning, Explainable AI, Constrained Optimization},
abstract = {Efficient fertilizer use is important for sustainable intensification, yet uniform recommendations tend to ignore sharp spatial and seasonal variability in soils, climate, and crop response. This study develops a machine learning–based and constrained optimization framework to generate site-specific recommendations for nitrogen (N), phosphorus (P2O5), and potassium (K2O) using a national-scale dataset of 7,180 Moroccan cereal data-points spanning three seasons and eight regions. A diverse suite of 47 model variants was compared under random and temporal sampling regimes to evaluate interpolation versus forecast performance. The best-performing model achieved high yield-prediction accuracy under the random split (sMAPE  ≈  4.5%, R2 ≈ 0.96), with yield variation primarily explained by geospatial, seasonal, and nutrient–soil interaction features. In contrast, performance under a temporal split declined (sMAPE  ≈  17.8%, R2 ≈ 0.17), reflecting structural and regional non-stationarity across seasons. Accordingly, all recommendation experiments relied on the globally best surrogate model trained under the random regime, while temporal outcomes were used for diagnostic purposes. Embedding the best-performing predictors within penalty-weighted objective functions and diverse optimization algorithms (deterministic, stochastic, metaheuristic, learning-based, and hybrid) produced model-simulated NPK decision-support recommendations. These recommendations increased simulated yields by up to 683 kg/ha ( ≈  20% over a 3.4 t/ha baseline) while improving nutrient-use efficiency under explicit environmental constraints. The framework establishes a constrained learning-to-optimize decision-support paradigm that converts agronomic observations into model-simulated fertilizer recommendations intended to prioritize rapid field testing.}
}
```


## Contact

* **Oumnia Ennaji** – [oumnia.ennaji@um6p.ma](mailto:oumnia.ennaji@um6p.ma)
* **Abdelghani Belgaid** – [abdelghani.belgaid@um6p.ma](mailto:abdelghani.belgaid@um6p.ma)
* **Achraf El Allali** (Corresponding Author) – [achraf.elallali@um6p.ma](mailto:achraf.elallali@um6p.ma)


## License

This project is released under a **non-commercial research use only license**. Use, distribution, and modification are permitted strictly for academic and research purposes. Commercial use is prohibited without prior written permission. 
