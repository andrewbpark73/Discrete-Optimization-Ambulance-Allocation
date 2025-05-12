# Fairness Overtime for Ambulance Allocation

## Project Information

**Course:** ORIE 5213 Discrete Optimization for Urban Planning and Mobility (2025SP)

**Contributors:**
- Andrew Park (Cornell Tech)
- Leihao Wang (Cornell Tech)
- Nina Wang (Cornell Tech)

**Advisor:** Prof. Andrea Lodi (Cornell Tech), Zhi Liu (Cornell Tech)

An optimization model that addresses fairness in ambulance allocation over time, using Gurobi optimization solver to minimize fairness gaps and overtime while ensuring efficient ambulance deployment and response planning.

## Project Structure

```
ambulance/
├── ambulance_model.ipynb         # Main Jupyter notebook containing the optimization model
├── configurations/               # Configuration files
├── data/                        # Input data files
├── results/                     # Model results and outputs
└── README.md                    # This file
```

## Dependencies

The project requires the following Python packages:
- gurobipy
- pandas
- numpy
- matplotlib
- networkx
- gdown

## Setup Instructions

1. Install the required dependencies:
```bash
pip install gurobipy pandas numpy matplotlib networkx gdown
```

2. Download the dataset:
```python
!gdown --folder https://drive.google.com/drive/folders/11Tx0kHH_8YVdTqHarfuBpTxGyN0JlLan
```

## Project Overview

This project implements an optimization model for ambulance allocation. The model uses Gurobi optimization solver to find optimal solutions for ambulance allocation in terms of fairness and overtime.

### Key Features

- Ambulance allocation optimization
- Fairness gap minimization
- Overtime minimization
- Configurable parameters
- Result visualization

### Gurobi License Requirements

- Gurobi license is required to run the optimization model.
- Place "gurobi.lic" file in the data folder.

### Results

The model generates results that include:
- Optimal ambulance allocation with fairness gap
- Consistency constraints experiments
- Performance over different size of configurations
- Performance visualizations

## Usage

1. Open `ambulance_model.ipynb` in Jupyter Notebook
2. Run all cells sequentially
3. Review results in the `results/` directory
4. Adjust configurations as needed
5. Rerun the model with new parameters

## Results Directory

The `results/` directory contains:
- Optimization solution files
- Performance metrics
- Visualization plots
- Log files

## Notes

- The model uses Gurobi optimization solver which may require a license for commercial (or academic) use
- Ensure sufficient memory is available for large-scale optimization problems
- Results may vary based on input data and configuration parameters

## Contributing

Contributions to improve the model, add new features, or enhance documentation are welcome. Please follow these guidelines:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is intended for educational and research purposes. Please check the license requirements for Gurobi optimization solver if using for commercial or academic applications.

## Contact

For questions or issues, please open an issue in the repository or contact the project maintainer.
