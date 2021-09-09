# Exercise 5 Solution

```
plt.figure()
plt.figure(figsize=(12,4))

plt.subplot(1,2,1) 
plt.plot(t,ina,'b')
plt.plot(t,ik,'r')
plt.xlabel('t')
plt.ylabel('Current')

plt.subplot(1,2,2) 
plt.plot(ina,ik)
plt.xlabel('I_Na')
plt.ylabel('I_K')
```
