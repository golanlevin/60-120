# Bitsy: Some Design Strategies

*Adapted/cribbed from lecture notes by Paolo Pedercini. This is his work!* 

---

## Tiles & Layouts

It’s OK to leave areas untiled. You can use negative space and the background color to communicate what areas are walkable. 

![effective_negative_space.png](bitsy_tips/effective_negative_space.png)

Especially for natural environments, make slight variations of tiles in order to break up repetition and make it look less grid-like. 

![variegated_grid.png](bitsy_tips/variegated_grid.png)

If your avatar and sprites walk on tiles of two colors, make your avatar have transparency by adding the following code:

```
BGC *
```
...right under the corresponding game data. Doing so requires a sprite color that stands out against the other two:

![avatar_with_transparency.png](bitsy_tips/avatar_with_transparency.png)


Avoid square tiles and straight edges when making non-architectural spaces.

![avoid_square_tiles.png](bitsy_tips/avoid_square_tiles.png)

![avoid_square_tiles_2.png](bitsy_tips/avoid_square_tiles_2.png)

Making tilesets is pretty much about rounding corners and creating patterns that break the grid. 

![tilesets.png](bitsy_tips/tilesets.png)

![tilesets_demo.png](bitsy_tips/tilesets_demo.png)

Modular tiles are powerful, but consider patterns that cover multiple tiles to add some variation. Like this:

![multi-tile-trees.png](bitsy_tips/multi-tile-trees.png)

versus this:

![square_trees.png](bitsy_tips/square_trees.png)

## Dithering

You only have two colors, but you can use techniques like **dithering** to add depth and gradients. 

![dithering_1.png](bitsy_tips/dithering_1.png)

![dithering_2.png](bitsy_tips/dithering_2.png)

[*Dithering*](https://en.wikipedia.org/wiki/Dither) is the problem of rendering a continuous-tone (or high bit-depth) raster image with fewer bits. There are many, many different techniques.

![dithering.png](bitsy_tips/dithering.png)

## Navigation

Try to convey exits and walkable areas without using arrows and explicit signage. You can have multiple exits that take you to the same room for more open-ended levels.

![bad-signage.png](bitsy_tips/bad-signage.png)

The classic exit-reentry problem: a door is approached by moving left; the avatar spawns in the second room to the right of the entrance; the player keeps pressing left and goes back to the first room. *Annoying and confusing*. Either maintain cinematic and spatial continuity, or spawn the player away from an exit that could cause that problem.

![bad-exits.png](bitsy_tips/bad-exits.png)

---

## Spatial Geometries

**Pure 2D** (Typography, 2D abstraction)

![bitsy_alphabet.png](bitsy_tips/bitsy_alphabet.png)


**Plan View** (Top Down: Maps, Mazes)

![realm-of-the-dead-sorceress.png](bitsy_tips/realm-of-the-dead-sorceress.png)

![bitsy_maze.gif](bitsy_tips/bitsy_maze.gif)


**Section View** (Platformers, ladders, etc)

![section_1.png](bitsy_tips/section_1.png)

![a-secret-bitsy-game-section.png](bitsy_tips/a-secret-bitsy-game-section.png)


**Landscape** (Perspective) View

![pond.png](bitsy_tips/pond.png)

![beach.png](bitsy_tips/beach.png)

Bitsy games don’t have to be top down or side view, but consider that other layouts may make the 4-direction movement and the wall collisions more awkward.

![diagonal.png](bitsy_tips/diagonal.png)

---

### But I *wanted* it to be inscrutable!

Paolo writes: *"You may be tempted to create some challenge by making the player’s progression less intuitive e.g. with hidden passages and non-obvious interactions. *Obfuscation is not puzzle design:* good puzzles are always readable. You know what you can do and what you have to do, the challenge is figuring out how."*

![inscrutable.png](bitsy_tips/inscrutable.png)

### On Defaults

Paolo writes: *"Do not under any circumstances use the default Bitsy music. Turn it off. The default music just tells the players that you don’t know what you are doing and that they should not play your thing."* Here's how to do it:

![turn_off_tune.png](bitsy_tips/turn_off_tune.png)

### The End

Unless it makes sense conceptually, you don’t want the player to wander around trapped in your game forever. Give your game a proper ending.

![the-end.png](bitsy_tips/the-end.png)

---

<!--
Recovered from: 
* [here](http://mycours.es/gamedesign2021/bitsy-2/)
* [here](https://web.archive.org/web/20230923021529/https://golancourses.net/60120/daily-notes/unit-3-interactive-narrative/design-strategies/)
* [here](https://web.archive.org/web/20230929093115/http://mycours.es/digitalmedia/bitsy/)
* [here](http://mycours.es/gamedesign2021/brainstorm-bitsy-world/)
* [here](https://ems.andrew.cmu.edu/2022f/daily-notes/unit-3-interactive-narrative/design-strategies/index.html)
-->