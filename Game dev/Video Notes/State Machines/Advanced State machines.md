
# Dependency injection 

supplying dependencies at runtime instead of hard coding them 

ex: state needs *a player* and not a *specific* instance of a player

# hierarchical state machines
- inheriting and overriding the base code to achieve a certain functionality
- in this example it is a dash state:![[Pasted image 20250808210045.png]]

# managing multiple things at once
![[Pasted image 20250808210324.png]]

this is an example of when you want to track shooting AND movement at the same time and not having to make a state for every possible permutation of action. -> you simply make 2 different state machines and pipe the events from the parent to both state machines

this is known a concurrent state machine

there is a time when youll need to share data between the states (even though we want to keep them independent of one another) like when you cant jump when charging a big attack or you cant charge a big attack when jumping so

# how to share data between states

ways of doing that include:

- lift data up the heirarchy
	- for example player stamina or cooldown are saved in the player node itself
	  
- create a data store that used by a data store to read write and share data
	- can range from a simple dictionary on the managing state machine to a separate component with its own custom logic etc
	  
- return an object when switching between states that has the target state and any data it needs to be aware of