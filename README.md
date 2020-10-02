# WRLD Software Engineering Exercise

At WRLD we are bringing maps to life - it's important for us to be able to analyze data about map features.

Consider a map that has the following properties;

- the map is two dimensional
- the map is perfectly square with dimensions 10000000x10000000
- the map has an associated set of many features
- the map does not "wrap around"

Each feature on the map is described by a 2D coordinate in the range (0, 0) to (10000000, 10000000). 

We would like to find the most isolated feature on the map, where the "most isolated feature" is the feature that is 
furthest (largest Euclidian distance) from any other feature. Because the map does not "wrap around", this should be a 
direct distance across the map.

<----10000000---->
 ---------------      -
| A             |     |
|               |     |
|               |  10000000
|               |     |
|          B  C |     |
|        E   D  |     |
 ---------------      -

In the example above, A is the most isolated feature on the square map with edge length 10000000.

We would like you to write a program that reads in many features from standard input, and outputs the name of the most isolated feature to standard output. The format of the input is the feature name, x coordinate and y coordinate separated by spaces.

Each feature is on a new line. There may be any number of features between 1 and 100000. The program should be fast, so the algorithm must be better than O(n^2) (optimized/early-out variants of O(n^2) are also unacceptable).

You may submit a solution using the language of your choice, but please bear in mind that we need to be able to build and run your solution, so instructions are appreciated.

You may use 3rd party code & libraries as long as they are attributed in some way.

Submissions are marked based on the following criteria:

- Correctness - The program should read the input format as specified and write the correct answer to standard output.
- Efficiency - The program should be fast, i.e., the algorithm should exhibit better than n^2 growth.
- Elegance - The program should be concise and simple

Two example inputs are provided; problem_small.txt should output place6 and problem_big.txt should output place55163

A sample invocation might look like:
$ ./most_isolated < problem_big.txt
place55163

This exercise can be completed in an evening. If you think it is going to take longer, it is worth re-reading this document and re-evaluating your approach.