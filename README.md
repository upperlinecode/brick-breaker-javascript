# Brick Breaker

[![Run on Repl.it](https://repl.it/badge/github/upperlinecode/brick-breaker-javascript)](https://repl.it/github/upperlinecode/brick-breaker-javascript)

## What We're Building

Brick Breaker is a classic game in which a player uses a paddle to bounce a ball around and break some bricks. If you haven't seen it previously, that sentence probably sounded really strange. Feel free to google it and play around for a minute or two.

This afternoon, you'll be working with your partner to create a simple version of this game. Since you have all the tools you need, and we'll be moving into project mode soon, this lab will be quite self-guided. Start by making a list of major elements of the game (physical things and logical bits), and then plan the order in which you're going to implement them. Then you can get to work.

If you'd like a little more structure than that, feel free to follow the general guide below.

## A Possible Approach

### Step One: Start off by creating a paddle which the player can move left and right.

1. Draw a horizontal rectangle near the bottom of the screen.

2. Create an object called `paddle` with properties `x` and `y`, and itilialize it to somewhere reasonable in the `setup`. Then replace the coordinates of the rectangle with `paddle.x` and `paddle.y`.

3. Add a definition for `function keyPressed()`, and within it, add two conditionals. The first should check if `keyCode === LEFT_ARROW`, and if so, should decrease `paddle.x` by a small amount. The second should do the same for the right arrow.

### Step Two: Next, we'll add a bouncing ball.

1. Create another object, this one called `ball` which will store the position of the ball (`x` and `y`) and the velocity of the ball (`vx` and `vy`). Initialize each of these four values to something reasonable in the `setup`.

2. Draw a small circle at `(ball.x, ball.y)`. Each frame, in the `draw` loop, increase `ball.x` and `ball.y` by `ball.vx` and `ball.vy`, respectively.

3. Also in the draw loop, add three conditionals which will allow the the ball to bounce off the top, left, and right sides of the screen. For example, if the radius of the ball is 10 pixels, a conditional to bounce the ball off the top of the screen should check if `ball.y < 5` and if so, should set `ball.vy` to `-ball.vy`.

4. Add a fourth conditional which will cause the ball to bounce of the paddle. This will look similar to the others, but depends on the paddle's position.

5. What should happen if the ball reaches the bottom of the screen? Stop everything and display a message? Restart the game?

### Step Three: It's finally time to add bricks.

1. The easiest way to do this is probably with a `Brick` class. The class should have three methods, a `constructor`, a method called `display`, and one called `checkHit` which will check if the ball has come in contact with it.

2. Create an array and start it with just three bricks. Iterate over the array and call `display` and `checkHit` for each brick in the `draw` loop.

3. Want to add a score? What about lives?

### Bonus Challenges

We're not expecting you to get here, but if you do, there are a number of cool ways you can expand this project.

1. If you played a version of this game online, you may have noticed that the ball bounces off the paddle at weird angles depending on where they come into contact. This introduces a bit of strategy into the game.
2. Some bricks could take multiple hits to destroy. Can you change the color of bricks to make it clear how many hits are left?
3. Perhaps you could introduce a control scheme with the mouse, where the paddle moves at some reasonable speed toward the mouse's `x` position.
