# INFORMS_GrowingPains
A solution to the INFORMS [Growing Pains](https://pubsonline.informs.org/doi/10.1287/ited.2016.0167cs) large scale vehicle routing optimization case study using Google OR-Tools.

## Description
The case study, which was based on a real customer problem submitted to The Institute for Operations Research and the Management Sciences ([INFORMS](https://www.informs.org/)), is a challenging capacitated vehicle routing problem with time windows (CVRP-TW) problem. CVRP-TW is a variation of the [Vehicle Routing Problem](https://en.wikipedia.org/wiki/Vehicle_routing_problem) (which itself is a generalization of the familiar [Traveling Salesman Problem](https://en.wikipedia.org/wiki/Travelling_salesman_problem) where the vehicles are limited by capacity and deliviries and/or pickups can only take place within certain times ranges (time windows). Such problems are common in logistics and fleet management.

In this case study, there are 123 locations to serve, which results in an extremely large combinatorial search space. It is usually impractical or impossible to find an optimal solution to a problem of this size. An approach used to find a good solution to these problems is [Constraint Programming](https://en.wikipedia.org/wiki/Constraint_programming#:~:text=Constraint%20programming%20(CP)%20is%20a,a%20set%20of%20decision%20variables.), which searches a large space of feasible solutions for one(s) which meet(s) the decision criteria. This implementation uses Google's open source suite of optimization and operations research tools [Google OR-Tools](https://developers.google.com/optimization) to find a solution. The project walks through the implementation from start to finish showing how to process the data, apply the OR-Tools solvers to find a solution, and examine the results. The final solution presented here can probably be improved by running the solvers for a much longer time or on very powerful hardware.

## Files
There are three Python notebooks in this repo:
- `GrowingPains_EDA_DataPrep.ipynb` explores the data provided in the case study and prepares it for use with the solver.
- `GrowingPains_ProblemSolution.ipynb` sets up the problem constraints and solver, then runs the solver to find a solution. The solution time in the notebook is limited to only 15 minutes but increasing run time can potentially find better solutions.
- `GrowingPains_ProcessingResults.ipynb` is for post-processing results. Some example tables and route maps are provided.
