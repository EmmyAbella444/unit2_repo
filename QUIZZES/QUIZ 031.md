![Screen Shot 2022-12-26 at 15 54 13](https://user-images.githubusercontent.com/111819437/209514483-358b5a69-c835-4e32-8785-3151a28cebec.png)

# Code
```.py
import numpy as np
import requests
from matplotlib import pyplot as plt


req = requests.get('http://192.168.6.142/readings')
data = req.json()
readings = data['readings'][0]

plt.style.use('ggplot')  # background theme
ax = plt.axes()
ax.set_facecolor("#ffafcc")  # background color

temp = []
for sample in readings:
    if sample['sensor_id'] == 1:
        temp.append(sample['value'])
print(len(temp))

# Slice temperature to the region of interest
temp_afternoon_mon = temp[610:800]
x_afternoon_mon = []
for i in range(len(temp_afternoon_mon)):
    x_afternoon_mon.append(i)  # Adding the value of i to the list sample

plt.scatter(x_afternoon_mon,temp_afternoon_mon)

m,b=np.polyfit(x_afternoon_mon,temp_afternoon_mon,1)
x_line = [0,len(temp_afternoon_mon)]
y_line = []
for i in x_line:
    y_line.append(m*i+b)
print(m,b)
plt.plot(x_line,y_line,'black')

# Quadratic model
a1 , a2, a3 = np.polyfit(x_afternoon_mon,temp_afternoon_mon,2)
y_model_squad = []
for i in x_afternoon_mon:
    y_model_squad.append(a1*(i)**2+a2*i+a3)

plt.plot(x_afternoon_mon,y_model_squad, 'blue')

plt.show()
```
