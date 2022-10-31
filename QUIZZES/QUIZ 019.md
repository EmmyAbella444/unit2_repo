# QUIZ 019

![Screen Shot 2022-10-30 at 17 05 16](https://user-images.githubusercontent.com/111819437/198868708-2dd546c4-271f-44c9-91ce-a26a624760fe.png)

## Code
```.py
def get_l3t33r(msg):
    str_vowels= ""  #Create an empty str
    for letter in msg: #For loop to read each  caracter in the str
        if letter == "a":
            str_vowels+='4'  #Replace a for 4 and add to the new str
        elif letter == "e":
            str_vowels+='3'  #Replace e for 3 and add to the new str
        elif letter == "i":
            str_vowels+='1'  #Replace i for 1 and add to the new str
        elif letter == "o":
            str_vowels+='0'  #Replace o for 0 and add to the new str
        elif letter == ' ':
            str_vowels+='_'  #Replace spaces for and add to the new str
        else:
            str_vowels+=letter #add the consoants of the orginal string to the new str


    return(str_vowels) #Return the new str

print(get_l3t33r("Hello World"))
print(get_l3t33r("Why did I choose CS?"))
print(get_l3t33r("Remember the Figure Caption"))
```
## Evidence
![Screen Shot 2022-10-28 at 11 58 03](https://user-images.githubusercontent.com/111819437/198485354-76ec339e-d7dc-42e4-80ae-16f727e48b4c.png)

## Flowchart
![Flowchart - QUIZZ 017 (6)](https://user-images.githubusercontent.com/111819437/198920573-09ac0004-5205-4350-a95a-d279f1560111.png)


## Boolean circuit for:
AB + not(B+C) + B(notC notA)


