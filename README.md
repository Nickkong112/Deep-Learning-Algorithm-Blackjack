# Reinforce-Learning-Algorithm-Blackjack

Deep Learning Blackjack is a set of an adam-optimizer generated neural networks that are trained to play blackjack. In order to create this model, we created our own training dataset. This dataset is built upon two subsets of data, consisting of simulated blackjack games. First, a set of simulated games created using the safe action method, and second, a set of simulated games created using a random action method. For each subset, we generated 170,000 completed blackjack games, and merged them all into a training dataset. We have trained each test neural network on 3 different datasets using the adam optimizer algorithm. The result is a capable blackjack playing neural network.

The first method is the safe action method. In this mode, the computer player only hits (takes another card) if they are completely guaranteed to not bust (go over 21). This results in a computer player that always hits if their hand has 11 or fewer total points, and stays if they have a hand point value of 12 or higher.

The second method is a random action method. The computer player will always perform a random choice with equal probability between hitting or staying, with no current hand point value consideration.

To generate the training dataset, 170,000 games were simulated for each of the computer player methods. These games were combined into one dataset of 340,000 sample games, and a neural network was trained from this dataset, plus each method on their own of 170,000 games each, using the adam optimizer every time . Finally, each neural network played 50,000 games of blackjack, and the results were recorded for analysis.

Below is the statistical table from a deep learning AI that is trained on the random action dataset.

              player has a usable ace                        player has no usable ace    
          11 12 13 14 15 16 17 18 19 20 21               11 12 13 14 15 16 17 18 19 20 21 
       2   H  H  H  S  S  H  H  S  H  S  S            2   S  H  S  S  H  S  S  S  S  S  S  
    D  3   H  H  H  S  S  H  S  H  S  S  S         D  3   H  S  H  H  S  S  S  S  S  S  S  
    e  4   H  H  S  S  H  H  H  H  S  S  S         e  4   H  S  S  S  S  S  H  S  S  S  S  
    a  5   S  S  S  S  H  H  H  S  S  S  S         a  5   H  S  S  H  H  H  S  S  S  S  S  
    l  6   H  S  H  S  H  H  H  H  S  S  S         l  6   H  H  H  S  S  S  S  S  S  S  S  
    e  7   S  H  S  S  H  H  H  S  S  S  S         e  7   S  S  S  S  H  H  S  S  S  S  S  
    r  8   S  S  H  H  S  S  S  H  S  S  S         r  8   H  H  H  S  H  S  S  S  S  S  S  
       9   H  H  H  S  S  H  H  S  S  S  S            9   H  H  H  S  S  S  S  H  S  S  S  
      10   H  H  H  H  S  S  S  H  S  S  S           10   H  H  H  H  S  S  H  H  S  S  S  
      11   S  S  H  H  S  H  H  S  H  S  S           11   H  S  S  S  S  H  H  H  S  H  S

We can see how our model will play based on the inputs of the player’s cards, dealer face up card, and if the player has an ace or not. Our AI table is currently not ideal for making a profit against the dealer, but our AI is able to play blackjack with an overall win average of 32%.
