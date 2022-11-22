# QUIZ 028
![Screen Shot 2022-11-22 at 13 27 25](https://user-images.githubusercontent.com/111819437/203221455-9e08d23d-75c8-40a5-abe8-14dfbef7ae29.png)


## CODE
```.py
from matplotlib import pyplot as plt
data = {'x':[0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19],
'y':[24,1,2,25,26,21,23,34,49,2,19,32,7,17,36,7,45,28,40,46]}

# Add new data
data["title"] = []
data["title"].append("Quiz028")

# Print data
print(data["x"])
print(data["y"])
print(data["title"])

# Make graph
plt.style.use('ggplot')  # background theme
ax = plt.axes()
ax.set_facecolor("#ffafcc")  # background color
plt.plot(data["x"], data["y"], color="#f72585")  # Make graph line
plt.title("Quiz 028")  # Graph title
plt.show()
```
## Evidence

![Screen Shot 2022-11-22 at 13 22 03](https://user-images.githubusercontent.com/111819437/203220781-f67b0ad8-80e9-4578-9133-208bc1b67a33.png)


## Convert red=10, green=255, blue=255 to hex color
