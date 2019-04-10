# MIDI-RANGER-Tutorials-Render
## PURPOSE 
If you don't have a good video card, but you want to render a high quality video (like 1080p60) using MIDI RANGER, this page will be helpful. Please pay attention: 
* If you want to render video like this, you must have more than 30Gb space in **"C:/"** (for temporary storage, typically 1080p60 may cast 5-7Gb per minute).  
## HOW
1. You need to be able to play the song that you need to render in game, and set the "resolution" in "Options" to what you want to render. (but don't need to set FPS)
2. Add  
    > ### -DUMPMOVIE -BENCHMARK -FPS=60 -NOTEXTURESTREAMING

    to launch options via steam. (or using cmd)
3. Run MIDI RANGER, and every frame will be saved in "~~~~".
4. Use other video software to compress those PNGs into a single video. (FFMpeg recommended)

    