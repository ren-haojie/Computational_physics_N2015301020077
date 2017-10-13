				   
    import math
    import matplotlib.pyplot as plt
    t=[]
    dt=0.01
    g=9.8
    end_time = 200
	a=30/180*math.pi
	b=45/180*math.pi
	c=60/180*math.pi
	theta = [a,b,c]
	t.append(0)
	x_1=[]
	v_x_1=[]
	y_1=[]
	v_y_1=[]
	x_1.append(0)
	y_1.append(0)
	v_x_1.append(600*math.cos(theta[0]))
	v_y_1.append(600*math.sin(theta[0]))
	for i in range(int(end_time/dt)):
	m=x_1[i]+v_x_1[i]*dt
	x_1.append(m)
	n=v_x_1[i]
	v_x_1.append(n)
	o=y_1[i]+v_y_1[i]*dt
	y_1.append(o)
	p=v_y_1[i]-g*dt
	v_y_1.append(p)
	print ('x_1[-1],y_1[-1]')

	x_2=[]
	v_x_2=[]
	y_2=[]
	v_y_2=[]
	x_2.append(0)
	y_2.append(0)
	v_x_2.append(600*math.cos(theta[1]))
	v_y_2.append(600*math.sin(theta[1]))
	for i in range(int(end_time/dt)):
	m=x_2[i]+v_x_2[i]*dt
	x_2.append(m)
	n=v_x_2[i]
	v_x_2.append(n)
	o=y_2[i]+v_y_2[i]*dt
	y_2.append(o)
	p=v_y_2[i]-g*dt
	v_y_2.append(p)
	print ('x_2[-1],y_2[-1]')
		
	x_3=[]
	v_x_3=[]
	y_3=[]
	v_y_3=[]
	x_3.append(0)
	y_3.append(0)
	v_x_3.append(600*math.cos(theta[2]))
	v_y_3.append(600*math.sin(theta[2]))
	for i in range(int(end_time/dt)):
	m=x_3[i]+v_x_3[i]*dt
	x_3.append(m)
	n=v_x_3[i]
	v_x_3.append(n)
	o=y_3[i]+v_y_3[i]*dt
	y_3.append(o)
	p=v_y_3[i]-g*dt
	v_y_3.append(p)
	print(' x_3[-1],y_3[-1]')

	plt.figure(figsize=(10,8))
	plt.plot(x_1,y_1,label="$30^\circ$",color="r")
	plt.plot(x_2,y_2,label="$45^\circ$",color="b")
	plt.plot(x_3,y_3,label="$60^\circ$",color="y")
	plt.title('the trial of the cannonball,no drag')
	plt.xlabel('x(m)')
	plt.ylabel('y(m)')
	plt.ylim(0,15000)
plt.xlim(0,40000)
plt.legend()
plt.show()
