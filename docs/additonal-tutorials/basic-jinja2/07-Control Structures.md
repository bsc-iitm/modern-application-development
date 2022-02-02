## Control Structures

- In Jinja2 loop (Iterative) statements and conditional (Branching) statements comes under the name of control structures, since they affect flow of a program. 
- Control structures use blocks enclosed by {%   %} characters.

## Branching statements

- jinja2 conditional statement is represented as if statement. 
- For multi branching we can use elif and else for ending the if statement.

## Comparison operators 
- ==, !=, >, >=, <, <= are the operators used for comparison statements. 
- They are represented as binary operators. 
- Because for comparison minimum two variables or operands required. 
- For example, if a>=b: in this statement a and b are compared.
- If the condition is true the the statement inside if will be executed. 
- If the condition is false then, any elif statements are there that statements will be analyzed. 
- If all conditions return false then the else statement will be executed.


## python code for conditional statements
```python linenums="1"
from jinja2 import Template

template = "First number {{n1}} and second number {{n2}}"
t1 = "{% if n1 > n2 %} {{n1}} is greater {%elif n1 == n2 %}{{n1}} and {{n2}} are equal {% else %} {{n2}} is greater {% endif %}"
data = {
    "n1": input("Enter 1st number "),
    "n2": input("Enter 2nd number "),
}

j2_template = Template(template)
print(j2_template.render(data)) # two values are passed

j2_template1 = Template (t1) 
print(j2_template1.render(data))# two values are passed
```

## Output 
- Enter 1st number 6
- Enter 2nd number 6
- First number 6 and second number 6
- 6 and 6 are equal 

## Logical operators

- Jinja2 provides logical operators in the form of and, or and not. 
- AND => if both the conditions returns True the output is True otherwise false. 
- OR => if any one of the condition is True the output is True otherwise false. 
- Not => if the input is true the output is false, similarly if the input is false the output is true. 
- Example for conditional statements using logical operators is shown below.
## python code for conditional statements - Logical operators
```python linenums="1"
from jinja2 import Template

template = "First number {{n1}} , second number {{n2}} and third number{{n3}} "
t1 = "{% if (n1 > n2) and n1 > n3 %} {{n1}} is greater {%elif (n2> n1) and (n2 >n3) %}{{n2}} is greater {% else %} {{n3}} is greater {% endif %}"
data = {
    "n1": input("Enter number 1 "),
    "n2": input("Enter number 2 "),
    "n3": input("Enter number 3 "),
}

j2_template = Template(template)

print(j2_template.render(data)) # three values are passed


j2_template1 = Template (t1) 


print(j2_template1.render(data))# three values are passed
```
## Output
- Enter number 1 6
- Enter number 2 7
- Enter number 3 4
- First number 6 , second number 7 and third number 4 
- 7 is greater

## Boolean codition checking

- Based on the Truthiness of the variables, the condition statements works.
## python code for conditional statements - Boolean operators
```python linenums="1"
from jinja2 import Template
template = "{% if x and y %} Both x and y are True. x: {{ x }}, y: {{ y }} {% endif %} {% if x or z %} At least one of x and z is True. x: {{ x }}, z: {{ z }} {% endif %} {% if not z %} z is not True. z: {{ z }} {% endif %}"

data = {
  "x": True,
  "y": True,
  "z": False,
}
j2_template = Template(template)

print(j2_template.render(data))
```
## Output
- Both x and y are True. x: True, y: True   At least one of x and z is True. x: True, z: False   z is not True. z: False

## Looping statements 
- These statements are otherwise known as Iterative statements. 
- If a particular set of statements to be executed more than one time, then that set of statements can be placed inside this looping statements. 
- A simple example is shown below.
## python code for Iterative statements 
```python linenums="1"
from jinja2 import Template
template = "{% for item in seq %} {{ item }} {% endfor %}"
data ={
    "seq":[1,2,3,4,"five"],
}
j2_template = Template(template)

print(j2_template.render(data))
```
## Output
- 1  2  3  4  five

## Reference
https://jinja.palletsprojects.com/en/2.10.x/templates/