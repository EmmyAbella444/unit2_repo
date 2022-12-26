# QUIZ 029
![Screen Shot 2022-11-29 at 13 42 42](https://user-images.githubusercontent.com/111819437/204440711-1d10bead-4d52-41a2-b74c-8837848c0b86.png)

## Code
```.py
from Library import colors_purple
def dictionary(dict,msg:str):
    for i in msg:  # Analise each letter of the msg
        if i in dict.keys():  # Check if the letter in the msg is in the key
            dict[i] += 1  # add 1 to the key in the dictionary
    return(dict)  # return dictionary

my_dict1={'w':0,'l':0,'c':0}  # Data for case 1
msg1 = "Hello world"

my_dict2={'a':0,'e':0,'i':0,'o':0,'u':0}  # Data for case 2
msg2 = "Why did I chose CS?"

case1 = dictionary(my_dict1,msg1)
case2 = dictionary(my_dict2,msg2)

print(colors_purple(case1))
print(colors_purple(case2))
```

## Evidence

![Screen Shot 2022-11-29 at 13 45 50](https://user-images.githubusercontent.com/111819437/204441142-4f8662c1-820d-4e90-b477-b2a659f9203f.png)

## How many different colors could you represent in a 6 bit computer?

To calculate how many different colors can be captured or displayed, simply raise the number 2 to the power of the number of bits used to record or display the image.So:
2^6 = 64

64 colors.


Bibliography:
The Math of Color Dept, https://www.scss.tcd.ie/Cathal.OConnor/website-digital-video/4%20The%20Arithmetic%20of%20Color%20Depth.html. 
