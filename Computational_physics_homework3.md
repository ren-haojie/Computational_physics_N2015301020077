#1.2
the position of an object moving horizontallly with a constant velocity,v,.is described by the equation dx/dt=v. Assuming that the velocity is a constant,say v=40m/s,use the Euler method to solve for x as a function of time.Compare your result with the exact solution.

由dx/dt=v可解出x=v*t+a(a为常数）
用欧拉法解
x(t+dt)=x(t)+v*dt
```
import matplotlib.pyplot as plt
x=[]
t=[]
v=40
dt=0.01
endtime=5
x.append(10)
t.append(0) of time
for i in range(int(endtime/dt)):
	x.append(x[i]+v*dt)
	t.append(t[i]+dt)
	print(t[-1] ,x[-1])
    
plt.figure(figsize=(10,5))
plt.plot(t,x,color="blue",linewidth=2)
plt.title('x=vt')
plt.xlabel('t')
plt.ylabel('x')
plt.ylim(0,200)
plt.show()
```
[result](https://github.com/ren-haojie/Computational_physics_N2015301020077/blob/master/python.png)

