.. toctree::
   :maxdepth: 2
   :caption: Contents:



Objective and Implementations
================================
.. topic:: **Objective**

    Our work builds upon the foundational research of Santiago Videgain and Pablo Garcia Sanchez (2021) in their paper titled ’**Performance Study of Minimax and Reinforcement Learning Agents Playing the Turn-based Game Iwoki**’. 



    In this paper, a series of intelligent agents with different reasoning and decision capacities have been developed based on different artificial intelligence techniques applied to game theory, such as Minimax or Reinforcement Learning. Their capabilities have been tested by playing games with each other, against human players, obtaining remarkable results.

    The objective of this paper is to determinate which implementations are most appropriate for agents who play iwoki in order to win and to evaluate which configurations optimize results.


    *We have attempted to adapted the concepts and analysis methods from this paper and implement them for classic game of checkers.*





.. topic:: **Our Implementations**

     1. A 2 player Checkers game
     2. Implementation of Minimax Bot
     3. Implementation of Reinforcement Learning Bot(Q Learning)
     4. Comparision and Analysis of these two bots against each other, human player and random agent






.. topic:: **Game Implementation**

     1. We have build the game logic in **Python language**
     2. The Board representation throughout the code in is in **Numpy**
     3. For UI we have used the **Pygame**
     4. To store Q values and minimax state-reward data, we used **JSON** file
