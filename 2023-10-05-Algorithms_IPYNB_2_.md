---
toc: True
comments: True
layout: post
title: 3.3 and 3.4 Algorithms
description: 3.3 and 3.4 Algorithms
courses: {'csp': {'week': 6}}
type: tangibles
---

# Homework


```python
f0 = 0
f1 = 1
fiblist = [f0, f1]
r = int(input("How many items do you want in your fibonacci sequence? Enter a number 2 or greater: "))
if r < 2:
    print("Please enter a number greater than or equal to 2")
else:
    for i in range(r-2):
        x = fiblist[-1]
        y = fiblist[-2]
        fiblist.append(x + y)  # Add the sum of the previous 2 numbers to the list
    print(fiblist)

```

    [0, 1, 1, 2, 3]



```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        swapped = False
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swapped = True
                if not swapped:
                    break
    return arr
arr = [64, 34, 25, 12, 22, 11, 90]
bubble_sort(arr)
print("Sorted array is:", arr)

```

    Sorted array is: [11, 12, 22, 25, 34, 64, 90]



```python
def is_palindrome(word):
    return f"{word} is a {word.lower() == word.lower()[::-1]} palindrome"

print(is_palindrome("word"))
print(is_palindrome("nitin"))
print(is_palindrome("Nitin"))
```

    word is a False palindrome
    nitin is a True palindrome
    Nitin is a True palindrome



```python
grocery_list = ["apples", "bananas", "carrots", "dates", "eggplants", "figs"]

sorted_grocery_list = sorted(grocery_list)

print("Original Grocery List:")
print(grocery_list)
print("\nSorted Grocery List:")
print(sorted_grocery_list)
```

    Original Grocery List:
    ['apples', 'bananas', 'carrots', 'dates', 'eggplants', 'figs']
    
    Sorted Grocery List:
    ['apples', 'bananas', 'carrots', 'dates', 'eggplants', 'figs']

