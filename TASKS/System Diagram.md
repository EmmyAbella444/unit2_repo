
# Task 2 - System Diagram
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

A = True
B = True
C = True

while True:
    n = validate_int_input("Please enter a number: ")  # Ask the user for a number

    for i in range(8):
        if i % 2 == 0:  # Change B by multiples of 2
            B = not B
        if i % 4 == 0:
            A = not A  # Change A by multiples of 4
        C = not C  # Change C one time per loop

        if i == n:
            board.digital[12].write(int(A))       # Variable A attributed to port 12 in the arduino
            board.digital[9].write(int(B))        # Variable B attributed to port 9 in the arduino
            board.digital[5].write(int(C))        # Variable C attributed to port 5 in the arduino
            print(f"{i}={int(A)}{int(B)}{int(C)}")
            time.sleep(1)  # Pause one second to run the loop again

```

## Evidence

### Reflection
