# QUIZ 020

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
## Evidence ![Screen Shot 2022-11-01 at 9 13 35](https://user-images.githubusercontent.com/111819437/199132458-8d5e828e-bea2-4c50-bf8a-95a52b0b6d4c.png)

## Truth Table and Circuit for Light = S1S2 + (S2+S3(notS1))S1
