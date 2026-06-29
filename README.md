# Dynamic Delta Hedging Simulation
### By: Amartiya Kakodiya | IIT Kharagpur

## Overview
This project simulates dynamic delta hedging of a short call 
options position using Monte Carlo GBM price paths. Tracks 
daily P&L, hedge slippage and rebalancing costs across 1000 
simulation paths. Analyses the impact of rebalancing frequency 
on hedging performance — the fundamental tradeoff between 
hedge accuracy and transaction costs.

## Tools
Python | NumPy | Matplotlib | SciPy

## Methodology
1. Built Black-Scholes pricing and Delta functions from scratch
2. Simulated 1000 GBM stock price paths over 252 trading days
3. Ran dynamic delta hedging simulation across all paths
4. Tracked P&L, hedge error and transaction costs per path
5. Analysed 5 rebalancing frequencies from Daily to Quarterly

## Key Results
- Paths Simulated:         1000
- Trading Days:            252
- Mean P&L:                $-13.27
- Mean Hedge Error:        $13.27
- Mean Transaction Cost:   $5.50
- Final Price Range:       $54.16 to $179.39

## Rebalancing Frequency Tradeoff
| Frequency  | Hedge Error | Transaction Cost |
|------------|-------------|------------------|
| Daily      | $13.27      | $5.50            |
| Weekly     | lower       | lower            |
| Monthly    | $9.50       | lowest           |
| Quarterly  | highest     | lowest           |

## Key Insights
- More frequent rebalancing reduces hedge error but raises costs
- Daily hedging is NOT always optimal due to transaction costs
- Monthly rebalancing shows better P&L due to lower costs
- This tradeoff is central to real world options market making
