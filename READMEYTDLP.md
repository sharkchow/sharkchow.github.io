## 在这份YT-DLP指南（2024年版）中，我们将探讨yt-dlp是什么，以及如何在您的Windows或Linux机器上下载和安装它。我们还将介绍必要的依赖项，包括FFmpeg，并指导如何使用yt-dlp下载视频。

## yt-dlp 指南
免责声明：本材料仅供参考。它并不构成对任何活动（包括非法活动）、产品或服务的认可。在使用我们的服务或依赖此处的任何信息时，您全权负责遵守适用的法律，包括知识产权法。对于因以任何方式使用我们的服务或此处包含的信息而造成的损害，我们不承担任何责任，除非法律明确要求。

## 目录 
什么是 yt-dlp？
如何下载和安装 YT-DLP？
安装依赖项：FFmpeg 和 FFProbe
如何在 Windows 和 Linux 中使用 YT-DLP。 
插件 yt-dlp 的高级用法。 
. yt-dlp 的优缺点。
常见问题解答：yt-dlp。
结语。 

## 1. 什麼是 yt-dlp?
   YT-DLP 是一个免费且开源的软件项目，是基于已停止维护的 youtube-dlc 项目而创建的（作为其分支）。yt-dlp 基于流行的 YouTube 下载器 youtube-dlc，但现在具有额外的功能和改进。该软件主要用于从 YouTube、Vimeo 和其他类似网站下载视频。 

下载和安装 yt-dlp 相对简单，但学习如何正确使用它可能需要一些时间。YT-DLP 是一个可在 Windows、macOS 和 Linux 操作系统上使用的命令行工具。由于没有“美丽”的前端 GUI，许多人会感到不适应，但它是目前最强大的 YouTube 下载器。 

## YT-DLP’s 有什么主要功能? 
网络选项： 更改 yt-dlp 与网络通信的方式。这包括选项，例 如设置代理、调整超时值和指定用户代理字符串。
跳过地理限制： 此功能允许您绕过可能基于位置阻止您访问特定视频的地理限制。您可以使用 yt-dlp 选项与 VPN 或代理一起绕过这些限制。
视频选择： 使用 yt-dlp，您可以从播放列表或频道选择要下载的视频。此外，您还可以下载整个播放列表和频道。 
下载选项： 此功能允许您控制下载过程。例如，您可以选择仅下载音频、仅下载视频或同时下载两者。您还可以设置视频质量和下载速度限制。
文件系统选项： 使用此功能，您可以指定已下载视频的输出目录和文件名模板。
缩略图图像： 与视频一起下载缩略图图像。您甚至可以指定图像格式和大小。
解决方案： 此功能为在下载过程中出现的问题提供各种解决方案。例如，您可以使用“-no-check-certificate”选项来绕过 SSL 证书验证。 
对失败的下载进行自动重试。 默认情况下，yt-dlp 会尝试三次下载视频，然后放弃并转到下一个。您还可以配置此次重试的次数。
视频格式选项： Yt-dlp 让您选择要下载的视频格式，例如 MP4、WebM 或 FLV。您还可以设置视频质量和分辨率。
字幕功能： 此 yt-dlp 选项允许您与视频一起下载字幕（嵌入）。您可以指定字幕格式和语言。
. 身份验证选项： 与某些网站进行身份验证，例如 YouTube 或 Vimeo。您可以使用用户名和密码或 API 密钥等选项进行身份验证。
. 后处理选项： 对已下载的视频执行各种后处理任务，例如合并或拆分视频文件、添加元数据或将视频转换为不同的格式。
. 与 SponsorBlock 集成： 此功能使您能够通过 SponsorBlock API 标记/删除 YouTube 视频中的赞助商部分。
2. 如何下載及安裝 YT-DLP?
前往 yt-dlp 官方 GitHub 存储库： https://github.com/yt-dlp/yt-dlp
向下滚动页面，直到看到下载按钮。这是一个内部锚点链接，会带您到 https://github.com/yt-dlp/yt-dlp#installation。
下载和安装 Yt-dlp
照片来自 Github
在这个安装页面上，向下滚动页面找到最新的发布文件。找到可执行文件，yt-dlp（推荐使用 zip 导入二进制文件的 Linux 或 BSD 版本）、yt-dlp.exe（适用于 Windows）或 yt-dlp_macOS（适用于 macOS）。如果您的操作系统不支持这些发布文件，请在此页面上向下滚动并找到“替代方法”以查找更多选项。 
• 选择您的平台或操作系统，下载适当的发布文件。 
下载和安装 Yt-dlp
照片来自 Github
a. 在Windows上下载及安装 yt-dlp。
为便于说明，我们将为 Windows 2022 Server 下载并运行 yt-dlp.exe。 
下载后，请验证大小、版本和公司。请看下面的截图。
下载和安装 Yt-dlp
注意： " yt-dlp.exe 文件不是安装程序，而是 yt-dlp 本身的可执行文件。在 Windows 环境中，可执行文件（带有 .exe 扩展名）是一个程序，点击后可直接运行，也可通过命令行执行。对于 yt-dlp您只需将 yt-dlp.exe 文件的目录中（例如 C:\ytdlp），并从那里直接运行。

