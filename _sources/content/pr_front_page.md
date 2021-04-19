# Introduction

In path relinking you take two solutions one of which is defined as the **current solution** and ther other the **guiding solution**.  You then take iterative (often greedy) steps to convert the current solution into the guiding solution.  The theory is that the path between the two solutions may include a better solution than the current incumbant.

A hybrid GRASP and Path Relinking (GRASP+PR) algorithm is one that combines the GRASP approach we have already seen with the Path Relinking metaheuristic.

There are a few key concepts that we need to learn to understand how to hybrid:

1. **Elite set tracking**
2. **Forward and backwards relinking**
3. **Evolutionary path relinking**

> One important lesson from optimisation is that good solutions are often clustered together. 