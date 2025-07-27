
## examples:
- when player is in range of enemy -> enemy changes into chase state, once player is out of range, return to original position 

## code based approach:
- good for simple cases where there isnt a lot of states to be tracked and taken care of
	- ex: when a turret has 3 states: scanning, firing, recharging, then loops back to firing

## node based approach:
- better organized and more convenient when dealing with larger/more complex systems