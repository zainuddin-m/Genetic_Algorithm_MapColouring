# Genetic Algorithm for Map Colouring Problem

This repository contains an implementation of a Genetic Algorithm (GA) to solve the **Map Colouring Problem** using Python. The goal of the Map Colouring Problem is to assign colours to regions of a map such that no two neighbouring regions share the same colour.

---

## **Features**
- **Encoding Scheme**: Each region is represented as an integer corresponding to one of the available colours.
- **Fitness Function**: Calculates the number of conflicts (neighbours with the same colour) in the colouring.
- **Genetic Operators**:
  - **Selection**: Tournament selection to favour fitter solutions.
  - **Crossover**: Two-point crossover to combine parent solutions while maintaining valid colour assignments.
  - **Mutation**: Randomly changes the colour of a region to maintain diversity.

---

## **Dependencies**
The following Python libraries are required:
- **numpy**: For mathematical operations.
- **DEAP**: A framework for evolutionary algorithms.
- **matplotlib**: For visualising the map.

## Install dependencies using:
pip install deap numpy matplotlib

## How It Works
Initialization: Generate a population of random colour assignments for the map regions.

Fitness Evaluation: Count the number of conflicts (same-colour neighbours) for each solution.

Selection: Use tournament selection to choose the best solutions for reproduction.

Crossover and Mutation: Combine and mutate solutions to explore new possibilities.

Evolution: Iterate over generations to improve the population.

Output: The algorithm outputs a conflict-free solution and a visualisation of the coloured map.


## Results
The genetic algorithm successfully finds a solution with no neighbouring regions sharing the same colour.
A visualisation of the coloured map is provided, showing the regions and their assigned colours.

## Code Highlights
Fitness Function: Evaluates the number of conflicts in the map colouring:
def evalMapColouring(ind):
    val = 0
    for i in range(numNames):
        for j in range(numNames):
            if neighbours[i][j] == 1 and ind[i] == ind[j]:
                val += 1
    return val,

## DEAP Framework: 
Used to handle population initialization, genetic operations, and evolution.

## Customization:
Update the adjacency matrix (neighbours) to define the map structure.

Adjust parameters like population size, crossover probability, mutation probability, and generations for experimentation.

## About This Project:
This code is part of my MSc Artificial Intelligence course, focusing on constraint satisfaction and evolutionary computation.

## Acknowledgments
Framework: DEAP Documentation

This project was created using academic materials from the CS5707 Artificial Intelligence course.
