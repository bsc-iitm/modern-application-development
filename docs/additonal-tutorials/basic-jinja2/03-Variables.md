## Variables 
- Template variables are defined by dictionary concept in python. 
- {{variable_name }} is the syntax used by the template to print the value.  
- Dot operator is used to access attributes of a variable.

## Example

- {{ IITM.course1 }}
- {{ IITM['course1'] }}

## If Jinja identifies an evaluation statement with an undefined variable, it will replace it with an empty string. 

## python variable code
```python linenums="1"
from jinja2 import Template

template = "Course {{ name }} is available {{ type }} in the {{ site }} datacenter."

data = {
    "name": "MAD1",
    "type": "Programming course",
    "site": "IITM",
}

j2_template = Template(template)

print(j2_template.render(data))
```

## Output 
- Course MAD1 is available Programming course in the IITM datacenter.

## Reference

https://youtu.be/2_RC4n-Lb8M
