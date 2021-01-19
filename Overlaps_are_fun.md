# Overlaps are fun

## Introduction @showdialog

In this tutorial you will create a game with 2 sprites, a ``||sprites:Player||`` sprite and a ``||sprites:Food||`` sprite. The goal of the game is to eat as much pizza as you can before the time runs out! Each time your player catches the pizza, you gain points and the countdown is restarted.

## Step 2

Open the ``||scene:Scene||`` Toolbox drawer and drag the ``||scene:set background color||`` block into the ``||loops:on start||`` block on your Workspace. Click **Next** to go to the next step in the Tutorial.

```blocks
// @highlight
scene.setBackgroundColor(0)
```

## Step 3

In the ``||scene:set background color||`` block, click on the grey color oval to open the color palette and select a background color. To see what this looks like in your game, look at the Game Simulator on the left side of the screen.

## Step 4

Open the ``||sprites:Sprites||`` Toolbox drawer and drag the first block, ``||variables:set mySprite||`` into the ``||loops:on start|`` block on your Workspace. This will create a new ``||sprites:Player||`` character for your game.

**Don't forget to re-name the mySprite variable, and give your character a good name!**

```blocks
let sally: Sprite = null
scene.setBackgroundColor(7)
// @highlight
sally = sprites.create(img`
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
`, SpriteKind.Player)
```

## Step 5

Draw your ``||sprites:Player||`` character by clicking on the grey square in the ``||variables:set mySprite||`` block to open the Sprite Editor. Use the color palette and design tools to draw an image on the canvas. Or, just choose one from the Gallery if you like!  

Click **Done** when you are finished.


## Step 6

Open the ``||controller:Controller||`` Toolbox drawer and drag the ``||controller:move mySprite with buttons||`` block after the ``||variables:set mySprite||`` block. This will allow you to move your ``||sprites:Player||`` sprite around the screen with the arrow keys. Try it out in the Game Simulator

```blocks
let sally: Sprite = null
scene.setBackgroundColor(7)
sally = sprites.create(img`
    . . . . . . 5 . 5 . . . . . . . 
    . . . . . f 5 5 5 f f . . . . . 
    . . . . f 1 5 2 5 1 6 f . . . . 
    . . . f 1 6 6 6 6 6 1 6 f . . . 
    . . . f 6 6 f f f f 6 1 f . . . 
    . . . f 6 f f d d f f 6 f . . . 
    . . f 6 f d f d d f d f 6 f . . 
    . . f 6 f d 3 d d 3 d f 6 f . . 
    . . f 6 6 f d d d d f 6 6 f . . 
    . f 6 6 f 3 f f f f 3 f 6 6 f . 
    . . f f d 3 5 3 3 5 3 d f f . . 
    . . f d d f 3 5 5 3 f d d f . . 
    . . . f f 3 3 3 3 3 3 f f . . . 
    . . . f 3 3 5 3 3 5 3 3 f . . . 
    . . . f f f f f f f f f f . . . 
    . . . . . f f . . f f . . . . .
`, SpriteKind.Player)
// @highlight
controller.moveSprite(sally)
```

## Step 7

Open the ``||sprites:Sprites||`` Toolbox drawer and drag another ``||variables:set mySprite||`` block into the ``||loops:on start||`` block on your Workspace. This will be the **pizza** sprite in our game.

```blocks
let sally: Sprite = null
let mySprite: Sprite = null
scene.setBackgroundColor(7)
sally = sprites.create(img`
    . . . . . . 5 . 5 . . . . . . . 
    . . . . . f 5 5 5 f f . . . . . 
    . . . . f 1 5 2 5 1 6 f . . . . 
    . . . f 1 6 6 6 6 6 1 6 f . . . 
    . . . f 6 6 f f f f 6 1 f . . . 
    . . . f 6 f f d d f f 6 f . . . 
    . . f 6 f d f d d f d f 6 f . . 
    . . f 6 f d 3 d d 3 d f 6 f . . 
    . . f 6 6 f d d d d f 6 6 f . . 
    . f 6 6 f 3 f f f f 3 f 6 6 f . 
    . . f f d 3 5 3 3 5 3 d f f . . 
    . . f d d f 3 5 5 3 f d d f . . 
    . . . f f 3 3 3 3 3 3 f f . . . 
    . . . f 3 3 5 3 3 5 3 3 f . . . 
    . . . f f f f f f f f f f . . . 
    . . . . . f f . . f f . . . . .
`, SpriteKind.Player)
controller.moveSprite(sally)
// @highlight
mySprite2 = sprites.create(img`
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
`, SpriteKind.Player)
```

## Step 8

In the new ``||variables:set mySprite||`` block, click on ``||variables:mySprite||`` to open the menu, and select ``Rename variable...`` Type in ``pizza`` as the new sprite name and click **Ok**.

## Step 9 @showhint

In the ``||variables:set pizza||`` block, click on the ``||sprites:Player||`` kind to open the menu of different Sprite kinds. Select ``||sprites:Food||`` as your ``||variables:pizza||`` sprite kind.

