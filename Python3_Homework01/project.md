#### Python 3: The Python Environment
### Lesson 1, Project 1

##### Here are your instructions:

Create a Python3_Homework01 project and assign it to your Python3_Homework working set. 

In the Python3_Homework01/src folder, create a program named adder.py; in it, create a function that takes two objects 
and adds them together only if they are both of the integer type. Raise a TypeError otherwise.  
Then, create a test_adder.py file that tests the correctness of this function.


When they are working to your satisfaction, submit adder.py and test_adder.py.


##### Overall Comments:

This is a good project in which to remove misconceptions about assertRaises.
```python3
        self.assertRaises(TypeError, adder, ("123", "456"))
```
You are correct to just name the callable after the expected exception, with 
no arguments, but then should use individual arguments for adder, and not
try to stuff everything in a tuple.  The above only succeeds in pass 
("123", "456") to x, the first parameter, and so raises a TypeError because
of a wrong number of arguments, not because they are strings.  Rather, go:
```python3
        self.assertRaises(TypeError, adder, "123", "456")
```

This allows the callable to even have keyword arguments, and is why message=
or any error message is not possible --
