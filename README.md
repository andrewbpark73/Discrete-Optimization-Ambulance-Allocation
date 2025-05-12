# Fairness Overtime for Ambulance Allocation

## Project Information

**Course:** ORIE 5213 Discrete Optimization for Urban Planning and Mobility (2025SP)

**Contributors:**
- Andrew Park (Cornell Tech)
- Leihao Fang (Cornell Tech)
- Nina Wang (Cornell Tech)

**Advisor:** Prof. Andrea Lodi (Cornell Tech), Zhi Liu (Cornell Tech)

Exploration of ambulance allocation problem with fairness over time, using Gurobi optimization solver to minimize fairness gaps over zones, while testing with various sizes of configurations for efficiency comparison.

## Project Status

This project is complete as of May 2025. The optimization model successfully achieves perfect fairness across all configuration sizes tested, with interesting patterns in movement requirements.

## Project Structure

```
ambulance/
├── ambulance_model.ipynb         # Main Jupyter notebook containing the optimization model
├── configurations/               # Configuration files for ambulance placement
├── data/                        # Input data files including zone networks and base locations
├── results/                     # Model results and outputs including visualizations
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

2. Download the dataset here:
```python
!gdown --folder https://drive.google.com/drive/folders/11Tx0kHH_8YVdTqHarfuBpTxGyN0JlLan
```
or here:
```
https://github.com/PhilippeOlivier/ambulances
```

## Project Overview

This project implements an optimization model for ambulance allocation. The model uses Gurobi optimization solver to find optimal solutions for ambulance allocation in terms of fairness and overtime.

### Key Features

- Ambulance allocation optimization
- Fairness gap minimization
- Overtime minimization
- Configurable parameters
- Result visualization

### Input Data

The input data includes:
- Network graph of zones and their adjacencies
- Base locations for ambulance stations
- Pre-computed configurations for ambulance placements

### Gurobi License Requirements

- Gurobi license is required to run the optimization model.
- Place "gurobi.lic" file in the data folder.

### Results

The model generates results that include:
- Optimal ambulance allocation with fairness gap
- Consistency constraints experiments
- Performance over different size of configurations
- Performance visualizations

### Key Findings

Our research revealed an interesting pattern where perfect fairness (zero fairness gap) can be achieved with minimal or zero ambulance movements at specific configuration sizes (around 250, 500, 750, 1250, 1500, and 1750 configurations). This suggests opportunities for highly efficient ambulance allocation strategies that maintain fairness while minimizing operational costs of relocations.

## Usage

1. Open `ambulance_model.ipynb` in Jupyter Notebook
2. Run all cells sequentially
3. Review results in the `results/` directory
4. Adjust configurations as needed
5. Rerun the model with new parameters

### Parameter Tuning

- **Configuration Size**: Experiment with different configuration sizes. Our results show that even small configuration sets (25-30) can achieve perfect fairness, but movement requirements vary significantly with configuration selection.
- **Movement Limit**: Adjust the maximum allowed movement between time periods based on operational constraints.

## Results Directory

The `results/` directory contains:
- Optimization solution files
- Performance metrics
- Visualization plots (ambulance distribution, movement heatmaps)
- Log files

### Interpreting Results

- **Fairness Gap**: A value of 0 indicates perfect fairness (all zones receive equal coverage)
- **Movement Heatmap**: Shows ambulance movements between bases across time periods
- **Ambulance Distribution**: Shows how ambulances are distributed across bases in each time period

## Notes

- The model uses Gurobi optimization solver which may require a license for commercial (or academic) use
- Ensure sufficient memory is available for large-scale optimization problems
- Results may vary based on input data and configuration parameters
- While fairness is consistently achievable, movement patterns are highly sensitive to the specific configurations included

## Contributing

Contributions to improve the model, add new features, or enhance documentation are welcome. Please follow these guidelines:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is intended for educational and research purposes. Please check the license requirements for Gurobi optimization solver if using for commercial or academic applications.

## Citation

If you use this work in your research, please cite:
```
Park, A., Fang, L., & Wang, N. (2025). Fairness Overtime for Ambulance Allocation.
Cornell Tech, New York. ORIE 5213 Course Project.
```

## Contact

For questions or issues, please open an issue in the repository or contact the project maintainer.