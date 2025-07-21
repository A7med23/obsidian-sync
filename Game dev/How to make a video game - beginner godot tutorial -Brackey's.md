- everything in godot is based on nodes (more on that after watching lukky's nodes video)

- scenes are used to make modular parts and collections of nodes and then combined (nested) together to make the game bigger and bigger -> example of that here is the player scene, platform scene, and coin scene -> then all are placed inside the grand "level 1" scene

# steps:

## Make game scene
- add player scene and camera node to it

## make player scene
- needs to have collision and animated sprite
- and add first basic controls script

## worldbuilding
### tile map layers node
- use erase tool and shift + click to reshape the tiles auto generated in the atlas as needed

# platforms

# pickups
- use area2d node to interact and not collide with the object
- use signals to detect and use functionality
- using physics layers fix the issue of the coin detecting any body that passes through it -> put the player on a different physics layer and use mask to make sure the coin only detects that physics layer (another solution is to use code to detect which object collided with the coin

# Dying 1.0

## limiting camera
- use ruler tool to find out the pixel range

## detecting entering dangerous area and restarting the game
- using a area2d node (naming it killzone) 
- **Do not give the node a collision shape in it's scene**, add the collision shape seperatly whenever it's added somewhere as you may need to change its shape for different objects

- use a timer to delay the respawning 

- to reference a node in your code just drag it and hold control while releasing

- use timer "timeout" function to do smth once the time is up

# Enemy

## animation

## movement and ray casting to detect when to change direction

# Dying 2.0

## slow motion effect
- done by changing the engine's timescale then reverting back to normal after respawning

## removing the player's collider after hitting the enemy to make them fall off the map

- use the body parameter thats passed into the collision -> it detects the player and can be used as a reference
- another way is to just reference the player directly

# Player 2.0
## adding run and jump animation

## pointing player in direction of movement

## making custom inputs for movement

# Text
- add labels and change their font and font size (in increments of 8)

# Score
## common practice to place gamewide variables in game manager
- make it a regular node not a node2D

# Audio

## music
- make the audio stream player a scene on it's own and then set it as an autoload scene (scenes that play globally persistent throughout the entire game regardless of what scene is loaded)

## coin pickup

### a timing issue
where the coin is killed the second it's picked up, which causes an issue where teh sound wont have a chance to fully play. a solution is making the object disappear in an animation and the sound play in that animation

- **you can call function in the animation player**

the use of that here is to call the queue free function at the end of the animation