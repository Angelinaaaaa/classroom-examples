# Functions Section Goals
- [Define and call a main function](#define-and-call-a-main-function)
- [**Define** a function](#define-and-call-custom-functions)
- [Define a function with parameters and return type](#parameters-and-return-type)
- [**Call** a function that you have defined](#define-and-call-custom-functions)
- [**Global** vs **local** variables](#global-vs-local-variables)
- [Pass one or more values to a function (**Arguments** and **Parameters**)](#pass-arguments)
- **Return** one or more results from a function
- [**Refactor** existing code into functions.](#refactor-existing-code)
- Trace with the call-stack
- [Annotating a Function](#annotating-a-function)

# Assertions
- [Test a custom function using assertions](#test-using-assertions)
- [Create a `tests` function for your assertions](#tests-function-for-assertions)
- [Create a test function for each of the functions you want to test](#test-function-for-each-function)


## Define and call a main function
```python
def main():
    print("Hello, world!")


if __name__ == "__main__":
    main()
```

## Define and call custom functions
```python
def main():
    say_hello()
    say_hello()
    say_goodbye()


def say_hello():
    print("hello")


def say_goodbye():
    print("goodbye")


if __name__ == "__main__":
    main()
```
**Outputs:**
```
hello
hello
goodbye
```

# Parameters and Return Type
```python
#   Function Name
#   |   Parameter
#   |   |   | Parameter type
#   |   |   |              Return Type
#   |   |   |              |
def add(a: int, b: int) -> int:
    pass
```

# Global vs Local Variables
```python
x = 50

def main():
    x = 10
    print(x)

print(x)


if __name__ == "__main__":
    main()
    print(x)
```
Outputs:
```
50
10
50
```

```python
x = 50

def main():
    global x
    x += 10
    print(x)

print(x)


if __name__ == "__main__":
    main()
    print(x)
```
Outputs:
```
50
60
60
```

## Pass Arguments
```python
def main():
    print("calling add with 3 and 4 as aguments")
    answer = add(3, 4)  # passing arguments
    print(answer)
   
def add(a, b):  # defining parameters
    return a + b


if __name__ == "__main__":
    main()
```

## Refactor Existing Code
Before:
```python
while True:
    print("menu list...")
    
    try:
        choice = int(input("Enter choice: "))
    except ValueError:
        print("invalid choice")
        continue
    
    if choice == 0:
        print("Zero stuff")
    elif choice == 1:
        print("one stuff")
    elif choice == 2:
        print("two stuff")
```
After:
```python
def main():
    while True:
        print("menu list...")
        
        try:
            choice = int(input("Enter choice: "))
        except ValueError:
            print("invalid choice")
            continue
        
        if choice == 0:
            zero_stuff()
        elif choice == 1:
            one_stuff()
        elif choice == 2:
            two_stuff()
    

def zero_stuff():
    print("Zero stuff")


def one_stuff():
    print("one stuff")


def two_stuff():
    print("two stuff")


if __name__ == "__main__":
    main()
```


## Test Using Assertions
```python
def add(a, b):
    return a + b


assert add(3, 4) == 7
assert add(-2, -5) == -7
print("All tests passed!")
```

## Tests function for assertions
```python
def add(a, b):
    return a + b


def tests():
    assert add(3, 4) == 7
    assert add(-2, -5) == -7
    print("All tests passed!")


if __name__ == "__main__":
    tests()
```

## Test function for each function
```python

def add(a, b):
    return a + b


def sub(a, b):
    return a - b


def tests():
    test_add()
    test_sub()
    print("All tests passed!")


def test_add():
    assert add(3, 4) == 7
    assert add(-2, -5) == -7


def test_sub():
    assert sub(5, 3) == 2


if __name__ == "__main__":
    tests()
```
## Annotating a Function
```python
def function_name(param1: type, param2: type) -> return_type:
    """Sort description of the function

    Args:
        param1: Explain the first parameter.
        param2: Explain the second parameter.
    Returns:
        Explain what the function returns
    """
    pass
```
