# QUIZ 022
![Screen Shot 2022-11-09 at 15 53 18](https://user-images.githubusercontent.com/111819437/200759744-228b05e9-9072-42f0-b69c-3bb887e59d75.png)



## Code to quiz 022
```.py
import random
random.seed(1234)  # Initiates in a specific number
def produce(n=int, m=int, s=int):
    print( f"|    x   |  y(x)  |")  # Table title
    for i in range (0,n):
        x = random.randint(0,100)
        y = x**(1/2*((m/s)**2)) # formula

        print(f"|{str(round(x,2)).center(8,' ')}|{str(round(y,2)).center(8,' ')}|")

sample = produce(5,3,2)
print(sample)
```
## Evidence

![Screen Shot 2022-11-09 at 14 22 34](https://user-images.githubusercontent.com/111819437/200745594-317fedcc-5f3c-4e3a-b633-b18b5bda5a3b.png)

## Flowdiagram

![Flowchart - QUIZZ 022](https://user-images.githubusercontent.com/111819437/200974778-449c577a-4a40-4532-b563-9b8abadfdb06.png)

## Proof that A (A + B) = A 
