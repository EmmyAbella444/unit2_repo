
# QUIZ 017

![Screen Shot 2022-10-26 at 14 11 26](https://user-images.githubusercontent.com/111819437/197940337-c8cd92d9-77ea-4cac-880e-29448990819b.png)

## CODE TO QUIZ 017 SL

```.py
def averageLenght(list):
    sum_of_letters = 0
    number_of_words = len(list)  # Count number of words in the list
    for words in list:
        Lenght_of_word = int(len(words))  # Count number of letters in the word
        sum_of_letters += Lenght_of_word  # Add the number of letters to the sum
        average = sum_of_letters/number_of_words  # Divide to  find the average

    return average


print(averageLenght(["Hello", "main"]))
print(averageLenght(["Peru", "France", "Nepal"]))
print(averageLenght(["Computer Science", "Art"]))
print(averageLenght(["one", "two"]))

```

### Evidence SL

![Screen Shot 2022-10-31 at 17 04 01](https://user-images.githubusercontent.com/111819437/198960563-d09e7687-1ecf-45c4-9be4-71954cfb30ee.png)


### Flowchart SL

![Flowchart - QUIZZ 017 (3)](https://user-images.githubusercontent.com/111819437/198322176-9c0729a7-dc5a-47f7-bb43-6fbbd38651dd.png)

## CODE TO QUIZ 017 HL
```.py
def averageLenght (list):
    number_of_words = len(list)  # Count number of words in the list
    count_letters = 0  # Variable to count number of letters
    for word in list:  # Divide the str by word
        for letter in word:  # Divide the word by character
            if letter not in " ":  # Checking the spaces
                count_letters = count_letters + 1  # Add the number of letters to the sum
        average = count_letters / number_of_words  # Divide to  find the average

    return average


print(averageLenght(["Hello", "main"]))
print(averageLenght(["Peru", "France", "Nepal"]))
print(averageLenght(["Computer Science", "Art"]))
print(averageLenght(["one", "two"]))

```
### Evidence HL

![Screen Shot 2022-10-31 at 17 18 02](https://user-images.githubusercontent.com/111819437/198962768-a26d29de-c0c9-413a-b638-dbc3d6b52218.png)

### Flowchart HL

![Flowchart - QUIZZ 017 (7)](https://user-images.githubusercontent.com/111819437/198964505-df0709d8-c04b-4eb2-807b-58f8ad24c511.png)


