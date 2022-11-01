# psycho403assign5
#===================== 
#IMPORT MODULES 
#=====================
#-
import numpy as np
#-from psychopy import core, gui, visual, event
#-import file save functions
import json
#-(import other functions as necessary: os...)
import os
import random
import time


#=====================
#PATH SETTINGS
#=====================

#-define the main directory where you will keep all of your experiment files 
main_dir = os.getcwd() 

#-define the directory where you will save your data
data_dir = os.path.join(main_dir,'data')

#-if you will be presenting images, define the image directory
image_dir = os.path.join(main_dir, 'images')

#-check that these directories exist
if not os.path.isdir(image_dir):
    raise Exception('Could not find the path!')
if not os.path.isdir(image_dir):
    raise Exception('Could not find the path!')
    
#=====================
#COLLECT PARTICIPANT INFO
#=====================
#-create a dialogue box that will collect current participant number, age, gender, handedness
#get date and time
#-create a unique filename for the data
#=====================
#STIMULUS AND TRIAL SETTINGS
#=====================
#-number of trials and blocks *

trials = 10
Blocks = 2

#-stimulus names (and stimulus extensions, if images) *

stimname='faces'
stimextend = 'jpg'
#-stimulus properties like size, orientation, location, duration *

stimsize = [200*200]
stimorien = 'landscape'
stimloc = [0,0]
stimdur = 1

#-start message text *
startmsg = 'Welcome, Welcome, Welcome! When your ready hit any button to get started!'
blockmsg = 'Press any key to continue'
end_trialmsg='End of trial'
#=====================
#PREPARE CONDITION LISTS
#=====================
#-check if files to be used during the experiment (e.g., images) exist
pics = []
for index in range(1,11):
    if index < 10:
        pics.append(stimname + "0" + str(index))
    else:
        pics.append(stimname + str(index) + stimextend)
for pic in pics:
    if pic in os.listdir(image_dir):
        print(pic + " was found!")
    else:
        raise Exception("The image lists do not match up!")
#-create counterbalanced list of all conditions *
stimimgs=list(zip(stimname, stimextend))
#=====================
#PREPARE DATA COLLECTION LISTS
#=====================
#-create an empty list for correct responses (e.g., "on this trial, a response of X is correct") *
CR =[] #CORRECT RESPONSE
#-create an empty list for participant responses (e.g., "on this trial, response was a X") *
PR = []#PARTICIPANT RESPONSE
#-create an empty list for response accuracy collection (e.g., "was participant correct?") *
RAC = []#
#-create an empty list for response time collection *
RT = [] #REACTION TIME
#-create an empty list for recording the order of stimulus identities *
S_ID = []
#-create an empty list for recording the order of stimulus properties *
S_PR = []
#=====================
#CREATION OF WINDOW AND STIMULI
#=====================
#-define the monitor settings using psychopy functions
#-define the window (size, color, units, fullscreen mode) using psychopy functions
#-define experiment start text unsing psychopy functions
#-define block (start)/end text using psychopy functions
#-define stimuli using psychopy functions
#-create response time clock
#-make mouse pointer invisible

#=====================
#START EXPERIMENT
#=====================
#-present start message text
#-allow participant to begin experiment with button press


#=====================
#BLOCK SEQUENCE
#=====================
#-for loop for nBlocks *
    #-present block start message
    #-randomize order of trials here *
    #-reset response time clock here
for block in range(Blocks):
    print('Welcome'+''+str(block+1))
    np.random.shuffleI(pics)
    
    #=====================
    #TRIAL SEQUENCE
    #=====================    
    #-for loop for nTrials *
        #-set stimuli and stimulus properties for the current trial
        #-empty keypresses
for trial in range(trials):
    print ('trial'+''+str(trial+1))
        #=====================
        #START TRIAL
        #=====================   
        #-draw stimulus
        #-flip window
        #-wait time (stimulus duration)
        #-draw stimulus
        #-...
        
        #-collect subject response for that trial
        #-collect subject response time for that trial
        #-collect accuracy for that trial
        
#======================
# END OF EXPERIMENT
#======================        
#-write data to a file
#-close window
#-quit experiment
