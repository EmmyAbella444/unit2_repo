# QUIZ 021
## Code
```.py
def get_Truth():
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
        print(f"| {int(A)} | {int(B)} | {int(C)} | {' '*8}{int(D)}{' '*8}|")

print(get_Truth())
```
## Evidence
![Screen Shot 2022-11-04 at 21 59 25](https://user-images.githubusercontent.com/111819437/199978705-ff4866f9-5a29-419d-8f05-28f24b22f553.png)


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


