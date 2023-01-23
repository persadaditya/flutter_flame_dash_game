
Learn how to build a platformer game with Flutter and Flame! In the Doodle Dash game, inspired by Doodle Jump, you play as either Dash (the Flutter mascot), or her best friend Sparky (the Firebase mascot), and try to reach as high as possible by jumping on platforms.

## What you'll learn
- How to build a cross-platform game in Flutter.
- How to create reusable game components that can render and update as part of the Flame game loop.
- How to control and animate your character's (called a sprite) movements through game physics.
- How to add and manage collision detection.
- How to add keyboard and touch input as controls for the game.

## Prerequisites
This codelab assumes that you have some Flutter experience. If not, you can learn the basics with the Your First Flutter App codelab.

## What you'll build
This codelab guides you through building a game called Doodle Dash: a platformer game featuring Dash, the Flutter mascot or Sparky, the Firebase mascot (the rest of this codelab references Dash, but the steps also apply to Sparky). Your game will have the following features:

- A sprite that can move horizontally and vertically
- Randomly generated platforms
- A gravity effect that pulls down your sprite
- Game menus
- In-game controls like pause and replay
- The ability to keep score
- Game play
- Doodle Dash is played by moving Dash left and right, jumping on platforms, and using power ups to increase her ability throughout the game. You start the game by choosing the initial difficulty level (1 through 5), and clicking Start.

![doodle dash game](https://codelabs.developers.google.com/static/codelabs/flutter-flame-game/img/d1e75aa0e05c526.gif)

## Levels

There are 5 levels in the game. Each level (after level 1) unlocks new features.

- Level 1 (default): This level spawns NormalPlatform and SpringBoard platforms. When created, any platform has a 20% chance of being a moving platform.
- Level 2 (score >= 20): Adds BrokenPlatform that can only be jumped on once.
- Level 3 (score >= 40): Unlocks the NooglerHat power up. This special platform lasts for 5 seconds and increases Dash's jumping ability by 2.5x her normal velocity. She also wears a cool noogler hat for those 5 seconds.
- Level 4 (score >=80): Unlocks the Rocket power up. This special platform, represented by a rocket ship, makes Dash invincible. It also increases Dash's jumping ability by 3.5x her normal velocity.
- Level 5 (score >= 100): Unlocks Enemy platforms. If Dash collides with an enemy, it's an automatic game over.
  Platform types by level

#### Level 1 (default)
![normal platform](https://codelabs.developers.google.com/static/codelabs/flutter-flame-game/img/9f88eba109da7270_1920.png)
*NormalPlatform*

![spring board](https://codelabs.developers.google.com/static/codelabs/flutter-flame-game/img/1d3e52fbc3721f18_1920.png)
*SpringBoard*


#### Level 2 (score >= 20)
![broken platform](https://codelabs.developers.google.com/static/codelabs/flutter-flame-game/img/5104812ae1b81eb0_1920.png)
*BrokenPlatform*

#### Level 3 (score >= 40)
![noogler hat](https://codelabs.developers.google.com/static/codelabs/flutter-flame-game/img/f1ecb43045e8b5a_1920.png)
*NooglerHat*

#### Level 4 (score >= 80)
![rocket](https://codelabs.developers.google.com/static/codelabs/flutter-flame-game/img/d4f119585c6506aa_1920.png)
*RocketLauncher*

#### Level 5 (score >= 100)
![enemy](https://codelabs.developers.google.com/static/codelabs/flutter-flame-game/img/bf23c8421424be2a_1920.png)
*Enemy*

## Losing the game
There are two ways to lose the game:
- Dash falls below the bottom of the screen.
- Dash collides with an enemy (enemies spawn at level 5).

## Power ups
Power ups enhance the character's playing ability such as increasing her jumping velocity, or allowing her to become "invincible" against enemies, or both. Doodle Dash has two power up options. Only one power up is active at a time.

The noogler hat power up increases Dash's jumping ability by 2.5x her normal jumping height. Plus she wears a noogler hat during the power up.
The rocket ship power up makes Dash invincible against enemy platforms (colliding with an enemy has no effect) and increases her jumping ability by 3.5x her normal jumping height. She flies in a rocket until gravity overcomes her velocity and she lands on a platform.



|  |  |
|--|--|
| ![enter image description here](https://codelabs.developers.google.com/static/codelabs/flutter-flame-game/img/ede04fdfe074f471.gif) | ![enter image description here](https://codelabs.developers.google.com/static/codelabs/flutter-flame-game/img/e1fece51429dae55.gif) |
