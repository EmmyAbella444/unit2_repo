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
