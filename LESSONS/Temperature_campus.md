# code
```.py
from matplotlib import pyplot as plt
import numpy as np

plt.style.use('ggplot')  # background theme

h=[57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0]
low=[53.0, 54.0, 54.0, 52.0, 54.0, 51.0, 53.0, 53.0, 50.0, 51.0, 52.0, 53.0, 49.0, 50.0, 50.0, 49.0, 50.0, 47.0, 50.0]
high= [58.0, 60.0, 61.0, 57.0, 56.0, 58.0, 58.0, 57.0, 56.0, 55.0, 54.0, 57.0, 54.0, 56.0, 53.0, 56.0, 53.0, 55.0, 52.0]

samples = []   # Empty list for samples
for i in range(len(h)):
    samples.append(i)  # Adding the value of i to the list sample

fig =plt.figure(figsize=(8,4))  # Size of the graph
plt.subplot(1,2,1)  # First graph
plt.plot(samples,h,color="#cdb4db")  # Graph line for h values
plt.plot(samples,low,color="#ffc8dd")  # Graph line for low values
plt.plot(samples,high,color="#ffafcc")  # Graph line for high values
plt.xlabel("Samples")  # print title in the x line
plt.ylabel("Temperature")  # print title in the y line

# Analyze the data
mean = []  # Empty list for mean
standard_dev = [] # Empty list for standard deviation
for i in range(len(h)):
    data = [h[i], low[i], high[i]]  # Create list with the data
    mean.append(np.mean(data))  # Add values of mean to the list mean
    standard_dev.append((np.std(data)))  # Add values of standard dev to the list standard deviation


plt.subplot(1,2,2)  # Second graph
plt.fill_between(samples,high,low,alpha=.5,linewidth=0,color="#f72585") # Show the high and low values in the graph
plt.errorbar(samples,mean,standard_dev, fmt="*")  # Error bar
plt.xlabel("Samples")   # print title in the x line
plt.ylabel("Temperature")   # print title in the y line
plt.suptitle('Temperature on Campus')  # Graph title
plt.show()
```
## Evidence
![Screen Shot 2022-11-20 at 19 37 00](https://user-images.githubusercontent.com/111819437/202897517-b8d515eb-fd47-4031-97a4-72fec6e68bd4.png)
