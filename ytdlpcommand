## yt-dlp 参数详解
## yt-dlp 是一款功能强大的命令行工具，用于从 YouTube 等视频网站下载视频和音频。它提供了丰富的参数选项，可以满足各种下载需求。

### 常用参数
-x 或 --extract-audio: 只提取音频，不下载视频。
--audio-format：指定输出音频格式，如 mp3、m4a 等。
--audio-quality：设置音频质量，例如 320K 表示 320kbps。
-o：指定输出文件名和路径，可以使用模板。
--write-thumbnail：下载视频缩略图。
--embed-thumbnail：将缩略图嵌入到视频文件中。
--merge-output-format：指定合并后的视频格式。
--list-subs：列出视频的所有字幕。
--write-sub：下载字幕。
--embed-sub：将字幕嵌入视频中。

### 参数模板
%(title)s: 视频标题
%(id)s: 视频 ID
%(ext)s: 文件扩展名
%(format)s: 格式代码

### 示例
Bash
# 下载视频并提取音频，保存为 mp3 格式
yt-dlp -x --audio-format mp3 https://www.youtube.com/watch?v=dQw4w9WgXcQ

# 下载视频并嵌入字幕，输出文件名包含标题和 ID
yt-dlp --embed-sub -o "%(title)s-%(id)s.%(ext)s" https://www.youtube.com/watch?v=dQw4w9WgXcQ

# 下载视频播放列表，并保存到指定目录
yt-dlp -o "/path/to/save/%(playlist)s/%(playlist_index)s-%(title)s.%(ext)s" https://www.youtube.com/playlist?list=PL...
请谨慎使用代码。

### 其他常用参数
--playlist-start: 从播放列表的指定索引开始下载。
--playlist-end: 下载到播放列表的指定索引。
--match-filter: 过滤视频，只下载符合条件的视频。
--no-playlist: 不下载整个播放列表，只下载第一个视频。
--ignore-errors: 忽略下载错误，继续下载下一个视频。

### 高级用法
自定义配置文件: 创建一个配置文件，将常用的参数保存起来，方便以后使用。
使用 Python 脚本: 通过 Python 脚本调用 yt-dlp，实现批量下载、自定义处理等功能。
利用插件: yt-dlp 支持插件扩展，可以实现更复杂的功能。
注意事项
版权: 请尊重版权，仅下载自己拥有版权或公开授权的视频。
网络环境: 下载速度会受到网络环境的影响。
更新: yt-dlp 经常更新，建议使用最新版本。
更多信息
官方文档: [移除了无效网址]
中文文档: https://www.rapidseedbox.com/zh/blog/yt-dlp-complete-guide
通过合理地组合这些参数，你可以实现各种各样的下载需求，比如下载高清视频、提取音频、下载字幕、批量下载等等。

### 想了解更多关于 yt-dlp 的用法，可以尝试以下关键词进行搜索：

yt-dlp 参数详解
yt-dlp 下载视频
yt-dlp 下载音频
yt-dlp 下载字幕
yt-dlp 批量下载

## 希望这份详细的介绍能帮助你更好地使用 yt-dlp！
