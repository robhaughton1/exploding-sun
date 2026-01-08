# Exploding Sun Animation

## Overview
This project is a JavaScript animation built in the ProcessingJS environment. The challenge provided only a starting variable; the full animation logic — including the `draw()` function, scene rendering, and conditional growth control, all written by me.

The goal was to animate a sun rising on the horizon and expanding over time. I also chose to add a stopping condition to prevent the sun from growing indefinitely. This behavior was **not required** by the challenge and represents my own extension of the project.

## Features
- Custom `draw()` function written from scratch  
- Frame-based animation using ProcessingJS  
- Dynamic scaling of the sun using a size variable  
- Conditional logic to stop the animation at a chosen maximum size  
- Layered scene with sky, sun, and land  

## Code Snippet
```javascript
// the starting size for the sun
var sunSize = 30; 

draw = function() {
    noStroke();

    // the beautiful blue sky
    background(82, 222, 240);

    // The sun, a little circle on the horizon
    fill(255, 204, 0);
    ellipse(200, 298, sunSize, sunSize);

    // The land, blocking half of the sun
    fill(76, 168, 67);
    rect(0, 300, 400, 100);

    // I wrote this conditional to stop the sun's growth.
    // This was not required by the original challenge.
    if (sunSize < 300) {
        sunSize = sunSize + 1;
    }
};
Exploding Sun Animation
Overview
This project is a small JavaScript animation built in the ProcessingJS environment as part of a Khan Academy challenge. The starter code provided the basic scene structure, but the animation behavior and growth‑control logic were implemented by me.

The goal was to animate a sun rising on the horizon and expanding over time. I added a conditional stopping point to prevent the sun from growing indefinitely, even though this behavior was not required by the challenge.

Features
Frame‑based animation using the draw() loop

Dynamic scaling of the sun using a size variable

Conditional logic to stop the animation at a chosen maximum size

Layered scene with sky, sun, and land

Code Snippet
javascript
// the starting size for the sun
var sunSize = 30; 

draw = function() {
    noStroke();

    // the beautiful blue sky
    background(82, 222, 240);

    // The sun, a little circle on the horizon
    fill(255, 204, 0);
    ellipse(200, 298, sunSize, sunSize);

    // The land, blocking half of the sun
    fill(76, 168, 67);
    rect(0, 300, 400, 100);

    // I added this conditional to stop the sun's growth.
    // This was not required by the original challenge.
    if (sunSize < 300) {
        sunSize = sunSize + 1;
    }
};
