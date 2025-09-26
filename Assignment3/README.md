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

## Answers to the questions
1. **Which mutation is most dangerous and why? Provide quantitative evidence.** <br>
Answer: Destroying the function of the central tumor supressor p53 is the most dangerous thing that can happen since it leads to failure of DNA damage responce. So, the loss of p53 is very dangerous and this happens in both Mutation A and Mutation C. <br>
Mutation A, due to the loss of p53, eliminates a major cell cycle arrest. <br>
Mutation C, due to keeping MDM2 ON, we neutralize the p53 function, mimicking a p53 knockout like in Mutation A. <br>
By comparing the attractors of these two mutations, we can see that a high procentage of initial states converge towards having Growth=1 and Death=0 that lead to the malignant attractor because they both eliminate the cell's key defence mechanis.
The Boolean network simulations show that the number of stable states is lower because the healthy cell arrests or apoptosis are less when removing the p53.


2. **Explain the role of feedback loops (e.g., MYC → MDM2 → p53)** <br>
MDM2, and MDM2 suppresses p53. p53 (and its proxy p21 = p53) inhibit MYC. This creates a mutual inhibition architecture: either a p53-high / MYC-low protective state or a p53-low / MYC-high pro-growth state. In Mutation C (MDM2 overexpression), p53 is forced low regardless of damage, which collapses the toggle into the MYC-high branch—functionally mimicking a p53 knockout. <br>

Oncogenic positive reinforcement via MYC → MDM2 ┤ p53 → (disinhibits) MYC: Because MYC → MDM2 and p53 = DNA_damage AND (NOT MDM2), high MYC raises MDM2, which lowers p53, which in turn releases MYC from inhibition (MYC = NOT p53 AND NOT p21, with p21 = p53). Net effect: a positive loop on MYC that drives the system toward Growth = ON and Death = OFF. This is why Mutation B (MYC amplification) and Mutation C (MDM2 overexpression) rapidly funnel many initial states into malignant-like attractors. <br>

Damage-response brake: DNA_damage → p53 → (p21, CDK2/Growth, Death): When DNA_damage = 1 and MDM2 is not high, p53 turns on, which (i) induces p21, shutting down CDK2 and Growth, and (ii) enables Death (Death = p53 AND DNA_damage AND (NOT Growth)). With Mutation A (p53 knockout), this brake is lost: p21 stays OFF, CDK2/MYC/Growth remain permissive, and Death is disabled.

3. **What are the limitations of this Boolean network model? Discuss 3 specific limitations.** <br>
No timing or dynamics: The model directly finds stable end-states/attractors but cannot capture realistic time-based patterns such as oscillations of p53 or temporary growth arrest. All processes are assumed to update synchronously, which simplifies but also distorts real behavior. <br>

Binary simplification: Each component is either fully ON or fully OFF, with no intermediate states. This ignores graded biological responses for example like low vs. high p53 activity leading to arrest vs apoptosis. As a result, different biological outcomes may collapse into the same Boolean state. <br>

Deterministic and no variability: Given the same starting state, the model always produces the same outcome. It cannot represent stochastic noise or variability across a cell population, even though in reality some cells might die while others survive under identical conditions. This makes the predictions more rigid than actual biology.
