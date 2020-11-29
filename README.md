# Reinforcement Learning Stock Trading Bot

## Summary
This notebook implements a stock trading bot using reinforcement learning. A deep neural network was used to obtain the best results.


## API 
The Yahoo Finance API was used to acquire the most up to date daily stock prices for stocks listed on most major stock exchanges.

## RL Algorithm
The reinforcement learning algorithm centers around the use of an 'n-day' state representation. I found it best to use 10 days for this purpose. Each iteration (or day), the agent evaluates this state representation and determines the best course of action for that day (buy/sell/hold). It also forms a new state representation for the following day.

## Neural Network and Optimzing Loss
The neural network is a fairly small and simple network with only two dense layers. I tried to keep the network simple to reduce training time and allow for quick results, however, varying the network architecture may improve results. Loss is calculated using MSE and optimized using SGD. SGD proved to work quite well for this bot and seems promising in future iterations. Parameters are tuned after every mini batch (currently 64 days), increasing the frequency significantly increases training time.

## What's next
I need to compare the results of this model with plainly buying and holding a stock, as well as test it out with stocks that have performed poorly over the last several years. In the case that this model does not stack up in those circumstances, I will first try to readjust the neural network, followed by parameters related to the state representation for a given day.

Additionally, more metrics, performance indicators and visuals would always be nice. Hope to turn this into a dashboard that can be easily used by non technical users. 
