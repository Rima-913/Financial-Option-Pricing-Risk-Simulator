# Financial-Option-Pricing-Risk-Simulator
## 🌟 Project Overview
Imagine you want to buy insurance for your car. The insurance company needs a way to calculate exactly how much that "policy" should cost today based on how likely you are to have an accident in the future.

In finance, Options are like those insurance policies. This project provides a toolkit to calculate the fair price of these "policies" (options) and manage the risks involved using advanced mathematical models and computer simulations.


## 📉 Core Concepts (The "What" and "Why")
### 1. What are Options?
An option is a contract that gives you the right to buy (Call Option) or sell (Put Option) a stock at a fixed price, but only for a limited time.



The Problem: Because stock prices are random, it’s hard to know what that right is worth today.


The Goal: Use math to find a "fair price" so traders don't overpay or under-invest.


### 2. Modeling Randomness (Brownian Motion)
Stock prices don't move in a straight line; they "jitter" randomly. We use Geometric Brownian Motion (GBM) to model this. Think of it as a "random walk" where the stock generally trends in one direction (drift) but with constant, unpredictable fluctuations (volatility).

## 🚀 Methods Used (The "How")
This project compares three different ways to find the fair price of an option:


### 1.The Gold Standard (Black-Scholes Model): 
A famous mathematical formula that gives an exact "theoretical" price instantly. It works perfectly in "ideal" conditions but can be too simple for complex real-world scenarios.

### 2.The "What-If" Simulator (Monte Carlo Simulation): 
Instead of one formula, we simulate 10,000 different possible "futures" for a stock. We calculate the payoff in every single scenario and take the average.

Upgrade: I used Stratified Sampling to ensure our "futures" are spread out evenly, making the result more accurate.

### 3.The Smart Simulator (Quasi-Monte Carlo):
Traditional simulations use "random" numbers, which can sometimes "clump" together.

This project uses Sobol sequences, which are "smarter" numbers designed to cover every possibility more uniformly. This makes the simulation much faster and more stable.

## 🛡️ Risk Management (The Greeks & Hedging)
Pricing the option is only half the battle. Traders also need to know how their "policy" value will change if the market moves.


The Greeks: We calculate sensitivities like Delta (how the price changes if the stock moves $1) and Vega (how it changes if the market gets more volatile).


Hedging: This is the strategy of taking opposite positions to "cancel out" risk, ensuring a portfolio stays stable even during market swings.

## 📊 Key Results
Using real-world data from HDFC Bank, the project found that:

The Black-Scholes benchmark price was 29.17.


The Quasi-Monte Carlo method reached a nearly identical result (29.15) but required fewer simulations to get there, proving it is a more efficient tool for professional traders.

## 🛠️ Tech Stack
Language: Python
Libraries: NumPy (Math), Pandas (Data), SciPy (Statistics), Matplotlib (Visualizing stock paths)
Techniques: Geometric Brownian Motion, Owen Scrambling, Finite Difference Methods.
