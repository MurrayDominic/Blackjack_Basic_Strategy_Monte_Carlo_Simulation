# Blackjack Basic Strategy Monte Carlo Simulator
  Monte Carlo simulation for estimating the expected value (EV) of basic blackjack actions (hit, stand, double) for every possible player initial hand against every dealer upcard.
  This tool independently simulates each possible action from the same starting position (using separate deck continuations) to produce accurate EV estimates. The result is a pandas DataFrame table that can be used to derive or verify a basic strategy chart.

## Features  
  Supports configurable rules:
    - Number of decks
    
    - Dealer hits or stands on soft 17 
    
    - Double down allowed
    
    - Blackjack payout
    
    - Deck penetration

## Requirements
  Python 3.6+
  pandas
  numpy
  collections
  random

## How It Works:
  Simulates thousands of full shoes
  For each dealt hand (non-blackjack), independently evaluates hit, stand, and double by continuing from the same deck state
  Records profit/stake for each action
  Aggregates results into EV = total winnings / total stake
  Handles card depletion within shoes

## Note
This is not the most efficient way to compute an exact basic strategy chart — a deterministic combinatorial model (or billion-hand simulation with optimal play) would be far more precise and faster.
This project was created as a learning exercise to practice Monte Carlo simulation techniques.
