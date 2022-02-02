## Arithmetic Expression

- Upto now we have seen variables assigned to string values. 
- Jinja2 supports other data types too. 
- Let's use integers to perform a arithmetic calculation. 
- Adding {{ X }} and {{ Y }} equals {{ X + Y }}. 
- The values assigned to the variables are integers. 
- Below example describes it.



## python code for Arithmetic Expressions
```python linenums="1"
from jinja2 import Template

template = "Adding {{ X }} and {{ Y }} equals {{ X + Y }}"

data = {
    "X": 7,
    "Y": 8,
}

j2_template = Template(template)

print(j2_template.render(data))
```

## Output 
- Adding 7 and 8 equals 15


