这是由msc二进制脚本文件反编译出的纯文本脚本。这组纯文本脚本完全还原了msc的所有内容。

每个脚本开头有两个table，每个entry包含了一个index和一个offset，offset的具体指向位置不明。

table之后就是指令了。
每个指令操作码由P、M、D、V、4、S、T中的一个开头，其中：
P开头的指令应该是司流程控制；
M开头的指令一部分是负责图片立绘显示；
D指令较少，部分意义不明；
V指令司声音控制；
S指令功能较杂；
T指令司文本显示；
4指令意义不明。

指令第二部分，若已解析则为
S- SetWindowCaption("紧紧将彼此的手相牵。")
这种形式，该指令将窗口标题设置为引号中的字符串。
未解析的话则为
P- i2(2m(0))
这种形式。表示这是P指令的第二条指令，指令传入参数为2m(0)。

Xm(Y)：Y为该参数的mode，是一个单字节变量，X为参数，是一个四字节变量。