# 第十五讲-GUI设计
## GUI 的一般设计方法
使用tkinter模块创建一个图形用户界面应用程序的步骤：

（1）创建主窗口。

（2）在主窗口中添加各种控件并设置其属性。

（3）调整对象的位置和大小。

（4）为控件定义事件处理程序。

（5）进入主事件循环。
## 常用控件
Label：标签，用于显示说明文字。

Message：消息，类似标签，但可显示多行文本。

Button：按钮，用于执行命令。

Radiobutton：单选按钮，用于从多个选项中选择一个选项。

Checkbutton：复选框，用于表示是否选择某个选项。

Entry：单行文本框，用于输入、编辑一行文本。

Text：多行文本框，用于显示和编辑多行文本，支持嵌入图像。

Frame：框架，是容器控件，用于控件组合与界面布局。

Listbox：列表框，用于显示若干选项。

Scrollbar：滚动条，用于滚动显示更多内容。

OptionMenu：可选项，单击可选项按钮时，打开选项列表，按钮中显示被选中的项目。

Scale：刻度条，允许用户通过移动滑块来选择数值。

Menu：菜单，用于创建下拉式菜单或弹出式菜单。

Toplevel：顶层窗口，这是一个容器控件，用于多窗口应用程序。

**Canvas：画布，用于绘图。**这个就是第14讲主要介绍的控件。
## 事件驱动
要使得窗口形成事件驱动，必须
```python
Tk窗口对象名.mainloop()
```
使其进入事件循环。
## 对象定位手段
除了 pack() 自动紧凑排列以外，还可以
```python
对象名.place(x=x坐标,y=y坐标)
```
以及 grid() 方法，自学。
> 以下内容需要对照 PPT 自学
## IntVar
### get() 函数
可以获取复选框的编号。
