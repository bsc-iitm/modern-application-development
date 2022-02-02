# Comments 
- Comments are mostly used for documentation purpose. 
- Comment lines are not executed by the python interpreter. 
- Comments come in handy when multiple people work on the same template. 
- You can also use comment syntax to disable parts of the template during debugging.
- Comments are added using hash tag # ... #. 
- That is anything typed after # is treated as a comment line and it will be ignored by the engine. 
- An example with comment lines are shown below 

## python code with comments

```python linenums="1"
#import Template Package #
from jinja2 import Template
# Define a template named IITM #
# Define two variables course1 and course 2#
template = """IITM {{ type }} 

course name {{ course1 }} 
course name {{ course2 }}

"""
# Assign values to two variables #
data = {
    "type": "University",
    "course1": "MAD 1",
    "course2": "MAD 2",
    
}
# Create jinja template object and render it#

j2_template = Template(template)

print(j2_template.render(data))

```
## Output 
- IITM  University
- course name MAD 1 
- course name MAD 2

## Reference
https://youtu.be/2_RC4n-Lb8M


