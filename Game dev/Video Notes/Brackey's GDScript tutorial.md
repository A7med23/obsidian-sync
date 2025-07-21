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

- can also be used with exported variables -> @export var player1_alignment :  Alignment (the colon is to set it's type) -> now we get a drop down menu in the di