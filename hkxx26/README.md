<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [ShootingParticles][1]
    -   [Parameters][2]
    -   [keyPressed][3]
    -   [clearParticles][4]
    -   [draw][5]
    -   [createToolbar][6]
    -   [positionToolbar][7]
    -   [createText][8]
    -   [changeGravity][9]
    -   [changeRandomise][10]
    -   [setVariables][11]
    -   [createParticle][12]
    -   [gravity][13]
        -   [Parameters][14]
    -   [gravity][15]
    -   [randomise][16]
        -   [Parameters][17]
    -   [randomise][18]
    -   [viscosity][19]
        -   [Parameters][20]
    -   [viscosity][21]
    -   [particleColor][22]
        -   [Parameters][23]
    -   [particleColor][24]
    -   [maximumParticles][25]
        -   [Parameters][26]
    -   [maximumParticles][27]
    -   [particles][28]
        -   [Parameters][29]
    -   [particles][30]
-   [Particle][31]
    -   [Parameters][32]
    -   [move][33]
    -   [display][34]
    -   [handleInteractions][35]
    -   [xPos][36]
        -   [Parameters][37]
    -   [xPos][38]
    -   [yPos][39]
        -   [Parameters][40]
    -   [yPos][41]
    -   [xVel][42]
        -   [Parameters][43]
    -   [xVel][44]
    -   [yVel][45]
        -   [Parameters][46]
    -   [yVel][47]
    -   [mass][48]
        -   [Parameters][49]
    -   [mass][50]
    -   [color][51]
        -   [Parameters][52]
    -   [color][53]

## ShootingParticles

A class that encompasses the toolbar, canvas including the draw-space.

### Parameters

-   `initGravity` **[boolean][54]** The initial boolean value for the gravity feature. (optional, default `true`)
-   `initRandomise` **[boolean][54]** The initial boolean value for the randomise feature. (optional, default `false`)
-   `initViscosity` **[number][55]** The initial value for the viscosity. (optional, default `0`)
-   `initParticleColor` **[string][56]** The initial particle colour. (optional, default `'white'`)
-   `initMaximumParticles` **[number][55]** The maximum amount of particles allowed in the space at one time. (optional, default `200`)

### keyPressed

Checks to see if the C key is pressed for clearing the particles.

### clearParticles

Clears all particles

### draw

The draw function for the ShootingParticles.

### createToolbar

Creates the toolbar which includes: the three sliders (colour, viscosity and size) and the two toggle buttons (gravity and randomise).

### positionToolbar

Positions the toolbar in respect to the current window size. Used when the toolbar is initially setup and when the window is re-sized.

### createText

Draws the toolbar text onto the screen.

### changeGravity

The function that is called when the gravity button is toggled. Sets the gravity variable to true when false and vice versa. Also changes the gravity button colour when toggled.

### changeRandomise

The function that is called when the randomise button is toggled. Sets the randomise variable to true when false and vice versa. Also changes the randomise button colour when toggled.

### setVariables

This is called from the draw function to set each of the colour, size & viscosity variables depending on the value on the sliders. If randomise is set to true the value of the colour & size slider is incremented.

### createParticle

Creates a new particle. Called when the mouse is pressed or dragged. A new particle is created as long as the cursor is outside of the toolbar. Also deletes the oldest particle if the particle limit is reached.

### gravity

Sets the gravity property.

#### Parameters

-   `newGravity` **[boolean][54]** The boolean variable to set the gravity on or off.

Returns **any** nothing

### gravity

Gets the boolean value of the gravity property.

Returns **[boolean][54]** this.\_gravity - Returns the boolean value of the gravity property.

### randomise

Sets the randomise property.

#### Parameters

-   `newRandomise` **[boolean][54]** The boolean variable to set the randomise on or off.

Returns **any** nothing

### randomise

Gets the boolean value of the randomise property.

Returns **[boolean][54]** this.\_randomise - Returns the boolean value of the randomise property.

### viscosity

Sets the viscosity property.

#### Parameters

-   `newViscosity` **[number][55]** The number variable to set the value of the viscosity.

Returns **any** nothing

### viscosity

Gets the number value of the viscosity property.

Returns **[number][55]** this.\_gravity - Returns the number value of the viscosity property.

### particleColor

Sets the particle colour property.

#### Parameters

-   `newParticleColor` **[string][56]** The string variable to set the active colour to be displayed.

Returns **any** nothing

### particleColor

Gets the string value of the particle colour property.

Returns **[string][56]** this.\_particleColor - Returns the string value of the particle colour property.

### maximumParticles

Sets the maximum particles property.

#### Parameters

-   `newMaximumParticles` **[number][55]** The number variable to set the maximum number of particles active on the canvas.

Returns **any** nothing

### maximumParticles

