---
layout: article
title: "Creating standalone Mac OS X applications with Python and py2app"
date: 2017-27-12 19:45:00+0200
coverPhoto: http://me.seekingqed.com/static/img/python2mac/python2mac.png
---

In this tutorial we’ll be using py2app to create a standalone OSX application from a Python 2 or 3 source code with a simple Tkinter user interface.

"py2app is a Python setuptools command which will allow you to make standalone application bundles and plugins from Python scripts. py2app is similar in purpose and design to py2exe for Windows."

```cmd
	# Create a custom directory
	$ mkdir MyApp
	$ cd MyApp

	# Use virtualenv to create an isolated environment
	$ virtualenv venv
	$ . venv/bin/activate
```

Now create a very simple Tkinter app with the filename `MyApp.py`:

```cmd
	import sys
if sys.version_info < (3, 0):
    # Python 2
    import Tkinter as tk
else:
    # Python 3
    import tkinter as tk
root = tk.Tk()
root.title("Sandwich")
tk.Button(root, text="Make me a MyApp").pack()
tk.mainloop()
```
#Install py2app
`$ pip install -U git+https://github.com/metachris/py2app.git@master`

This setup.py is a basic definition of the app:

```cmd
from setuptools import setup

APP = [MyApp.py']
DATA_FILES = []
OPTIONS = {'argv_emulation': True}

setup(
    app=APP,
    data_files=DATA_FILES,
    options={'py2app': OPTIONS},
    setup_requires=['py2app'],
)
```

If your application uses some data files, like a JSON, text files or images, you should include them in DATA_FILES. For example:
`DATA_FILES = ['testdata.json', 'picture.png']`





