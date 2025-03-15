
# Directional-Avatar Hack

![directional-avatar.gif](directional-avatar.gif)

*We will install a hack that allows you to make an avatar that flips direction, depending on which way the user is moving. It works by flipping the pixels of your avatar design, on-the-fly (so you don't need to design left-facing and right-facing avatars).*

---

## WARNING

Once you add this hack to your game, you'll lose this work if you try uploading the modified game back into the online editor. You should either: 

* Add this hack as the **last thing you do**, once your game is finished, **OR**
* Edit your game thereafter using an offline Bitsy editor such as [Borksy](https://ayolland.itch.io/borksy) or [Bitsy Savior](https://aloelazoe.itch.io/bitsy-savior). *Your mileage may vary!!!*

---

## Installation Steps

* **Make sure** your game has a directionally oriented avatar. By default, your character should be pointing to the *right*. I gave my avatar a nose and toes. 
* **Save** your game HTML to your computer.
* **Open** the game HTML file with a text editor. 
* In the text editor with the game HTML file open, **scroll** down to the bottom. You'll see a line of HTML which says `</script>` (i.e. the end of a script) right before another tag that says `<head>`.
* After the `</script>` tag, and before the `</head>`, **paste** the following lines. You are adding a pair of "begin-script" and "end-script" HTML tags:

```

<script>

</script>


```

* **Go** to the GitHub repository for the [directional-avatar.js hack](https://github.com/seleb/bitsy-hacks/blob/main/dist/directional-avatar.js).
* **Copy** all of the hack code from the GitHub code frame, starting from line 1, all the way down to the last line of code (e.g. 396).
* **Paste** the hack code *in between* the `<script>` and `</script>` tags that you just added.
* By default, this hack has `horizontalFlipAllowed: true`, but you can change this if you want. The hack also allows you to change the default value `verticalFlipAllowed: false`. You can **search** for this code if you want to modify it. 

---

## Example

You can study a working example in [this minimal game](directional-avatar-game.html). The hack begins at line 11960, and ends at line 12357 in the game's HTML file.




