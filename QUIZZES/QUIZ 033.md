# QUIZ 033

## CODE
```.py
import requests
import numpy as np
from matplotlib import pyplot as plt
from matplotlib.gridspec import GridSpec
from Library import get_sensor
from Library import smoothing


plt.style.use('ggplot')  # background theme

sensors = [6,8,9,10]
values = []
for s in sensors:
    # Get the values from the server
    value = get_sensor(id=s)
    # Smooth the data with a sie of 12 samples
    x, smoothed_value = smoothing(data=value[0:501])
    values.append(smoothed_value)

# Calculate the mean of the four sensors
mean_per_hour = []
for i in range(len(values[0])):
    # list comprehension
    data = [values[n][i] for n in range (len(sensors))]
    mean_per_hour.append(sum(data)/len(sensors))
print(f"Ready for plotting")

fig=plt.figure(figsize=(10,8))
gs = GridSpec(4,4,figure=fig)
# plot the mean of the sensors
ax = fig.add_subplot(gs[:,0:3]) # all the rows, col 0 to 2
plt.title("Average of sensors")
plt.plot(x,mean_per_hour,color="#f72585")
plt.ylim([20,28])
plt.xlabel("Samples per hour")
plt.ylabel("Celsius")

for row,my_color in [(0,"#f72585"), (1,"#f72585"), (2,"#f72585"),(3,"#f72585")]:
    ax = fig.add_subplot(gs[row,3])   # gs [row,col]
    plt.title(f"Sensor #{sensors[row]}")
    plt.plot(x,values[row],color= my_color)
    plt.tick_params('x', labelbottom=False)


plt.tick_params('x', labelbottom=True)
plt.show()

```
## EVIDENCE
