# MIDI-RANGER-教程-渲染
## 目的 
如果你没有一个好的显卡，但你想用MIDI RANGER渲染一个高质量的视频（如1080p60），这个教程会很有帮助。请注意：
* 如果要渲染这样的视频，则你的硬盘可用空间必须大于30GB。（用于临时存储，通常1080P60的视频每分钟需要5-7GB）。

## 准备
####  如果你的“C:/”不缺少空间，则可以跳过此部分。这个步骤能够将PNG序列呈现到您想要的目录中，而不是默认的“C:/”。
1. 运行一遍 MIDI RANGER。
2. 前往
    > ### C:\Users\\[Username]\AppData\Local\MyProject4\Saved
    
    确保这个文件夹已经被创建。
3. 选择一个用来存放临时PNG序列的位置，比如:
    > ### F:\ScreenshotSaved
    注意：路径中不允许带有空格！
4. 以**管理员**权限打开cmd.exe，执行这条命令:
    > ### mklink /D C:\Users\\[Username]\AppData\Local\MyProject4\Saved\\Screenshots F:\ScreenshotSaved
    这一步完成后，你就会发现在  
    **"C:\Users\[Username]\AppData\Local\MyProject4\Saved"**  
    下出现了一个文件夹链接，名为 **"Screenshots"**。

## 步骤
### 主要部分
1. 您需要能够在游戏中播放需要渲染的歌曲，并将 **“选项”** 中的 **“分辨率”** 设置为您想要渲染的分辨率。（但不需要设置FPS）
2. 把  
    > ### -DUMPMOVIE -BENCHMARK -FPS=60 -NOTEXTURESTREAMING

    加到steam的启动选项中。（也可以作为cmd的附加参数）
3. 运行MIDI RANGER，所有游戏的画面都会被存储到你选择的文件夹里。
4. 使用视频压缩软件，将PNG序列压制成视频。（推荐使用FFMPEG）
### 后期工作
在这里，我将向你展示如何使用FFMpeg将渲染的PNG序列转换为视频。
1. 安装FFMpeg。   
[FFMpeg下载链接](http://ffmpeg.org/download.html)
2. 执行以下指令:  
    > ### ffmpeg -r 60-i F:\ScreenshotSaved\WindowsNoEditor\MovieFrame%5d.png -vcodec mpeg4 F:\ScreenshotSaved\WindowsNoEditor\test.mp4
    视频会被存储到：  
    **"F:\ScreenshotSaved\WindowsNoEditor\test.mp4"**。  

注意: 
* 你最好将压制的帧数设置为与导出的帧数一致的值。
* 这些参数可能并不完美，如果你有更好的参数，可以分享给大家。

这样你就得到了一个全新的视频，而PNG序列也就可以删除了。