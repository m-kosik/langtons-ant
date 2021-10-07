## Langton's Ant
Langton's ant is a two-dimensional Turing machine invented in the late 1980s. The ant starts out on a grid of black and white cells and follows a simple set of rules that has complex emergent behavior. This repo contains a notebook which is simulating the run of a Langton's ant. 

### Game setup
Elements of the game:   
- grid: a two dimensional array of white and black cells represented by 0's (white) and 1's (black),   
- ant: wih a defined position (row, column) and direction (west - "W", east - "E", south - "S", north - "N").   

### Rules   
The ant can travel in any of the four cardinal directions at each step it takes. The ant moves according to the rules below:   
- At a white square (represented with 0), turn 90° right, flip the color of the square, and move forward one unit.   
- At a black square (represented with 1), turn 90° left, flip the color of the square, and move forward one unit.   
The grid has no limits and therefore if the ant moves outside the borders, the grid is expanded with 0s, respectively maintaining the rectangle shape.   
     
One can divide each ant's turn into four actions:   
- Change direction   
- Change color tile   
- Move to new square   
- Expand board if needed   
   
At the first iteration the ant turns accordingly to which color it stands on initially (right if on white, left if on black), then changes the tile color and, finally, moves one step forward (expanding the board if needed). Then, the next iteration begins.   
