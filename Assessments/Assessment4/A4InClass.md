# Calculator

## Problem One
###Statement:

A calculator company produces a scientific calculator and a graphing calculator. Long-term projections indicate an expected demand of at least 100 scientific and 80 graphing calculators each day. Because of limitations on production capacity, no more than 200 scientific and 170 graphing calculators can be made daily. To satisfy a shipping contract, a total of at least 200 calculators must be shipped each day.
If each scientific calculator sold results in a $2 loss, but each graphing calculator produces a $5 profit, how many of each type should be made daily to maximize net profits?

### Goal: Maximize profit.
We analyzed your current inventory and client engagements as a linear program to determine the optimal way to maximize profit through producing a certain amount of each calculator type. We denote the number of scientific calculators as S, the number of graphing and the calculators as G.

Max: 5G - 2S
subject to:
  S >= 100
  G >= 80
  G + S >= 200
  S <= 200
  G <= 170


### Optimal Amount of Calculators


## Problem 2
### Statement:
You need to buy some filing cabinets. You know that Cabinet X costs $10 per unit, requires six square feet of floor space, and holds eight cubic feet of files. Cabinet Y costs $20 per unit, requires eight square feet of floor space, and holds twelve cubic feet of files. You have been given $140 for this purchase, though you don't have to spend that much. The office has room for no more than 72 square feet of cabinets. How many of which model should you buy, in order to maximize storage volume?

### Introduction:
We analyzed the requirements to optimize the storage volume in your office as a linear program. Cx designates the number of filing cabinets of cabinets x, while Cy represents the number of cabinets of type Y that will be able to fit in your space given your finiacial standing.
Max: 8Cx + 12Cy
subject to:
10Cx + 20Cy <= 140
6Cx + 8Cy <= 72

After analyzing the problem our suggestions and findings are found below.

### Optimal Space Usage:
We recommend that you purchase eight cabinets of type X and 3 cabinets of type Y. This will consume your current budget of 140$ completely and you will also use up all 72 square feet of space available. You will gain 100 cubic feet of storage volume. The limiting factors in our analysis are both budget and available space. If you want to see an increase in the amount of storage space you would have to increase both of the variable amounts.

### Post Hoc analysis:
The shadow price for the budget is an increase in purchasable storage space by 1/5 of a square foot for every dollar added to the budget.  
It is 
