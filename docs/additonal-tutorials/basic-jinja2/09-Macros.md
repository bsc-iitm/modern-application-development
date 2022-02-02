## Macros 
- Macros are comparable with functions in regular programming languages. 
- They are represented as inline functions. Once macros are defined, the names of the macros can be inserted in places where they are required. 
- In the following code, name of the macro is macro_name. 
- A for loop is used to display the items of the data defined in dictionary.
- The macro is used inside the for loop to display the items in the dictionary. 


## python code for Macro

```python linenums="1"
from jinja2 import Template
template = "Available Devices are {% macro macro_name(name) -%}  {{ name }} devices, {%- endmacro -%} {% for item in devices -%} New {{ macro_name(item) }} {% endfor -%}"
data = {
    "devices" : ["laptop","desktop", "printer", "card", "voice"],
   
}
j2_template = Template(template)

print(j2_template.render(data))


```

## Output
- Available Devices are New laptop devices, New desktop devices, New printer devices, New card devices, New voice devices,

## Reference
https://jinja.palletsprojects.com/en/2.10.x/templates/