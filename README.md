# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.


///
According to the content of the class slides,the p of a good pivot is 1/2\

Median-of-three contains three elements, the first, middle, and last element in the array. and choose the median of those three elements as the pivot.\

It is known that the probability of any element being a good pivot is 2/4, the probability of being too small is 1/4, and the probability of being too large is 1/4\

There are four cases, each containing three types of element states.\

1
one good, one small, one big\
1/4*1/4*1/2 
There are 1+2+3 possible permutations, so the probability is 6*(1/32) = 3/16\

2
one good, one good, one small\
1/2*1/2*1/4  \
There are 1+2 possible permutations, so the probability is 3*(1/16) = 3/16\

3
one good, one good, one big\
1/2*1/2*1/4\
There are 1+2 possible permutations, so the probability is 3*(1/16) = 3/16\

4
all good pivot\
1/2*3 = 1/8\

1/8+（3/16）*3 = 11/16\

median-of-three approach p is higher than leftmost with 11/16 vs 1/2\

###
Source: ChatGPT help me how the Median-of-three and leftmost works.
Plagiarism Statement: “I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”
