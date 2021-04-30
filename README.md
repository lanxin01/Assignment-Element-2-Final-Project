# Assignment-Element-2-Final-Project   Aircraft combat game
1. Design background

Many years ago, WeChat had a game called Airplane Wars. The interface style is simple, easy to operate, and interesting. It is very popular in China. (Figure
It seems that its picture quality and gameplay are not outdated now, and then I want to implement this game with python.


2. Design Notes

Complete the function of launching bullets from the player's aircraft;
Realize collision detection between enemy aircraft and player aircraft bullets;
Add an explosion effect to the disappearing plane;
Calculate the score and update the score leaderboard.


3. Project features and functions

Increase the Bullet base class and Plane base class, increase the amount of code;
Realize the up, down, left, and right movement of the player’s aircraft and bullet launching;
Realize the random appearance and movement of enemy aircraft;
Realize collision detection between enemy aircraft and player aircraft, and collision detection between bullets and aircraft;
Realize the explosion effect of the plane being hit.  


4. Theoretical basis

The main technical route or method I have taken is the introduction of the system development environment. The current program is based on python as the programming language, and the main function implementation depends on the pygame module, as well as sys and random. Mainly use the position change between surface objects, and then use event monitoring to let the program run. After the position of the Surface object changes during operation, the interface is refreshed, and when the user operates the mouse and keyboard, the corresponding event is monitored when the operation is completed.


5. Creation process

The first thing to do is to install and use pip install pygame. Then I will draw the elements of the game interface. The composition of the interface is not complicated, including player aircraft, enemy aircraft, bullets, scoreboard and other elements.

First, create a file named main.py as the main file. I first created the interface with a size of 480*800.
![image](https://github.com/lanxin01/Week-3-Exercise---The-Python-Challenge-/blob/main/1.png)

Create a Bullet class to store bullets. Create and initialize objects such as bullets and airplanes, and then add methods to move them. In the bullet class, the initialization method of the parent class is called to initialize the properties of the sprite.

![image](https://github.com/lanxin01/Week-3-Exercise---The-Python-Challenge-/blob/main/2.png)

In the plane class, various behaviors of the plane are stored.

Initialize the rectangle where the picture is, and the coordinates of the upper left corner of the rectangle, and initialize the player's airplane speed. get_rect will return the rectangular area of the Surface, .centerx and .bottom are its two attributes
