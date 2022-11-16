# QUIZ 024

![Screen Shot 2022-11-15 at 13 30 22](https://user-images.githubusercontent.com/111819437/201826647-e39e4ab4-e3ea-46ae-b77f-391dc655cb43.png)

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
        x_str = f"{st:.2f}"  # Round the value to two decimal numbers
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

![Screen Shot 2022-11-13 at 19 23 58](https://user-images.githubusercontent.com/111819437/201517001-fbf528bf-a08c-4629-8760-f98d023217f9.png)

![Screen Shot 2022-11-16 at 19 39 28](https://user-images.githubusercontent.com/111819437/202158869-8f741561-c00d-49ac-ad35-dec5084e2f14.png)

![Screen Shot 2022-11-16 at 19 39 38](https://user-images.githubusercontent.com/111819437/202158892-262fee66-6418-458c-8368-5c07566ca8a7.png)

![Screen Shot 2022-11-16 at 19 42 09](https://user-images.githubusercontent.com/111819437/202159392-d224d3e3-5e38-4b17-add6-8cb53379e94c.png)





## Circuit for
not(bit0 bit1 +not(bit0 +bit1)

![Screen Shot 2022-11-12 at 16 39 50](https://user-images.githubusercontent.com/111819437/201463212-12132772-21e3-4e8a-889e-5441ecf807cc.png)
