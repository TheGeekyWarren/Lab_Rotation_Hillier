# Lab_Rotation_Hillier
This is a brief guide to navigate the files in this repository.
Here, you'll find a brief on what each file does. 
Feel free to play with the code, and if you have improved on any of the codes, feel free to get in touch!
Go nuts! XD

## Files and their descriptions
### [Bouncing_Ball_Flicker.ipynb](https://github.com/TheGeekyWarren/Lab_Rotation_Hillier/blob/main/Bouncing_Ball_Flicker.ipynb) - 
This is the code for the bouncing ball game developed to engage visual smooth pursuit.
* For collecting data with the bouncing ball game, download the script named Bouncing_Ball_Flicker.ipynb from the github link above. 
* Open the script and now make sure you have already installed all the packages needed for the script to run. 
now scroll down on the script till you reach a part that is flanked by dashed lines that says ‘edit here only’ 
take a look through the lines note the parameters you are allowed to customize for the game to run the way you want. Edit this section to your taste. 
* Keep in mind that while editing fps, you need to keep an eye on the fps of the monitor/display you are using. set it accordingly so that you don’t have frame loss. 
* Distance from the monitor is something you need to approximate and input at the start. 
* Next, change the visual angle and the colour of the ball during the flicker according to each subject such that the flicker is just noticeable only when you foveate the ball, but at an angular velocity for which smooth pursuit is not strenuous to maintain. (Make sure the flicker is not noticeable from peripheral vision.)
* Once you have made the necessary edits, you can scroll lower to the next set of dashed lines within the while loop. This optional bit is to modify the difficulty of the game. Switch between the already existing and commented section based on your preference - the currently commented bit makes the ball change direction randomly in the middle while the currently active bit makes the ball change direction only at the edge. 
* The trajectory of the ball is saved in a newly created folder within the current working directory named Trajectories in a csv file called Trajectory followed by the date and time of running the code. 
Note that there is also an option called disp within the editable parameters section. This is in case you are using multiple monitors/displays connected to your system. By default, the value of that parameter should be 0. 
 
