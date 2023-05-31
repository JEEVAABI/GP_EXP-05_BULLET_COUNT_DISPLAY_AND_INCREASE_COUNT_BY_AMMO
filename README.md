# GP_EXP-05_BULLET_COUNT_DISPLAY_AND_INCREASE_COUNT_BY_AMMO
### Experiment:05 – The player controller adds ammo to increase the bullet count and display in play-mode
### AIM:
To add ammo to increase the bullet count and display in play-mode.


### ALGORITHM(for adding bullet count):
```
1.	Create a HUD Blueprint:
•	In the Content Browser, right-click in the desired folder.
•	Select Create Basic Asset > Blueprint Class.
•	In the Class Settings window, search for "HUD" and select it as the parent class.
•	Name the Blueprint (e.g., "GameHUD") and click Create.
2.	Open the GameHUD Blueprint:
•	Open the GameHUD Blueprint you just created.
•	In the Blueprint editor, find the Canvas panel on the left.
•	Add a Text block widget to the Canvas panel to display the bullet count.
•	Position the Text block widget on the canvas as desired.
3.	Create a reference to the player character:
•	In the GameHUD Blueprint, create a variable of the player character's class to store a reference to it.
•	To do this, go to the Variables panel and click the "+" button.
•	Set the variable type to the class of your player character (e.g., ThirdPersonCharacter).
•	Name the variable (e.g., PlayerCharacter).


4.	Update the bullet count display:
•	In the GameHUD Blueprint, locate the Event Tick event.
•	Drag off the PlayerCharacter variable and search for "Get Bullet Count" (assuming you have a bullet count variable in your player character Blueprint).
•	Connect the output of the Get Bullet Count node to the Text block widget's Text property.
•	You may need to format the bullet count value as a string before connecting it to the Text property.
5.	Set the GameHUD as the active HUD:
•	Open your player character Blueprint.
•	In the Blueprint editor, locate the Event Begin Play event.
•	Drag off the execution line and search for "Create Widget".
•	In the Create Widget node, select the GameHUD Blueprint you created.
•	Drag off the return value of the Create Widget node and search for "Add To Viewport".
•	Compile and save the player character Blueprint.
6.	Test the bullet count display:
•	Play the game in the editor.
•	Ensure that the bullet count is displayed on the screen as you interact with the game, such as firing bullets or picking up ammo.
```

OUTPUT:
IN PLAY MODE
 
CANVAS
 
BULLET COUNT GRAPH
 





### ALGORITHM(for adding ammo):
```
1.	Create an ammo actor:
•	In the Content Browser, right-click in the desired folder.
•	Select Create Basic Asset > Blueprint Class.
•	In the Class Settings window, search for "Actor" and select it as the parent class.
•	Name the Blueprint (e.g., "AmmoActor") and click Create.
2.	Set up the ammo actor:
•	Open the AmmoActor Blueprint.
•	In the Blueprint editor, you can add a static mesh or other visual representation to represent the ammo pickup.
•	Add a collision component (e.g., Box Collision) to detect the player's interaction.
•	Configure the collision component's properties, such as its size and collision settings.
•	Create a custom event in the Blueprint to handle the player's interaction with the ammo actor.
3.	Implement the player's interaction with the ammo actor:
•	Open the player's character Blueprint.
•	In the Blueprint editor, locate the event that handles the collision or overlap with the ammo actor.
•	Add a new custom event node to handle the interaction.
•	Implement logic to increase the bullet count for the player:
•	Access the player's character or controller reference.
•	Increment the bullet count variable or property.
•	Play a sound or visual effect to indicate the pickup.
•	Destroy the ammo actor after it has been collected.

4.	Place the ammo actor in the level:
•	Drag and drop the AmmoActor Blueprint into the level where the player can interact with it.
•	Adjust its position and orientation as needed.
5.	Test the ammo pickup functionality:
•	Compile and save the AmmoActor Blueprint and the player's character Blueprint.
•	Play the game and navigate the player character to the ammo actor.
•	Ensure that when the player character overlaps or collides with the ammo actor, the bullet count increases, and the ammo actor disappears.
```

OUTPUT:
AMMO IN PLAY MODE

EVENT GRAPH

INCREASE THE BULLET COUNT IN AMMO ACTOR
 
AFTER HITTING AMMO
 
## RESULT:
Thus, added ammo to increase the bullet count and displayed in play-mode.



