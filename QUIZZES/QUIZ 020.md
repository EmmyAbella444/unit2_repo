# QUIZ 020
![Screen Shot 2022-11-03 at 10 58 43](https://user-images.githubusercontent.com/111819437/199634678-556e611e-7d58-4b48-843f-ccea9e677b25.png)

## CODE QUIZ 020
```.py
def get_Truth():
    A = True
    B = True
    C = False
    print("| A | B | C |")
    for i in range(8):
        C = not C      
        if i % 2 == 0:  # Change B by multiples of 2
            B = not B
        if i % 4 == 0:  # Change A by multiples of 4
            A = not A
        print(f"| {int(A)} | {int(B)} | {int(C)} |")

print(get_Truth())
```
## Evidence 

![Screen Shot 2022-11-01 at 9 13 35](https://user-images.githubusercontent.com/111819437/199132458-8d5e828e-bea2-4c50-bf8a-95a52b0b6d4c.png)

## Truth Table and Circuit for Light = S1S2 + (S2+S3(notS1))S1
| S1 	| S2 	| S3 	| S1S2 	| notS1 	| S2+S3 	| S2+S3(notS1) 	| (S2+S3(notS1))S1 	| S1S2+(S2+S3(notS1))S1 	|
|----	|----	|----	|------	|-------	|-------	|--------------	|------------------	|-----------------------	|
| 0  	| 0  	| 0  	| 0    	| 1     	| 0     	| 0            	| 0                	| 0                     	|
| 0  	| 0  	| 1  	| 0    	| 1     	| 1     	| 1            	| 0                	| 0                     	|
| 0  	| 1  	| 0  	| 0    	| 1     	| 1     	| 1            	| 0                	| 0                     	|
| 0  	| 1  	| 1  	| 0    	| 1     	| 1     	| 1            	| 0                	| 0                     	|
| 1  	| 0  	| 0  	| 0    	| 0     	| 0     	| 0            	| 0                	| 0                     	|
| 1  	| 0  	| 1  	| 0    	| 0     	| 1     	| 0            	| 0                	| 0                     	|
| 1  	| 1  	| 0  	| 1    	| 0     	| 1     	| 0            	| 0                	| 1                     	|
| 1  	| 1  	| 1  	| 1    	| 0     	| 1     	| 0            	| 0                	| 1                     	|

![Screen Shot 2022-11-04 at 17 56 49](https://user-images.githubusercontent.com/111819437/199932836-c8a2edfb-89a7-4a52-a2ab-a159af48d04a.png)



