# Seq2SeqReordering
This project was done for the exam of Deep Learning course. 

The purpose of this project is to take in input a sequence of words corresponding to a random permutation of a given english sentence, and reconstruct the original sentence. 

The output can be either produced in a single shot, or through an iterative (autoregressive) loop generating a single token at a time.

CONSTRAINTS:
* No pretrained model can be used.
* The neural network models should have less the 20M parameters.

Let s be the source string and p your prediction. The quality of the results will be measured according to the following metric:
1.  look for the longest substring w between s and p
2.  compute |w|/|s|

If the match is exact, the score is 1. 

When computing the score, you should NON consider the start and end tokens.

Let's do an example.

original = "at first henry wanted to be friends with the king of france"
generated = "henry wanted to be friends with king of france at the first"
print("your score is ",score(original,generated))

your score is  0.5423728813559322

The score must be computed as an average of at least 3K random examples taken form the test set.

