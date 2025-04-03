# Notes on "Artificial neural networks for predicting the performance of heat pumps with horizontal ground heat exchangers"

## Overview
This research paper investigates the application of Artificial Neural Networks (ANNs) for predicting the performance of Ground Coupled Heat Pump (GCHP) systems with horizontal Ground Heat Exchangers (GHEs) in rural industry applications, specifically for poultry sheds in Australia.

## Key Points

### System Description
- Ground Coupled Heat Pump (GCHP) is a highly energy efficient HVAC system that uses the ground as a heat source when heating and as a heat sink when cooling
- The paper focuses on horizontal Ground Heat Exchangers (GHEs) which are typically installed in rural areas at 1-2m depth
- Well-designed GCHP systems with horizontal GHEs can operate at a coefficient of performance (COP) between 3 and 5

### Machine Learning Approach
- Artificial Neural Networks (ANNs) were used to predict the COP and GHE inlet and outlet temperatures
- The ANN model was trained using over 700,000 hourly performance data items
- Data covered 80+ different yearly loading patterns under three different climate conditions
- The training data was generated using a Transient System Simulation Tool (TRNSYS) model

### Results and Performance
- The trained ANN can predict performance even under climatic conditions and locations not specifically trained for
- High accuracy achieved with limited types of input data (less than 5% error in most cases tested)
- Computational efficiency: ANN model is 100 times faster than TRNSYS simulations and 10,000 times faster than finite element models
- With only three types of input data, the error is less than 10% in most cases tested

### Application Context
- Focus on rural industry applications, specifically poultry farming in Australia
- Poultry industry in Australia raises over 600 million chickens yearly
- Energy for heating and cooling large poultry breeding houses costs approximately A$80 million per year
- GCHP adoption can transform the poultry farming industry by reducing energy consumption, GHG emissions, and chicken mortality

### Advantages Over Traditional Methods
- Commercial software packages (Ground Loop Design, GLHEPRO) have limitations for horizontal GHEs
- Analytical models that work for vertical GHEs cannot be directly used for horizontal GHEs
- The ANN approach overcomes these limitations and provides fast, accurate predictions

## Reference
Zhou, Y., Narsilio, G., Makasis, N., Soga, K., Chen, P., & Aye, L. (2024). Artificial neural networks for predicting the performance of heat pumps with horizontal ground heat exchangers. Frontiers in Energy Research, 12. https://doi.org/10.3389/fenrg.2024.1423695
