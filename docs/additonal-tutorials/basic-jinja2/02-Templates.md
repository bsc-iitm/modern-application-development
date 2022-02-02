## Templates 
- Templates are functions with detailed API. 
- These templates can generste any kind of output. 
- {{variable_name}} is the syntax for substituting value to a variable.
- Below is an example of jinja2 templates. 

## python template code
- Example 1
```python linenums="1"
from jinja2 import Template

t = Template ("Hello {{name1}} welcome!") # {{name1 value is assigned}}
print(t.render(name1 ="Banu"))# name1 is the variable name
t = Template ("your age is {{age}}")
print(t.render(age = input("Enter your Age")))# age value is assigned based on the values given in input prompt

```
## Output 
- Hello Banu welcome!
- Enter your Age13
- your age is 13
## Example 2
```python linenums="1"
from jinja2 import Template

template = """IITM {{ course }}

course name {{ course1 }}
course name {{ course2 }}

"""
data = {
    "course": "University",
    "course1": "MAD 1",
    "course2": "MAD 2",
}

j2_template = Template(template)
print(j2_template.render(data))

```
## Output
- IITM University

- course name MAD 1
- course name MAD 2


## Reference
https://youtu.be/2_RC4n-Lb8M
