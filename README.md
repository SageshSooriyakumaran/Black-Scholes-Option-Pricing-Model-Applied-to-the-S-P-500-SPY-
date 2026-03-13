# Black-Scholes Option Pricing Model Applied to the S&P 500 (SPY)


This project utilizes the Black-Scholes model in Python and applies it to the S&P 500 ETF fund to estimate the historical volatility from SPY, as well as calculating option prices and Greek variables (Δ, Γ, Θ, ν, ρ). 
Finally, the program visualizes option payoff structures and models multiple sensitivities.

The project demonstrates financial engineering concepts including:

- stochastic modeling  
- derivatives pricing  
- volatility estimation  
- numerical root finding
- parameter sensitivity

This implementation demonstrates how theoretical pricing models can be combined with real market data to estimate option values and risk sensitivities.

## Mathematical Model

The Black–Scholes formula for a European call option is:

C = S₀ N(d₁) − K e^{-rT} N(d₂)

where

d₁ = [ ln(S₀ / K) + (r + σ²/2)T ] / (σ √T)

d₂ = d₁ − σ √T

Variables:

S₀ = underlying asset price  
K = strike price  
T = time to expiration  
r = risk-free interest rate  
σ = volatility  
N(x) = cumulative normal distribution  

## Program Workflow

How the Program Works:

1. Being written in Python, the program retrieves market data (SPY) using the yfinance API.
2. Estimates the historical volatility from the S&P 500.
3. Prices European call and put options.
4. Calculates Greek values.
5. Utilizes .plot to visualize option payoff, option price vs underlying price, and option price vs volatility.
6. Implied volatility visualization: BS(σ) = Market Price


## Libraries Used

- yfinance
- numpy
- matplotlib.pyplot
- scipy.stats
- scipy.optimize
- datetime


## System Workflow Flowchart

The following flowchart presents the pipeline of the option pricing applied to SPY market data utilizing the Black-Scholes option program.

<img width="1340" height="1623" alt="Black_Scholes_Flowchart" src="https://github.com/user-attachments/assets/381526c8-094c-4e42-a3a8-66cb64b8a815" />


## Data Source

Market data is retrieved from Yahoo Finance using the yfinance API.

- Underlying asset in this program: **SPDR S&P 500 ETF (SPY)**
- Risk-free rate: **10Y Treasury Yield (^TNX)**


## Models and Numerical Optimization Algorithms Implemented

- Black-Scholes-Merton option pricing
- Implied volatility (BrentQ numerical root finding)
- Option calculator (Greek values)


## Visualizations
The following visualizations illustrate how the Black–Scholes model
responds to changes in key parameters such as volatility and the
underlying asset price.

1. Payoff Diagram
    Shows the payoff structure of European call and put options at expiration.
2. Option Price as a Function of Underlying Price
    Illustrates how option value changes as the underlying SPY price moves.
3. 3. Historical volatility estimation from SPY
      
4. Option Price as a Function of Volatility
     
5. Implied Volatility Visualization (BS(σ)=MarketPrice)
  Shows how volatility affects option valuation and demonstrates how implied volatility is determined.


## Example Output
Underlying (SPY): 664  
Strike: 664  
Time to Expiry: ~9 days  
Black–Scholes Call Price: 8.07

BS call Price: 8.283872901652558
greeks:
Δ Call 0.5292
Δ put -0.4708
Γ gamma 0.0206
V vega 40.982
θ call -174.7193
θ put -145.2813
ρ call 8.2508
ρ put 7.6893
Implied Volatility: 0.22950480243286417

## Graphs 

<img width="713" height="1177" alt="image" src="https://github.com/user-attachments/assets/8383672e-ae58-409a-8404-eced414aef25" />

<img width="863" height="583" alt="image" src="https://github.com/user-attachments/assets/0fe7f34b-23b5-472e-addf-c0b5617c6314" />

<img width="856" height="583" alt="image" src="https://github.com/user-attachments/assets/024ee614-895a-4f97-942d-f88eae120637" />




The Black–Scholes model assumes:

- only European options
- constant volatility  
- log-normal asset price distribution  
- continuous trading  
- no transaction costs
- lack of momentum in markets

In real markets, options often exhibit volatility smiles and other effects that are not captured by the model.



## References

Black, F., & Scholes, M. (1973).  
"The Pricing of Options and Corporate Liabilities."  
Journal of Political Economy.

Columbia University.  
Foundations of Financial Engineering – Black–Scholes Model Lecture Notes.

Investopedia.  
Black–Scholes Model Explanation and Applications.

MIT – Topics in Mathematics with Applications in Finance.  
Course materials on derivatives pricing and financial mathematics.



YouTube Educational Lectures on Option Pricing:
- Black Scholes Explained - A Mathematical Breakdown (Finance Explained)
- Quant Finance with Python | Stock Market Modeling (Daniel Boctor)
- Black–Scholes Model Explained INTUITIVELY explained for Option Traders (Volatility Vibes)
- Option Price and Probability Duality (MIT OpenCourseWare)
- The Trillior Dollar Equation (Veritasium)

Aswell as multiple other academic sources. 

## Acknowledgements

This project was developed while studying option pricing theory,
financial engineering, and derivatives markets using a combination
of academic papers, university lecture notes, and educational
resources.

The implementation and code were written independently while
learning the mathematical and financial principles behind the
Black–Scholes model.



