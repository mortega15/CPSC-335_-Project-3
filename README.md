# CPSC-335_-Project-3
__Group Members: Maria Ortega and Neal Vaghasia__

                            INTRODUCTION
This project required at least two people to work on it. The project consisted of using two different algorithm patterns to solve the problem presented below:

![image](https://user-images.githubusercontent.com/79822470/122872363-34327d80-d2e5-11eb-95c4-cf31159ed6f5.png)


There were three components:
1. Designing an exhaustive search algorithm
2. Analyzing efficiency classes for two different algorithms
3. Implementing the algorithms and measuring the results.

                            PART 1: ALGORITHM DESIGN
The pseudocode for the bisection method was provided, to find the _n_th root of x:

def root_dbh(n, x):

    return root_db_helper(n, x, 0, x)

def root_dbh_range(x, n, lo, hi):

    mid = (lo + hi) / 2
    
    if mid == lo:
    
        return None
    elif midn == x:
    
        return mid
        
    elif midn < x:
    
        return root_dbh_range(x, n, mid, hi)
        
    else:
    
        return root_dbh_range(x, n, lo, mid)
        
        
The next step for this part was to design the algorithm with clear pseudocode to solve this problem using the exhaustive search pattern.


                            PART 2: EFFICIENCY ANALYSIS
For this part of the project we had to look at the algorithms from Part 1 to derive the complexity function T(_n_) , and then prove the efficiency class _O(f(n)_ that T(_n_) belongs to.

Exhaustive Search Pattern:

![image](https://user-images.githubusercontent.com/79822470/122873779-08b09280-d2e7-11eb-9b82-26fa96a2ab4a.png)

Bisection Method:

![image](https://user-images.githubusercontent.com/79822470/122873918-3ac1f480-d2e7-11eb-9069-03b59b848424.png)


                            PART 3: IMPLEMENTATION AND MEASUREMENT
For this part we implemeted both algorithms in C++17 using the unsigned integer type uint64_t. Each code counted and reported the number of times the main loop was ran. In the recursive case it was the number of times root_dbh_range() was called.

For the measurement part we used the code to find the 11th root of 16'985'107'389'382'393'856. What we found was that the exhaustive search pattern was faster than the bisection method. 

Sample output:

elapsed time for exhaustive search: 3.9e-06s

56

elapsed time for bisection: 4.9e-06s

56
