# Prime Grid Labeling
Description: generate an n by m matrix numbered 1 to n*m where each item in the matrix is only neighbored by numbers that are coprime to the item.

## Repo Structure
- `Scripts` folder includes all the code used. 
    - In version `1.0` the python program is a greedy algorithm that recursively shuffles a list of numbers 1 to (n*m) and tries to place them in a locally optimal way. If there are no available numbers in the list, it calls the function again and reshuffles.
    - In version `2.0` the python program is the same, but it tries shuffling the remaining available numbers before it calls the function and wipes the slate. Additionally, uses an `lru_cache` decorator for the `gcd` and `areCoprime` functions to (hopefully) speed it up
    - The C program uses a genetic algorithm run for many generations with mutations built in to foster genetic diversity for the generation of systems.
    - The `Utils` folder contains the scripts made to stress test the different versions of the script. This data gets put into a file in a directory that corresponds to the provided when the script is run.
- `Data` folder includes a markdown file explaining the series of tests run on the two programs, including trendlines and analysis of the two algorithms.