# Connect Four

![](./assets/img/connect4-regular.png)
Gameplay image on standard board

This is a connect four game that you can play against an AI opponent. I wrote this game from scratch in a way that allows you to choose the size of the n x m board. The AI opponent plays with a minimax algorithm and uses alpha-beta pruning for efficiency. The depth can be changed easily--at higher depths, the program takes longer to run on each turn, but the computer will play more optimally. Find the code for this project [here](https://github.com/ghartmann4/connectfourgame).

![](./assets/img/connect4-large.png)
Gameplay image on large board

## Minimax Algorithm
A minimax algorithm works recursively by assuming that each player will try to maximize their own score and minimize their opponent's score. The algorithm works to a certain depth, and calls itself at each new level to pick find the best move. When the limit of the depth is reached, if the position reached is not terminal, an evaulation function is used to estimate the evaluation the position (that is, it assigns a numerical value that esimates if the position is better for Player 1, better for Player 2, or equal).

This score is passed back to one earlier level in the recursion, and so on. It's typical to use a positive score to indicate an evaluation that is better for Player 1 and a negative score to indicate an evaluation that is better for Player 2, as I have done here. At this earlier level, all of the positions that can be reached are compared, and the move that leads to the best result is chosen. (If it is Player 1 to play in that position, the move that leads to the highest evaluation will be returned, while if it is Player 2 to play, the move that leads to the lowest evaluation will be returned.) This move and corresponding evaluation are then passed back to the prior level in the recursion again. The process continues in this way until the initial level of recursion is reached, which returns a move to play in the position that was originally passed to the function.

While the code can be a bit complicated, the idea of minimax is simple: imagine playing a game and thinking a few moves ahead. You would think to yourself, "if I go here, then they will go here, then I will go here..." and so on, always trying to keep in mind that your opponent will employ the same logic to make their moves.

In practice, a depth of even just 4-5 seems to provide an even match for most human players (at least for my family and friends), and at depth of 7 it plays nearly perfectly. 

## Alpha-beta Pruning

Minimax algorithms can be costly because they 

## Position Evaluation
The position evaluation function.
