# Matplotlib

### In the last Lesson 11/11, we had a homework to search about hot to use the Matplotlib. I searched about how to do different types of graphs:

```.py
# Function Graphing - Different types of graphs

import matplotlib.pyplot as plt


category = ['A', 'B', 'C']  # List with categories - Data X
values = [7, 32, 88]  # List with the values - Data Y

plt.figure(figsize=(9, 3))  # Size of the graph

plt.subplot(131)  # the figure has 1 row, 3 columns, and this plot is the first plot.
plt.bar(category, values,color="r")
plt.subplot(132)  # the figure has 1 row, 3 columns, and this plot is the second plot.
plt.scatter(category, values,color="b")
plt.subplot(133)  # the figure has 1 row, 3 columns, and this plot is the third plot.
plt.plot(category, values,color="g")
plt.suptitle('Different types of graphs')  # Graph title
plt.show()

# The subplot() function takes three arguments that describes the layout of the figure.
# The layout is organized in rows and columns, which are represented by the first and second argument.
# The third argument represents the index of the current plot.

```
![Screen Shot 2022-11-15 at 8 27 01](https://user-images.githubusercontent.com/111819437/201789099-712a6418-dc3d-4386-8e6b-729685f121be.png)
