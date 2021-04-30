# Assignment-Element-2-Final-Project   Aircraft combat game

Presentation vedio link

1. Design background

Many years ago, WeChat had a game called Airplane Wars. The interface style is simple, easy to operate, and interesting. It is very popular in China. (Figure
It seems that its picture quality and gameplay are not outdated now, and then I want to implement this game with python.

![image](https://github.com/lanxin01/Assignment-Element-2-Final-Project/blob/main/0.png)



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

1⃣️ Create a file named main.py as the main file. I first created the interface with a size of 480*800.
![image](https://github.com/lanxin01/Assignment-Element-2-Final-Project/blob/main/1.png)

2⃣️ Create a Bullet class to store bullets. Create and initialize objects such as bullets and airplanes, and then add methods to move them. In the bullet class, the initialization method of the parent class is called to initialize the properties of the sprite.

![image](https://github.com/lanxin01/Assignment-Element-2-Final-Project/blob/main/2.png)

In the plane class, various behaviors of the plane are stored.

3⃣️ Initialize the rectangle where the picture is, and the coordinates of the upper left corner of the rectangle, and initialize the player's airplane speed. get_rect will return the rectangular area of the Surface, .centerx and .bottom are its two attributes.
![image](https://github.com/lanxin01/Assignment-Element-2-Final-Project/blob/main/3.png)

4⃣️ Set the function for firing bullets.

5⃣️ Four functions to control aircraft movement
![image](https://github.com/lanxin01/Assignment-Element-2-Final-Project/blob/main/4.png)
The screen_rect in the code can get the rectangular border of the game window, and the rect object can get the rectangular border of the airplane image. You can limit the movement range of the aircraft through their attributes right, left, top, and bottom.

The moving direction is divided into up, down, left, and right, and the boundary needs to be judged.

6⃣️ Enemy aircraft

7⃣️ Resource initialization and parameter configuration

pygame.init() imports and initializes all pygame modules. Before using other modules, you must first call the init method
pygame.quit() uninstalls all pygame modules and is called before the end of the game

8⃣️ Main game loop

The infinite loop is the game loop, and the beginning of the game loop represents the official start of the game;
Move the position of all images every 1/60 seconds;
Detect user interaction (player operations, such as moving the mouse, pressing the keyboard, etc.);
Update all image positions;
Update the screen display.
![image](https://github.com/lanxin01/Assignment-Element-2-Final-Project/blob/main/6.png)

9⃣️ Listen to events in the game

After the game is launched, the user's actions for the game, such as: clicking the close button, moving the mouse, pressing the button...
In pygame, through pygame.event.get(), you can get the list of events currently done by the user
The player can do many things at the same time, so the return value is a list.
![image](https://github.com/lanxin01/Assignment-Element-2-Final-Project/blob/main/7.png)

Finally, after the screen object completes all the blit methods, call the display.update method in turn, and you can also see the final drawing result on the screen.



