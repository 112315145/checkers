.. toctree::
   :maxdepth: 2
   :caption: Contents:


Reinforcement Learning Bot
================================
.. topic:: **Q Learning**

    The Q-learning algorithm process is a Reinforcement learning algorithm where the agent learns by exploring the environment and updating the Q-table based on the rewards received.



.. topic:: **RL Bot Training by making it play against Minimax Bot**

     **Initial Training:** We began training the RL bot by having it compete against Minimax bot of varying depths, including depths 1, 2, and 3.

     **Minimax State Caching:** To accelerate the Minimax evaluation process, we saved the Minimax state and its corresponding best action in a JSON file. This allowed us to reuse this information when necessary, avoiding redundant calculations.



.. list-table:: **Training mode: against Minimax Bot**
   :header-rows: 1

   * - Depth
     - First win at ep
     - Time (s)
     - Total Q values
     - Updated Q values
     - Q-file size (MB)
     - Total Minimax states
     - Acessed Minimax states
     - Minimax file size (MB)

   * - 1
     - 1
     - 0
     - 38
     - 0
     - 0.04
     - 35
     - 0
     - 0.02
   * - 2
     - 306
     - 15
     - 6,180
     - 1,210
     - 0.51
     - 6,981
     - 1,166
     - 0.77
   * - 3
     - 4,244
     - 11.50
     - 72,731
     - 26,306
     - 8.74
     - 82,236
     - 25,911
     - 5.95


.. topic:: **Once RL bot wins a game against minimax, it achieves perfect play against Minimax bot of that specific depth**

     This is because, for a specific board state, minimax algorithm follows a deterministic path based on its search depth. Consequently, the RL bot only requires sufficient exploration to identify weaknesses in Minimax’s decision-making process.

     **Drawback:** *While this training method allows the RL bot to excel against Minimax, it may not be optimal for playing against human opponents.* Simply exploiting weaknesses in Minimax's algorithm might not translate well to human-like strategies. Therefore, we also trained our RL agent against other RL agent to improve its generalizability and adaptability.


.. topic:: **RL Bot Training by making it play against RL Agent**

     * In this training method, both agents learned concurrently, interacting and improving their strategies simultaneously.
     * The Q-table, which stores the board state and corrosponding Q values, was saved to a JSON file.
     * We conducted a comprehensive evaluation of our model by training it on different combination of parameters and opponents(Minimax and RL).This involved training the model on approximately 700,000 episodes, distributed across different files.
     * We have gathered the statistical data by training our model against another RL agent for 100,000 episodes. During this training, we systematically varied the value of epsilon, a crucial parameter that controls the exploration-exploitation trade-off in reinforcement learning.


.. list-table:: **Training Mode: against RL Agent**
   :header-rows: 1

   * - Epsilon
     - Games Played
     - Wins
     - Loses
     - Draws
     - Time Taken (s)
     - Avg. Moves
     - Total Values
     - Updated Q values
     - Q-file size(MB)
     - Dump Lag (s)

   * - 1-0.1
     - 10000
     - 3226
     - 3065
     - 3709 
     - 05:37 
     - 62.5089 
     - 287,425 
     - 1535 
     - 35.3 
     - 0
   * - 0.20
     - 10000
     - 3208
     - 3139 
     - 3653 
     - 05:26 
     - 62.3761 
     - 565,889 
     - 3317 
     - 69.5 
     - 3
   * - 0.10
     - 10000
     - 3217
     - 3176 
     - 3553 
     - 04:06 
     - 62.294 
     - 839,939 
     - 4651 
     - 103 
     - 5
   * - 0.05
     - 10000
     - 3270
     - 3111 
     - 3619 
     - 02:58 
     - 62.1713 
     - 1,111,161 
     - 5055 
     - 136 
     - 7
   * - 0.01
     - 10000
     - 3007
     - 3233 
     - 3760 
     - 03:04 
     - 62.7485 
     - 1,380,788 
     - 6810 
     - 169 
     - 8
   * - 0.01
     - 10000
     - 3153
     - 3111 
     - 3736 
     - 03:11 
     - 62.7629 
     - 1,648,987 
     - 7109 
     - 202 
     - 11
   * - 0.01
     - 10000
     - 3134
     - 3234
     - 3632 
     - 03:00 
     - 62.2524 
     - 1,914,617 
     - 7797 
     - 235 
     - 12
   * - 0.01
     - 10000
     - 3250
     - 3008 
     - 3742 
     - 02:58 
     - 62.8426 
     - 2,180,578 
     - 8470 
     - 267 
     - 13
   * - 0.01
     - 10000 
     - 3146
     - 3179
     - 3675 
     - 03:00 
     - 62.4083 
     - 2,445,756 
     - 8146 
     - 300 
     - 15
   * - 0.01
     - 10000 
     - 3065
     - 3128 
     - 3807 
     - 03:04 
     - 62.8942 
     - 2,710,314 
     - 9238 
     - 333 
     - 17


.. topic:: **Observations**

     1. **Consistent Performance:** The number of wins, losses, and draws remained relatively stable throughout the training process, indicating that both agents were learning at a similar pace. As the exploration rate decreased (epsilon decreased), more Q-values were updated, suggesting a shift towards exploitation.
     2. **State Exploration:** A significant number of new Q-values were added to the Q-table during training. This indicates that the model was encountering previously unseen game states, highlighting the vast complexity of the checkers game.
     3. **Dump lag:** Loading and dumping of Qtable from JSON file takes time. This is due to increase in file size.
     4. **Training Depth:** The agent was able to achieve 100% accuracy against a Minimax agent with a depth of 1 very early in training. However, it struggled to maintain this level of performance against a Minimax agent with a depth of 2, suggesting that lot more training is necessary for it to play effectively.
