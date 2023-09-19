# Doozy_Platformer
 Overview of platformer project made during Tech Academy Live Project

 ## Summary of skills obtained
- Experience with Unreal Engine:
  1) Use of blueprints scripring; 
  2) Use of landscape and modelling modes;
  3) Use of animations and materials;
  4) Using VFX and lighting effects;
  5) Implementation of HUD widgets;
  6) Using game instance.
- Better understanding of general project management concepts such as Agile, including daily stand-ups, code retrospectives, and planning for future tasks.
- Better understanding of the principles of working with version control systems.

## Initial assets
Tech Academy provided me with an initial resource pack that included: various meshes for level design, several blueprints of gameplay elements such as buttons and moving platforms, various visual effects and materials. These resources helped me a lot in terms of level design for the project.

Pressing the button that activates the moving platform:

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExam9zcDBqMWM2cGFiY2Y5NDg1OG0xczdyOWU4cXFvcTc5ZWU1eDYyNiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/WvPXQF3EsrPzVtWeir/giphy.gif)

Fan usage:

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExaTR6ZjhncjFyemNraGNsOXN5M2F5MWJucnZtZTdwbmwwODdqcHRseiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/rmJTeiH01qr3w7Okg5/giphy.gif)

## Level Design
I started creating my level using landscape mode, which provides powerful terrain creation tools. After creating the terrain, I created a demo of my level using modeling tools, especially CubeGrid.

Overview of the created level

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdWo2ODk4Ym9vbzZpangzMmFqcjB2eXV2ZjhsY3hpb2hjZXJmZzRnNyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/thwG9fnzxqj2y9ss1f/giphy-downsized-large.gif)

## Creating character
I decided not to use the built-in character provided by Tech Academy and created my own with custom animations that I took from Mixamo.com.  I created my own character blueprints for character spawn and damage (however, I copied the character movement blueprint from the third person character blueprint).

![](https://media.giphy.com/media/oEKYnkH3d7OJHCuR6C/giphy-downsized.gif)

## Collectables
In my game I created 3 different types of collectibles:
- Coins. By picking up a coin, you increase the character's point meter;
- Extra life. Gaining an extra life gives the character an extra heart in the top left corner;
- Final goal. Picking up the final goal ends the level and displays a Win widget where the player can advance to the next level, restart the current one, or go to the main menu.


![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZmtmMGVtMXRhY3FieGd4bzI5b2ZqeTUwMW1lN2JmNGozOWlldGZhOCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/RvDuraarRdyadJhKCV/giphy.gif)



## Health and Respawn Systems
I created my own health system: the character initially has 3 lives and can lose a heart by falling at a certain velocity or by collision with lava material.
The character can also pick up extra lives in the form of hearts hidden in different locations.
If a character loses a heart, he is respawned at his last spawn location. If the character has no hearts left, the Death Screen widget is displayed and the player can restart the game.


Picking up an extra life:

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExamNjanBzaDFyb281d3V0Y3p0bXhmaHFsMmhiOWpxeWNldXB6ZG5lciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/xnTZVDYPUog0F1jpal/giphy.gif)


Character falls, looses a life and respawns:

![](https://media.giphy.com/media/hwl0VcJEPl51ew9XBy/giphy-downsized.gif)

Character overlaps lava, loses a life and respawns:

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbDdvNDN6c3cyb2d1Z2J4dDFhenBzdnljbnZndjh5d3BtcWtzaWhqYSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/WTx4ConNEIO3etCWvt/giphy.gif)


## Collisions
In my game I created different collision mechanic:
1) Character with collectibles;
2) Crate Collision: A crate can respawn if it collides with PainCausingVolume (placed in certain areas of the map), stompers, or lava material. This mechanic was implemented in order to give player endless amunt of tries for the sections of level, where crate can fall down and block further passage of the level.
3) Collision with spawning pad: spawning pad is activating, character spawn location is updated to a new one.
4) Collision with pressure plate: it can be a trigger for activating another game elements.


The box is destroyed when colliding with stompers (destroyed only after 1.5 seconds of such a collision):

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExMWp3M3ZjMHZndmFvOGU0OWJkYTh0cWFibWhqZ2ZteXJ2NXMxdnNkdSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/K89EtACtq2uoJPEzi3/giphy.gif)


Crate collides with pressure plate and opens a door:

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExc3VuMGNleDJsYnBwYzM4a3hxdDNmcm9sNnBrb3IyZDhzYXFqd3NheCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/4VI6QvmYG6zZVbYJC0/giphy.gif)


## Blueprints
Most of the blueprints I created for this project are available for review at https://github.com/Kypok1995/Doozy_Platformer/tree/main/Blueprints with comments about the logic of these blueprints.