b. 在 Linux (Ubuntu) 中下载和安装 yt-dlp.
为了说明问题，我们将在 Ubuntu 22.04 中下载和安装 yt-dlp 的最新版本。确保您的 Ubuntu 机器已经更新到最新版本。 
下面的命令从 GitHub 下载 yt-dlp 程序的最新版本，并将其安装在 /usr/local/bin 目录下，文件名为 yt-dlp。 
$ sudo wget https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -O /usr/local/bin/yt-dlp
1
$ 苏都 wget https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -O /usr/local/bin/yt-dlp
下载和安装 Yt-dlp
以下命令将 /usr/local/bin 目录中的 yt-dlp 文件的权限设置为允许所有用户（所有者、组和其他人）读取和执行该文件。 
$ sudo chmod a+rx /usr/local/bin/yt-dlp
1
$ 苏都 chmod a+rx /我们/本地/箱柜/yt-dlp
• 这个命令是必要的，以允许用户从命令行运行 yt-dlp 命令。
下载和安装 Yt-dlp
3.安装依赖项: FFmpeg 和 FFProbe
在继续使用 yt-dlp 之前，强烈建议您安装 FFmpeg 和 FFprobe。还有其他关于网络、元数据和其他杂项的“可选”依赖项， 但 FFmpeg 和 FFprobe 几乎是“必需”的。

FFmpeg 是处理视频、音频和其他多媒体文件的多媒体框架。yt-dlp 使用它执行各种多媒体操作，包括合并不同格式的视频或音频文件。没有它，yt-dlp 将无法合并所请求的格式。例如，您可能下载一个没有音频的 1080p 视频。 
FFProbe 是随 FFmpeg 一起提供的命令行工具。FFProbe 用于分析和从多媒体文件（如视频和音频）中提取信息。Yt-dlp 需要使用 FFProbe 从正在下载的多媒体文件中提取元数据。这些元数据包括视频或音频编解码器、分辨率、持续时间、比特率和其他有关多媒体文件的技术细节等信息。如果没有 FFprobe，yt-dlp 将无法提取这些元数据，并且它的某些功能可能无法正常工作。
下载并安装 Yt-dlp 的依赖项
照片来自 Github
在安装 FFmpeg 和 FFprobe 之前，请确保您的计算机已经更新到最新版本。
a. 在 Linux 上安装 FFmpeg 和 FFprobe。
要在 Linux 机器上（Ubuntu 22.04）安装 FFmpeg，请使用以下命令： 

$ sudo apt install ffmpeg
1
$ 苏都 适切 安装 ffmpeg
要检查安装和当前版本，请使用以下命令： 
$ ffmpeg -version
1
$ ffmpeg -版本
下载并安装 Yt-dlp 的依赖项
FFprobe 安装？ 安装 FFmpeg 包时会自动安装 FFprobe。无需额外安装 FFprobe。要测试 FFprobe 是否已安装，请使用“ffprobe”命令：

