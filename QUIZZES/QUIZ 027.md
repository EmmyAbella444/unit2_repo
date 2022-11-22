# Quiz 027
![Screen Shot 2022-11-22 at 13 29 06](https://user-images.githubusercontent.com/111819437/203221681-dcb5ce06-fbb4-4779-afda-a533689a2ee9.png)


## Code
```.py
from matplotlib import pyplot as plt
import numpy as np

plt.style.use('ggplot')  # background theme

sensorA = [16,24,24,9,23,26,26,23,25,14]   # Lists for the sensors
sensorB = [2,19,25,10,11,24,17,7,24,17]
sensorC = [15,11,24,21,6,2,18,27,1,16]


samples = []   # Empty list for samples
for i in range(len(sensorA)):
    samples.append(i)  # Adding the value of i to the list sample

mean = []  # Empty list for mean
standard_dev = []   # Empty list for standard deviation
minimum = []   # Empty list for minimum values
maximum = []  # Empty list for maximum values
for i in range(len(sensorA)):
    data = [sensorA[i], sensorB[i], sensorC[i]]  # Create list with the data
    mean.append(np.mean(data))   # Add values of mean to the list mean
    maximum.append(max(data))  # Add values of maximum to the list maximum
    minimum.append((min(data)))  # Add values of minimum to the list minimum
    standard_dev.append((np.std(data)))   # Add values of standard dev to the list standard deviation

plt.fill_between(samples,minimum,maximum,alpha=.5,linewidth=0,color="#ffafcc")  # Show the maximum and minimum values in the graph
plt.errorbar(samples,mean,standard_dev, fmt="*")  # Error bar

plt.show()  # Show graph
```
## Evidence

![Screen Shot 2022-11-20 at 18 57 40](https://user-images.githubusercontent.com/111819437/202895891-eb080c98-2d66-4cd1-89bb-493f077c41df.png)

## Convert the following rgb color to hex to rgb: red=250, green=100, blue=10
![WhatsApp Image 2022-11-20 at 19 09 44](https://user-images.githubusercontent.com/111819437/202896373-65495b2f-d460-4565-abac-1bb630d7d81c.jpeg)


