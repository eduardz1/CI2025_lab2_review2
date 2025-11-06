# CI2025_lab2

To solve this problem I used an eveolution approach. To make the testing easier I divided the code in imports, parameters, functions and resolving code.
The parameters are fine-tuned after a lot of tries on the code.
The functions are equal for all problem size. My individuals are formed by a vector represented by the solution and the fitness value. The population is an heap formed by all the individuals. The use of an heap is due to make the insert and removing faster. 
The number of generations are choose at run time based on the dimension of the problem. 

The first population is always chosend randomly, after that for every new generations we take the better 30% of the population and we make "couples", these couples will become the parents. Every couple make a new children that will be insert in the population after checking his fitness, with a probability of mutation. The mutation probability decrease after a certain amount of steps, 20 times in total. 
After the recombination we make a survivor selection, we only save the best 200 individuals and starts over.

On my PC, a MacBook with M1 processor the code run at around this time:
1000 = 8 minutes
500 = 4 minutes
200 = 1 minutes and 25
100 = 12 seconds
50 = less than a second
10 = less than a second