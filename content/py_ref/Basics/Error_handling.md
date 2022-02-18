
---
title: "Error handling"
date: 2022-15-02T14:10:12+01:00
draft: true
tags: ["test", "python", "markdown"]
categories: ["post"]
---

# Handling exceptions


```python
var1 = 'a'

try:
    var2 = var1 + 1.0 # TypeError exception raised if var1 is not a number
    print(f'var2 = {var2}')

except TypeError:
    print('Error: var1 must be a float or int')
```

    Error: var1 must be a float or int
    

# Raising exceptions


```python
var1 = -1

try:
    if var1 <= 0:
        # ValueError exception raised if var1 <= 0
        raise ValueError('Error: var1 must be positive')
    else:
        var2 = var1 + 1.0
        print(f'var2 = {var2}')

except ValueError as err:
    print(err)
```

    Error: var1 must be positive
    

# Else and finally clauses


```python
var1 = 1

try:
    if var1 <= 0:
        # ValueError exception raised if var1 <= 0
        raise ValueError('Error: var1 must be positive') 
    else:
        var2 = var1 + 1.0
        print(f'var2 = {var2}')

except ValueError as err:
    print(err)

else:
    print('No errors were raised')

finally:
    print('finally clause always executes')
```

    var2 = 2.0
    No errors were raised
    finally clause always executes
    
