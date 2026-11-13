# A Regret Minimization Implementation for Rock Paper Scissors

## Overview

Regret matching (the core of CFR) is an algorithm to find the Nash equilibrium for a game with imperfect information. This sounds scary, but what it really means is we are trying to find an unexploitable strategy - a strategy where we cannot be beaten, as the opponent cannot improve their payoff by changing their strategy. It works by minimising regret, an intuitive idea. Consider a round of RPS where your opponent plays rock and you play scissors. You regret not playing paper the most, and so next time you'll play paper. This is iterated over multiple rounds and this algorithm promises it converges to an unexploitable average strategy when both players use it.

## Included in this folder

1. A static strategy bot in Python - the `regret_matching_rps.py` file has an implementation of the bot where it calculates the average strategy using regret matching when facing a fixed opponent strategy (you could edit it to play around). For example, if your opponent is biased towards playing paper, your average strategy will be biased towards playing scissors.
2. An interactive browser game - playable [here](https://bhatia-kartik.github.io/regret-minimization/rps/), with code in `index.html`, this game allows you to see regret matching live in action. I made it because having read that humans are terrible at being random, I felt that if you have a certain style of playing RPS, the CFR algorithm can capture that and thus beat you in the long term. It also uses local cache to save your observed strategy and the bot's average and displays them as bars for you to visually see what's going on, along with your win, loss and draw rate. A fun thing is to try and predict the bot's next move and play accordingly, which will eventually lead you to the Nash equilibrium for RPS - 1/3 probability for all three actions.
3. My solution for Ex 2.5, as mentioned in the main README.