下载并安装 Yt-dlp 的依赖项
b. 在 Windows 上安装 FFmpeg 和 FFprobe。
请前往 https://ffmpeg.org/ 并下载 Windows 平台的 FFmpeg 包（.EXE 文件）。发布版本通常比 Git 主版本更稳定，后者会更频繁地发布。 
选择您需要的版本，下载 7z 或 zip 文件并解压缩。 
下载并安装 Yt-dlp 的依赖项
照片来自 Github
下载 FFmpeg 包并将其保存在任何您想要的位置。
我们创建了一个名为“PATH_Programs-ytdpl”的新文件夹，我们将移动并解压缩 FFmpeg 包到该文件夹中。 
在 ffmpeg-(文件名) > bin > 目录下，您将看到三个工具：ffmpeg、ffplay 和 ffprobe。将这三个应用程序移动（解压缩）到您的新文件夹中。 
下载并安装 Yt-dlp 的依赖项
记录路径（例如：C:\PATH_Programs -ytdlp），并前往“编辑系统环境变量”。此 Windows 实用程序允许您修改操作系统和计算机上运行的应用程序所使用的环境变量。我们接下来将定义的 PATH 环境变量指定了操作系统在查找可执行文件时应搜索的目录列表。
• 要打开此功能，请转到 Windows 搜索栏，输入“path”。
下载并安装 Yt-dlp 的依赖项
• 在“系统属性”>“高级”中，转到“环境变量”。
下载并安装 Yt-dlp 的依赖项
在“环境变量”中，在“管理员的用户变量”下选择 Path（1）> 然后单击“编辑”。 
下载并安装 Yt-dlp 的依赖项
• 新的“编辑环境变量”窗口将打开。单击“新建”（1）> 输入存储 FFmpeg 的路径（2）> 单击“确定”（3）。 
下载并安装 Yt-dlp 的依赖项
• 现在，无论何时您想从任何文件夹或位置运行 FFmpeg，计算机都会知道它的位置，并允许您使用它。 
现在，从 Windows 命令提示符中测试 FFmpeg 配置。打开“cmd”并键入“ffmpeg”。您应该会得到以下输出。 
下载并安装 Yt-dlp 的依赖项
现在，从 Windows 命令提示符中测试 FFmpeg 配置。打开“cmd”并键入“ffmpeg”。您应该会得到以下输出。

准备好用Seedbox提升您的下载体验了吗？

了解RapidSeedbox如何通过以下方式增强您的YT-DLP体验：快速且安全的下载，轻松流媒体播放，充足的存储空间和全天候访问

---
今天就用RapidSeedbox升级您的下载体验！
4. 如何在 Windows 和 Linux 中使用 YT-DLP。
正如您可能已经知道的那样，yt-dlp 是一个命令行工具，因此要使用它（在 Windows 或 Linux 上），您将需要通过命令提示符或终端运行。如果您已经下载并安装了 yt-dlp 及其依赖项，请打开终端。 

免责声明： 使用 yt-dlp 等工具从 YouTube 下载视频可能会侵犯内容创建者的服务条款、版权和知识产权。认识并遵守您所在司法管辖区有关下载和分发受版权保护的材料的适用法律和法规非常重要。本说明不构成法律建议，不应被视为法律建议。

a. 如何在 Windows 中使用 yt-dlp? 
yt-dlp 运行在命令行中，它没有前端 GUI。当您第一次在 cmd.exe 中运行它时（没有任何参数），您会注意到一个错误消息（例如以下消息）：“yt-dlp.exe：错误：您必须提供至少一个 URL”
使用 Yt-dlp
让我们继续访问帮助菜单。要查看所有选项的列表，请键入“yt-dlp --help”命令。类似以下菜单将显示在您的终端（或命令提示符）中：
使用 Yt-dlp
要使用 yt-dlp，请确保您在 yt-dlp.exe 所在的位置，并使用“yt-dlp（后跟 YouTube URL）”使用它，例如： 
yt-dlp https://www.youtube.com/watch?v=1PmJeP-TphM
1
yt-dlp https://www.youtube.com/watch?v=1PmJeP-TphM
使用 Yt-dlp
Yt-dlp 允许您使用参数在下载 YouTube 视频时提供更多选项。 
例如，您可以准确地告诉 yt-dlp 您想要的格式以及如何下载它。为此，您可能必须首先找出可用的格式：使用以下命令：
yt-dlp -F --list-formats https://www.youtube.com/watch?v=1PmJeP-TphM
1
yt-dlp -F --清单-格式 https://www.youtube.com/watch?v=1PmJeP-TphM
使用 Yt-dlp
现在，您可能想要下载格式为 (-f) 最佳质量视频和最佳音频（具有特定格式）的 YouTube 视频（即 https://www.youtube.com/watch?v=1PmJeP-TphM）；为此，请使用以下命令：
yt-dlp -f “bestvideo&#91;ext=mp4]+bestaudio&#91;ext=m4a]” https://www.youtube.com/watch?v=1PmJeP-TphM

