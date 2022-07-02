# Connect4
Supervised learning neural network to play Connect 4


## Project Description
This project was done for the 2022 summer session of DIS Artificial Neural Networks and Deep Learning, and it aimed to teach a neural network to play the game Connect 4 using a small dataset of human-played games.
## Data Collection
Because there was no suitable database of Connect 4 games, I played a number of games using a pygame implimentation of connect 4, gathering the data for board states and feeding it to the model. Overall, the model viewed about 1000 positions over a variety of games and learned which moves were played in those positions by a real player.
## Outcome
The model obtained a test accuracy of about 45%-50% and a training accuracy of about 70-80%, being fairly consitent at picking the move played in a position or an equally good one. When the trained model played full games against human players, it chose logical moves in the openning following principles such as center control, even when its opponent played move orders not seen in the dataset. Overall, the model succeeded at playing at a decent level when the position was normal and balanced, and given some mistakes on the human's end could even come out on top.
## Issues & Future
Although the model succeeded in implementing several basic strategies from the dataset, it fell short of playing to the level of a human all the time. It often failed to understand its opponent's threats or create a multi-move strategy beyond playing near the center and grouping its chips together. In a position it had not seen before, it might even miss an instant win for itself, particularly when its opponent was also about to win on the next move. In general, the model responded to agression from the opponent poorly, either being too defensive or completely ignoring the incoming danger. 

While the dataset could teach the model proper moves in certain situations, 1000 solved positions could not prepare it for the trillions of possible boards it might encounter. Even teaching it to play perfectly for the first 10 moves of the game would require an much larger amount of data to account for the freedom of both players to play suboptimal or even losing moves.

Although supervised learning could teach the model how to play in given situations, it could not instill in the model a full understanding of the game that would allow it to make the best move in situations far from what it had seen before. However, despite the small amount of data, it was able to implement basic strategy concepts after a very short training time and played remarkably solid games. This shows that supervised learning still has a place in efforts to train networks for games, but its results should be a base for further efforts rather than the end goal. The quick, basic understanding of common positions and strategies combined with a deaper, more nuanced understanding cultivated through processes such as reinforcement learning could create a model that balances time to train with ultimate effectiveness.

## References
KeithGalli -- Pygame implementation of Connect4 used to gather data and test model (https://github.com/KeithGalli/Connect4-Python)

Daniel Svendsen -- Assisted with code writing and debugging (https://github.com/dhsvendsen)
