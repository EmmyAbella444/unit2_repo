# QUIZ 025

![Screen Shot 2022-11-16 at 18 45 58](https://user-images.githubusercontent.com/111819437/202146569-e3118522-fe03-4492-b168-d3b8f5517e08.png)


## Code

```.py
from matplotlib import pyplot as plt

print(f"|{'x'.center(10)}|{'y(x)'.center(10)}|")  # Print the title of the table
x_out = []  # Create empty list for X
y_out = []  # Create empty list for Y
st = -10.2
for _ in range(100):
        st += 0.2  # Add 0.2 to the initial value of St
        x_out.append(st)  # add values of x to the list y_out
        y = abs(st)  # Equation
        y_out.append(y)   # add values of y to the list y_out
        y_str = f"{y:.2f}"  # Round the value to two decimal numbers
        x_str = f"{st:.2f}"  # Round the value to two decimal numbers
        print(f"|{(x_str).center(10)}|{str(y_str).center(10)}|") # Print the table

plt.style.use('ggplot')  # background theme
ax = plt.axes()
ax.set_facecolor("violet")  # background color
plt.plot(x_out, y_out, color="b")   # b = blue - color for line
plt.title("Absolute Value")  # Graph Title
plt.xlabel("x")  # Print "x" in the  x line
plt.ylabel("f(x) = |x|")  # Print the equation in the y line
plt.show()  # Show the graph
```
## Evidence

![Screen Shot 2022-11-15 at 9 42 08](https://user-images.githubusercontent.com/111819437/201798222-83af9508-d2d1-4301-8d3f-2dbb5e4f23ef.png)

## Convert to decimal FFA5
