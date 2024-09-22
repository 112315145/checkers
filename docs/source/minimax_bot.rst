.. toctree::
   :maxdepth: 2
   :caption: Contents:


Minimax Bot
================================
.. topic:: **What is the Minimax Algorithm and How it works?**

    The Minimax algorithm is a decision-making technique commonly used in game theory and artificial intelligence. It's a backtracking algorithm that helps players determine the optimal move in a two-player game, assuming that both players are playing optimally.

    It helps players find the best possible move by creating a tree of all possible game states and assigning values to each outcome. The algorithm then works backward, selecting the move that leads to the highest value for the current player.




.. topic:: **Recursion and Depth Limit**

     **Problem**: The Minimax algorithm can become computationally expensive as the search depth increases. The number of possible game states grows exponentially with depth, leading to longer computation times.

     *We find depth 3 suitable to play against human. It provided good results without time lag.*



.. list-table:: **Minimax Bot vs Random Agent**
   :header-rows: 1

   * - Depth
     - Games Played
     - Wins
     - Loses
     - Draws
     - Time Taken
     - Avg. Moves
   * - 1
     - 100
     - 44    
     - 12     
     - 44     
     - 5.37        
     - 63.82
   * - 2 
     - 100  
     - 78 
     - 0
     - 22
     - 9.49 
     - 52
   * - 3  
     - 100
     - 89
     - 0 
     - 11
     - 29.31
     - 50.14
   * - 4 
     - 100
     - 72 
     - 1 
     - 27 
     - 155.22 
     - 55.98 
   * - 5 
     - 10
     - 8 
     - 0
     - 2
     - 56.62 
     - 53.2
   * - 6
     - 10 
     - 7 
     - 0 
     - 3
     - 211.16
     - 58.6
   

.. topic:: **Observations**

     1. **Increased Depth, Increased Wins:** As the depth of the Minimax algorithm increases, the probability of the RL agent winning also tends to increase. This suggests that a deeper search horizon provides the Minimax agent with a greater advantage in evaluating the game state.
     2. **Increased Depth, Slower Response:** A direct consequence of increasing the Minimax depth is a significant increase in the time required for the Minimax bot to compute its move. This is because the algorithm explores a larger number of possible game states as the depth grows.

