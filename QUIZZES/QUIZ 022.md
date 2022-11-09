# QUIZ 022

## Code to quiz 022
```.py
import random
random.seed(1234)
def produce(n=int, m=int, s=int):
    print( f"|    x   |  y(x)  |")
    for i in range (0,n):
        x = random.randint(0,100)
        y = x**(1/2*((m/s)**2))

        print(f"|{str(round(x,2)).center(8,' ')}|{str(round(y,2)).center(8,' ')}|")

sample = produce(5,3,2)
print(sample)
```
## Evidence

## Flowdiagram
