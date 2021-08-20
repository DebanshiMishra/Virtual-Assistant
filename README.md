# Virtual-Assistant
An AI chatbot that answers the general queries of the user.

## Motivation :
Nowadays many companies are making extensive use of chatbots such as google assistant or cortana where the input is in the form of speech i.e, they implement speech recognition .

## Introduction:
We Implemented a Chat-bot that answers general queries of the user. What makes this chatbot unique is that we get the output in complete sentences and not just a simple yes or no.

## Models and Algorithms :
We are implementing this chatbot using SEQ2SEQ model in which we use 2 RNN layers i.e, encoder(input) and decoder(output) layers. Before feeding the input to the encoder layer we pre-process the dataset that we obtain from the cornell movie corpus data. Some of the pre-processing techniques involve cleaning and padding of sentences , filtering of these sentences based on a threshold length and we also used word embeddings of the input.

Here if we would have used simple RNN to train the model , the problem of vanishing gradient would have arised in the updation of weights resulting in poor training of the model . To prevent this we have used LSTM RNN cell which takes care of the important information being lost in the sentence using a memory cell state. Also we are using Attention Mechanisms for decoding large sequences of words.

Finally, We used beam search decoding to get the decoder output from the chatbot.

## Evaluation :
For evaluating out chatbot we manually gave inputs to our chatbot and we saw that for every 10 questions 6-7 of them were giving correct output
