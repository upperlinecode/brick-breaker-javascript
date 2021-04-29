# Brick Breaker

## What We're Building

Brick Breaker is a classic game in which a player uses a paddle to bounce a ball around and break some bricks. If you haven't seen it previously, that sentence probably sounded really strange. Feel free to google it and play around for a minute or two.

This afternoon, you'll be working with your partner to create a simple version of this game. Since you have all the tools you need, and we'll be moving into project mode soon, this lab will be quite self-guided. Start by making a list of major elements of the game (physical things and logical bits), and then plan the order in which you're going to implement them. Then you can get to work.

If you'd like a little more structure than that, feel free to follow the general guide below.

## A Possible Approach

Start off by creating a paddle which the player can move left and right. This'll require a variable for it's position and a definition of `keyPressed` among other things.

Then move onto the ball. It'll need a position and a velocity, and logic to bounce it off walls and the paddle. If you found a version of this game online, you may see the ball bouncing at odd angles. If you're in the mood, think about how you could calculate irregular angles yourself, though this is not a key part of the game.

What should happen if the ball reaches the bottom of the screen? Stop everything and display a message? Restart the game?

Now it's time to add bricks. This will probably be easiest with a `Brick` class. The most complex logical element here is detecting collisions and reacting to them. If you played a version where bricks took multiple hits to destroy, feel free to implement this or not.

Want to add a score? What about lives?

If you've gotten this far (and don't worry at all if you haven't), you can go back and polish things up.
