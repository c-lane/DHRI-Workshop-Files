# Functions

Broadly defined, a function is a block of reusable code that performs a specific task. Often, a function takes an input, transforms the input, and returns an output. Imagine, for instance, a [penny press](https://en.wikipedia.org/wiki/Elongated_coin) at a popular tourist attraction that accepts a penny (the input), flattens and embosses the penny (the transformation), and spits out an elongated coin with a new design, perhaps an image of the Statue of Liberty (the output)! Or, for those of you who remember high school algebra, the function `f(x) = x + 1` means that given an input `x`, the function will return `x + 1`. For example, if I substituted `2` for `x`, my function would read `f(2) = 2 + 1`, or `f(2) = 3`. In this case, my input was `2`, the transformation was to add `1`, and the output was `3`. These are the basic concepts that make up a function in Python as well! 

## Writing your first function

In a text editor, let's write a Python function that prints the output from our alegebraic equation `f(x) = x + 1` above:

```python
def add_one(x):
  print(x + 1)
```

Let's break that down. When creating a function, we begin by writing `def` before our chosen function name. The function name is typically descriptive in nature. We named the above function `add_one` following [Python naming conventions](https://www.python.org/dev/peps/pep-0008/#function-and-variable-names), as the function will be ADDING 1 to our inputted integer. We always need a closed parentheses `()` after our function name, which in this case, takes one argument (or input), which we will temporarily call `x` (we can name this parameter whatever we want, as long as we use the same name within the body of the function). Then, we end the first line with a `:`, return, and indent by 2 spaces to write code describing what this function should "do." In this case, we want the function to `print` the result of adding `1` to our input, or `x`. Remember, we need parentheses every time we print something!

Next, if we want to call our function from the terminal, we will need to actually pass in an argument to see a result! Let's add the following line of code below our function (make sure this next line isn't indented):

```python
add_one(2)
```

Here, we are telling the computer to pass in `2` to see if we get our expected output of `3`. Now, save this file to your Desktop as `function.py`, and run the script from your terminal:

```console
$ cd Desktop
$ python function.py
```

Did you get `3`? 

### Optional 
To see the magic of the function in action, try going back to your text editor and adding extra lines of code with different arguments, making sure to hit "save" after doing so:

```python
add_one(155)
add_one(5)
add_one(-1)
```

Call `function.py` again from the terminal. Do you notice how the function printed the sum of each of these numbers plus one? Writing this function helped us to automate this simple process of addition for each given input! Granted, creating a whole function just to add "one" to something may seem unnecessarily complicated, but once you have learned the basics of function-writing, the possibilities are powerful and limitless!

### Advanced
Note that writing a function this way only prints the result, but does not actually `return` it. Read more about the difference between `print` and `return` [here](https://pythonprinciples.com/blog/print-vs-return/). If we wanted our function to actually perform the operation AND print it, we could revise our code as follows:

```python
def add_one(x):
  return x + 1

print(add_one(2))
```

## Writing your second function

Our functions do not have to be "mathematical" in nature. Let's say that I wanted to say a friendly hello, but didn't want to type out a long sentence every time I wanted to do so. I could automate this process by writing the following function:

```python
def greet():
  print("Hello! How are you today?")
```

Remember, we also need to call the function if we want it to run. So, add the following line after your code:

```python
greet()
```

Save the file as `greet.py`, and call it from your terminal. You might have noticed that this time, we didn't pass in an argument! Note that a function doesn't have to take an input (or argument), or it can take several arguments! There is a lot of flexbility involved in writing your own functions, which you can craft carefully to do exactly what you want them to! Read more about some of the many things you can do with functions on the online web tutorial [W3Schools](https://www.w3schools.com/python/python_functions.asp).

## Challenge

How could we change our greeting function to say hello to a specific person? Hint: your print statement will need to use string interpolation. We did this in "3. Variables" when we assigned y to "hello" `y = "hello"`, and then added `y + " and goodbye"`, which yielded the result `"hello and goodbye"`.

## Solution
```python
def greet(person):
  print("Hello " + person + "! How are you today?")

greet("Sara")
```
The result of calling this in your terminal prints `"Hello Sara! How are you today?"`

## Evaluation

Which of the following are not true about a function?:
- A function can be reused
- A function can take any number of arguments (including no arguments)
- A function needs to be called in order to run
- A function can only perform mathematical operations*

## Keywords
- [argument] - "An argument is the value that is sent to the function when it is called." —[W3Schools](https://www.w3schools.com/python/python_functions.asp)
- [parameter] - "A parameter is the variable listed inside the parentheses in the function definition." —[W3Schools](https://www.w3schools.com/python/python_functions.asp)
- [function] A function is block of reusable code that performs a specific task.


