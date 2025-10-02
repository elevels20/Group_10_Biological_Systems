 # Assignment 4

In this file, all questions from the assignment are answered.

## Objective


## Contributions
All group members contributed equally to this assignment. 

## Answers to the questions: 
1. **Open the model and run it – as it is – for 4h. What is happening? What do you observe?**

a. initial state
![Initial state](screenshots_simulation/initial_0h.png)

b. after one hour
![State after one hour](screenshots_simulation/after_1h.png)

c. after two hours
![State after two hours](screenshots_simulation/after_2h.png)

d. after three hours
![State after three hours](screenshots_simulation/after_3h.png)

e. after four hours
![State after four hours](screenshots_simulation/final_4h.png)


We have a pathogen infection model where the pathogen is represented in red and produces a chemical that weakens the plant cell wall represented in green. We can observe over the course of 4 hours what happens to the plant.

In the beggining we have a healthy plant cell wall. All the cells are organized in a neatly sheet and there is a clear delimitation between them. We can see the begginning of a pathogen cell in red that is making contact with the plant.

After an hour, the infection is starting to spread to the very close neighbouring cells. They start turning a dark green and brownish color meaning the pathogen is slowly getting to them.

After two/three hours, the infections starts spreadin to underlying cells as well, not just the ones in close procimity. the cells start collapsing between each other changing their initial organization. The pathigen also seems to have grwon in size and is reachjing easier to the other cells.

After four hours, the pathogen is significantly bigger and the cells underneath it have been completly damaged. Around the infected area the cells have collapsed and the growing proccess has completly stoped since the whole outside wall is infected and there are no more green cells.

2. **Describe in your own words what the code in this section does (CellHouseKeeping)**

In the CellHouseKeeping we usualluy keep track of the cell behavior. For example, the cell's growth rate and when it grows. Or the cell's differentiation like when the cell changes its type and what are the conditions of different cell types.

In our case, if the cell is of type 2 (so a pathogenic fungi), we enlarge the target area. This shows how much it expands in the tissue.
Each cell also monitors a toxin concentration. If the pathogen chemical reaches a high level (a certain threshold), the cell walls will be weakened, which allows the pathogen to get through. On the other hand, when the chemical concentration is low (below the threshold), the cell walls remain stiff.

3. **Cell to cell transport and cell dynamics. Compare the equations to the sketch of the network. What information is missing?**
![Sketch of network](Assignment4_exercise3.png)

4. **Adjust the diffusion coefficient for the pathogen’s chemical (decrease by a factor of 10, then increase by a factor of 10). Document the simulations and describe in your own words what changes.**


5. **Let’s suppose the plant has developed a defense mechanism that detects the chemical and triggers a signal for uninfected plant cells to strengthen their cell walls. How could this be implemented in the model?**
