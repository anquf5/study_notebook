# Functions

### Defining Functions

{% hint style="info" %}
We start a function definition with the _**def**_ keyword, followed by the name we want to give our function. After the name, we have the _**parameters**_, also called _arguments_, for the function enclosed in parentheses.&#x20;

<mark style="color:blue;">A function can have no parameters, or it can have multiple parameters.</mark> Parameters allow us to call a function and pass it data, with the data being available inside the function as variables with the same name as the parameters. Lastly, we put a <mark style="color:orange;">colon</mark> at the end of the line.

After the colon, the function body starts. It’s important to note that in Python the function body is delimited by <mark style="color:blue;">indentation</mark>. This means that all code indented to the right following a function definition is part of the function body. The first line that’s no longer indented is the boundary of the function body. It’s up to you how many spaces you use when indenting -- just make sure to be consistent. <mark style="color:blue;">So if you choose to indent with four spaces, you need to use four spaces everywhere in your code.</mark>
{% endhint %}

```
def greeting(name):
    print("Welcome, " + name)
    
greeting("Kay") #Welcome, Kay

def hello(name, department):
    print("Welcome, " + name)
    print("You are in " + department)

hello("Bob", "Software Engineer")
```

### Returning Values

```
def area_triangle(base, height):
    return base*height/2

area_a = area_triangle(5,4)
area_b = area_triangle(7,3)
sum = area_a + area_b
print("The sum of both area is: " + str(sum))
```

```
def convert_seconds(seconds):
    hours = seconds // 3600
    minutes = (seconds - hours * 3600) // 60
    remainint_seconds = seconds - hours * 3600 - minutes * 60
    return hours, minutes, remaining_seconds
    
hours, minutes, seconds = convert_seconds(5000)
print(hours, minutes, seconds) #1 23 20
```

{% hint style="info" %}
<mark style="color:red;">// is floor division</mark>
{% endhint %}

```
def greeting(name):
    return "Hello " + name

result = greeting("Alice")
print(result) # none
```

{% hint style="info" %}
**None**

A special data type in Python used to indicate that things are empty or that they returned nothing
{% endhint %}

{% hint style="info" %}
When we call the function, we can <mark style="color:blue;">store the returned value in a variable</mark>. Return values allow our functions to be more flexible and powerful, so they can be reused and called multiple times.

<mark style="color:blue;">Functions can even return multiple values</mark>. <mark style="color:red;">Just don't forget to store all returned values in variables!</mark> You could also have a function return nothing, in which case the function simply exits.
{% endhint %}

### Code Style

* **Make code as self-documenting as possible**

Written in a way that's readable and doesn't conceal its intent

```
def calculate(d):
    q = 3.14
    z = q * (d ** 2)
    print(z)
    
calculate(5)
```

refactor:

```
Def circle_area(radius):
    pi = 3.14
    area = pi * (radius ** 2)
    print(area)
    
circle_area(5)
```

* **Use comment**

```
# this is your comment
```
