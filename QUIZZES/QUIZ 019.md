# QUIZ 019

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
![Flowchart - QUIZZ 017 (4)](https://user-images.githubusercontent.com/111819437/198500303-dc4403be-9e85-47a3-8492-d3b3b34f23ab.png)
