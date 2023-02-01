## Activity 5

### Name:

### Description

Assume the following state space:

- edge('A', 'B')
- edge('A', 'I')
- edge('I', 'G')
- edge('I', 'C')
- edge('C', 'F')
- edge('G', 'F')
- edge('C', 'D')
- edge('C', 'E')
- edge('E', 'H')
- edge('G', 'H')

Assume the start state is 'A' and the goal state is 'H'

### Solution

TODO: Run the DFS, BFS algorithms. Indicate the path your algorithm generated from start to goal. Indicate which node was expanded and what is in the fringe at each step. If there is no path, state so, while still showing the steps of your algorithm.

| Expand Node | Fringe |
| ------------|------- |
|             |        |
|             |        |
|             |        |
|             |        |
|             |        |
            
            
**Path:** ... => ... => etc.

### Sample Solution

#### DFS

|Expand Node 	| Fringe |
| ------------|------- |
|A 	|B,I|
|B 	| I |
|I  |	C,G|
|C 	| G,D,E,F|
|G  |	D,E, F,H|
| D      |       E,F,H|
| F       |      G,H|
| E     |        H|

Path: ... => ... => etc. A -> i -> G -> H A-> I -> C -> E -> H


#### BFS

Expand Node |	Fringe
------------|------- 
- |	A
A |	B,I
B |	I
I |	G,C
G | 	C
C |	F, H
F |	H
H |	End

Path: A => I => G => H.



#### Iterative Deepening Search

Depth Limit 1

Expand Node  |	Fringe
------------|------- 
A  |	B I
B  |	N/A
I  |	G C

Depth Limit 2

Expand Node 	Fringe
------------|------- 
A |	B I
B |	N/A
I |	G C
G| 	F H

Depth Limit 3
Expand Node |	Fringe
------------|------- 
A 	|B I
B 	|N/A
I 	|G C
G 	|F H
F 	|N/A
H 	|SOLUTION

Path: A => I => G => H