
# Task 2: System Diagram
![Screen Shot 2022-11-09 at 14 29 56](https://user-images.githubusercontent.com/111819437/200759418-37b7f9b5-03aa-4d2c-9519-d639d2666938.png)

## Materials


## System


## Code

```.py
from pyfirmata import Arduino
import time
from Validate_input import validate_int_input

board = Arduino('/dev/cu.usbserial-1420')
print("Communication Successfully started")

A = True  # Starts A as True
B = True  # Starts B as True
C = True  # Starts C as True

while True:
    n = validate_int_input("Please enter the number that you want to see in the LEDs: ")  # Ask the user for a number and confirm if the user entered a number with the function validate input

    for i in range(8):
        if i % 2 == 0:  # Change B by multiples of 2
            B = not B
        if i % 4 == 0:
            A = not A  # Change A by multiples of 4
        C = not C  # Change C one time per loop

        if i == n:
            board.digital[12].write(int(A))       # Variable A attributed to port 12 in the arduino and send the value of A
            board.digital[9].write(int(B))        # Variable B attributed to port 9 in the arduino and send the value of B
            board.digital[5].write(int(C))        # Variable C attributed to port 5 in the arduino and send the value of C
            print(f"{i}={int(A)}{int(B)}{int(C)}")  # Print the number in base 2
            time.sleep(1)  # Pause one second to run the loop again

```

## Evidence

### Reflection
