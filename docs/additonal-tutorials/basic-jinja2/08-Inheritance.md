## Inheritance 
- The most powerful part of Jinja is template inheritance. 
- Template inheritance allows you to build a base “skeleton” template that contains all the common elements of your choice and defines blocks that child templates can override. 
- A simple example is given in Replit website - https://tempinh.devir5.repl.co. 
## The following programs specify how it executes:
- create main.py and create a folder templates. 
- Within templates folder create base.html (base class) and index.html(derived class).

## python code for inheritance
- File: main.py
```python linenums="1"
from flask import Flask, render_template
import random

app = Flask("app")

@app.route("/")
def home():
	# Generate the home page
  return render_template("index.html")
  
app.run(host = "0.0.0.0", port = "8080")

```
- File: base.html
```HTML linenums="1"
<!doctype html>
<html>
  <head>
    {% block head %}
    
    <title>{% block title %}Hello{% endblock %} </title> My Webpage - From Base class
    {% endblock %}
  </head>
  <body>
      {% block content %}
      {% endblock %}
      {% block footer %}
      &copy; Copyright 2022 by IITM - From base class
      {% endblock %}
    
  </body>
</html>

```
- File: index.html
```HTML linenums="1"
<!DOCTYPE html>
<html>
    <head>
        <title>Home Page</title>
				
    </head>
    <body>
      
      {% extends "base.html" %}
      {% block content %}
      
			<h1>Main Page - From child class</h1>
      <div>
      Welcome to IITM App Development course - From Child class
      </div>
      
      
			{% endblock %}
    </body>
</html>
```
## Output
-  https://tempinh.devir5.repl.co








