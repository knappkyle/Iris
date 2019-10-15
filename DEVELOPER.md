Welcome!
------------------------------------------------------------------------------------------------------------------------
This Project is a first person exploration/survival game, where the player must solve puzzles and hide from a monster.

Data
------------------------------------------------------------------------------------------------------------------------
The game is kept on gitlab as a unity project folder.
We give our clients a brief video showcasing what was accomplished that sprint and a zip file.
Every Thursday at 5pm we meet with our clients to do progress checks and plan for upcoming deadlines.
At the end of every sprint we provide a zip file with a .exe inside so they can see our progress. 

Build
------------------------------------------------------------------------------------------------------------------------
To build the game, simply download the game. Then launch unity 2.91f to load the project. Then click build in unity. This will present the main menu where you can select start and quit commands. Also as an alternative running the .exe file within the project folder will work.

Design
------------------------------------------------------------------------------------------------------------------------
The design of game is going towards mansion survival game where the player solves puzzles to go to the next floor and eventually out of the mansion. 
    Main Character:
    -the main character does not have an appearance as it is a first person game, so it is represented in unity as a capsule.
    -The main character can jump, move and look around.
    -Jumping is done through the PlayerController.cs script. The player can use the jump key (space bar) to jump. It works using a sphere collider set at the bottom of the capusle. This tests if the character is on any object that belongs to the groundLayer. If the sphere detects a groundLayer than the character will be able to jump. If it does not detect a groundLayer than the character will not be able to jump. 
    -Movement is done through the Character_Controller.cs script. This checks for horizontal and vertical changes through the use of the movement keys (a,w,s,d). It also locks the cursor state, meaning that the cursor is not shown in game until the player presses the esc key.
    -Camera rotation is done through the Camera_Mouse_Look.cs script. This sets sensitivity, smoothing, minAngle, maxAngle as variables for ease of change in unity. Sensitivity is how fast the camera rotates. Smoothing makes camera rotation feel cleaner and not sudden. minAngle refers to how low the camera can rotate on the y axis before it is stopped, and maxAngle refers to how high it can rotate before it is stopped. The script also rotates the character model when rotating on the x axis as well.
    -Menu is handled by panels and a START.cs script. When the game is loaded, the menu shows up with a "play" and "quit" option. Pressing start will have the game shift to the beginning scene, while quit will exit the game. 
    -Character can pick items up which are added to an inventory. 
    -Inventory can be accessed using 'tab' key.
    -Inventory is updated when items are added or used.
    -Puzzles can be accessed using 'e' key.
    -Puzzles bring up an interactable canvas.
    -Raycasting is all done via the Player_Pickup.cs script which checks for a collider with a onTrigger check and then it checks the tag.
    -Using items will be done through the Use_Item.cs script which is called from the Pickup_Items.cs script.
    -Doors will require keys to open and those keys must be in the inventory. 
    -Solving Puzzles will drop keys are items that will allow the player to get keys.    
	-Avoiding the monster while solving these puzzles will be the main concept of this game. 
	-Puzzles have a variety of uses. To unlock doors, collect items and various other elements to progress in the game. 
    -Notes are used to tell the player hints and add story elements. Each note has a game object with a note.cs script on it, as well as a box collider with onTrigger checked and the not tag selected. Then those connect to a unique canvas object.

Workflow
------------------------------------------------------------------------------------------------------------------------
Workflow is handled in one week sprints. Each sprint each contributer takes an issue and attempts to complete it for that sprint. Sprints start on Monday and end the following Monday. When the issue is being worked on, the contributer needs to track how much time is spent on the issue by leaving a comment in gitlab with the /spent timespent command. After the issue is completed, the contributer must close that issue. Each contributer must work on their seperate branch and then those branches must be merged into the master branch. The documentation is updated each week by Monday. 


Testing
------------------------------------------------------------------------------------------------------------------------
Testing is handled through written statements on how each issue should function. The actual testing is done manually. For example "The character cannot jump when in midair". The testing is done by the person who worked on the issue. If the test fails then the issue must be worked on more, in order to succeed on the test
In some cases testing over rides previous data where that test isnt possible to check anymore as the game progresses things change and tests needed to be updated weekly.


