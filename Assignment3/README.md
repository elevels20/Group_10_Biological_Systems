 # Assignment 2

## Code
All code for this assignment can be found in [CodeAssignment3.ipynb](CodeAssignment3.ipynb). The start of this notebook is the completed BooleanModeling.ipynb notebook from the practical. After this (in the same file), the actual assignment can be found. 

To run the notebook:
1. Open the file in Jupyter Notebook.  
2. Run all cells in order, starting from the top.

## Objective
The goal of this assignment was to analyze the impact of cancer-causing mutations on cell regulatory networks through Boolean network modeling.

## Contributions
All group members contributed equally to this assignment. 

## Answers to the questions: 
1. **Which mutation is most dangerous and why? Provide quantitative evidence.**
Answer: Destroying the function of the central tumor supressor p53 is the most dangerous thing that can happen since it leads to failure of DNA damage responce. So, the loss of p53 is very dangerous and this happens in both Mutation A and Mutation C.
Mutation A, due to the loss of p53, eliminates a major cell cycle arrest.
Mutation C, due to keeping MDM2 ON, we neutralize the p53 function, mimicking a p53 knockout like in Mutation A.
By comparing the attractors of these two mutations, we can see that a high procentage of initial states converge towards having Growth=1 and Death=0 that lead to the malignant attractor because they both eliminate the cell's key defence mechanis.
The Boolean network simulations show that the number of stable states is lower because the healthy cell arrests or apoptosis are less when removing the p53.


2. **Explain the role of feedback loops (e.g., MYC → MDM2 → p53)**


3. **What are the limitations of this Boolean network model? Discuss 3 specific limitations.**
