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
