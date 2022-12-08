# QUIZ 030
![Screen Shot 2022-12-08 at 9 27 31](https://user-images.githubusercontent.com/111819437/206326537-a8d5e814-09d8-48c5-9323-b521524c0ced.png)

## CODE
```.py
from matplotlib import pyplot as plt

plt.style.use('ggplot')  # background theme


h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0,
     53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0,
     49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]  # List for data

# Empty list and for to create list with samples(Values of X)
x = []
for i in range(0,len(h)):
    x.append(i)

size_window = 4  # Value for smoothed window
h_smth = []  # H smoothed
x_smth = []  # X smoothed
for i in range(0,len(h),size_window):  # for to add smoothed values to the list
     values = h[i:i+size_window]
     h_smth.append(sum(values)/size_window)
     x_smth.append(i)


# Print graph 
plt.subplot(2,1,1)
plt.plot(x,h,'o-', color="#f72585")
plt.title("Normal version")
plt.subplot(2,1,2)
plt.plot(h_smth,x_smth, color="#f72585")
plt.title("Smoothed version")
plt.show()
```

## EVIDENCE
![Screen Shot 2022-12-08 at 9 53 05](https://user-images.githubusercontent.com/111819437/206329604-0c9c30a6-6bca-4296-8e34-32275ea98af8.png)


## When was the internet first created? 
