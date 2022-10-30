# QUIZ 018
![Screen Shot 2022-10-30 at 16 46 38](https://user-images.githubusercontent.com/111819437/198867945-cb497537-5092-42cd-b5b4-97c55c7b57cc.png)


## CODE 

```.py
import math
def number_of_matches(Lenght,Speed):
    Meter_per_second = Speed/100   #Convert centimeter/seconds to meter/seconds
    Time = (Lenght/Meter_per_second)/5   #Find the total of seconds to complete the lenght and then divie to discover the number of matches


    return math.ceil(Time) #Round the number up to the nearest whole number

print(number_of_matches(100,100))
print(number_of_matches(250,110))
print(number_of_matches(500,150))
print (number_of_matches(12345,123))
```


## EVIDENCE
![Screen Shot 2022-10-27 at 23 27 49](https://user-images.githubusercontent.com/111819437/198314202-f59721a9-93ba-474e-a059-5ffd2868478e.png)

## FLOWCHART 

![Flowchart - QUIZZ 017 (2)](https://user-images.githubusercontent.com/111819437/198321636-93ae2b93-9605-4d30-b085-d5f54be3346c.png)


