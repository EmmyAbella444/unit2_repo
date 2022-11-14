# QUIZ 021

![Screen Shot 2022-11-09 at 14 23 27](https://user-images.githubusercontent.com/111819437/200745804-bfb1c236-a99f-4da6-bc34-c1e07e222172.png)


## Code
```.py
from Library import colors_purple
def get_Truth(table=""):
    A = True
    B = True
    C = True
    print("| A | B | C |AB+(not B)+(notBC)|")

    for i in range(8):
        C = not C
        if i % 2 == 0:  # Change B by multiples of 2
            B = not B
        if i % 4 == 0:  # Change A by multiples of 4
            A = not A
        D = bool((A and B) or (not B) or (not (C and B)))
        table += colors_purple(f"| {int(A)} | {int(B)} | {int(C)} | {' '*8}{int(D)}{' '*8}|\n")

    return table

print(get_Truth())
```
## Evidence

![Screen Shot 2022-11-15 at 8 32 38](https://user-images.githubusercontent.com/111819437/201789737-f8ed286c-f707-4810-8a5e-a03b6edd2cdb.png)


## Flowchart
![Flowchart - QUIZZ 017 (9)](https://user-images.githubusercontent.com/111819437/200097837-82c9751e-6862-4130-b8d0-68c7015f22b3.png)


## Truth Table and circuit for: X = ZW ⊕ (Z ⊕ Y(not W))

| W 	| Y 	| Z 	| ZW 	| notW 	| Z ⊕ Y 	| Z ⊕ Y(not W) 	| X = ZW ⊕ (Z ⊕ Y(not W)) 	|
|---	|---	|---	|----	|------	|-------	|--------------	|-------------------------	|
| 0 	| 0 	| 1 	| 0  	| 1    	| 1     	| 1            	| 1                       	|
| 0 	| 0 	| 0 	| 0  	| 1    	| 0     	| 0            	| 0                       	|
| 0 	| 1 	| 1 	| 0  	| 1    	| 0     	| 0            	| 0                       	|
| 0 	| 1 	| 0 	| 0  	| 1    	| 1     	| 1            	| 1                       	|
| 1 	| 0 	| 1 	| 1  	| 0    	| 1     	| 0            	| 1                       	|
| 1 	| 0 	| 0 	| 0  	| 0    	| 0     	| 0            	| 0                       	|
| 1 	| 1 	| 1 	| 1  	| 0    	| 0     	| 0            	| 1                       	|
| 1 	| 1 	| 0 	| 0  	| 0    	| 1     	| 0            	| 0                       	|

![Screen Shot 2022-11-05 at 12 25 21](https://user-images.githubusercontent.com/111819437/200098908-42fee63b-86cc-481b-87a8-4f36dd943b53.png)


