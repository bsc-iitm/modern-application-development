## Filters 
- Variables can be modified by filters. 
- Filters are separated from the variable by a pipe symbol (|) and may have optional arguments in parentheses. 
- Multiple filters can be chained. 
- The output of one filter is applied as input to the next filter.

- Here's an example showing a simple filter in action:

## Template:

- course name: {{ course_name | capitalize }}

## Data:

- course_name: mad1 
## Output: 
- Course name: Mad1
- Charecter M is capitalized

- We passed course_name variable to capitalize filter. 
- As the name of the filter suggests, First charecter of the string is capitalized. 


- In the below example name variable assigned to the data "mad1" is capitalized and the result is shown

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






