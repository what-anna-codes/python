# [Vowel Balance](https://www.freecodecamp.org/learn/daily-coding-challenge/08-11)

## Instructions

> Given a string, determine whether the number of vowels in the first half of the string
> is equal to the number of vowels in the second half.\
> (...)\
> If there's an odd number of characters in the string, ignore the center character.  

## Solution
```

def split_in_half(s):
    center = len(s) // 2
    return { "left": s[:center], "right": s[-center:] }

def count_vowels(s):
    return sum(map(s.lower().count, ['a', 'e', 'i', 'o', 'u']))

def is_balanced(s):
    halves = split_in_half(s)
    return count_vowels(halves["left"]) == count_vowels(halves["right"])

```

## Built-in tools used
* `String split()` with negative indexing
* floor division
* `map()` & `sum()` functions 

## What went well
1. **Code organization**. The two helpers - `split_in_half()` and `count_vowels()` - are concise, have descriptive names, and mirror the two steps required to complete the challenge: halving the input string and counting the vowels in both halves.
3. **The use of map()**. How to count all vowels in a string? NOT with `maketrans() + translate()`.\
   Initially, I wanted to translate all input string vowels into a single vowel ("a"), then call count("a") on both halves of the input string.\

## Sources
[Stack Overflow: Count multiple letters in string - Python](https://stackoverflow.com/questions/32414205/count-multiple-letters-in-string-python)
