# QUIZ 024

### Code
```.py
from matplotlib import pyplot as plt

print(f"|{'x'.center(10)}|{'y(x)'.center(10)}|")  # Print the title of the table
x_out = []  # Create empty str for X
y_out = []  # Create empty str for Y
st = -10.2
for _ in range(100):
        st += 0.2   # Add 0.2 to the initial value of St
        x_out.append(st)  # add values of x to the list y_out
        y = 2*(st+5)**2  # Equation
        y_out.append(y)  # add values of y to the list y_out
        y_str = f"{y:.2f}"  # Round the value to two decimal numbers
        x_str = f"{y:.2f}"  # Round the value to two decimal numbers
        print(f"|{(x_str).center(10)}|{str(y_str).center(10)}|")  # Print the table


plt.style.use('ggplot')  # background theme
ax = plt.axes()
ax.set_facecolor("violet")  # background color
plt.plot(x_out, y_out, color="b")   # b = blue - color for line
plt.title("Parabola")  # Graph Title
plt.xlabel("x")  # Print "x" in the  x line
plt.ylabel("$y=2*(x+5)**2$")  # Print the equation in the y line
plt.show()
```
### Evidence

![Screen Shot 2022-11-12 at 17 35 39](https://user-images.githubusercontent.com/111819437/201466142-25c8c4ed-035c-40ae-b238-e267c67ce95f.png)

### Flowdiagram

## Circuit for
not(bit0 bit1 +not(bit0 +bit1)

![Screen Shot 2022-11-12 at 16 39 50](https://user-images.githubusercontent.com/111819437/201463212-12132772-21e3-4e8a-889e-5441ecf807cc.png)