1
2
yt-dlp -f "最佳视频&#91；绵延=mp4]+最佳音效&#91；绵延=m4a]" https://www.youtube.com/watch?v=1PmJeP-TphM
 
使用 Yt-dlp
要了解更多关于这些参数以及如何正确使用它们的信息，请使用“yt-dlp --help”命令。 
就是这样；我们使用 yt-dlp 下载了两个 YouTube 视频。
使用 Yt-dlp
b. Linux 下的 yt-dlp 命令
与 Windows 相同，在 Ubuntu Linux 中，如果您在终端控制台中键入 yt-dlp [without arguments]，您将收到一个错误消息。 
使用 Yt-dlp
• 如果需要查看 yt-dlp 帮助菜单，请使用以下命令 yt-dlp --help。
• 如果您想要使用最佳质量的视频和最佳质量的音频下载 YouTube 视频，请使用以下命令：
yt-dlp -f 'bv*+ba' https://www.youtube.com/watch?v=1PmJeP-TphM
1
yt-dlp -f bv*+ba https://www.youtube.com/watch?v=1PmJeP-TphM
使用 Yt-dlp
注意： 如果您看到以下警告消息：“您已请求合并多个格式（视频和音频），但尚未安装 FFmpeg。这些格式不会被合并。”，这意味着您尚未安装 FFmpeg... 要了解如何安装 FFmpeg，请返回“安装 FFmpeg”部分。 

现在，如果您想要为您的 YouTube 视频下载特定格式怎么办？一个有用的格式命令是“-F --list-formats”。例如，我们想列出视频上可用的格式 
yt-dlp -F --list-formats https://www.youtube.com/watch?v=1PmJeP-TphM
1
yt-dlp -F --清单-格式 https://www.youtube.com/watch?v=1PmJeP-TphM
使用 Yt-dlp
例如，从上面的输出中，您可以看到此 YouTube 视频可用于以 144p、360p 和 720p 的视频和音频分辨率进行下载。现在，让我们指定要下载的格式。 
我们将使用另一个视频作为示例。首先（如前所示）查看可用格式，然后使用命令“-f 'bv*[height=…]+ba'”指定格式。例如， 
yt-dlp -F --list-formats https://www.youtube.com/watch?v=9jw9W7kUBFk
1
yt-dlp -F --清单-格式 https://www.youtube.com/watch?v=9jw9W7kUBFk
yt-dlp -f 'bv*&#91;height=720]+ba' https://www.youtube.com/watch?v=9jw9W7kUBFk
1
yt-dlp -f 'bv*[height=720]+ba' https://www.youtube.com/watch?v=9jw9W7kUBFk
使用 Yt-dlp
• 使用以上一组命令将帮助您更具体地指定您想要下载的 YouTube 视频格式。而不是下载最高的（例如 4K），您可以指定音频和视频格式。 
另外，您会注意到此时没有显示 FFmpeg 警告消息。这是因为此时我们已经正确安装了 FFmpeg。 
5. dlp 插件的高级用法.
以下我们将为您展示 yt-dlp 插件的另外两个高级用法。我们将在 Linux 上展示这些示例。  

a. 配置 yt-dlp.conf 文件。 
yt-dlp 插件还提供了一系列默认选项，它会自动实现，包括首选视频格式，如 mkv、mp4、webm 等。要创建一个 yt-dlp 可以使用的配置文件，请在配置文件中输入支持的命令。配置文件可以从系统（/etc/yt-dlp.conf）、用户配置、主目录配置、便携式或主配置加载。 

使用文本编辑器从终端打开（或创建）yt-dlp.conf： 
sudo vim /etc/yt-dlp.conf
1
苏都 vim /等等/yt-dlp.conf
或 
sudo vi /etc/yt-dlp.conf
1
苏都 vi /等等/yt-dlp.conf
下面的配置文件是一个示例（但您可以根据自己的喜好进行自定义）。使用下面的配置，yt-dlp 将自动将所有视频保存在特定路径（/Youtube）中，并将它们重命名为 Title.extension。yt-dlp 默认将 YouTube 视频保存到其默认路径，并将 URL 作为主标题。 
此配置还将嵌入缩略图、元数据和英文字幕。 

