---
layout: post
title: Hacks
permalink: /hacks/
---

{% include nav/home.html %}

 <div>

 <p style="color: white; font-size: 1.5em; padding: 10px;">
 <strong> Variable Naming Convention Hack </strong> </p>
 
  <p style="font-size: 1em; padding: 10px;"> <ul> camelCase is commonly used in programming for variables, functions, and object properties, especially in languages like JavaScript and Java.


 UPPER_CASE snake_case is typically used for constants in many programming languages, such as Python and C.


 PascalCase is often used for class names and constructors in object-oriented languages, like C# and Java.
 </p>
</div>


## RPG Project Hack

### Original code (in snake_case)

```js
import GameControl from '{{site.baseurl}}/assets/js/rpg/GameControl.js';

// Background data
const image_src = "{{site.baseurl}}/images/rpg/water.png";
const image_data = {
    pixels: {height: 580, width: 1038}
};
const image = {src: image_src, data: image_data};

// Sprite data
const sprite_src = "{{site.baseurl}}/images/rpg/turtle.png";
const sprite_data = {
    SCALE_FACTOR: 10,
    STEP_FACTOR: 1000,
    ANIMATION_RATE: 50,
    pixels: {height: 280, width: 256},
    orientation: {rows: 4, columns: 3 },
    down: {row: 0, start: 0, columns: 3 },
    left: {row: 1, start: 0, columns: 3 },
    right: {row: 2, start: 0, columns: 3 },
    up: {row: 3, start: 0, columns: 3 },
};
const sprite = {src: sprite_src, data: sprite_data};

// Assets for game
const assets = {image: image, sprite: sprite}

// Start game engine
GameControl.start(assets);
```
## Fixed code (in camelCase)

```js
import gameControl from '{{site.baseurl}}/assets/js/rpg/GameControl.js';

// Background data
const imageSrc = "{{site.baseurl}}/images/rpg/water.png";
const imageData = {
    pixels: {height: 580, width: 1038}
};
const image = {src: image_src, data: image_data};

// Sprite data
const spriteSrc = "{{site.baseurl}}/images/rpg/turtle.png";
const spriteData = {
    scaleFactor: 10,
    stepFactor: 1000,
    animationRate: 50,
    pixels: {height: 280, width: 256},
    orientation: {rows: 4, columns: 3 },
    down: {row: 0, start: 0, columns: 3 },
    left: {row: 1, start: 0, columns: 3 },
    right: {row: 2, start: 0, columns: 3 },
    up: {row: 3, start: 0, columns: 3 },
};
const sprite = {src: spriteSrc, data: spriteData};

// Assets for game
const assets = {image: image, sprite: sprite}

// Start game engine
gameControl.start(assets);
```
</div>


### Things that I changed
- I changed many variables from snake_case and UPPER_CASE into camelCase