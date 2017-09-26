# Codurance Katacombs

Inspired by [Colossal Cave Adventure](https://en.wikipedia.org/wiki/Colossal_Cave_Adventure) this is a kata idea for building a text adventure game which can be expanded *incrementally* and *indefinetly* limited only by imagination.

The game is based on a console application describing a fictional underground world to be explored by the player via a set of commands.
The world is a collection of environments connected to eachother via specific connection points (doors, passages, gates, stairs, etc). Each environment is divided in locations and the player can move among them using cardinal points for directions. 
It is possible to just look in every directions, but not all the directions are always available for being looked at, nor to move to. 

When looking somewhere without anything interesting the system should reply ***"Nothing interesting to look at there!"***. 
When a general action is not available the system will reply ***"I can't do that here!"***.
When the system can't understand the command it should prompt ***"I don't understand that. English please!"***.

#### *Startup*

The game at startup describe the **main description** of the initial location. When the player moves to another location, the system will always prompt the main description for that location.

    YOU ARE STANDING AT THE END OF BRICK LANE BEFORE A SMALL BRICK BUILDING CALLED THE OLD TRUMAN BREWERY. 
    AROUND YOU IS A FOREST OF INDIAN RESTAURNTS.  A SMALL STREAM OF CRAFTED BEER FLOWS OUT OF THE BUILDING AND DOWN A GULLY.
    >
    
 
 #### Exploring the world 
 
  * #### *Moving* 
     **GO** followed by the letter of the cardinal point
    ```
    > GO N => move to the NORTH
    > GO E => move to the EAST
    > GO S => move to the SOUTH
    > GO W => move to the WEST
    ```
    
  * #### *Looking*
    **LOOK** allows to look in every direction to have an idea of the surrounding environment. 
    ```
    YOU ARE STANDING AT THE END OF A ROAD BEFORE A SMALL BRICK BUILDING. 
    AROUND YOU IS A FOREST.  A SMALL STREAM FLOWS OUT OF THE BUILDING AND DOWN A GULLY.
    > LOOK N
    I CAN SEE A SMALL BRICK BUILDING WITH A WOODEN WHITE DOOR
    ```
 
    ```
   
  #### Changing environment
Passing from an environment to another is done by opening doors, gates, passages. 

 * #### *Opening*
    **OPEN** allows to look in every direction to have an idea of the surrounding environment. 
    ```
    YOU ARE STANDING AT THE END OF A ROAD BEFORE A SMALL BRICK BUILDING. 
    AROUND YOU IS A FOREST.  A SMALL STREAM FLOWS OUT OF THE BUILDING AND DOWN A GULLY.
    > LOOK N
    I CAN SEE A SMALL BRICK BUILDING WITH A WOODEN WHITE DOOR
