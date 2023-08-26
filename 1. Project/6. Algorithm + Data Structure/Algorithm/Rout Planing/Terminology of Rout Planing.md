1. agent: entity that perceives its environment and acts upon that environment
2. state: a configuration of the agent and its environment
3. initial state: the state in which the agent begins 
4. actions: choices that can be made in a state 
	- choices that can be made in a state 
5. transition model: a description of what state results from performing any applicable action in any state
	- RESULT(s, a) returns the state resulting from performing action a in state s
6. state space: the set of all states reachable from the initial state by any sequence of actions
	- a [[Graph]]
7. goal test: way to determine whether a given state is a goal state
8. path cost(weight): numerical cost associated with a given path
9. solution: a sequence of actions that leads from the initial state to a goal state
10. optimal solution: a solution that has the lowest path cost among all solutions
11. node: a data structure that keeps track of 
	- a state 
	- a parent (node that generated this node) 
	- an action (action applied to parent to get node) 
	- a path cost (from initial state to node)


- Start with a frontier that contains the initial state. 
- Repeat: 
	- If the frontier is empty, then no solution. 
	- Remove a node from the frontier. 
	- If node contains goal state, return the solution. 
	- Expand node, add resulting nodes to the frontier.