Gets the number value of the maximum particles property.

Returns **[number][55]** this.\_maximumParticles - Returns the number value of the maximum particles property.

### particles

Sets the particles list property.

#### Parameters

-   `newParticles` **[array][57]** The array that contains all the particle classes active on the board.

Returns **any** nothing

### particles

Gets the array of the particles property.

Returns **[array][57]** this.\_particles - Returns the array of the particles property.

## Particle

A class that represents the Particle component.

### Parameters

-   `x` **[number][55]** The initial x co-ordinate for the particle. (optional, default `0`)
-   `y` **[number][55]** The initial y co-ordinate for the particle. (optional, default `0`)
-   `velX` **[number][55]** The initial velocity with respect to the x-axis for the particle. (optional, default `random(-.1,.1)`)
-   `velY` **[number][55]** The initial velocity with respect to the y-axis for the particle. (optional, default `random(-.1,.1)`)

### move

Moves the particle depending on it's current position and velocities.

### display

Draws the particle onto the canvas.

### handleInteractions

Updates the particle velocity depending on the distance to the other particles and if it is in close proximity to the mouse.

### xPos

Sets the x position property.

#### Parameters

-   `newXPos` **[number][55]** The number variable to set the value of the x position.

Returns **any** nothing

### xPos

Gets the number value of the x position property.

Returns **[number][55]** this.\_xPos - Returns the number value of the x position property.

### yPos

Sets the y position property.

#### Parameters

-   `newYPos` **[number][55]** The number variable to set the value of the y position.

Returns **any** nothing

### yPos

Gets the number value of the y position property.

Returns **[number][55]** this.\_yPos - Returns the number value of the y position property.

### xVel

Sets the x velocity property.

#### Parameters

-   `newXVel` **[number][55]** The number variable to set the value of the x velocity.

Returns **any** nothing

### xVel

Gets the number value of the x velocity property.

Returns **[number][55]** this.\_xVel - Returns the number value of the x velocity property.

### yVel

Sets the y velocity property.

#### Parameters

-   `newYVel` **[number][55]** The number variable to set the value of the y velocity.

Returns **any** nothing

### yVel

Gets the number value of the y velocity property.

Returns **[number][55]** this.\_yVel - Returns the number value of the y velocity property.

### mass

Sets the mass property.

#### Parameters

-   `newMass` **[number][55]** The number variable to set the value of the mass.

Returns **any** nothing

### mass

Gets the number value of the mass property.

Returns **[number][55]** this.\_mass - Returns the number value of the mass property.

### color

Sets the particle colour property.

#### Parameters

-   `newColor` **[string][56]** The string variable to set the colour of the particle.

Returns **any** nothing

### color

Gets the string value of the particle colour property.

Returns **[string][56]** this.\_color - Returns the string value of the particle colour property.

## 

Sketch from [https://www.openprocessing.org][58],

Called: Jelly Sim,

Original Sketch By: nebulaeandstars,

Adapted Sketch By: hkxx26

Link: [https://www.openprocessing.org/sketch/587065][59],

Licence: [https://creativecommons.org/licenses/by-sa/3.0/][60]

**Meta**

-   **license**: CC-BY-SA-3.0

[1]: #shootingparticles

[2]: #parameters

[3]: #keypressed

[4]: #clearparticles

[5]: #draw

[6]: #createtoolbar

[7]: #positiontoolbar

[8]: #createtext

[9]: #changegravity

[10]: #changerandomise

[11]: #setvariables

[12]: #createparticle

[13]: #gravity

[14]: #parameters-1

[15]: #gravity-1

[16]: #randomise

[17]: #parameters-2

[18]: #randomise-1

[19]: #viscosity

[20]: #parameters-3

[21]: #viscosity-1

[22]: #particlecolor

[23]: #parameters-4

[24]: #particlecolor-1

[25]: #maximumparticles

[26]: #parameters-5

[27]: #maximumparticles-1

[28]: #particles

[29]: #parameters-6

[30]: #particles-1

[31]: #particle

[32]: #parameters-7

[33]: #move

[34]: #display

[35]: #handleinteractions

[36]: #xpos

[37]: #parameters-8

[38]: #xpos-1

[39]: #ypos

[40]: #parameters-9

[41]: #ypos-1

[42]: #xvel

[43]: #parameters-10

[44]: #xvel-1

[45]: #yvel

[46]: #parameters-11

[47]: #yvel-1

[48]: #mass

[49]: #parameters-12

[50]: #mass-1

[51]: #color

[52]: #parameters-13

[53]: #color-1

[54]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean

[55]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number

[56]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[57]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array

[58]: https://www.openprocessing.org

[59]: https://www.openprocessing.org/sketch/587065

[60]: https://creativecommons.org/licenses/by-sa/3.0/
