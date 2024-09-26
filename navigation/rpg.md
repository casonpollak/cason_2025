---
layout: base
title: RPG
permalink: /rpg/
---

<canvas id='gameCanvas'></canvas>

<script type="module">
    import GameControl from '{{site.baseurl}}/assets/js/rpg/GameControl.js';

    // Import the audio file
    const backgroundMusic = new Audio('{{site.baseurl}}/assets/rpg/audio/minecraftbg.mp3');
    backgroundMusic.loop = true;  // Set to loop

    // Background data
    const image_src = "{{site.baseurl}}/images/rpg/pixel background.jpg";
    const image_data = {
        pixels: {height: 1080, width: 1920}
    };
    const image = {src: image_src, data: image_data};

    // Sprite data
    const sprite_src = "{{site.baseurl}}/images/rpg/green character.png";
    const sprite_data = {
        SCALE_FACTOR: 10,
        STEP_FACTOR: 1000,
        ANIMATION_RATE: 50,
        pixels: {height: 72, width: 48},
        orientation: {rows: 4, columns: 3},
        down: {row: 0, start: 0, columns: 3},
        left: {row: 2, start: 0, columns: 3},
        right: {row: 3, start: 0, columns: 3},
        up: {row: 1, start: 0, columns: 3},
    };
    const sprite = {src: sprite_src, data: sprite_data};

    // Assets for game
    const assets = {image: image, sprite: sprite};

    // Start game engine
    GameControl.start(assets);

    // Start the background music when the game starts
    backgroundMusic.play();


</script>

