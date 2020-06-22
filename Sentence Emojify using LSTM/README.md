# Sentence Emojify using LSTM
we are going to use LSTM neural network to build an Emojifier. 
Have you ever wanted to make your text messages more expressive? 
Your emojifier app will help you do that. So rather than writing: 
"Congratulations on the promotion! Let's get coffee and talk. Love you!"
The emojifier can automatically turn this into: "Congratulations on the promotion! +1 Let's get coffee and talk. coffee Love you! heart"
we will implement a model which inputs a sentence (such as "Let's go see the baseball game tonight!") 
and finds the most appropriate emoji to be used with this sentence (baseball)

# Using word vectors to improve emoji lookups


#### Inputs and outputs to the embedding layer

* The `Embedding()` layer's input is an integer matrix of size **(batch size, max input length)**. 
    * This input corresponds to sentences converted into lists of indices (integers).
    * The largest integer (the highest word index) in the input should be no larger than the vocabulary size.
* The embedding layer outputs an array of shape (batch size, max input length, dimension of word vectors).

* The figure shows the propagation of two example sentences through the embedding layer. 
    * Both examples have been zero-padded to a length of `max_len=5`.
    * The word embeddings are 50 units in length.
    * The final dimension of the representation is  `(2,max_len,50)`. 

<img src="images/embedding1.png" style="width:700px;height:250px;">
