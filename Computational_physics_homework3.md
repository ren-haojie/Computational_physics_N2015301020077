#1.2
the position of an object moving horizontallly with a constant velocity,v,.is described by the equation dx/dt=v. Assuming that the velocity is a constant,say v=40m/s,use the Euler method to solve for x as a function of time.Compare your result with the exact solution.

由dx/dt=v可解出x=v*t+a(a为常数）
用欧拉法解可得
x(t+dt)=x(t)+v*dt
代码如下
```
import matplotlib.pyplot as plt
import numpy as np
x=[]
t=[]
x_thory=[]
t_thory=[]
v=40
dt=0.01
endtime=5
x.append(10)
t.append(0)
t_thory=np.linspace(0,5,100)
x_thory=v*t_thory+10
for i in range(int(endtime/dt)):
	x.append(x[i]+v*dt)
	t.append(t[i]+dt)
	print(t[-1] ,x[-1])
    
plt.plot(t,x)
plt.xlabel('t')
plt.ylabel('x')
plt.title('x=40t+10')

plt.plot(t_thory,x_thory)
plt.xlabel('t_thory')
plt.ylabel('x_thory')


plt.show()

```
代码运行后的图像可以看出两条函数图像重合
[result](https://github.com/ren-haojie/Computational_physics_N2015301020077/commit/57d7a40be918da4f82456dbbc4a883ad25b453f0)
结果与结论：对于一次函数用欧拉法近似对于结果没有影响，与结果一致

