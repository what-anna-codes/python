# [Number Pattern Generator](https://www.freecodecamp.org/learn/learn-python-loops-and-sequences/lab-number-pattern-generator/build-a-number-pattern-generator)

## Solution 1 (long)
```

# def number_pattern(n):
#     if not isinstance(n, int):
#         return 'Argument must be an integer value.'
#     if n < 1:
#         return 'Argument must be an integer greater than 0.'
#     output = ''
#     for num in range(1,n + 1):
#         output += str(num) + ' '
#     return output.strip()

```

### Solution 2 (short)
```

def number_pattern(n):
    if not isinstance(n, int):
        return 'Argument must be an integer value.'
    if n < 1:
        return 'Argument must be an integer greater than 0.'
    output = "".join([f'{num} ' for num in range(1, n + 1)]).strip()
    return output

```

## Topics practised:
* list comprehension pattern
* ranges
* f-strings & string methods like `str.join()` (Sidenote: it does feel weird that this method is not called on a list; but easier to understand after reading [this thread on StackOverflow](https://stackoverflow.com/questions/493819/why-is-it-string-joinlist-instead-of-list-joinstring) if you're interested.)

## Notes
An easy task turned into an quick list comprehension practise.