![Set sprite kind](https://raw.githubusercontent.com/mlupo/overlaps-are-fun/master/sprite-kind.jpg)


## Step 10

Click on the grey box for ``||variables:set pizza||`` and then select the **Gallery** view. Scroll to find the image of a small pizza (or any other image you like!) and select it to load into the image editor.

## Step 11 

Open the ``||sprites:Sprites||`` Toolbox drawer and drag the ``||sprites:on sprite overlaps otherSprite||`` block onto your Workspace (you can place this anywhere).

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {

})
```

## Step 12 @showhint

In the ``||sprites:on sprite overlaps otherSprite||`` block, click on the second ``||sprites:Player||`` kind after ``||variables:otherSprite||`` to open the menu. Select ``||sprites:Food||`` as its kind.

![Overlap sprite kind](https://raw.githubusercontent.com/mlupo/overlaps-are-fun/master/overlap-kind-sprite.png)

## Step 13

When our ``||sprites:Player||`` overlaps with the ``||variables:pizza||`` sprite, let's add a point to our game score. Open the ``||info:Info||`` Toolbox drawer and drag the ``||info:change score||`` block into the ``||sprites:on sprite overlaps otherSprite||`` block.

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    // @highlight
	info.changeScoreBy(1)
})
```

## Step 14

Let's set the position for ``||variables:pizza||`` to random locations around the screen. Open the ``||sprites:Sprites||`` Toolbox drawer and drag the ``||sprites:set mySprite position||`` block into the ``||sprites:on sprite overlaps otherSprite||`` block on your Workspace.

```blocks
let mySprite: Sprite = null
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
	info.changeScoreBy(1)
    // @highlight
    mySprite.setPosition(0, 0)
})
```

## Step 15

In the ``||sprites:set mySprite position||`` block, click on the ``||variables:mySprite||`` variable to open the menu, and select your ``||variables:pizza||`` sprite.

![Change mySprite to pizza](https://raw.githubusercontent.com/mlupo/overlaps-are-fun/master/sprite-position-rename.png)

## Step 16

Open the ``||math:Math||`` Toolbox drawer and drag two ``||math:pick random||`` blocks onto the Workspace. Drop one into the ``x`` coordinate of the ``||sprites:set pizza position||`` block, and the other into the ``y`` coordinate replacing the ``0`` values.

```blocks
let pizza: Sprite = null
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    pizza.setPosition(Math.randomRange(0, 10), Math.randomRange(0, 10))
})
```

## Step 17

The Arcade game screen is `160` pixels wide, and `120` pixels high. In the first ``||math:pick random||`` block in the `x` coordinate of the ``||sprites:set pizza position||`` block, change the maximum value from ``10`` to **160**. In the second ``||math:pick random||`` block in the ``y`` coordinate, change the maximum value from ``10`` to **120**.

```blocks
let pizza: Sprite = null
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
	info.changeScoreBy(1)
    pizza.setPosition(Math.randomRange(0, 160), Math.randomRange(0, 120))
})
```

## Step 18

Let's restart our countdown each time. Open the ``||info:Info||`` Toolbox drawer and drag a ``||info:start countdown||`` block into the ``||sprites:on sprite overlaps otherSprite||`` block on your Workspace.

```blocks
let pizza: Sprite = null
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
	info.changeScoreBy(1)
    pizza.setPosition(Math.randomRange(0, 160), Math.randomRange(0, 120))
    // @highlight
    info.startCountdown(10)
})
```
## Complete

Congratulations, you have completed your game! Use the Game Simulator to play by moving your ``||sprites:Player||`` around the screen to try and eat as much pizza as possible before the time runs out. What's your high score?

```blocks
let pizza: Sprite = null
let sally: Sprite = null
scene.setBackgroundColor(7)
sally = sprites.create(img`
    . . . . . . 5 . 5 . . . . . . . 
    . . . . . f 5 5 5 f f . . . . . 
    . . . . f 1 5 2 5 1 6 f . . . . 
    . . . f 1 6 6 6 6 6 1 6 f . . . 
    . . . f 6 6 f f f f 6 1 f . . . 
    . . . f 6 f f d d f f 6 f . . . 
    . . f 6 f d f d d f d f 6 f . . 
    . . f 6 f d 3 d d 3 d f 6 f . . 
    . . f 6 6 f d d d d f 6 6 f . . 
    . f 6 6 f 3 f f f f 3 f 6 6 f . 
    . . f f d 3 5 3 3 5 3 d f f . . 
    . . f d d f 3 5 5 3 f d d f . . 
    . . . f f 3 3 3 3 3 3 f f . . . 
    . . . f 3 3 5 3 3 5 3 3 f . . . 
    . . . f f f f f f f f f f . . . 
    . . . . . f f . . f f . . . . . 
`, SpriteKind.Player)
controller.moveSprite(sally)
pizza = sprites.create(img`
. . . . . . b b b b . . . . . .
. . . . . . b 4 4 4 b . . . . .
. . . . . . b b 4 4 4 b . . . .
. . . . . b 4 b b b 4 4 b . . .
. . . . b d 5 5 5 4 b 4 4 b . .
. . . . b 3 2 3 5 5 4 e 4 4 b .
. . . b d 2 2 2 5 7 5 4 e 4 4 e
. . . b 5 3 2 3 5 5 5 5 e e e e
. . b d 7 5 5 5 3 2 3 5 5 e e e
. . b 5 5 5 5 5 2 2 2 5 5 d e e
. b 3 2 3 5 7 5 3 2 3 5 d d e 4
. b 2 2 2 5 5 5 5 5 5 d d e 4 .
b d 3 2 d 5 5 5 d d d 4 4 . . .
b 5 5 5 5 d d 4 4 4 4 . . . . .
4 d d d 4 4 4 . . . . . . . . .
4 4 4 4 . . . . . . . . . . . .
`, SpriteKind.Food)

sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
	info.changeScoreBy(1)
    pizza.setPosition(Math.randomRange(0, 160), Math.randomRange(0, 120))
    // @highlight
    info.startCountdown(10)
})
```

