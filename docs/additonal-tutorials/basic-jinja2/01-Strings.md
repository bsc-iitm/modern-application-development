# Strings
- Any values given with in double quotes are represented as string values. Eg. "welcome"
- Below code is an example for assigning string values to the variables. 
- Any words preceeded by '$' symbol is substituted with the same named variables. 
- In python the data type of variable changed based on the values assigned. 
- Example 1, age = "twenty" . In this the variable is string. 
- Example 2, age = 20. In this variable is integer;

## python string code
```python linenums="1"
from string import Template # import Template from string package
t= Template ('$name is the $role of $organization') # substitute variables $name = Rovan, $role = Manager and $organization = IITM
s = t.substitute(name = 'Rovan', role = 'Manager', organization = 'IITM') #store the output string in the variable s
print(s)
```

## Output 
- Rovan is the Manager of IITM


## Reference
https://youtu.be/2_RC4n-Lb8M