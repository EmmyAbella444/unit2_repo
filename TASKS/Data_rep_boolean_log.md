
# Task 1: Data Rep. and Boolean logic 

## Boolean Logic
Draw the circuit for the boolean equations provided


| Boolean Equation 	| Circuit 	|
|------------------	|---------	|
|   AB+not(A+B)               	|     ![TASK (1)](https://user-images.githubusercontent.com/111819437/199027024-f22597cc-e6a2-4013-a182-f690759f9ff6.png)    	|
|   not(A(A+B))+B               	|      ![Cópia de TASK](https://user-images.githubusercontent.com/111819437/199029661-4dc6cf19-d40e-4201-ba84-9f00ccd7621e.png)
|   ((not A) and B) or (A and B)   |   ![Cópia de Cópia de TASK](https://user-images.githubusercontent.com/111819437/199033423-569e2a0e-7301-4101-96d6-faf55afc8a76.png)
|  not(ACB)+not((A+C)B) |![Cópia de Cópia de Cópia de TASK](https://user-images.githubusercontent.com/111819437/199036622-65925df6-586a-4161-895f-9baf71dca03d.png)
| not(b1b2b3)+not(b1+b3)(b1+b2)                 	| ![QUIZ 019 (1)](https://user-images.githubusercontent.com/111819437/199040567-3ae6da06-cfdd-46ad-acbb-a751edbb7b8d.png)
        	
## Get the Equation
### Write the boolean equation for the circuit shown
![Screen Shot 2022-11-03 at 10 55 14](https://user-images.githubusercontent.com/111819437/199634427-61bd4c69-3fca-49c7-98b2-4c5320052670.png)

![Screen Shot 2022-11-02 at 8 00 48](https://user-images.githubusercontent.com/111819437/199358282-aa6774b9-e83c-4b0e-a417-3603afd763fc.png)

![Screen Shot 2022-11-03 at 10 51 43](https://user-images.githubusercontent.com/111819437/199634124-ec8cc2c4-9ce1-4ab2-8356-fab1ebfc4d12.png)


## Truth table
### Write the truth table for the equations below

### X = A and B

| A 	| B 	| X=AB 	|
|---	|---	|------	|
| 0 	| 0 	| 0    	|
| 0 	| 1 	| 0    	|
| 1 	| 0 	| 0    	|
| 1 	| 1 	| 1    	|

### Out = input1 or input2

| Input 1 	| Input 2 	| Input 1 or Input 2  	|
|---------	|---------	|---------------------	|
| 0       	| 0       	| 0                   	|
| 1       	| 0       	| 1                   	|
| 0       	| 1       	| 1                   	|
| 1       	| 1       	| 1                   	|

### Light = not(S1) + not(S2 + S3) + S1S2not(S3)

| S3 	| S2 	| S1 	| not(S1) 	| S2+S3 	| not(S2+S3) 	| S1S2 	| not(S3) 	| S1S2not(S3) 	| (not(S1))+(not(S2+S3)) 	| (not(S1))+(not(S2+S3))+(not(S2+S3)) 	|
|----	|----	|----	|---------	|-------	|------------	|------	|---------	|-------------	|------------------------	|-------------------------------------	|
| 0  	| 0  	| 0  	| 1       	| 0     	| 1          	| 0    	| 1       	| 0           	| 1                      	| 1                                   	|
| 0  	| 0  	| 1  	| 0       	| 0     	| 1          	| 0    	| 1       	| 0           	| 1                      	| 1                                   	|
| 0  	| 1  	| 0  	| 1       	| 1     	| 0          	| 0    	| 1       	| 0           	| 1                      	| 1                                   	|
| 0  	| 1  	| 1  	| 0       	| 1     	| 0          	| 1    	| 1       	| 1           	| 0                      	| 1                                   	|
| 1  	| 0  	| 0  	| 1       	| 1     	| 0          	| 0    	| 0       	| 0           	| 1                      	| 1                                   	|
| 1  	| 0  	| 1  	| 0       	| 1     	| 0          	| 0    	| 0       	| 0           	| 0                      	| 0                                   	|
| 1  	| 1  	| 0  	| 1       	| 1     	| 0          	| 0    	| 0       	| 0           	| 1                      	| 1                                   	|
| 1  	| 1  	| 1  	| 0       	| 1     	| 0          	| 1    	| 0       	| 0           	| 0                      	| 0                                   	|

### Login = not(P1P2P3) + not((P3not(P2P1))) + not(P1 + P3)
| P1 	| P2 	| P3 	| P1P2 	| P1P2P3 	| not(P1P2P3) 	| not(P1P2) 	| (P3)not(P1P2) 	| not((P3)not(P1P2)) 	| P1+P3 	| not(P1+P3) 	| (not(P1P2P3))+not((P3)not(P1P2)) 	| (not(P1P2P3))+(not((P3)not(P1P2)))+(not(P1+P3)) 	|
|----	|----	|----	|------	|--------	|-------------	|-----------	|---------------	|--------------------	|-------	|------------	|----------------------------------	|-------------------------------------------------	|
| 0  	| 0  	| 0  	| 0    	| 0      	| 1           	| 1         	| 0             	| 1                  	| 0     	| 1          	| 1                                	| 1                                               	|
| 0  	| 0  	| 1  	| 0    	| 0      	| 1           	| 1         	| 1             	| 0                  	| 1     	| 0          	| 0                                	| 0                                               	|
| 0  	| 1  	| 0  	| 0    	| 0      	| 1           	| 1         	| 0             	| 1                  	| 0     	| 1          	| 1                                	| 1                                               	|
| 0  	| 1  	| 1  	| 0    	| 0      	| 1           	| 1         	| 1             	| 0                  	| 1     	| 0          	| 0                                	| 0                                               	|
| 1  	| 0  	| 0  	| 0    	| 0      	| 1           	| 1         	| 0             	| 1                  	| 1     	| 0          	| 1                                	| 1                                               	|
| 1  	| 0  	| 1  	| 0    	| 0      	| 1           	| 1         	| 1             	| 0                  	| 1     	| 0          	| 0                                	| 0                                               	|
| 1  	| 1  	| 0  	| 1    	| 0      	| 1           	| 0         	| 0             	| 1                  	| 1     	| 0          	| 1                                	| 1                                               	|
| 1  	| 1  	| 1  	| 1    	| 1      	| 0           	| 0         	| 0             	| 1                  	| 1     	| 0          	| 1                                	| 1                                               	|


## Data Conversion
Information can be represented in different systems, for example the number 10  in decimal (system base 10) can be represented in binary (system base 2) as 1010 or 12 in base 8. 

It is critical for you to understand how to represent information in different ways, this will help you visualize how the computer processes data.

![Screen Shot 2022-11-04 at 16 34 45](https://user-images.githubusercontent.com/111819437/199918065-9120535b-0bdc-48f4-9139-54474b6f03f2.png)

   
