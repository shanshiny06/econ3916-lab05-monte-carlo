# econ3916-lab05-monte-carlo
# Monte Carlo Engine -- Probability & Simulation

## Objective

This project builds and tests simulation-based tools for estimating probabilities and financial risk measures when exact analytical answers are hard to compute directly.

## Methodology

- Simulated 10,000 coin flips and tracked the running proportion of heads over time to visualize how the Law of Large Numbers pulls a sample proportion toward its true probability
- Simulated 10,000 Monty Hall games comparing the "always switch" and "always stay" strategies
- Simulated a disease screening test applied to 100,000 people, using a 1% disease prevalence, 95% sensitivity, and 90% specificity, to examine how a positive test result relates to the true probability of being sick
- Computed Monte Carlo Value at Risk and Expected Shortfall for a 1 million dollar portfolio, using simulated daily returns to estimate both the 95% and 99% confidence levels
- Verified that Monte Carlo estimation error shrinks proportionally to 1 over the square root of the number of simulations, by estimating pi and tracking how the estimate's error decreased as the sample size grew
- Asked an AI to write a reusable Value at Risk and Expected Shortfall function, then checked its output against my own hand-calculated numbers to confirm it was correct

## Key Findings

- Switching doors in the Monty Hall problem won 66.94% of simulated games, closely matching the theoretical expectation of 66.67%, confirming that switching doubles your odds compared to staying
- In the disease screening simulation, only 9.2% of people who tested positive were actually sick, despite the test's 95% sensitivity, illustrating the base rate fallacy: when a disease is rare, most positive results are false alarms rather than true cases
- The 95% Value at Risk for the portfolio was 19,494 dollars, while the 95% Expected Shortfall was 24,230 dollars, showing that once losses cross the VaR threshold, they tend to be meaningfully worse on average than the threshold itself
- Checking an AI-generated risk function against my own calculations showed that AI can draft working code quickly, but the function initially left an important assumption about input format unstated, which only became clear once I compared its output directly against numbers I had already computed by hand
