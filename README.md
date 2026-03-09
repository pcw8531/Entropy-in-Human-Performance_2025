# Strategic Entropy in Human Performance

Data and analysis code supporting the manuscript:

**Park, C. (2025). Strategic Entropy in Human Performance: Navigating the Optimal Ground Between Order and Disorder.**

Seoul National University, Department of Physical Education  
Ethics approval: SNUIRB No. 1509/002-002

## Repository Structure

```
├── data/
│   ├── study1_circadian.csv      # Individual entropy H(x) and temperature (n=8, 4 time points)
│   └── study2_expertise.csv      # Individual entropy and accuracy (n=10 experts, n=10 novices)
│
├── analysis/
│   ├── circadian_analysis.py     # Study 1: circadian modulation statistics
│   ├── expertise_analysis.py     # Study 2: expert-novice comparisons, Table 2 values
│   └── bootstrap_validation.py   # Bootstrap resampling (10,000 iterations) for both studies
│
├── Data_Analysis.ipynb           # Full analysis notebook with figure generation
├── LICENSE                       # MIT License
└── README.md
```

## Quick Start

```bash
# Reproduce Study 1 statistics (Section 2.1)
python analysis/circadian_analysis.py

# Reproduce Study 2 statistics (Section 2.3, Table 2)
python analysis/expertise_analysis.py

# Reproduce bootstrap validation (Figures 1 and 4)
python analysis/bootstrap_validation.py
```

Each script prints a verification block showing exact values reported in the manuscript.

## Key Findings

| Finding | Value | Section |
|---------|-------|---------|
| Circadian entropy peak (05:00 h) | 5.246 ± 0.226 SE bits | §2.1 |
| Circadian entropy trough (17:00 h) | 4.544 ± 0.316 SE bits | §2.1 |
| Temperature-entropy correlation | r = −0.72 | §2.1 |
| Expert trajectory entropy | 3.556 ± 0.011 SE bits | §2.3 |
| Novice trajectory entropy | 3.184 ± 0.005 SE bits | §2.3 |
| Expert absolute error | 2.130 ± 0.045 SE cm | §2.3 |
| Regime transition threshold | H_m = 3.1 bits | §2.4 |
| Bootstrap: circadian difference | 95% CI [−0.066, 1.418] | §2.1 |
| Bootstrap: trajectory entropy | 95% CI [0.358, 0.403] | §2.3 |

## Data Description

**study1_circadian.csv**: 32 rows (8 participants × 4 circadian time points). Each row contains participant ID, measurement time, Shannon entropy H(x) in bits computed from bimanual coordination trajectories, and core body temperature in °C.

**study2_expertise.csv**: 20 rows (10 experts + 10 novices). Each row contains participant ID, group, trajectory entropy, angular entropy, joint entropy (all in bits), and absolute perceptual error in cm.

## Requirements

- Python 3.x
- NumPy, SciPy, Pandas

## License

MIT License. See LICENSE file.

## Citation

If you use this data or code, please cite the manuscript (reference to be updated upon publication).
