# MIDI-RANGER-Tutorials-Render
## PURPOSE 
If you don't have a good video card, but you want to render a high quality video (like 1080p60) using MIDI RANGER, this page will be helpful. Please pay attention: 
* If you want to render video like this, you must have more than 30Gb space. (for temporary storage, typically 1080p60 may cast 5-7Gb per minute)

## PREPARE
####  You can escape this part if your "C:/" does not lack space. If you do like this, you will be able to render PNG sequence to a directory you want rather than defaultly in "C:/".
1. Run MIDI RANGER Casually.
2. Go to
    > ### C:\Users\\[Username]\AppData\Local\MyProject4\Saved
    
    make sure this directory exists.
3. Choose a location that you want to save the temporary PNG files. For example:
    > ### F:\ScreenshotSaved
    Caution: Space is **not** allows in this directory.
4. Open cmd as **administrator**, run this command:
    > ### mklink /D C:\Users\\[Username]\AppData\Local\MyProject4\Saved\\Screenshots F:\ScreenshotSaved
    After this you will find a new folder link in 
    **"C:\Users\[Username]\AppData\Local\MyProject4\Saved"**  
    which called **"Screenshots"**.  

## HOW
### MAIN
1. You need to be able to play the song that you need to render in game, and set the "resolution" in "Options" to what you want to render. (but don't need to set FPS)
2. Add  
    > ### -DUMPMOVIE -BENCHMARK -FPS=60 -NOTEXTURESTREAMING

    to launch options via steam. (or using cmd)
3. Run MIDI RANGER, and every frame will be saved in the directory you choose before.
4. Use other video software to compress those PNGs into a single video. (FFMpeg recommended)
### AFTER WORK
Here I will show you how to transfer your rendered PNG sequence into video using FFMpeg.  
1. Install FFMpeg.  
[FFMpeg Download link](http://ffmpeg.org/download.html)
2. Run this command:  
    > ### ffmpeg -r 60-i F:\ScreenshotSaved\WindowsNoEditor\MovieFrame%5d.png -vcodec mpeg4 F:\ScreenshotSaved\WindowsNoEditor\test.mp4
    Then the video will be rendered to **"F:\ScreenshotSaved\WindowsNoEditor\test.mp4"**.  

Caution: 
* you are supposed to let the Frame Rate same with what you render.  
* Maybe this parameters is not perfect, you can share us your parameters.

Then you get a brand new video, and you can delete PNG files so that you can render next time.