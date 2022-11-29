# QUIZ 029
## Code
```.py
purple_bold = "\33[0;35m"
end_code = "\033[00m"
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

print(f"{purple_bold}{case1}{end_code}")
print(f"{purple_bold}{case2}{end_code}")
```

## Evidence
![Screen Shot 2022-11-29 at 11 08 16](https://user-images.githubusercontent.com/111819437/204421480-ecdc68ad-bbcc-4b4c-a5e4-e6c3cb04b7a9.png)
