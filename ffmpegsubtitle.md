# 使用 ffmpeg 进行字幕格式转换
## 我们制作视频的时候经常会使用到字幕，而常见的字幕又有多种格式，例如 srt、ass、vtt 等

srt 简单、兼容性好，是最被广泛使用的格式
ass 支持颜色、文字特效，拥有比 srt 更多的高级功能
vtt 这种格式和 srt 几乎没什么太大区别
查看 ffmpeg 中所支持的字幕格式
### 使用下面的命令可以查看 ffmpeg 中所支持的字幕格式列表，以大写 S 开头的表示字幕格式

ffmpeg -encoders
ffmpeg 字幕格式转换命令
### 在 ffmpeg 中使用以下这样的命令格式来对字幕文件进行操作

ffmpeg -i <原字幕文件> <新字幕文件>
一些 ffmpeg 字幕格式转换示例

## 这里只列出了部分格式的示例，其他格式也是类似的使用方法

srt 转 ass
ffmpeg -i BladeRunner2049.srt BladeRunner2049.ass
ass 转 srt
ffmpeg -i BladeRunner2049.ass BladeRunner2049.srt
srt 转 vtt
ffmpeg -i BladeRunner2049.srt BladeRunner2049.vtt
关于中文字幕编码的错误

## 如果使用 ffmpeg 转换字幕时出现类似下面这样的错误信息

Invalid UTF-8 in decoded subtitles text; maybe missing -sub_charenc option
Error while decoding stream #0:0: Invalid data found when processing input
则需要为原字幕文件指定 GBK/GB2312 字符集编码

ffmpeg -sub_charenc GBK -i BladeRunner2049.srt BladeRunner2049.vtt


# 使用 ffmpeg 进行视频字幕压制

## 了解字幕压制的几种方式
## 首先介绍下 ffmpeg 进行字幕压制的常见方式。视频字幕通常有两种方式来进行压制：

### 内嵌字幕（Soft subtitles）：内嵌的字幕可以单独使用，通常与视频文件分开存储。
硬字幕（Hard subtitles）：硬字幕直接将字幕图像化，融入到视频画面中，后期无法分离。
内嵌字幕压制示例
内嵌字幕允许我们在观看视频时随意打开和关闭字幕，比较灵活。使用 ffmpeg 制作内嵌字幕的例子：

ffmpeg -i input.mp4 -i subtitle.srt -c copy -c:s mov_text output.mp4
参数解释：

input.mp4 你的视频文件。
subtitle.srt 你的字幕文件。
-c copy 拷贝所有流（视频、音频、字幕）。
-c:s mov_text 将字幕编码为 mov_text 格式，这是常用 MP4 文件中的字幕格式。
硬字幕压制示例
### 硬字幕直接在视频上绘制字幕，是最常见的字幕压制方式，你平时在网上下载观看的大部分大片基本都是这种方式。接下来我们介绍两种常见字幕格式（SRT 和 ASS）的硬字幕压制示例，因为它们使用的命令格式稍有不同

## SRT 字幕压制
### 使用 SRT 字幕进行硬字幕压制的命令如下：

ffmpeg -i input.mp4 -vf subtitles=subtitle.srt -crf 16 output.mp4
参数解释：

-vf subtitles=subtitle.srt 使用字幕滤镜(subtitles)将 SRT 字幕应用到视频上。
### ASS 字幕压制
### 相对于 SRT，ASS 字幕格式支持设置样式和文字特效。使用 ffmpeg 压制的命令为：

ffmpeg -i input.mp4 -vf ass=subtitle.ass -crf 16 output.mp4
参数解释：

-vf ass=subtitle.ass 使用字幕滤镜(ass)将 ASS 字幕应用到视频上。
### 在使用嵌入式字幕压制时不需要对视频进行重新编码，而使用硬字幕压制时，因为需要将文字融入到视频画面中，会进行重新编码，在上述硬字幕压制时可以设置一些视频编码参数，例如 -crf 16 等等，之前的视频转码教程讲过，这里不再赘述。

## 字幕文本样式
### 常见的字幕格式 SRT 和 ASS 他们有一些区别，SRT 不支持文字特效， 而 ASS 字幕格式支持丰富的样式和特效，可以用来制作一些花里胡哨的字幕效果。ASS 字幕文件各式也比较复杂，下面是一段简单的 ASS 字幕文件例子：

[Script Info]
; Script generated by FFmpeg/Lavc61.3.100
ScriptType: v4.00+
ScaledBorderAndShadow: yes
YCbCr Matrix: None

[V4+ Styles]
Format: Name, Fontname, Fontsize, PrimaryColour, SecondaryColour, OutlineColour, BackColour, Bold, Italic, Underline, StrikeOut, ScaleX, ScaleY, Spacing, Angle, BorderStyle, Outline, Shadow, Alignment, MarginL, MarginR, MarginV, Encoding
Style: Default,Arial,16,&Hffffff,&Hffffff,&H0,&H0,0,0,0,0,100,100,0,0,1,1,0,2,10,10,10,1

[Events]
Format: Layer, Start, End, Style, Name, MarginL, MarginR, MarginV, Effect, Text
Dialogue: 0,0:00:04.00,0:00:10.74,Default,,0,0,0,,I was at Agenda 2000 and one of the people who was there was Craig Mundy who is some kind of
Dialogue: 0,0:00:10.74,0:00:15.66,Default,,0,0,0,,high mucky muck at Microsoft. I think vice president of consumer products or something
Dialogue: 0,0:00:15.66,0:00:23.76,Default,,0,0,0,,like that. And I hadn't actually met him. I bumped into him at an elevator and an elevator and I
Dialogue: 0,0:00:23.76,0:00:29.12,Default,,0,0,0,,looked at his badge and said, I see you work for Microsoft. And he looked back at me and said,
Dialogue: 0,0:00:29.12,0:00:34.42,Default,,0,0,0,,oh yeah, and what do you do? And I thought he seemed just sort of a tad dismissive. I mean,
Dialogue: 0,0:00:34.46,0:00:40.68,Default,,0,0,0,,here's the archetypal guy in a suit looking at a scruffy hacker. And so I gave him the
Dialogue: 0,0:00:40.68,0:00:43.62,Default,,0,0,0,,thousand yard stare and said, I'm your worst nightmare.
### 在这个例子中，Style 部分定义的样式包括字体、字号、颜色、边框、阴影等。Dialogue 部分则描述了具体的字幕内容。可以使用 Aegisub 这类字幕编辑器来定制你的字幕样式

### 脚本程序下载

script.bat
### 使用方法是：下载 script.bat 文件，然后准备好视频文件和字幕文件(srt或者ass)，确保字幕文件名称和视频文件名称保持一致。然后将视频文件用鼠标托放到 script.bat 程序图标上即可自动运行。
