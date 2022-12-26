# QUIZ 032

![Screen Shot 2022-12-26 at 16 06 12](https://user-images.githubusercontent.com/111819437/209515858-cc979700-afd7-47a7-b00c-8007f591b3a3.png)


## Code
```.py
import requests
from matplotlib import pyplot as plt

plt.style.use('ggplot')  # background theme



req = requests.get('http://192.168.6.142/readings')
data = req.json()
readings = data['readings'][0]

Sensor_9 = []  # List for values of sensor 9 
for sample in readings:
    if sample['sensor_id'] == 9:
        Sensor_9.append(sample['value'])

size_window = 12 # Value for smoothed window
h_smth_9 = []  # Values smoothed
x_smth_9 = []  # Values smoothed
for i in range(0,len(Sensor_9),size_window):
     values = Sensor_9[i:i+size_window]
     h_smth_9.append(sum(values)/size_window)
     x_smth_9.append(i)

Sensor_10= []  # List for values of sensor 10 
for sample in readings:
    if sample['sensor_id'] == 10:
        Sensor_10.append(sample['value'])

h_smth_10 = []  # Values smoothed 
x_smth_10 = [] # Values smoothed
for i in range(0,len(Sensor_10),size_window):
     values = Sensor_10[i:i+size_window]
     h_smth_10.append(sum(values)/size_window)
     x_smth_10.append(i)

difference = [] # Calculating the difference 
for i in range (len(x_smth_9)):
    difference.append(h_smth_9[i]-h_smth_10[i])
    
# Empty list and for to create list with samples(Values of X)
x = []
for i in range(0,len(x_smth_9)):
    x.append(i)

# Print graph 
plt.figure(figsize=(11, 11))
plt.subplot(3,1,1)
plt.title("#Sensor 9")
plt.plot(x_smth_9[0:-1],h_smth_9[0:-1],color="#f72585")


plt.subplot(3,1,2)
plt.title("#Sensor 10")
plt.plot(x_smth_10[0:-1],h_smth_10[0:-1],color="#f72585")


plt.subplot(3,1,3)
plt.title("#Difference")
plt.plot(x,difference,color="#f72585")


plt.show()
```
## What are the three main operators used in boolean logic?
The three basic boolean operators are: AND, OR, and NOT.
![maxresdefault](https://user-images.githubusercontent.com/111819437/209516069-0b76af6e-61e8-4e94-a658-fee4d2e27a48.jpeg)
