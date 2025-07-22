- vector 2 and vector 3 can be used to set 2d and 3d positions respectively

- adding "@export" before a var allows it to be adjusted in the editor

- for n in 8 -> n starts at 0 and ends in 7

## dictionary
- sample usage of a dictionary:
	-  players = {"mk": 1, "jimmy": 2}
	- print("mk") produces 1

	- for username in players: print(username + ": " + str(players[username]) )

## enums
- can be used to assign states

example: enum Alignment {ALLY, NEUTRAL, ENEMY}

var player1_alignment = Alingment.ALLY

- can also be used with exported variables -> @export var player1_alignment :  Alignment (the colon is to set it's type) -> now we get a drop down menu in the editor with the 3 alignments available

## match
- basically a switch statement

- example is:
	- match player1_alignment:
		- Alignment.NEUTRAL:
			- do smth
		- Alignment.ALLY:
			- do smth
		- "underscore then colon" is the default action if none of the cases are met

## modifying nodes 2.0

- the $ is short hand for get_node("node/path")

- can make a var with type node (var ex : Node) and export it and drag and drop nodes in it
- and can use that to check for node type

## signals
- they are useful for decoupling (pushing changes/executing functions without being integrated with the button/trigger of that)

- example is a player leveling up -> need to update stats and UI and Unlocks
- updating all of that from the player script can get messy/crowded so -> we create a level up signal and use it to activate functions in the stuff we need to update independantly off the player
![[Pasted image 20250722040218.png]]

![[Pasted image 20250722040314.png]]
can also connect the signal through code and not through the editor

## get/set

- getters and Setters are used to add code to when a variable is changed
- for example, clamping the value of a variable in a range when an attempt to CHANGE the a:
![[Pasted image 20250722040558.png]]