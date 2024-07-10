# Machine Learning

![image](./assets/img/ML-classifier-graph.png)

This image shows the "explain classification" feature of the classifier, for review entered, "Delicious cupcakes! The frosting is a little cheap, but overall good value."

Machine Learning models are powerful ways to find patterns in large amounts of data. This classifier was trained on a database of 4,000 Amazon product reviews which were labelled as positive or negative. Using the trained model, a user can type in their own review, and the model will predict whether it is a positive or negative review.

Because this model relies only on words, bigrams (two-word pairs), and punctuation, it is actually relatively easy to understand how a rating was derived. This is in contrast to more complicated ML models, which may have multiple hidden layers of calculations, or simply too many dimensions to visualize or reason about. In this case, though, words and bigrams are associated with positive or negative reviews, and given certain weights. The "Explain Classification" function displays a bar graph of the 5 most influential positive and 5 most influential negative elements along with the overall weighted average and classification.

Using this model, it is fun to enter your own product reviews and to see how the model performs. 4,000 reviews is actually a relatively small number to be trained on, so there are lots of words the model has never seen before, and it understandably makes mistakes in confusing cases. That said, some of the things that it does gauge accurately are pretty cool. For instance:

"Wow!" is predicted as a positive review while
"wow." is predicted as a negative review

## Perceptron, SVM, Pegasos

blah blah blah

## Tuning Parameters

explanation

## Explanation Function


graphs!
