# While Loops

### Initializing

To give an initial value to a variable

```
x = 0
while x < 5:
    print("Not there yet, x=" + str(x))
    x = x + 1
print("x=" + str(x))
```

A _while_ loop will continuously execute code depending on the value of a condition. It begins with the keyword _while,_ followed by a comparison to be evaluated, then a colon. On the next line is the code block to be executed, indented to the right. Similar to an _if_ statement, the code in the body will only be executed if the comparison is evaluated to be true. What sets a _while_ loop apart, however, is that this code block will keep executing as long as the evaluation statement is true. Once the statement is no longer true, the loop exits and the next line of code will be executed.

```
def attempts(n):
    x = 1
    while x <= n:
        print("Attempt " + str(x))
        x += 1
    print("Done")
    
attempts(5)
```

```
username = get_username()
while not valid_username(username):
    print("Invalid username")
    username = get_username()
```

{% hint style="info" %}
You'll want to watch out for a common mistake: forgetting to initialize variables. If you try to use a variable without first initializing it, you'll run into a **NameError**. This is the Python interpreter catching the mistake and telling you that you’re using an undefined variable. The fix is pretty simple: initialize the variable by assigning the variable a value before you use it.

Another common mistake to watch out for that can be a little trickier to spot is forgetting to initialize variables with the correct value. If you use a variable earlier in your code and then reuse it later in a loop without first setting the value to something you want, your code may wind up doing something you didn't expect. Don't forget to initialize your variables before using them!
{% endhint %}
