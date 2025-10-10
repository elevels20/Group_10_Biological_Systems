 # Assignment 5
The notebook of this assignment can be found in [Assignment5.ipynb](Assignment5.ipynb).

## Objective
The objective of this assignment is to apply computational modelling methods to explore how biological brain structure can inform and constrain artificial neural networks within the visual system.

## Use of Generative AI
We found this assignment quite difficult to do, so we used generative AI (ChatGPT and Gemini) to solve the exercises. <br>
The transcript of the Gemini conversation can be found [here](Gemini_transcript). <br>
The transcript of the ChatGPT conversation can be found [here](https://chatgpt.com/share/68e96677-5664-8005-a417-fb3573fcfdf3)

## Contributions
All group members contributed equally to this assignment. 

## Answers to the questions 1, 2 and 3: 

### The regions involved in processing visual information along both the ventral and dorsal pathway
**Human brain:** <br>
Some of the visual information processing regions for the human brain are: 
- **V1** 
- **V2** 
- **V3**
- **V4**
- **V5**
- **Area hOc4d right (Cuneus)** 
- **Area hOc3d right (Cuneus)** 
- **Area hOc5 (LOC) right** 

For a lot of areas, information on cell density was missing, for example for the dorsal occipital cortex Area hOc6 (POS). For that reason, we extracted information of Area hOc1 (V1, 17, CalcS) from both left and right, to make a total of six.
We extracted information from the areas:
- **V1**: Mapped to "Area hOc1 (V1, 17, CalcS) right"
- **V1**: Mapped to "Area hOc1 (V1, 17, CalcS) left"
- **V2**:  Mapped to "Area hOc2 (V2, 18) right" 
- **Area hOc4d right (Cuneus)**
- **Area hOc3d right (Cuneus)** 
- **Area hOc5 (LOC) right** 

**Monkey brain:** <br>
Some of the visual information processing areas for the monkey are: 
- **V3d**
- **V3A**
- **V4dl**
- **V4dm**
- **V6Adl**
- **V6Adm**

However, there is no information in the interactive viewer of Siibra to be found on these regions. <br>

**Marmoset brain:** <br>
Some of the visual information processing regions for the marmoset are: 
- **primary visual cortex**
- **visual area 2**
- **visual area 3 (ventrolateral posterior area)**
- **visual area 4 (ventrolatereral anterior area)**
- **visual area 5 (middle temporal area)**
- **visual area 6 (dorsomedial area)**
However, there is no information in the interactive viewer of Siibra to be found on these regions.

Because there is no data available for the monkey and marmoset brain, we choose to only implement the human model and then compare different variants.
The extracted information about the cell density and structural connectivity can be found in [here](Human_brain_data).