使用 Yt-dlp
• 现在让我们尝试一下全新的 yt-dlp 配置： 
yt-dlp https://www.youtube.com/watch?v=z8HY1aVzZDM
1
yt-dlp https://www.youtube.com/watch?v=z8HY1aVzZDM
使用 Yt-dlp
使用此配置文件，您可以自动化整个 YouTube 下载过程。这可以节省时间，因为您不再需要为每一行视频下载输入配置。配置文件将使用您个性化的下载格式进行处理。

注意（适用于 Windows 用户）： 建议将此配置文件放置在“${APPDATA}/yt-dlp/config”中，并将其保存为 .txt。AppData 文件夹位于“C:\Users\\AppData\”下，通常是一个隐藏文件夹。在此配置文件中设置配置行类似于我们在本节中在 Linux 中所做的操作。

b. 使用 Bashrc 文件。 
使用 bashrc 文件是优化 yt-dlp 下载过程的另一种方式。这些文件包含 Bash shell 的 shell（命令行界面）设置。bashrc 文件在每次打开新的终端会话时执行，它可以用于配置 shell 的各种设置和别名。bashrc 文件对于 yt-dlp 来说非常有用，因为您可以使用它来设置别名或 shell 函数，简化 yt-dlp 的使用。例如，您可以创建一个别名，通过在终端中输入单个命令，自动下载您喜欢的格式和质量的视频。这可以节省您的时间，使得定期使用 yt-dlp 更加容易。

• 在 Ubuntu 中找到 .bashrc 文件，可以前往 home/ubuntu > .bashrc。
使用 Yt-dlp
• 使用以下任何一个文本编辑器打开 .bashrc 文件。 
sudo vi ~/.bashrc
1
苏都 vi ~/.bashrc
或者

sudo nano ~/.bashrc
1
苏都 纳米 ~/.bashrc
• 输入您想要的 yt-dlp 的 bashrc 别名。例如：
# yt-dlp aliases
alias ydl='yt-dlp'
alias ydlmp4='yt-dlp -f "bestvideo&#91;ext=mp4]+bestaudio&#91;ext=m4a]/best&#91;ext=mp4]/best"'
alias ydlmkv='yt-dlp -f "bestvideo&#91;ext=mkv]+bestaudio&#91;ext=mka]/best&#91;ext=mkv]/best"'
1
2
3
4
# yt-dlp 别名
别称 ydl=yt-dlp
别称 ydlmp4='yt-dlp -f "bestvideo[ext=mp4]+bestaudio[ext=m4a]/best[ext=mp4]/best"'
别称 ydlmkv=yt-dlp -f "bestvideo[ext=mkv]+bestaudio[ext=mka]/best[ext=mkv]/best"'
使用 Yt-dlp
要激活别名，请关闭并重新打开终端窗口或运行以下命令：
$ source ~/.bashrc
1
$ 消息来源 ~/.bashrc
现在，让我们测试一下别名。使用别名应该可以让我们在使用 yt-dlp 下载 YouTube 视频时更加轻松。例如，通过输入“ydlmp4”，您可以避免编写冗长的命令，例如 bestvideo[ext=mp4]+bestaudio[ext=m4a]/best[ext=mp4]/best。
• 现在有很多事情正在发生！正如您从下面的输出中所看到的那样...我们的别名正在工作，配置正在尝试嵌入缩略图、字幕、元数据等。此外，视频正在保存在（和使用）/Youtube/%(title)s.%(ext)s 中——其中标题是视频的名称，而不是 URL。 
使用 Yt-dlp
c. 使用 yt-dlp 将大量数据管理和下载到种子盒子中。 
如果您使用 yt-dlp 下载和管理大量数据，那么种子盒子（ 种子盒子 ）可能是一个很好的解决方案。种子盒子是专为匿名下载和上传数字文件（如种子、NZB、视频和音乐）而设计的远程 VPS 或专用服务器。 此外，由于种子盒子专为下载和上传而设计，它们通常提供高速下载。 

例如，您可以远程连接到您的种子盒子，并使用其强大的资源来使用 yt-dlp 下载视频。种子盒子还提供像 Plex 或 Kodi 这样的流媒体平台，以及其他管理您的媒体收藏的好方法。如果您以后决定更改格式、压缩或编码，种子盒子也配备了强大的媒体转换器，如 手刹。您可以使用 FTP 或 Sync 协议轻松下载所有媒体内容。

这种组合可以实现快速高效的下载和轻松管理所有下载内容。

