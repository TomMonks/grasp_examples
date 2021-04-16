# Introduction

Greedy Randomised Adaptive Search Procedure (**GRASP**) was introduced by Rio and Resende in 1989.

It is an extremely simple multi-start **metaheuristic** and in its basic form based on two phases:
1. an initial semi-greedy construction/repair phase 
2. a period of local search to improve on the initial solution.

The basic GRASP algorithm is outlined below.  Note that the TSP implementation in these notes always results in feasible solutions.  Optionally GRASP may include a **repair** function used to modify infeasible solutions created during the construction phase.

```
def basic_grasp():
    
    best = []
    do 
    
        s = greedy_construction()
        s = local_search(s)

        if cost(s) > cost(best):
            best = s
    
    until max iterations or time limit reached.
    
    return best
```


There are a large number of variations in how GRASP can be implemented! One powerful extension is to hybridise GRASP with another meta-heuristic called **Path Relinking**.

```{note}
In path relinking you take two solutions one of which is defined as the **current solution** and ther other the **guiding solution**.  You then take iterative (often greedy) steps to convert the current solution into the guiding solution.  The theory is that the path between the two solutions may include a better solution than the current incumbant. 
```





