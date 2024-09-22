.. toctree::
   :maxdepth: 2
   :caption: Contents:



Comparision and Analysis
================================
.. topic:: **Minimax Bot Strengths**

     1. **No Training Required:** Minimax is a deterministic algorithm that doesn't require any prior training or learning.
     2. **Optimal Decision-Making:** Minimax assumes that both players always play their best moves, ensuring that it makes optimal decisions based on its search depth.
.. topic:: **Minimax Bot Weaknesses**

     1. **Depth Limitation:** The Bot becomes slow after increasing depth (more than 4).
     2. **Static Strategy:** Always follow a same particular strategy based on its search depth, making it vulnerable to opponents who can adapt or exploit its weaknesses.

.. topic:: **RL Bot Strengths**

     1. **Opponent Versatility:** RL bot can learn to play against various types of opponents.
     2. **Faster Decisions:** An RL bot makes decisions faster than a minimax algorithm because they can retrieve actions from a Q-table instead of re-evaluating the entire game tree.


.. topic:: **RL Bot Weaknesses**

     1. **Training Time:** RL bots require significant training time to learn optimal policies.
     2. **Initial Performance:** Before sufficient training, RL bot performs poorly and make suboptimal decisions.



.. topic:: **Analysis**

     1. **With Human as opponent:** *Minimax bot plays  better than RL bot*
     2. **In a checkers game between Minimax bot and RL bots:** *The RL bot can exhibits perfect play when trained against Minimax bot of that specific depth.*




