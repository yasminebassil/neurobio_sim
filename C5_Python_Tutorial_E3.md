# Exercise 3 Solution

Here's the solution to Exercise 3. 

```
import math

def Nernst(outside,inside,valence):
  return 58/valence * math.log10(outside/inside)

print('Na+ reversal potential = ' + str(Nernst(140,14,1)) + ' mV')
print('K+ reversal potential = ' + str(Nernst(5,124,1)) + ' mV')
```
