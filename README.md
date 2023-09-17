# Doozy_Platformer
 Overview of platformer project made during Tech Academy Live Project

 ## Summary of skills obtained
- Experience with Unreal Engine:
  1) Using blueprints scripring; 
  2) Using landscape and modelling modes;
  3) Using animations and materials;
  4) Using VFX effects and lightning;
  5) Implementing HUD widgets;
  6) Using game instance.
- Better understanding of common project management concepts as Agile. including Daily StandUps, code retrospective and planning of future tasks.
- Better understanding principles of working with source control  systems.

## Initial assets
Tech Academy provided me initial pack of assets, which included: various meshes for level design, several blueprints with gameplay elements such as buttons and moving platforms, different VFX effects and materials. This assets significantly helped me with level design part of the project.

Pressing a button, which activates moving platform:

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExam9zcDBqMWM2cGFiY2Y5NDg1OG0xczdyOWU4cXFvcTc5ZWU1eDYyNiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/WvPXQF3EsrPzVtWeir/giphy.gif)

Using a fan:

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExaTR6ZjhncjFyemNraGNsOXN5M2F5MWJucnZtZTdwbmwwODdqcHRseiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/rmJTeiH01qr3w7Okg5/giphy.gif)

## Level Design
I started building my level with landscape mode, which provides powerfull tools for creating landscape. After creation of my landscape, I built demo version of my level using a modelling tools, especially CubeGrid.

Overview of created level

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdWo2ODk4Ym9vbzZpangzMmFqcjB2eXV2ZjhsY3hpb2hjZXJmZzRnNyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/thwG9fnzxqj2y9ss1f/giphy-downsized-large.gif)

## Creating character
I decide not to use built-in character provided by Tech Academy and created my own one with custom animations which I took from Mixamo.com website. I created my own character blueprints for spawning and damaging a character (howewer blueprint for character movement I copied from 3rd Person Character blueprint). 

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExaWg2M3hhMzIyazZmcGI5b2d3cnIxYmZjcDFlMHczcTVxbWg3NHk3NyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/oEKYnkH3d7OJHCuR6C/giphy-downsized-large.gif)

## Collectables
In my game I created 3 different types of collectables:
- Coins. Picking up a coin increase a score counter of the character;
- Extra life. Picking up an extra life gives character extra life (additional heart in upper left corner);
- End Goal. Picking up an end goal finishes a level and shows Win Widget, where player can choose to go to the next level, restart current or navigate into main menu.


![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZmtmMGVtMXRhY3FieGd4bzI5b2ZqeTUwMW1lN2JmNGozOWlldGZhOCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/RvDuraarRdyadJhKCV/giphy.gif)



## Health and Respawn Systems
I created my own health system: initially character got 3 lifes and he can loose a hearts by falling with particular velocity or overlapping lava material. 
Also character can pickup extra lifes in the form of hearts hidden in different locations.
If character looses a heart - he respawns on his latest spawn location. If character got no hearts left - Death Screen widget is showing and player can restart the game.


Picking up an extra life:

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExamNjanBzaDFyb281d3V0Y3p0bXhmaHFsMmhiOWpxeWNldXB6ZG5lciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/xnTZVDYPUog0F1jpal/giphy.gif)


Character falls, looses a life and respawns:

![](https://media.giphy.com/media/hwl0VcJEPl51ew9XBy/giphy-downsized.gif)

Character overlaps lava, looses a life and respawns:

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbDdvNDN6c3cyb2d1Z2J4dDFhenBzdnljbnZndjh5d3BtcWtzaWhqYSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/WTx4ConNEIO3etCWvt/giphy.gif)


## Collisions
In my game I created different collision mechanic:
1) Character with collectables;
2) Crate collision: crate can be respawned, if it collides with PainCausingVolume (placed in certain areas of map), stompers or lava material.
3) Collision with spawning pad: spawning pad is activating, character spawn location is updated to a new one.


Crate is destroyed by collision with stompers (it is destroying only after 1.5 sec of such collision):

![](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExMWp3M3ZjMHZndmFvOGU0OWJkYTh0cWFibWhqZ2ZteXJ2NXMxdnNkdSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/K89EtACtq2uoJPEzi3/giphy.gif)


## Blueprints
Most of blueprints I created for this project are availiable to check at https://github.com/Kypok1995/Doozy_Platformer/tree/main/Blueprints with comments about logic behind these blueprints. 









