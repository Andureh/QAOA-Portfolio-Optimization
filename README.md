# QAOA Portfolio Optimization

Final project for the QC803 course at the University of Southern Denmark (SDU).

This project applies the Quantum Approximate Optimization Algorithm (QAOA) to the portfolio optimization problem. We compare several classical optimizers (COBYLA, SPSA, Powell) against a greedy baseline, and study how circuit depth, constraint penalty factors and noise affect the quality of the solutions.

The full analysis and results are in the report, [`QC803FinalReport.pdf`](QC803FinalReport.pdf); the code is in the notebook [`src/qc803_project/project.ipynb`](src/qc803_project/project.ipynb).

## Project structure

```text
.
├── pyproject.toml              # Project configuration and dependencies
├── README.md
├── QC803FinalReport.pdf        # Report: analysis and results
└── src/
    └── qc803_project/
        ├── __init__.py
        └── project.ipynb       # Code: data fetching, QAOA, solvers and experiments
```

## Installation

Requires Python 3.11.

Dependencies:

- `qiskit`, `qiskit-aer` and `qiskit-algorithms`
- `qiskit-optimization` and `qiskit-finance`
- `yfinance` (real market data)
- `numpy`, `pandas` and `matplotlib`

Install them with:

```bash
pip install qiskit==1.0.1 qiskit-aer==0.13.3 qiskit-algorithms==0.3.0 qiskit-optimization==0.6.1 qiskit-finance==0.4.1 yfinance numpy pandas matplotlib
```

## Usage

The entire analysis is in the Jupyter notebook `src/qc803_project/project.ipynb`. Open it and run the cells in order.

## Experiments

- **QAOA vs greedy algorithm:** QAOA solutions compared with a classical greedy baseline.
- **Optimizer analysis:** COBYLA, SPSA and Powell as the classical optimizer inside QAOA.
- **Depth analysis:** the effect of the QAOA circuit depth.
- **Penalty analysis:** the impact of constraint penalty factors on the approximation ratio.
- **Noise analysis:** robustness against depolarizing noise.

## Authors

- André Gomes
- Martín Marcuello

## License

MIT, see [LICENSE](LICENSE).
