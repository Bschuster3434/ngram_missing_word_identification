ngram_missing_word_identification
=================================

Project used to help solve the 'Billion Word Imputation' competition on Kaggle.

http://www.kaggle.com/c/billion-word-imputation

The goal of this project is to test the hypothesis that analyzing the Part of Speech
tags for n-grams can identify a missing word in a sentence. The ngrams are being 
constructed from the billion-word benchmark corpus from Cornell University.

My belief is that this process would be valuable in detecting gramatical errors in
an ill-formed sentence. I will also explore if this method would be valuable in finding
proper nouns and adjectives/adverbs.

SPRINT 1 RESULTS

After several weeks of research, the results have come in. I have looked at the first 1m
sentences in the training set and analyzed their tri-gram 'pos' structures. I have decided
that trigrams that don't appear as often as other trigrams in a sentence have less of a
likelyhood of being gramatically correct. I have also decided that just because a particular
pos in the start of the trigram is unlikely does not mean that the rest of the trigram is 
gramatically incorrect. This is an assumption that needs testing, but one that I took for
this study.

All in all, the results were not as support of my result as I was hoping. In 58% of cases, my
six separate metrics all missed the correct position of the missing trigram position. Only in 
~18% of cases did all six metrics find the correct pos, and only in 25% of the instances was 
there a majority agreement on the right trigram. Because of the tricky nature of this problem,
this may be good enough, but my hope would be to identify the wrong pos more than 50% of the
time.

In the future, I hope to expand on this model. My first instinct is to dive further into the
results and see which trigrams I was best able to identify. I would then tweak my model
until I was able to get to my 50% benchmark.