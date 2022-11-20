![Screen Shot 2022-11-20 at 18 02 15](https://user-images.githubusercontent.com/111819437/202893903-a2e71433-028b-40ce-803b-5ae85426c06d.png)

# Code
```.py
from matplotlib import pyplot as plt
import numpy as np

plt.style.use('ggplot')  # background theme
ax = plt.axes()
ax.set_facecolor("#ffafcc")  # background color

h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0,
     54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0,
     52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0,
     49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0,
     48.0, 48.0, 48.0, 49.0]

sample = []  # empty list

for i in range(len(h)):  # Adding the value of i to the list sample
     sample.append(i)

plt.plot(sample,h,color="w",linestyle = "none", marker="*")  # Drawn the points in the graph in color white


m, b = np.polyfit(sample,h, 1)  # Discovers values of M and B in the equation and print
print(f"The module for the data is y={(round(m,2))}x+{(round(b,2))}")
print(f"|{'x'.center(10)}|{'y(x)'.center(10)}|")  # Print the title of the table
model_x = []  # Create empty list for X
model_y = []  # Create empty list for Y

for i in range (0, 31):
    model_x.append(i)  # add values of x to the list model_x
    y = m*i+b  # Equation
    model_y.append(y)  # add values of y to the list model_y
    y_str = f"{y:.2f}"  # Round the value to two decimal numbers
    x_str = f"{i:.2f}"
    print(f"|{(x_str).center(10)}|{str(y_str).center(10)}|") # Print the table

plt.plot(model_x, model_y, color='w')  # Drawn the line in the graph in color white
plt.title("Relative humidity")  # Graph Title
plt.ylabel("Relative humidity")  # print title in the y line
plt.xlabel("Sample")  # print title in the x line

plt.show()  # Show graph

```
## Evidence
![Screen Shot 2022-11-20 at 18 29 34](https://user-images.githubusercontent.com/111819437/202894940-06c0b9cd-914a-4d33-a589-fd1b0ac41bf5.png)


## Convert the following color in hex to rgb #e6e627

![WhatsApp Image 2022-11-20 at 18 46 00](https://user-images.githubusercontent.com/111819437/202895469-83ccbe34-8344-49c9-8345-49271a948de7.jpeg)

