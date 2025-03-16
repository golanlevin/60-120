
# Opaque Tiles In Bitsy

*We will enable opaque tiles in Bitsy using the [opaque-tiles](https://github.com/seleb/bitsy-hacks/blob/main/dist/opaque-tiles.js) hack. Known to work for Bitsy 8.13.*

---

## Warning

Once you add this hack to your game, you'll lose this work if you upload the game back into the online editor. 

---

## Installation Steps

* **Create** a game. **Make** a tile-type whose name is (for example) `opaque`. **Make** a room that uses some of those tiles. 
* **Download** the HTML file of your room, and **open** this HTML file in a text editor. 
* Near the very end of the file, just before the `</head>` tag, **add** the following HTML tags, which indicate that we are adding another script: 

```

<script>

</script>


```

* **Copy** the code of the [opaque-tiles hack](https://github.com/seleb/bitsy-hacks/blob/main/dist/opaque-tiles.js). It's about 268 lines of code. 
* **Paste** the opaque-tiles code in-between the `<script>` and `</script>` tags that you just added. 
* **Update** the `tileIsOpaque` function below to match your needs, by commenting/uncommenting and editing the code. You have four suggested options (*use only one!*):
  1. `return tile.name == 'opaque';` <br/>*Tiles which have the typename `opaque` (or whatever name you choose) will be opaque.* 
  2. `return ['wall', 'column', 'door'].indexOf(tile.name) !== -1;` <br/>*You can provide a specific list of opaque tile types*
  3. `return tile.name && tile.name.indexOf('opaque') !== -1;` <br />Tiles whose names include the word `opaque` (such as `opaqueDoor`) will be opaque. 
  4. `return true;` <br/>*All tiles will be opaque!*
* For example, my `hackOptions` function looks like this: 

```
var hackOptions = {
	tileIsOpaque: function (tile) {
		return tile.name == 'obstacle'; // specific opaque tile
	},
};

```


---

## Example

* You can study a working example in [this minimal game](opaque_tile_game.html). 
* This game is silent in room 0, plays wind sounds in room 1, and river sounds in room 2. 
* [**Live version**](https://raw.githack.com/golanlevin/60-120/main/2025/lectures/interactive_narrative/bitsy_hacks/opaque_tile/opaque_tile_game.html)


