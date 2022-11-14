# QUIZ 022
![Screen Shot 2022-11-09 at 15 53 18](https://user-images.githubusercontent.com/111819437/200759744-228b05e9-9072-42f0-b69c-3bb887e59d75.png)



## Code to quiz 022
```.py
from Library import colors_purple
import random
random.seed(1234)  # Initiates in a specific number
def produce(n=int, m=int, s=int,table=""):
    print( f"|    x   |  y(x)  |")  # Table title
    for i in range (0,n):
        x = random.randint(0,100)
        y = x**(1/2*((m/s)**2)) # formula

        table += colors_purple(f"|{str(round(x,2)).center(8,' ')}|{str(round(y,2)).center(8,' ')}|\n")
    return table

sample = produce(5,3,2)
print(sample)
```
## Evidence
![Screen Shot 2022-11-15 at 8 34 02](https://user-images.githubusercontent.com/111819437/201789999-21cba870-c3f0-42df-8fb7-b30700a97383.png)


## Flowdiagram

![Flowchart - QUIZZ 022](https://user-images.githubusercontent.com/111819437/200974778-449c577a-4a40-4532-b563-9b8abadfdb06.png)

## Proof that A (A + B) = A 

| A 	| B 	| A + B 	| A(A + B) 	|
|---	|---	|-------	|----------	|
| 0 	| 0 	| 0     	| 0        	|
| 0 	| 1 	| 1     	| 0        	|
| 1 	| 0 	| 1     	| 1        	|
| 1 	| 1 	| 1     	| 1        	|

Colum *A* and Colum *A(A + B)* are equal
