# MIDI-RANGER-Common-Error
## PURPOSE ##
Here I will write some error easy to occur, and if you have have encountered other error which can be solved, you can put it here.
## CONTENT
### 1. KEYS CAN NOT BE RESET
> All the keys can only be pressed or lighted but can not be darkened and reset to its original location.  

#### Solutions:
This error may occur when you using an old **".mid"** file.
It's because old **".mid"** file only contains a note's **"start time"** and length, but no **"NOTE OFF"** signal.  

You need to edit this **".mid"** file using any DAW, select all note, set the **"OFF VELOCITY"** of every note event  to **0** rather than other value or Nothing.