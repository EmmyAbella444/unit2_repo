
# Task 2: System Diagram - Part A
![Screen Shot 2022-11-09 at 14 29 56](https://user-images.githubusercontent.com/111819437/200759418-37b7f9b5-03aa-4d2c-9519-d639d2666938.png)

## Materials

1 arduino UNO,3 LEDs,1 USB,3 resistors,8 jumpers and 1 Breadboard

## System

![WhatsApp Image 2022-12-01 at 21 47 35 (1)](https://user-images.githubusercontent.com/111819437/205056836-00a28b1b-e555-4eb6-9254-327caf2b0dc2.jpeg)

## Code

```.py
from pyfirmata import Arduino
import time
from Validate_input import validate_int_input
from Library import colors_purple

board = Arduino('/dev/cu.usbserial-1420')
print("Communication Successfully started")



while True:
    n = validate_int_input("Please enter the number that you want to see in the LEDs: ") # Ask the user for a number and confirm if the user entered a number with the function validate input

    A = True  # Starts A as True
    B = True  # Starts B as True
    C = True  # Starts C as True
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
                print(colors_purple(f"{i}={int(A)}{int(B)}{int(C)}"))  # Print the number in base 2
                time.sleep(1)  # Pause one second to run the loop again


```

## Evidence
![Screen Shot 2022-12-01 at 21 45 01](https://user-images.githubusercontent.com/111819437/205056223-0f37c9a7-f503-4a96-b51e-6e32ccfd4d2a.png)

https://user-images.githubusercontent.com/111819437/205056932-096da479-c65c-44ff-932b-af3f35a34a1f.mp4


# Task 2: System Diagram - Part B

![Screen Shot 2022-11-12 at 16 19 50](https://user-images.githubusercontent.com/111819437/201462529-b5bfac82-be7b-40c7-9aeb-8da239116a61.png)

## Materials

1 arduino UNO,1 LED,1 USB,3 resistors,8 jumpers, 1 Breadboard and 2 Buttons

## System 
## Code
## Reflection

# Task 2: System Diagram - Part C

![Screen Shot 2022-11-16 at 19 31 35](https://user-images.githubusercontent.com/111819437/202157141-24e4aa95-9349-4e83-901d-f4d18e12432d.png)


## Materials
1 arduino UNO, 1 usb cable and 1 sensor DHT11.
## System 
![WhatsApp Image 2022-11-20 at 19 12 55](https://user-images.githubusercontent.com/111819437/202897017-bb397fcf-848c-4614-b0da-e1092b9e286b.jpeg)


## Code
```.py
import matplotlib.pyplot as plt
import serial
import time
arduino = serial.Serial(port='/dev/cu.usbserial-1420', baudrate=9600, timeout=.1)

plt.style.use('ggplot')  # Background theme

def read():
    data = ""
    while len(data)<1:
        data = arduino.readline()
    return data

humidity = []    # Empty list for humidity
temperature = []    # Empty list for temperature
for i in range(10):
    print(f"Reading Sample:{i}")  # message to allow the user know which sample is being read
    time.sleep(0.1)
    value = read()  # wait until data is in the port
    msg = value.decode('utf-8')
    if "Hello" not in msg:  # not analise the first line
        msg = msg.split(" ")   # Split by space
        tem = msg[1].split(":")  # Split the second term in the list by :
        hum = msg[0].split(":")  # Split the first term in the list by :
        humidity.append(float(hum[1][0:5]))  # Add the values of humidity to the list
        temperature.append(float(tem[1][0:5]))  # Add the values of temperature to the list


print(humidity,temperature)  # Print the lists

samples = []  # Empty list for samples
for i in range(len(humidity)):
    samples.append(i)  # Adding the value of i to the list sample

fig =plt.figure(figsize=(9,4))  # Size of the graphs 

plt.subplot(1,2,1)   # first plot
plt.plot(samples,humidity,color = "#cdb4db")
plt.xlabel("Samples")
plt.ylabel("Humidity")

plt.subplot(1,2,2)  # Second Plot
plt.plot(samples,humidity,color = "#ffafcc")
plt.xlabel("Samples")
plt.ylabel("temperature")

plt.suptitle('Temperature and Humidity on Asama Lounge') # Graphs title

plt.show()
```
## Video and Evidence
![Screen Shot 2022-11-18 at 12 25 20](https://user-images.githubusercontent.com/111819437/202896883-91b5e590-3366-4473-8d12-d219bde69f30.png)
![Screen Shot 2022-11-18 at 12 25 29](https://user-images.githubusercontent.com/111819437/202896886-2db200cc-119b-4033-810f-0348b6ef3c27.png)


https://user-images.githubusercontent.com/111819437/202896978-17d54fdf-ce6b-4fb7-aab9-895db7595065.mp4



## Reflection




