# SpleeterGUI-backup
SpleeterGUI - 音乐源分离桌面应用程序 https://makenweb.com/SpleeterGUI

### 英特尔奔腾和赛扬CPU 无法运行 spleeter

无需安装 python 或 spleeter，此应用程序包含预装了 spleeter 的便携式 python 版本。

官网说在 2023 年初从我的网站上删除之前，我会在短时间内提供此最终版本

此仓库仅作为备份

英特尔奔腾和赛扬CPU 无法运行 spleeter
如果您没有运行 intel i5/7/9 或 Ryzen 5/7 或不确定您的 CPU 是否支持 AVX，请在尝试安装或运行 spleeter 之前使用AVXcheck 实用程序。


常见问题

#1：导入错误：DLL 加载失败：动态链接库 (DLL) 初始化例程失败。
无法加载本机 TensorFlow 运行时。
TLDR; TensorFlow 无法运行，因为你的 CPU 不支持它。

python 包“TensorFlow”有问题，它无法在您的计算机上运行。
您的 CPU 型号不支持 AVX 指令集。
Intel Pentium & Celeron CPU 无法运行 sleeter。
对于 SpleeterGUI 2.5 及更高版本，顶部菜单栏中有一个 spleeter 核心更新功能，单击“帮助”，然后单击“Spleeter 核心升级”。
这应该使 python 的包管理器完成安装并纠正安装中的任何错误。
可以在这里找到更多信息 https://github.com/tensorflow/tensorflow/issues/31033

#2：输出文件夹包含单独的零件文件，但它们都是相同的。
SpleeterGUI 与除预训练模型文件之外的所有内容打包在一起，这些文件是在您首次运行每个部件模式（2stem、4stem、5stem）时获取的。
一旦下载了其中的每一个，就不需要进一步下载。
如果您的所有输出文件都相同，那么 Python 的这个下载过程已被防病毒或防火墙阻止。
确保 Python 可以下载并重试。

#3: save_path 为 None 时无法加载
类似于上面的问题#2。
当 python 下载预训练模型文件时出现问题。
修复方法是删除它们并再次运行。
转到C:\Users\<yourname>\AppData\Roaming\SpleeterGUI\pretrained_models并删除 2stem、4stem、5stem 文件夹。

#4：未找到 VCRUNTIME.DLL
您需要从 Microsoft 安装 vc_redist.x64
选择 vc_redist.x64.exe


#5:错误：需要以下参数：-i/--inputs
您正在运行使用不同命令行序列的旧版本的 spleeter。通过单击“UpdateSpleeter core”升级到最新版本或手动运行命令

#6: jitdebug 错误
Spleeter 应用程序发生了可怕的事情，您需要从这里获取一个新副本。
常见问题

#1：为什么 2.6 版的下载量更大？
SpleeterGUI 现在附带运行所需的所有文件。
以前的版本没有预训练模型文件，因为它们在初始安装程序中添加了太多内容，但这被证明是有问题的，因为 Python 需要下载权限并且一些反病毒/反恶意软件阻止了它（参见常见问题 2 和 3）

#2：一些输出词干在开头有一个咔哒声
spleeter 软件中存在一个错误，会导致音频的第一帧出现咔哒声，Deezer 已意识到该问题，并且应该很快就会修复。
从 1.5.1 开始到当前（在撰写本文时）1.5.4 的 Spleeter 版本已知具有此功能。
当 Deezer 应用修复后，您可以通过单击“帮助 -> Spleeter 核心更新”来升级您的 spleeter 版本。

如果您想将 spleeter 版本降级到 1.4.3，请在出现弹出/点击问题之前下载此 python 文件夹
并在此处替换 python 文件夹 C:\Users\<YOURNAME>\AppData\Roaming\SpleeterGUI

#3：是否有 Apple Mac 版本？
我的 GUI 项目只能在 Windows 上运行，也许试试https://github.com/Andrew5Pun/Spleet-It。

如果您知道如何操作，您仍然可以通过在终端中键入命令来运行 Spleeter ...
可以在此处找到视频教程https://www.youtube.com/watch?v=cFj5heNlW98


使用图形处理器
如果可以，Spleeter 现在将自动使用 GPU。

一些有用的命令
这些将在高级页面中运行，其中显示“执行命令”

卸载spleeter -m pip uninstall spleeter tensorflow
安装 spleeter -m pip install spleeter
更新sleeter -m pip install --upgrade spleeter

训练狂欢
我还没有能够成功地训练 spleeter。
SpleeterGUI 3+ 中确实存在训练和添加自定义模型的能力，但在我让它工作之前被禁用。

请求协助
如果您已尝试此页面上的所有内容，请检查 https://github.com/boy1dr/SpleeterGui/issues 以查看您的问题是否已得到处理。
否则在该页面上提出问题。



推荐的电脑规格
英特尔 i5（第 4 代+）
8GB内存
Windows 10 64 位
Nvidia GTX1050 或更好（如果使用 CUDA 方法）
经过测试的硬件运行良好
英特尔 i5 4460、8GB 内存、GTX1660ti
英特尔 i7 7700、16GB 内存、GTX1060
锐龙 5 3600、32GB 内存、GTX1660ti
不推荐
英特尔赛扬处理器
视窗 32 位
Windows 7的
视窗XP
~2011 年之前购买的计算机


如何使用
下载并运行安装程序。然后双击 SpleeterGUI.exe 桌面快捷方式运行它。
要分离的部分（人声/伴奏/贝司等）
重新组合 选择将哪些词干重新组合在一起（如果您正在学习鼓并且只想从一堆歌曲中删除鼓，则很有用）
全带宽：这可以实现全质量处理，但结果会因歌曲而异。
保存到：点击该按钮，为分离的歌曲选择放置位置。
选择 1 首或多首歌曲并将它们拖入应用程序以开始处理。
对于 2.6 之前的 SpleeterGUI 版本...
第一次处理歌曲时，spleeter 下载一些资源文件时会有延迟。
如果输出文件夹中没有文件或您看到错误消息，则说明出现了问题。最常见的情况是您的计算机没有满足运行 spleeter 的最低要求。
如果您遇到问题，请检查 https://github.com/boy1dr/SpleeterGui/issues 以查看 anser 是否存在，否则会创建一个新问题，我会检查一下。
