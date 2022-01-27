## Variables 
- Template variables are defined by the context dictionary passed to the template. 
- {{ }} tells the template to print the value, this won't work in expressions like you're trying to do. 
- Instead, use the {% set %} template tag and then assign the value the same way you would in normal python code. 
- You can use a dot (.) to access attributes of a variable in addition to the standard Python “subscript” syntax ([]).

## Example

- {{ IITM.course1 }}
- {{ IITM['course1'] }}

## IITM.course1 in Jinja does the following things on the Python layer:

- check for an attribute called course1 on IITM (getattr(IITM, 'course1'))

- if there is not, check for an item 'course1' in IITM(IITM.__getitem__('course1'))

- if there is not, return an undefined object.

## IITM['course1'] works mostly the same with a small difference in sequence:

- check for an item 'course1' in IITM. (IITM.__getitem__('course1'))

- if there is not, check for an attribute called course1 on IITM. (getattr(IITM, 'course1'))

- if there is not, return an undefined object.

## By default, when encountering an evaluation statement with undefined variable Jinja will replace it with an empty string. 

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


