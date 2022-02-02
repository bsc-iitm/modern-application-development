# Filters 
- Values of the variables can be modified by filters. 
- Pipe symbol is used for Filters to seperate the variable. 
- single variable can have multiple filters. 
- In multiple filters, the output of one filter is applied as input to the next filter.

- Below example shows a single filter in action:

## Template:

- course name: {{ course_name | capitalize }}

## Data:

- course_name: mad1 
## Output: 
- Course name: Mad1
- Charecter M is capitalized

- We passed course_name variable to capitalize filter. 
- As the name of the filter suggests, First charecter of the string is capitalized. 


- The code for above example is given below

## python code with filters

```python linenums="1"
from jinja2 import Template

template = "Course {{ name | capitalize }} is available {{ type }} in the {{ site }} datacenter."

data = {
    "name": "mad1",
    "type": "Programming course"
    "site": "IITM",
}

j2_template = Template(template)

print(j2_template.render(data))

```
## Output 
- Course Mad1 is available Programming course in the IITM datacenter.



## Reference
https://jinja.palletsprojects.com/en/2.10.x/templates/


