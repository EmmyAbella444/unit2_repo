# QUIZ 023
![Screen Shot 2022-11-10 at 8 07 58](https://user-images.githubusercontent.com/111819437/200961608-587db8c0-4717-4fa9-8025-f2cf00113d1c.png)

## Code
```.py
import random
random.seed(1234)
from matplotlib import pyplot as plt


def produce(n=int, m=int, s=int):
    print(f"|{'x'.center(10)}|{'y(x)'.center(10)}|")
    x_out = []  # Create empty str
    y_out = []
    for _ in range(n):
        x = random.randint(0,100)
        x_out.append(x)  # add values of x
        y = x ** (1/2*((m/s)**2))
        y_out.append(y)  # add values of y
        y_str = f"{y:.2f}" # Round the value to 2 decimal places 
        print(f"|{str(x).center(10)}|{y_str.center(10)}|")

    return y_out, x_out

data_y,data_x = produce(n=10,m=5,s=2)
plt.style.use('ggplot')  # background theme
ax = plt.axes()
ax.set_facecolor("violet")  # background color
plt.plot(data_x, data_y, color="b", marker="o")  # b = blue (color for lines)
plt.xlabel("x")  # Print "x" in the  x line
plt.ylabel("$y=x^(1/2((m/s)^2}$")  # Print the equation in the y line
plt.show()

```
## Evidence
![Screen Shot 2022-11-10 at 15 20 26](https://user-images.githubusercontent.com/111819437/201015511-1652b6dd-dc09-43d3-9d05-fbdb7239f55b.png)


## Truth table for:A(A ⊕ B)  

| A 	| B 	| A ⊕ B 	| A(A ⊕ B) 	|
|---	|---	|-------	|----------	|
| 0 	| 0 	| 0     	| 0        	|
| 0 	| 1 	| 1     	| 0        	|
| 1 	| 0 	| 1     	| 1        	|
| 1 	| 1 	| 0     	| 0        	|
