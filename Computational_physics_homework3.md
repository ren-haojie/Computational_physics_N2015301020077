
```
import matplotlib.pyplot as plt
x=[]
t=[]
v=40
dt=0.01
endtime=5
x.append(10)
t.append(0)
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

