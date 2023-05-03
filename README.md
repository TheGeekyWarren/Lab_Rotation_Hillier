# Lab_Rotation_Hillier
This is a brief guide to navigate the files in this repository.
Here, you'll find a brief on what each file does. 
Feel free to play with the code, and if you have improved on any of the codes, feel free to get in touch!
Go nuts! XD

All codes are written Jupyter lab. If you don't have jupyter notebook, GET IT! It's really convenient. Just type
```
$ pip install jupyter
```
and you're good to go. If you still want to stick with your text editor, then use the following commands to convert the downloaded .ipynb script to .py (replace <name_of_file> with the name of your file)- 
```
 $ pip install ipynb-py-convert
 $ ipynb-py-convert <name_of_file>.ipynb <name_of_file>.py
```

## Files and their descriptions
### [Bouncing_Ball_Flicker.ipynb](https://github.com/TheGeekyWarren/Lab_Rotation_Hillier/blob/main/Bouncing_Ball_Flicker.ipynb) 
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
 
### [Image_capture.py](https://github.com/TheGeekyWarren/Lab_Rotation_Hillier/blob/main/Image_Capture.py) and [Stream_viewer.ipynb](https://github.com/TheGeekyWarren/Lab_Rotation_Hillier/blob/main/Stream_viewer.ipynb)
These scripts are for capturing an image from your Raspberry Pi module connected to a Raspberry Pi Camera module V2.1 and streaming them to your python-running device of choice.
* Firstly, since the new Bullseye os of the Raspberry pi is not entirely compatible with older interfaces, you need to take a different route to activate the camera than the direct activation in “raspberry pi preferences’ (an easier way to do this is downgrading the OS to Buster, but if you don’t want to downgrade everything for just the camera, this works too.)
* For this, open command prompt and enter 
```
$ sudo raspi-config
```
* Go down to “interface options”  and enable legacy camera. (all navigated by keyboard)
* Once done, see if the camera is connected using the command – 
```
$ vcgencmd get_camera
```
* This command should show you three stats – supported, detected and libcamera interfaces. Ideally, the first two should have a value of 1 and the last one – libcamera interfaces – will have a value of 0. (libcamera is the new update which is not compatible with the older cameras)
* Use command – 
```
$ raspistill -o test.jpg
```
* to test if the camera is working. The image captured will be stored in the base directory of the user. 
If everything is smooth till now, then you can proceed to the code. 
* Download the python script named Image_capture.py
* Before running the code, make sure you install vidgear using pip in the raspberry pi. 
* Parallelly, download the python script named Stream_viewer.ipynb on the receiver system (this is a file used with jupyter notebook) (ensure the receiver system has vidgear and opencv installed)
* Change the ip address in both the scripts (on both receiver system and the pi) to the IP address of the receiver system. 
* Now you're good to go. Run the script on the pi and without much delay, run the script on the receiver system as well. 
* Notes – the program can be closed at any time by pressing 'q' on the OpenCV window. You can also edit the name of the video file you want to store it as, as well as the fps and the format. Keep in mind that the code run on the raspberry pi waits for only a few seconds to receive feedback from the receiver system's code before shutting off. So it is recommended to start running boh codes within a few seconds of each other. 

### Simplified Codes
These codes are the kinda simplified and straightforward runs for DeepLabCut analysis using Model Zoo's 'primate face' model. First, enter the path of the video of choice in  lets you downsample the video of choice, then create a new folder and use it as your current working directory, where you can hen analyse the video using DeepLabCut.
* [Simplified_code-AGC.ipynb] (https://github.com/TheGeekyWarren/Lab_Rotation_Hillier/blob/main/Simplified_Code-AGC.ipynb) 
