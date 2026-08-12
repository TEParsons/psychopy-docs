.. _eyetrackermarkercomponent:

-------------------------------
Eyetracker Marker Component
-------------------------------

Add a text marker in the hdf5 file

Categories:
    Eyetracking
Works in:
    PsychoPy

**Note: Since this is still in beta, keep an eye out for bug fixes.**

Parameters
-------------------------------

Basic
===============================

The required attributes of the stimulus, controlling its basic function and behaviour


.. _eyetrackermarkercomponent-startVal:
Send when... 
    When the Eyetracker Marker Component should start, see :ref:`startStop`.
    
.. _eyetrackermarkercomponent-startEstim:
Expected start (s) 
    If you are using frames to control timing of your stimuli, you can add an expected start time to display the component timeline in the routine.
    
.. _eyetrackermarkercomponent-startType:
Start type 
    How do you want to define your start point?
    
    Options:
    
    * time (s)
    
    * frame N
    
    * condition
    
.. _eyetrackermarkercomponent-durationEstim:
Expected duration (s) 
    If you are using frames to control timing of your stimuli, you can add an expected duration to display the component timeline in the routine.
    
.. _eyetrackermarkercomponent-message:
Text 
    Text to send to the eyetracker (128 characters max)
    
.. _eyetrackermarkercomponent-category:
Category 
    Optional grouping text for the message (32 characters max)
    
Data
===============================

What information about this Component should be saved?


.. _eyetrackermarkercomponent-saveStartStop:
Save onset/offset times 
    Store the onset/offset times in the data file (as well as in the log file).
    
.. _eyetrackermarkercomponent-syncScreenRefresh:
Sync timing with screen refresh 
    Synchronize times with screen refresh (good for visual stimuli and responses based on them)
    