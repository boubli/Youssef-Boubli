---
layout: article
title: "Creating standalone Mac OS X applications with Python and py2app"
date: 2016-27-12 19:45:00+0200
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
root.title("MyApp")
tk.Button(root, text="Make me a MyApp").pack()
tk.mainloop()
```
# Install py2app

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

# Build the app for development and testing

`$ python setup.py py2app -A`

This creates the following files and directories:


```
	.
	├── build
	│   └── bdist.macosx-10.10-x86_64
	│       └── python2.7-standalone
	│           └── app
	│               ├── Frameworks
	│               ├── collect
	│               ├── lib-dynload
	│               └── temp
	├── MyApp.py
	├── dist
	│   └── MyApp.app
	│       └── Contents
	│           ├── Info.plist
	│           ├── MacOS
	│           │   ├── MyApp
	│           │   └── python -> /Users/chris/Projects/chris/python-gui/tkinter/env/bin/../bin/python
	│           ├── PkgInfo
	│           └── Resources
	│               ├── __boot__.py
	│               ├── __error__.sh
	│               ├── lib
	│               │   └── python2.7
	│               │       ├── config -> /Users/chris/Projects/chris/python-gui/tkinter/env/bin/../lib/python2.7/config
	│               │       └── site.pyc -> ../../site.pyc
	│               ├── site.py
	│               └── site.pyc
	└── setup.py
```

This is not a standalone application, and the applications built in alias mode are not portable to other machines!

The app built with alias mode simply references the original code files, so any changes you make to the original MyApp.py file are instantly available on the next app start.

The resulting development app in dist/MyApp.app can be opened just like any other .app with the Finder or the open command ($ open dist/MyApp.app). To run your application directly from the Terminal you can just run:

`$ ./dist/MyApp.app/Contents/MacOS/MyApp`



