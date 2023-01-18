# Authourship-Attribution
Authourship attribution with naive bayes using word and ngram


This is an example use of the Naive Bayes algorithm. The system is trained on five texts by four authors: Austen, Kipling, Carroll and Grahame. It is then required to guess the author of an additional text (which -- spoiler alert -- is Jane Austen's Emma).

## Requirements

You'll need the docopt package to run the code from the terminal. If you need to install it on your system, do:

    sudo pip3 install docopt-ng
    
## Run the code

To run the code, type:

    python attribution.py --words data/emma.txt

Or alternatively:

    python attribution.py --chars 3 data/emma.txt

The first alternative computes a model over words, as we saw in class. The second alternative uses character ngrams of the size given to the system.

The output of the code tells you which operations the classifier is currently performing: computing prior probabilities, conditional probabilities, etc. Then, for illustration, it outputs the 10 features with highest conditional probability for the class under consideration (i.e. for each author). It gives you an idea of which words / ngrams are most important for each author. Finally, you get sorted log figures for the probability of each class. The first entry in that list is the author guessed by the system.
