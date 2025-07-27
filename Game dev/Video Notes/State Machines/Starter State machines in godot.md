
## examples:
- when player is in range of enemy -> enemy changes into chase state, once player is out of range, return to original position 

## code based approach:
- good for simple cases where there isnt a lot of states to be tracked and taken care of
	- ex: when a turret has 3 states: scanning, firing, recharging, then loops back to firing

## node based approach:
- better organized and more convenient when dealing with larger/more complex systems

## Setup

### connecting Player to state machine

- ![[Pasted image 20250727224542.png]]

### State_Machine (the controller)

- ![[Pasted image 20250727200035.png]] this is to pass the player as the parent to all the child states

- ![[Pasted image 20250727200106.png]] this delegates the already delegated process and physics process to the child states and if they return "true" instead of null -> that signals that a state change should occur

### child state blueprint

- ![[Pasted image 20250727200229.png]] each of the processes return null to signal that a state change is not to be done along with the enter and exit functions