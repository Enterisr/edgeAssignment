## Background:
Team Fnatic and Team Liquid are long time rivals in the CS:GO tournaments.
Both teams qualified for the finals in the ESL Pro League 2021.
Team Fnatic is Edge’s preferred and strategic customer/ partner. Along the usual training by Edge, we have decided to aid with calculating and portraying their skills and performance in the training sessions.

Edge’s most talented technology department took on this challenge.

**Your mission**, dear potential colleague, is to implement a function that takes in the training session information and output the html displaying the session analysis as it will be described.

## Input:
1. Each player, during a training session (or even a competitive game), makes a lot of moves and decisions = **Measurements**. The input of the function you will write is an **array of measurement hashes**.
2. You will calculate a grade for each measurement entry based on the criteria listed below. You will also combine all similar measurement type entries (such as **move**) into an average creating an accumulated **measurement type value**. Different measurement types are combined to create a **Skill**. A **Skill** accumulated value is calculated based on a combination of the accumulated values of the different **measurement types**. More specifically, it is the **weighted average** of the different measurement types values (examples follow). 
3. The Skills for the assignment are Speed and Accuracy.
4. Speed’s measurement types are:
  **Move** - The time of a mouse movement from mid screen to a target (value in miliSeconds int) – Can happen several times in a session.
  **Bomb** - The total time it took to implant a bomb – Can happen only once at the most (value in boolean).
5. Accuracy’s measurement types are:
  **Misses** - The distance of a shot from a target’s head (value in pixels int) – Can happen several times in a session.
  **Headshot** – A direct hit in the head of a target (value in boolean) - Can happen several times in a session.
  **Body hit** - A direct hit in the body of a target (value in boolean) - Can happen several times in a session
6. Here is an example of an input:
```
[
{time: 40, type: 'Move', value: 65},
{time: 40, type: 'Misses', value: 105},
{time: 100, type: 'Misses', value: 50},
{time: 120, type: 'Move', value: 105},
{time: 140, type: 'Move', value: 90},
{time: 160, type: 'Headshot', value: true},
{time: 280, type: 'Move', value: 400},
{time: 280, type: 'Misses', value: 55},
{time: 600, type: 'Misses', value: 110},
{time: 900, type: 'Misses', value: 88},
{time: 1260, type: 'Body', value: true},
{time: 10080, type: 'Move', value: 44},
{time: 10500, type: 'Misses', value: 222},
{time: 10600, type: 'Misses', value: 99},
{time: 10700, type: 'Move', value: 300},
{time: 12600, type: 'Body', value: true},
{time: 16780, type: 'Misses', value: 50},
{time: 21000, type: 'Body', value: true},
{time: 27000, type: 'Misses', value: 8},
{time: 27060, type: 'Misses', value: 510},
{time: 27160, type: 'Move', value: 140},
{time: 27480, type: 'Move', value: 200},
{time: 27900, type: 'Misses', value: 99},
{time: 27980, type: 'Body', value: true},
{time: 28500, type: 'Headshot', value: true},
{time: 29000, type: 'Bomb', value: true},
]
```
**Grade:**
1. **Move** – 100 if <105 mSec. 70 if >=105 mSec and <250 mSec.  0 if >=250 mSec
2. **Bomb** - 100 if <40000 mSec. Else – 0.
3. **Misses** - 100 if <60 pixels. 70 if >=60 pixels and <400 pixels.  0 if >=400 pixels
4. **Headshot** – 100 if Hit.
5. **Body hit** - 80 if Hit.

## Output:
An html page containing a graph and an accumulation score for each skill.

1. **Graphs** – Create a graph for each skill. For every measurement indicate the grade (and its measurement name) over on time. See attached image for an example output graph.

2. **Accumulation** – Each skill gets a final score, based on its accumulated measurements. Remember that each measurement type has its own weight. The accumulation of a skill is the weighted average of the different measurements. For example if the average *moves* is 64 and the average bomb is 50, Speed’s final grade could be 70% of average moves and 30% of average bomb: `64\*0.7 + 50\*0.3 = 59.8`. Feel free to define the weights value.


## Deliverables: 
1. Create a pure JS, React or Ruby based solution that takes in the array of measurements and outputs an HTML file containing the graphs and accumulated scores. Make sure to also include the weights you have used for calculating the skills. Feel free to design the graphs and add details as you see fit. You may use third party libraries.
2. **Bonus (Extra Credit):** Add tests.
3. Please keep your solution simple and readable.
4. Please do not submit your solution as a comment. Instead create a fork or a public gist.

Time Frame for the Sprint:  
Pls Deliver your work within a 7 day period.


Good luck.
We are available for questions and clarifications.

Edge Gaming Team