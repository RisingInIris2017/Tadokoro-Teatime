# 个人笔记CheatSheet
## pyinstaller 笔记
如果要打包一个包含控制台交互的程序，比如带有 input() 的程序，

必须在 pyinstaller 打包时，指明

`--console`

否则程序不会响应 input() 语句。
