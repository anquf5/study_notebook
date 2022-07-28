# Conditionals

### Comparing Things

```
print(10>1) # True
print("cat" == "dog) #False
print(1 != 2) #True
print(1 < "1") #Type error
print(1 == "1") #False
```

### Logical Operators

{% hint style="info" %}
**And**

To evaluate as true, the _**and**_ operator would need both expressions to be true at the same time

**Or**

If we use the _**or**_ operator instead the expression will be true if either of the expressions are true, and false only when both expressions are false.

**Not**

the not operator inverts the value of the expression that's in front of it.
{% endhint %}

In Python, we can use comparison operators to compare values. When a comparison is made, Python returns a boolean result, or simply a True or False.&#x20;

* To check if two values are the same, we can use the equality operator: **==**&#x20;
* To check if two values are not the same, we can use the not equals operator: **!=**&#x20;

We can also check if values are greater than or lesser than each other using **>** and **<**. If you try to compare data types that aren’t compatible, like checking if a string is greater than an integer, Python will throw a **TypeError**.&#x20;

We can make very complex comparisons by joining statements together using logical operators with our comparison operators. These logical operators are **and**, **or**, and **not**. When using the **and** operator, both sides of the statement being evaluated must be true for the whole statement to be true. When using the **or** operator, if either side of the comparison is true, then the whole statement is true. Lastly, the **not** operator simply inverts the value of the statement immediately following it. So if a statement evaluates to True, and we put the **not** operator in front of it, it would become False.

### If Statements

{% hint style="info" %}
**Branching**: The ability of a program to alter its execution sequence
{% endhint %}

The body of the if block will only execute when the condition evaluates to true; otherwise, it skipped.

We can use the concept of **branching** to have our code alter its execution sequence depending on the values of variables. We can use an _if_ statement to evaluate a comparison. We start with the _if_ keyword, followed by our comparison. We end the line with a colon. The body of the _if_ statement is then indented to the right. If the comparison is _**True**_, the code inside the _if_ body is executed. If the comparison evaluates to _**False**,_ then the code block is skipped and will not be run.

```
def function():
    if(condition):
        print("")
```

### Else Statements

```
def is_positive(number):
  if number > 0:
    return True
  else:
    return False
```

when a return statement is executed, the function exits so that the code that follows doesn't get executed.

```
def is_positive(number):
  if number > 0:
    return True
  return False
```

{% hint style="info" %}
We just covered the _if_ statement, which executes code if an evaluation is true and skips the code if it’s false. But what if we wanted the code to do something different if the evaluation is false? We can do this using the _else_ statement. The _else_ statement follows an _if_ block, and is composed of the keyword _else_ followed by a colon. The body of the _else_ statement is indented to the right, and will be executed if the above _if_ statement doesn’t execute.

We also touched on the modulo operator, which is represented by the percent sign: **%**. This operator performs integer division, but only returns the remainder of this division operation. If we’re dividing 5 by 2, the quotient is 2, and the remainder is 1. Two 2s can go into 5, leaving 1 left over. So 5%2 would return 1. Dividing 10 by 5 would give us a quotient of 2 with no remainder, since 5 can go into 10 twice with nothing left over. In this case, 10%2 would return 0, as there is no remainder.
{% endhint %}

### elif Statements

```
def hint_username(username):
    if len(username)<3:
        print("xxx")
    elif len(username)>15:
        print("yyy")
    else:
        print("zzz")
```

{% hint style="info" %}
The main difference between elif and if statements is we can only write an elif block as a companion to an if block. That's because the condition of the elif statement will only be checked if the condition of the if statement wasn't true.
{% endhint %}

### Conditionals Cheat Sheet

#### Comparison operators

| Comparison Operators | Description                |
| -------------------- | -------------------------- |
| a == b               | a is equal to b            |
| a != b               | a is different than b      |
| a < b                | a is smaller than b        |
| a <= b               | a is smaller or equal to b |
| a > b                | a is bigger than b         |
| a >= b               | a is bigger or equal to b  |

#### Logical Operators

| Logical Operators | Description                                                      |
| ----------------- | ---------------------------------------------------------------- |
| a and b           | True if both a and b are True. False otherwise.                  |
| a or b            | True if eigher a or b or both are True. False if both are False. |
| not a             | True if a is False, False if a is True                           |