6. yt-dlp的优点及缺点
虽然 yt-dlp 具有许多出色的功能和特点，使其成为最好的 YouTube 下载器之一，但它也有一些缺点需要您了解。 以下是使用 yt-dlp 的一些优点和缺点。

a. 优点:
免费且开源： yt-dlp 是完全免费的。它也是由一个强大的开发者社区维护的开源项目。
多平台支持： yt-dlp 可用于 Windows、Linux 和 macOS。这种多平台支持使其适用于广泛的用户。
多种下载选项： 虽然 yt-dlp 是最好的“下载 YouTube 视频”工具之一，但它还有其他选项，这些选项在其他视频下载器中很难看到，包括视频格式、字幕选择和缩略图图像。
自动重试：yt-dlp 具有一些出色的自动化功能。其中最好的功能之一是它可以自动重试下载失败的内容，节省您的时间和精力。
支持更多的网站和扩展： yt-dlp 不仅支持 YouTube，还支持 Vimeo 和优酷等其他网站。它还支持浏览器扩展，如 SponsorBlock，可以让您跳过 YouTube 视频中的赞助片段。
缺点:
没有图形用户界面(GUI)： 使用 yt-dlp 的一个缺点是缺乏 GUI。yt-dlp 是一个命令行工具，这可能不适合那些喜欢图形用户界面的用户。
需要配置：从我们的逐步指南中，您可能已经注意到 yt-dlp 需要一些配置知识。要使用 yt-dlp，您必须学习配置行以获取所需的输出格式、音频质量或其他选项。 
没有官方软件包： yt-dlp 没有适用于某些平台的官方软件包。如果您有技能和耐心从源代码构建或依赖第三方存储库，则没有官方软件包可能不会对您造成不利影响。 
法律问题： 下载 YouTube 视频在技术上违反了其服务条款。因此，公司可能会起诉您。然而，许多用户仍然决定这样做，而公司也没有惩罚用户下载他们的视频的意愿。然而，了解下载受版权保护的材料的法律影响仍然非常重要。
7. YT-DLP: 常见问题.
Q: 使用 yt-dlp 相对于使用 youtube-dl 有哪些优点？

A：yt-dlp 提供了额外的功能和选项，这些在 youtube-dl 中不可用。它还有一个活跃的开发社区，确保漏洞得到快速修复和新功能得到添加。请查看我们之前的部分： 优缺点。.

Q: 如何安装 yt-dlp？

A：您可以通过下载二进制可执行文件或通过操作系统的软件包管理器来安装 yt-dlp 在 Linux、Windows 或 macOS 上。要了解如何安装 yt-dlp，请返回“如何下载和安装 yt-dlp”部分。 

Q: 我可以使用 yt-dlp 下载不同格式的视频吗？

A：是的，您可以使用 yt-dlp 下载不同格式的视频。您可以使用命令行选项或编辑配置文件来指定格式。

Q: 使用 yt-dlp 下载 YouTube 视频是否合法？

A：YouTube 上的某些内容可能受版权保护，未经许可下载可能是非法的。从 YouTube 下载视频违反 YouTube 的服务条款。但仍然有许多人这样做，而 YouTube 已经决定不采取行动。 

Q: 我可以使用 yt-dlp 下载整个播放列表吗？

A：是的，yt-dlp 允许您通过指定播放列表的 URL 来下载整个播放列表。

Q: yt-dlp 是否支持字幕？

A：是的，yt-dlp 支持多种格式的字幕。您可以在下载中嵌入字幕并指定首选字幕语言。

Q: 我可以使用 yt-dlp 下载仅包含音频的文件吗？

A：是的，yt-dlp 允许您以多种格式（如 MP3 和 AAC）下载仅包含音频的文件。

Q: yt-dlp 是否在积极维护中？

A：是的，yt-dlp 由一组专业开发人员积极维护，定期发布更新和漏洞修复。.

8. 结语。
总之，yt-dlp 是一个功能强大、功能丰富的视频下载器。它已成为受欢迎的 youtube-dl 插件的最佳替代品。凭借其广泛的选项列表和对各种格式和视频站点的支持，yt-dlp 成为领先的 YouTube 下载平台并不足为奇。

如果您还没有尝试过 yt-dlp，我们鼓励您尝试一下。您很快就会发现为什么 yt-dlp 成为下载视频的首选。
