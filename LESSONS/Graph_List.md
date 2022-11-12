# Lesson - Create a graph for two list
## We received two lists of number and create a graph 

```.py
import matplotlib.pyplot as plt
import numpy as np

x = [1, 2, 3, 1.5, 4, 2.5, 6, 4, 3, 5.5, 5, 2]
y = [3, 4, 8, 4.5, 10, 5, 15, 9, 5, 16,13,3]

plt.style.use('ggplot')  # Theme background
ax = plt.axes()
ax.set_facecolor("violet")  # Color background Violet
plt.scatter(x, y, color="r", marker='o')  # drawn a scatter plot graph in color red
plt.title("Scatter Plot of the data")  # Graph Title
plt.xlabel("X")  # Print "X" in the X label
plt.ylabel("Y=2.78x+-1.2")  # Print the equation in the y label



m, b = np.polyfit(x, y, 1)   # Discovers values of M and B in the equation and print
print(f"The module for the data is y={(round(m,2))}x+{(round(b,2))}")

model_x = []   # Create an empty list
model_y = []  # Create an empty list
for i in [1,6]:
    model_x.append(i)  # Add the values of X in the empty list
    y = m*i+b   # Equation 
    model_y.append(y)   # Add the values of y in the empty list


plt.plot(model_x, model_y, color='b', marker='.')  # Drawn the line in the graph in color blue
plt.show()  # Show graph
```
