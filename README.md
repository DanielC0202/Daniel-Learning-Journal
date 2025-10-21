# Daniel-Learning-Journal


This is My Programming Learning Journal

 ## 14/10/2025 ##

 IF I create a repository without anything, there will not be anything on the page, simply add a README through the blue Hyperlink.

 ## 21/10/25 ## 

 I am working on a Component that requires me to have basic 2D fighting game movement, which entails: Back & forth X axis movement; A rigid jump that can only go in 3 directions, Directly up, up and forwards, or up and backwards; And a dash, both on the ground and in the air.

 Problem 1.

 - I tried to create a simple Side Switching system by using Physiscs.linecast but it did not work as I misunderstood how this Function worked, it creates a line between two points, and looks for anything that intersects this line it has created, so trying to use it means the character cannot have anything inbetween the two characters.

Solution: 

- After Looking at the API a bit, I found a page discussing direction and distance, and on this page is a variable made for this "var heading" which calculates the distance between two transforms that you set. I used this to calculate the x distance between my player and enemy, and if the players X transform was greater than the enemy's than run a function that will swap sides. Time to Create that function.

Problem 2.

- Once the game checks if you are above 0, it does side switch, but it does this for every frame you are on one specific side of the screen, so I need to make it so that it only happens once you cross the midpoint.

Solution:

- I created 2 if statement's, asking if you are on the Left side of the screen or the right, if you are on the left it runs to check if the number is Greater than 0, and if you are on the right, it checks if the number is less than 0.

Problem 3:

- I tried to make it so that when the player sideswitched, the enemy also side switched, but in doing so they both started infinitely side switching and I did not know why.

Solution:

- I had placed the Call for the enemy SideSwitch in the same place as the call for the player, instead of inside the function that is called.
