# Expressions and Variables

## Data Type

{% hint style="info" %}
string, float, int

**Boolean:** One of two possible states, true or false
{% endhint %}

`print (1 + "8" ) # error`

use the _<mark style="color:red;">type</mark>_ <mark style="color:red;"></mark><mark style="color:red;"></mark> function to get the type

```
print (type("a")) # <class 'str'>
print(type(2)) # <class 'int'>
```

## Variables

{% hint style="info" %}
Names that we give to certain values in our programs
{% endhint %}

Assignment: The process of storing a value inside a variable

```
length = 10
width = 2
```

Expression: A combination of numbers, symbols, or other variables that produce a result when evaluated.

```
area = length * width
print(area)
```

{% hint style="info" %}
Variable Naming Restrictions

* Don't use keywords or functions that Python reserves for its own, like print
* Don't use spaces
* Must start with a letter or an underscore(\_)
{% endhint %}

### Implicit conversion

The interpreter automatically converts one data type into another, like

```
print(7 + 9.5) #16.5
print("a" + "b" + "c") #abc
```

### Explicit Conversion

```
base = 6
height = 3
area = (base*height)/2
print("The area is " + str(area)) #The area is 9
```

{% hint style="info" %}
#### Implicit vs Explicit Conversion

**Implicit conversion** is where the interpreter helps us out and <mark style="color:red;">automatically</mark> converts one data type into another, without having to explicitly tell it to do so.

By contrast, **explicit conversion** is where we <mark style="color:red;">manually</mark> convert from one data type to another by calling the relevant function for the data type we want to convert to. We needed to call the _<mark style="color:orange;">**str()**</mark>_ function to convert the number into a string. Once the number was explicitly converted to a string, we could join it with the rest of our textual string and print the result.
{% endhint %}

##
