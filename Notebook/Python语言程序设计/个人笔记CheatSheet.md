# 个人笔记CheatSheet
## 编程技巧
### 字符串反序
对于需要反序的字符串 `string`, `string[::-1]` 就能实现反序，写成 `string[-1:0:-1]` 反而是错的。
## pyinstaller 笔记
如果要打包一个包含控制台交互的程序，比如带有 input() 的程序，

必须在 pyinstaller 打包时，指明

`--console`

否则程序不会响应 input() 语句。
