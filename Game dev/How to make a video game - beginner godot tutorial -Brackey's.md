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