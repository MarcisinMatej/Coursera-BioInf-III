# Coursera-BioInf-III
Solutions for coursera bio-inf courses. 

# Requirements
- Python 3.7.2
- Jupyter 

# How to use
Each notebook contains set of methods used for specific week assignment. Just start jupyter notebook / lab and run methods in each notebook.

## Week1 -> Intro (Money changes)
Basic algorithms for money exchange. 
Longets path in Directed acyclic graph solved by back-tracking

## Week2 -> Global allignment
Global allignment solved as finding the logest path in DAG, where DAG is constructed as manhattan grid for two alligned sequences. 

## Week3 -> Local and Gap allignment 
Global allignment with specific miss/match score (BLOSUM256) and also with gap allignment.

## Week4 -> Genome allignments 
Allignment of whole genomes.

Contains greedy allignment of reversal distance.

### Number of possible permutations of syntheny blocks
Lets say we have n blocks. first have to compute basic number number of permutations. That it is n! . However we must also take into account + and - directions. So to each permutation we can assign different signs. As we have 2 possible signs (+ and -) it means we have 2^n possible signs for each possible permutation. Thus we must multiply our permutations by the number o possible signs. Thus we have n!*2^n of possible reversals

### Number of possible reversals
Lets say we have n synteny blocks.
Consider the different reversals that can be applied to a permutation of length 3:

You can break the sequence ABC in 4 different places:

1   2   3   4
  A   B   C
Each reversal is the result of a pair of breakpoints, flipping the sequence between the breaks. There are 6 different pairs of breakpoints possible and thus 6 different reversals possible:

              breakpoints
 -A   B   C      1 2
 -B  -A   C      1 3
 -C  -B  -A      1 4
  A  -B   C      2 3
  A  -C  -B      2 4
  A   B  -C      3 4
Six is the number of combinations of 2 elements from a set of 4 elements (4 choose 2).

So just think, in how many places can you break a sequence of length 100?  Call this n.

And then, how many combinations of 2 elements are there in a set of n elements? Simple -> (n+1) over (n-1) combinations without repetitions.