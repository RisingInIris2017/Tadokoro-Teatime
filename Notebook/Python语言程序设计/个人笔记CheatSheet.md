# 个人笔记CheatSheet
## 编程技巧
### 字符串反序
对于需要反序的字符串 `string`, `string[::-1]` 就能实现反序，写成 `string[-1:0:-1]` 反而是错的。
## 编程实例与经验总结
```python
wordList = input('Enter a sentence:').split()
# 可以这样写，在这里 input 函数的返回值字符串直接调用了split()方法
```
```python
def cheer(teamName):
    print('''How do you spell winner?
    I know, I know!
    {}!
    And that\'s how you spell winner!
    Go {}!'''.format(' '.join(teamName.upper()),teamName))
    # join()方法：以调用此方法的字符串作为连接符，连接作为其参数的字符串中的各个字符
```
```python
def fcopy(inputFileName,outputFileName):
    inputFile = open(inputFileName,'r')
    outputFile = open(outputFileName,'w+')
    outputFile.write(inputFile.read())
    inputFile.close()
    # outputFile.close()
    # outputFile = open(outputFileName,'r')
    # 这里重新打开了文件，才正常读取。
    # flush()方法的正确使用方法是？
    outputFile.flush()
    outputFile.seek(0)
    # flush() 刷新后，文件指针指向文件尾部，因此再 read() 读不到内容。
    # 必须 seek(0) 将文件指针指向文件头部，再 read() 才能读到内容。
```
## pyinstaller 笔记
如果要打包一个包含控制台交互的程序，比如带有 input() 的程序，

必须在 pyinstaller 打包时，指明

`--console`

否则程序不会响应 input() 语句。
