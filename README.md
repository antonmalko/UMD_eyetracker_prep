# UMD_eyetracker_prep

A couple of eye-tracking scripts to prepare files for EyeLink 1000 eye-tracker and EyeTrack 0.7.1 program. Originally written by Alan Mishler in 2010. 

The instruction for ow to use them are in the headers of the scripts. The modifications I have made are:

1. eyetrack_reading.py: added two command line parameters to specify the experiment introduction text:
  + --intro-file FILENAME. FILENAME specifies the name of the file containing the intro text at a single line. New lines for the eye-tracker software to display should be specified explicitly with  "\n".
  + --intro-text TEXT. TEXT is a single line (quoted) with the intro text. Again, new lines should be specified explicitly with "\n". This option is mostly useful if you call `eyetrack_reading.py` from another script.
  
2. randomizer.py: there was the following bug. If you have N conditions in the experiment, then the Latin Square order for the N-th participant would be 8, regardless of what N is (and even if N < 8). Fixed.
