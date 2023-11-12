```
# import the reader function from the csv module
from csv import reader

# use the python built-in function open()
# to open the children.csv file
opened_file = open('children.csv')

# use csv.reader() to parse the data from
# the opened file
read_file = reader(opened_file)

# use list() to convert the read file
# into a list of lists format
children = list(read_file)

# remove the first row of the data, which
# contains the column names
children = children[1:]
```


# PS : Python Big Picture

```
sudo apt install tree
sudo apt install python3-pip
sudo apt install python3-flask
sudo apt install python3-django
python3 -m pip install flask
python3 -m pip install django
```

### Linux Scripting and Administration

* Read / Write
```
import json
with open('input.json','r') as input:
    obj = json.load(input)
    print(obj[key])
    with open('output.txt','w') as output:
        output.write(obj[key] + "\n")
        for k in obj[key]:
            output.write(k + "\n")
```

* Command line

```
import subprocess

pl = subprocess.Popen(['ps','-U','0'],stdout=subprocess.PIPE).communicate()[0]
print(pl.decode('utf-8'))
```

### Web Development

API
* Flask
* Bottle
* Pyramid

Website
* Django
* TurboGears
* web2py

App i.e. CMS , ERP
* Plone
* django-cms
* Mezzanine

---
## Flask Example
---
* service.py
```
from flask import Flask
app = Flask(__name__)

@app.route("/")
def hello():
    return "Hello World!"
    
@app.route("/user/<username>")
def show_user(username):
    return "User: %s" % username    
```
* terminal
```
$FLASK_APP=service.py flask run
```

* alternatively on terminal
```
$curl localhost:5000
$curl localhost:5000/user/jolson
```

---
## Django Example
---

```
django-admin startproject mysite
cd mysite
tree .
python3 manage.py runserver
```

### Application Scripting

---
## Blender
---

```
bpy.data.objects
list(bpy.data.objects)
cube = bpy.data.objects["Cube"]
cube.location

import mathutils
cube.location += mathutils.Vector((1,1,1))

```
