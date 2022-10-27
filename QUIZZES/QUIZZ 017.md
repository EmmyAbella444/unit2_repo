
# QUIZ 017

![Screen Shot 2022-10-26 at 14 11 26](https://user-images.githubusercontent.com/111819437/197940337-c8cd92d9-77ea-4cac-880e-29448990819b.png)

## CODE TO QUIZ 017 SL

```.py
def averageLenght(words):
    sum_of_letters = 0
    number_of_words = len(words) #Count number of words in the list
    for w in words:
        Lenght_of_word = float(len(w)) #Count number of letters in the list
        sum_of_letters += Lenght_of_word
        average = sum_of_letters/number_of_words

    return average


print(averageLenght(["Hello", "main"]))
print(averageLenght(["Peru", "France", "Nepal"]))
print(averageLenght(["Computer Science", "Art"]))
print(averageLenght(["one", "two"]))

```

## Evidence SL
![Screen Shot 2022-10-26 at 14 22 10](https://user-images.githubusercontent.com/111819437/197941608-04356079-784f-4f8b-8c1d-5aeeee1476af.png)

## Flowchart SL

![Flowchart - QUIZZ 017 (1)](https://user-images.githubusercontent.com/111819437/197941787-76b4a9bd-255a-4280-bbca-5fe4628d5b25.png)
