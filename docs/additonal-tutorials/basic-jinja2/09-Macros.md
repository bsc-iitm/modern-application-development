## Macros 
- Macros are comparable with functions in regular programming languages. They are represented as inline functions. 
- Once macros are defined, the names of the macros can be inserted in places where they are required.


## python code for Macro

```python linenums="1"
from jinja2 import Template
template = "Available Devices are {% macro def_if_desc(name) -%}  {{ name }} devices, {%- endmacro -%} {% for item in devices -%} New {{ def_if_desc(item) }} {% endfor -%}"
data = {
    "devices" : ["laptop","desktop", "printer", "card", "voice"],
   
}
j2_template = Template(template)

print(j2_template.render(data))

```

## Output
- Available Devices are New laptop devices, New desktop devices, New printer devices, New card devices, New voice devices,