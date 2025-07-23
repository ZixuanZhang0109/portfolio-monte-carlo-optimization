## Project Overview

Using a Monte Carlo approach, we simulate 700 return scenarios for the four selected assets. The simulation is based on a multivariate normal distribution defined by expected returns, standard deviations, and a correlation matrix.

Two strategies are evaluated:

- **Long Positions Only**: All portfolio weights are constrained to [0, 1] and sum to 1.
- **Shorts Allowed**: Portfolio weights may be negative (i.e., allow short selling) but still sum to 1.

For each portfolio, we compute:

- **Expected Return**:  
  \\( \\mu_p = \\mathbb{E}[w^\\top r] \\)

- **Portfolio Risk (Volatility)**:  
  \\( \\sigma_p = \\sqrt{w^\\top \\Sigma w} \\)

The opportunity sets for both strategies are visualized on a risk-return plot.

## Repository Contents

```
portfolio-monte-carlo-optimization/
├── ProgrammingAssignment2Report.pdf         # Final project report (PDF)
├── README.md                                # This file
├── asset_parameters.csv                     # Expected returns and standard deviations
├── asset_correlations.csv                   # Asset return correlation matrix
├── monte_carlo_portfolio.ipynb              # Main Jupyter Notebook implementation
├── monte_carlo_portfolio.html               # Exported HTML version of the notebook
├── portfolio_optimization_montecarlo.png    # Risk-return plot image
```

## How to Run

1. **Clone the repository**:

   ```bash
   git clone https://github.com/ZixuanZhang0109/portfolio-monte-carlo-optimization.git
   cd portfolio-monte-carlo-optimization
   ```

2. **Install required packages**:

   ```bash
   pip install numpy pandas matplotlib seaborn
   ```

3. **Run the Jupyter Notebook**:

   ```bash
   jupyter notebook monte_carlo_portfolio.ipynb
   ```

   Or open `monte_carlo_portfolio.html` directly in a browser to view the results.

## Data Files

- `asset_parameters.csv`: Contains expected annual return and standard deviation for each asset.
- `asset_correlations.csv`: Correlation matrix used to construct the covariance matrix for simulation.

You can modify these CSV files to explore other assets or parameter assumptions.

## Report

For a full explanation of the problem, methodology, and results, please see  
📄 `ProgrammingAssignment2Report.pdf`.

## AI Assistance Disclosure

This project made use of AI assistance (OpenAI ChatGPT) in:
- Designing simulation logic and helper functions
- Formatting the project report and README
- Generating code comments and documentation

All modeling decisions and simulation validations were reviewed and finalized by the project author.

## License

This project is provided for academic use and demonstration purposes only. No license is applied.
"""
