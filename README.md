# Keras-text-generator-

This project involved finding the optimum settings/architecture for a neural network to perform shakespearan text generation. I tuned the parameters of https://github.com/minimaxir/textgenrnn and compared it's results with my own homebrew neural network. 

I did this using jupyter notebook on my laptop and the project also involved creation of a GUI https://www.youtube.com/watch?v=943J1jRh9mk once the weghts were set. 

textgenrnn outperformed my network most likely due to it's "skip ahead layer". 

Hyperparameters
1.	Number of LSTM layers
Theory: Due to vanishing/exploding gradient I did not expect a deeper network to be better.
2.	Bidirectional enable
Theory: Words depend on context going forwards and backwards so I expected the bidirectional layers to improve performance.
3.	Dropout
Theory: Dropout is to help prevent overfitting which was never a concern with the default model so I do not expect it to matter.
4.	Word level (as opposed to character level)
Theory: Unsure. The textgenrnn creator said that word level is only good with much larger datasets.
5.	10 or 40 Characters as input (as opposed to 30)
Theory: More characters seemed like it would lead to network at creating meaningful outputs and fewer character would lead to worse output.
6.	40 Epochs (as opposed to 20)
Theory: This many epochs would lead to over fitting and be counter-productive. 

4 layers with LSTM nodes, width 256 each layer, and using the previous 30 character had the lowest loss rate. 
