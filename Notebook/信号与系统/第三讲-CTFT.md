# 第三讲-CTFT
## Sinc 函数
Sinc 和 Sa 函数的差别：

sinc(x)=sinc(&pi;\*x)/&pi;\*x=Sa(&pi;\*x)

Sa(x)=sin(x)/x=sinc(x/&pi;)

### sinc(x) 从负无穷到正无穷积分值为 1 的证明
&omega;<sub>c</sub> \* sinc(&omega;<sub>c</sub> \* t / &pi;) / &pi; -- CTFT -→ u(&omega; + &omega;<sub>c</sub>) - u(&omega; - &omega;<sub>c</sub>)

记左边时域函数为 x(t)，其傅里叶为矩形函数，记为 X(j&omega;)。

取 &omega; = 0，则计算出函数的直流增益，等于左边时域函数 x(t) 从负无穷到正无穷对 t 积分，即为所求积分。

X(j0) 等于 1，故所求积分值为 1，Q.E.D.
## 时域频域的对称特性
时域实偶，频域实偶；

时域实奇，频域虚奇。
## 插播一道考研真题
x(t) 的傅里叶变换为 X(j&omega;)，求 X(j&omega;) 的实部 Re{X(j&omega;)}。

[![BvtMm6.png](https://s3.ax1x.com/2020/11/11/BvtMm6.png)](https://imgchr.com/i/BvtMm6)

解：若直接变换太繁。题给信号是一个实信号，遇到求实部、虚部，要想到运用**奇偶分解**来做。

> 这里的内容需要查阅信号与系统课本或者 PPT 补上。
## 时域-频域对偶性的推导
[![BvNDDx.png](https://s3.ax1x.com/2020/11/11/BvNDDx.png)](https://imgchr.com/i/BvNDDx)

按步骤即可推导出对偶性，本质上还是傅里叶变换的定义式。

第三步是将 j&omega; 换成 t，t 换成 j&omega;。

所以：

**2&pi;x(-j&omega;) --FT-→ X(t)**
## 补充：广义帕塞瓦关系
```
∞                ∞
∫ x1(t)x2(t)dt = ∫ X1(jw)X2(-jw)dw 
-∞              -∞
```
